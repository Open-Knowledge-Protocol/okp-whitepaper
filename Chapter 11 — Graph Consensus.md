# Chapter 11 — Graph Consensus

A decentralized network needs agreement about what has happened.

When someone publishes a claim, adds evidence, creates a relationship, or retracts a previous contribution, independent nodes must agree that the operation is valid and has become part of the graph.

This is the role of **graph consensus**.

## Consensus About the Graph, Not the Truth

Consider the claim:

**“Drug X reduces the risk of Disease Y.”**

The network may reach consensus that:

- the claim was published,
- it was published by Researcher A,
- it references a particular study,
- it was published at a particular time,
- and its record has not been modified.

The network does **not** reach consensus that:

**“Drug X reduces the risk of Disease Y” is true.**

That judgment belongs to the knowledge and trust layers.

## Two Different Forms of Agreement

OKP separates two concepts:

```text id="ljr7vs"
NETWORK CONSENSUS

"Does this exist in the graph?"
            │
            ▼
   Open Graph Chain


KNOWLEDGE CONFIDENCE

"Should I trust this claim?"
            │
            ▼
Evidence + Provenance
+ Verification + Reputation
```

Network consensus is objective at the protocol level.

Knowledge confidence can vary between users, communities, and applications.

## Validating Graph Operations

Before accepting an operation, nodes can verify protocol-level rules.

For example:

```text id="8z7z7n"
Publish Claim
     │
     ▼
Check Signature
     │
Check IDs / References
     │
Check Schema
     │
Check Protocol Rules
     │
     ▼
Accept into Graph
```

Invalid operations are rejected.

A valid operation, however, can still contain a claim that later turns out to be wrong.

## Consensus Should Not Become Voting on Facts

A tempting approach would be to let validators vote on whether a claim is true.

OKP deliberately avoids this.

Ten thousand validators voting that a scientific claim is correct does not make it scientifically correct.

Similarly, a minority view should not disappear simply because most network participants disagree with it.

Claims should compete through evidence and verification, not control of network consensus.

## Conflicting Claims Can Coexist

Because consensus does not determine truth, conflicting claims can exist within the same graph.

```text id="hufv4c"
Evidence A
    │
 SUPPORTS
    ▼
 Claim A
    │
CONTRADICTS
    ▼
 Claim B
    ▲
 CHALLENGED_BY
    │
Evidence B
```

Both claims can be valid records in the network even though they cannot both accurately describe reality.

Applications can decide how to interpret them using their own trust models.

## What Consensus Guarantees

The Open Graph Chain should ultimately provide a small but powerful guarantee:

> **Participants can agree on the history and state of the graph without being required to agree on the meaning or truth of the knowledge inside it.**

This separation allows OKP to remain neutral infrastructure.

**Consensus protects the integrity of the knowledge graph. Evidence determines the credibility of its knowledge.**