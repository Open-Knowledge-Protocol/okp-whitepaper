# Chapter 12 — Distributed Graph Storage

The Open Knowledge Graph may eventually contain billions of entities, claims, and relationships.

Requiring every node to store the entire graph would make participation increasingly expensive and eventually limit decentralization.

The Open Graph Chain therefore distributes the graph across the network.

## Partitioning the Graph

The graph can be divided into smaller units called **shards**.

```text id="yk2x6w"
               Global Graph
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
     Shard A     Shard B     Shard C
```

Each shard contains part of the global knowledge graph and is maintained by multiple independent nodes.

The protocol determines where knowledge belongs and how it can be located.

## Keeping Connected Knowledge Close

Graph partitioning is different from splitting ordinary records.

Knowledge is highly connected.

For example:

```text id="g87p0u"
Person
  │
FOUNDED
  ▼
Company
  │
OPERATES_IN
  ▼
Industry
```

If every object is stored in a different part of the network, even simple graph queries become expensive.

The partitioning strategy should therefore try to keep frequently connected knowledge close together while still allowing the network to rebalance as the graph grows.

## Replication

A shard should never depend on one node.

Multiple nodes maintain copies:

```text id="l3q25f"
             Shard A
                │
       ┌────────┼────────┐
       ▼        ▼        ▼
     Node 1   Node 2   Node 3
```

If one node disappears, other replicas can continue serving the data.

The required replication level can depend on network rules, demand, and the importance of maintaining availability.

## Cross-Shard Relationships

Knowledge will inevitably connect across shards.

A relationship therefore needs to reference objects regardless of where they are physically stored.

```text id="7kr1ei"
Shard A                         Shard B

Company ──────────────────────► Country
           HEADQUARTERED_IN
```

The protocol can locate the relevant shard and continue the traversal.

Applications see one relationship even though the underlying data may exist on different machines.

## Distributed Traversal

Consider a query:

**“Which researchers published papers supporting claims about Drug X?”**

Answering it may require traversing:

```text id="nw92y6"
Drug X
   ↓
Claims
   ↓
Evidence
   ↓
Research Papers
   ↓
Researchers
```

Those objects may span several shards.

A query node coordinates the traversal, retrieves the required parts of the graph, and combines the results.

The goal is to hide the physical distribution of the graph from applications.

## Storage Can Evolve

There may not be one perfect partitioning strategy for all knowledge.

As the network grows, shards may need to split, merge, move, or increase replication.

Popular knowledge may be replicated more widely, while rarely accessed historical data may primarily be maintained by archive nodes.

These changes should affect where knowledge is stored, not its global identity.

## One Graph, Distributed Storage

The Open Knowledge Graph is therefore logically global but physically distributed.

```text id="acg1ss"
       Application
            │
            ▼
   Open Knowledge Graph
            │
     ┌──────┼──────┐
     ▼      ▼      ▼
  Shard A Shard B Shard C
     │      │      │
   Nodes  Nodes  Nodes
```

No participant needs to store the world's entire knowledge graph.

Yet any participant should be able to discover and traverse knowledge across it.

**Distribution makes the graph scalable. Replication makes it resilient. Global identity keeps it connected.**