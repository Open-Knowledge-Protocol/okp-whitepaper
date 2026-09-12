# Chapter 8 — Knowledge Evolution

Knowledge changes.

New research appears, errors are discovered, measurements improve, and previously accepted ideas are challenged.

Open Knowledge Protocol must preserve this evolution rather than treating every claim as permanent truth.

## Claims Are Not Rewritten

Once a claim is published, its original record should remain available.

If new information changes our understanding, a new claim can be created and connected to the previous one.

For example:

```text id="crf5h5"
Claim V1
   │
SUPERSEDED_BY
   ▼
Claim V2
   │
SUPERSEDED_BY
   ▼
Claim V3
```

This preserves the history of how knowledge evolved.

## Corrections and Retractions

A publisher may discover that a claim was incorrect.

Instead of deleting it, the publisher can issue a correction or retraction:

```text id="exj3ce"
Original Claim
      │
      ├── CORRECTED_BY ──► New Claim
      │
      └── RETRACTED_BY ──► Retraction
```

Applications can show the latest state while still allowing users to inspect the original record.

## New Evidence Can Change Confidence

A claim does not always need to be replaced.

New evidence may strengthen or weaken the confidence in an existing claim.

```text id="nykbw9"
Evidence A ── SUPPORTS ──► Claim
Evidence B ── SUPPORTS ──► Claim
Evidence C ── CHALLENGES ► Claim
```

As the evidence around a claim changes, applications may calculate its confidence differently.

The original claim and evidence remain part of the graph.

## Knowledge Through Time

Because previous states are preserved, OKP can answer not only:

**“What do we know?”**

but also:

**“What did we know at a particular point in time?”**

This is useful for scientific research, regulation, history, journalism, and AI systems that need to understand how knowledge has changed.

## Immutable History, Evolving Knowledge

Immutability should protect the history of knowledge, not freeze our understanding of the world.

A decentralized network should make it difficult to secretly rewrite the past while still allowing new evidence and better knowledge to emerge.

**In OKP, history is immutable, but knowledge is allowed to evolve.**