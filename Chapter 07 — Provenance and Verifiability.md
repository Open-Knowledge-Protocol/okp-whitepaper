# Chapter 7 — Provenance and Verifiability

A claim is more useful when its origin can be verified.

Open Knowledge Protocol keeps provenance as part of the knowledge itself, allowing anyone to trace a claim back to its sources and evidence.

## Provenance

Every claim can maintain information about its origin:

- Who published it
- When it was published
- Which sources were used
- What evidence supports it
- Whether it was derived from other claims

For example:

```text
Claim
  │
  ├── Published by → Researcher A
  ├── Source → Research Paper
  ├── Evidence → Dataset
  └── Published at → 2026
```

This creates a traceable path from knowledge to its origin.

## Provenance Relationships

Provenance is the record of **how a claim came to exist and what it is based on**.

It connects the main objects already present in the knowledge graph:

```text
Publisher
    │
 PUBLISHED
    ▼
  Claim
   │  \
   │   \ DERIVED_FROM
   │    ▼
   │   Claim
   │
   ├── HAS_SOURCE ──────► Source
   │
   └── SUPPORTED_BY ────► Evidence
                              │
                         EXTRACTED_FROM
                              ▼
                            Source
```

For example, consider the claim:

**“Drug X reduces the risk of Disease Y.”**

Its provenance could be:

```text
Researcher A
     │
  PUBLISHED
     ▼
   Claim
     │
     ├── HAS_SOURCE ───► Research Paper
     │
     └── SUPPORTED_BY ─► Clinical Trial Results
                              │
                         EXTRACTED_FROM
                              ▼
                        Research Paper
```

A **Source** is where information came from.

**Evidence** is the specific information used to support a claim.

A **Publisher** is the person, organization, or agent that introduced the claim into OKP.

A **Claim** is the statement being made.

Provenance is the connected history between these objects.

## Provenance Data Model

The relationships above can be represented by a provenance record attached to a claim.

A minimal model could contain:

```text
Provenance Record
  │
  ├── claim_id
  ├── publisher_id
  ├── source_ids[]
  ├── evidence_ids[]
  ├── derived_from[]
  ├── created_at
  ├── content_hash
  └── signature
```

**claim_id** identifies the claim whose origin is being described.

**publisher_id** identifies who introduced the claim into OKP.

**source_ids** reference the sources used to create the claim.

**evidence_ids** reference the specific evidence supporting it.

**derived_from** references earlier claims when the claim was derived from existing knowledge.

**created_at** records when the contribution was made.

**content_hash** provides a cryptographic fingerprint of the submitted content.

**signature** proves that the provenance record was created or approved by the stated publisher.

A single claim may have additional provenance records as new participants contribute evidence, verification, or challenges. This allows its history to grow without rewriting the original contribution.

## Cryptographic Verification

Publishers can digitally sign their contributions.

Documents and evidence can be represented by cryptographic hashes. This allows anyone to verify that the referenced content has not been changed since it was added.

The protocol can therefore verify:

**who published something and whether the referenced evidence remains unchanged.**

It does not automatically verify that the claim itself is true.

## Independent Verification

Other participants can examine a claim and publish their own verification or challenge.

For example:

```text
Researcher A
     │
   publishes
     ▼
   Claim
   /   \
SUPPORTS  CHALLENGES
  /          \
Verifier B  Verifier C
```

These actions become part of the graph rather than replacing the original claim.

## Verifiable Knowledge

This allows applications to look beyond a claim itself.

An AI agent could retrieve a claim and inspect its original source, supporting evidence, publisher, verification history, and challenges before deciding whether to use it.

**OKP makes knowledge verifiable by preserving the path from a claim back to the people, sources, and evidence behind it.**