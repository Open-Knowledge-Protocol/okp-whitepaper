# Chapter 13 — Decentralized Query Protocol

Storing knowledge is useful only if it can be discovered and queried.

Open Knowledge Protocol provides a common way for applications and AI agents to interact with the Open Knowledge Graph without needing to know which nodes physically store the data.

## Querying Knowledge

The protocol should support several types of queries.

### Direct Lookup

Retrieve a known object using its global identity.

```text id="vuv79x"
GET entity:okp://entity/abc123
```

### Graph Traversal

Explore relationships between knowledge objects.

```text id="6x3lzg"
Person
  │
FOUNDED
  ▼
Company
  │
HEADQUARTERED_IN
  ▼
Country
```

### Search

Find entities, claims, sources, or evidence when their identifiers are not known.

Search may include:

- Keyword search
- Semantic search
- Entity search
- Relationship search

### Provenance Queries

Applications can ask where knowledge came from.

```text id="f4gb8z"
Claim
  ↓
Evidence
  ↓
Source
  ↓
Publisher
```

### Historical Queries

Because knowledge evolution is preserved, applications can query the graph at a particular point in time.

For example:

**“What evidence supported Claim X in 2025?”**

## Distributed Query Execution

The requested knowledge may exist across several shards.

```text id="g2kvug"
Application
     │
     ▼
 Query Node
     │
 ┌───┼────────┐
 ▼   ▼        ▼
S1   S4       S9
 │   │        │
 └───┼────────┘
     ▼
 Combined Result
```

The query node discovers the relevant shards, coordinates the required graph traversal, and returns a combined result.

Applications interact with the logical graph rather than individual storage nodes.

## Verifiable Results

A decentralized query should not require blind trust in the query node.

Where possible, results can include enough information for the client to verify important parts of the response.

For example:

```text id="hw61u7"
Query Result
   │
   ├── Knowledge Objects
   ├── Provenance
   ├── Signatures
   └── Verification Proofs
```

This allows applications to separate **query execution** from **trust in the result**.

## Querying for AI

AI agents are an important consumer of OKP.

Instead of retrieving only documents, an agent could request:

```text id="yk9pq5"
Question
   ↓
Relevant Entities
   ↓
Claims
   ↓
Supporting Evidence
   ↓
Contradicting Claims
   ↓
Provenance
   ↓
AI Context
```

This gives an AI system structured context together with the information required to evaluate its reliability.

## An Open Interface

OKP should define the query semantics and response model while allowing different interfaces to exist.

These may include APIs, graph query languages, SDKs, agent protocols, or compatibility layers for existing standards.

The goal is not to force every application to use one query syntax.

The goal is to ensure that they can all access the **same connected knowledge network**.

**Knowledge can be stored across thousands of nodes while remaining accessible as one queryable graph.**