# Chapter 10 — Open Graph Chain Architecture

The Open Graph Chain is a peer-to-peer network of independent nodes that collectively maintain the Open Knowledge Graph.

No node needs to store the entire graph. Instead, storage, replication, validation, indexing, and queries are distributed across the network.

## Network Architecture

At a high level:

```text
                     Applications / AI Agents
                              │
                              ▼
                         OKP Protocol
                              │
                              ▼
                         Query Nodes
                              │
                    ┌─────────┴─────────┐
                    ▼                   ▼
                Graph Shard         Graph Shard
                    │                   │
              ┌─────┼─────┐       ┌─────┼─────┐
              ▼     ▼     ▼       ▼     ▼     ▼
            Node  Node  Node    Node  Node  Node
                    │                   │
                    └────── Network ────┘
```

Together, these nodes expose the distributed graph as one logical knowledge network.

## Graph Nodes

Graph Nodes are the core participants in the network.

They can store portions of the graph, accept graph operations, validate data, replicate knowledge, and serve queries.

A node may store only a subset of the global graph.

## Graph Shards

The global graph is divided into **graph shards**.

A shard contains a portion of the entities, claims, relationships, evidence, and provenance in the network.

Multiple nodes can maintain copies of the same shard.

```text
Graph Shard A
     │
 ┌───┼───┐
 ▼   ▼   ▼
N1  N2  N3
```

Replication prevents knowledge from depending on a single machine.

How the graph is partitioned and how related knowledge is kept close together is discussed in a later chapter.

## Validators

Before an operation becomes part of the graph, the network must validate it.

Validation can include checking:

- Digital signatures
- Object identifiers
- Schema rules
- References to existing objects
- Protocol rules
- Authorization where required

Validation confirms that an operation is valid according to the protocol.

It does **not** confirm that the knowledge itself is true.

## Index and Query Nodes

Storing the graph and finding knowledge within it are different problems.

Query nodes can maintain indexes that make it easier to discover where knowledge is stored and execute queries across multiple shards.

For example:

```text
Query:
"Find research that challenges Claim X"

             │
             ▼
        Query Node
             │
       ┌─────┴─────┐
       ▼           ▼
    Shard A      Shard F
       │           │
       └─────┬─────┘
             ▼
          Result
```

This allows applications to interact with the network without knowing which physical nodes contain each part of the graph.

## Different Nodes Can Play Different Roles

Not every participant needs to perform every function.

A network participant may operate as a:

**Storage Node** — stores and replicates graph data.

**Validator Node** — validates graph operations.

**Query Node** — executes distributed graph queries.

**Indexer Node** — maintains indexes for locating knowledge.

**Archive Node** — maintains larger portions of historical graph state.

A single machine may perform several of these roles.

## One Logical Graph

Physically, knowledge may be distributed across thousands of independent nodes.

Logically, applications should experience it as one connected graph:

```text
Distributed Nodes
       │
       ▼
Open Graph Chain
       │
       ▼
Open Knowledge Graph
```

The architecture therefore separates **where knowledge is physically stored** from **how knowledge is logically connected**.

This allows the graph to grow without requiring any single organization or machine to contain the world's knowledge.

**Many nodes maintain the network, but together they form one Open Knowledge Graph.**