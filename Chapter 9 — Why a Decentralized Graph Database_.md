# Chapter 9 — Why a Decentralized Graph Database?

The Open Knowledge Graph is intended to become shared infrastructure.

If the entire graph is stored in a database controlled by one organization, that organization ultimately controls access, availability, and the future of the graph.

OKP therefore requires a decentralized storage layer.

## Why a Graph Database?

Knowledge is naturally connected.

A person can found a company. A company operates in an industry. A research paper supports a claim. Another claim can contradict it.

These relationships are as important as the individual records.

```text id="nj2sxh"
Person ── FOUNDED ──► Company
                         │
                      OPERATES_IN
                         ▼
                      Industry
```

A graph database makes these relationships first-class and allows applications to traverse them efficiently.

## Why Decentralized?

A traditional graph database still has an owner.

Even if its data is publicly accessible, whoever operates the database can change access rules, remove information, shut down the service, or transfer control.

In OKP, independent nodes collectively maintain the graph.

```text id="ykfml2"
          Open Knowledge Graph
                  │
        ┌─────────┼─────────┐
        ▼         ▼         ▼
      Node A    Node B    Node C
        │         │         │
        └────── Network ────┘
```

No single node should be required for the graph to continue operating.

## Why Not Store Everything on a Traditional Blockchain?

Traditional blockchains are designed around transactions and replicated state.

Knowledge graphs have different requirements.

They may contain billions of entities and relationships and need operations such as:

- Graph traversal
- Relationship queries
- Entity lookup
- Semantic search
- Historical queries
- Provenance traversal

Replicating the complete graph across every node would eventually become expensive and inefficient.

OKP therefore requires a storage network designed specifically for decentralized graph data.

## The Open Graph Chain

We call this decentralized storage layer the **Open Graph Chain**.

The Open Graph Chain is responsible for distributing, replicating, validating, indexing, and serving the Open Knowledge Graph across independent nodes.

Unlike a traditional blockchain where transactions are the primary object, the Open Graph Chain is designed around **knowledge objects and their relationships**.

The exact mechanisms for partitioning, replication, consensus, and graph queries are described in the following chapters.

**If knowledge is to become shared infrastructure, the graph that stores it should not have a single owner.**