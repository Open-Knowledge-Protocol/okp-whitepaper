# Chapter 5 — The Knowledge Model

For knowledge from different people, organizations, and applications to connect, they must share a common structure.

Open Knowledge Protocol defines a small set of building blocks for representing knowledge.

## Entities

An **Entity** represents something that exists or can be identified.

Examples include:

**Person, Organization, Country, Product, Event, Research Paper, Law, Disease, or Concept.**

Entities can be connected to other entities and referenced by many different claims.

## Claims

A **Claim** is a statement about one or more entities.

For example:

**Marie Curie → won → Nobel Prize in Physics**

A claim is not automatically treated as a fact. It can be connected to its source, evidence, publisher, verification history, status, and confidence.

### Claim Status

The **status** describes the current state of a claim.

For example:

- **Unverified** — the claim has been added but not independently verified.
- **Supported** — evidence or independent verification supports the claim.
- **Disputed** — credible evidence or other claims challenge it.
- **Retracted** — the publisher has withdrawn the claim.
- **Superseded** — newer knowledge has replaced or refined it.

Status can change as new evidence becomes available.

### Confidence

**Confidence** represents how strongly the available evidence supports a claim.

For example, a claim supported by several reliable and independent sources may have higher confidence than one based on a single unverified source.

Confidence is not the same as truth. It is a signal that helps applications understand the strength of the available evidence.

Different applications may also calculate confidence differently depending on their own trust models.

## Relationships

Relationships connect entities and claims to each other.

For example:

**Research Paper → SUPPORTS → Claim**

**Claim A → CONTRADICTS → Claim B**

**Company → FOUNDED_BY → Person**

These relationships turn isolated information into a connected graph.

## Sources and Evidence

A **Source** identifies where information came from, such as a research paper, government record, book, website, or dataset.

**Evidence** provides support for a specific claim.

Keeping these connections allows users and applications to trace knowledge back to its origin.

## Knowledge as a Graph

Together, these building blocks create a graph:

```text
Source
   │
   ▼
Evidence
   │
   ▼
Claim ───── CONTRADICTS ───── Claim
   │
   ├── Status
   ├── Confidence
   │
   ▼
Entity ───── Relationship ──── Entity
```

New knowledge does not need to replace existing knowledge. It can extend, support, challenge, or connect to what already exists.

This common model allows knowledge created independently across the world to become part of the same network.

**The value of the Open Knowledge Graph comes not only from what it contains, but from how everything within it is connected.**