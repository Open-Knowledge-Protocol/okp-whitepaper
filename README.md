# Open Knowledge Protocol

**An open protocol for decentralized, verifiable, and shared knowledge.**

Open Knowledge Protocol (OKP) explores a simple idea:

> Knowledge is built collectively. Its infrastructure should belong to everyone.

Today, knowledge is fragmented across websites, databases, research repositories, organizations, and AI systems. Even when information is publicly accessible, the infrastructure connecting and organizing it is usually controlled by individual organizations.

OKP proposes an open protocol for building a decentralized global knowledge graph that no single organization owns.

---

## The Architecture

OKP is organized around four distinct layers:

```text
┌─────────────────────────────┐
│      Application Layer      │
│  Search • AI • Agents • Apps│
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│       Knowledge Layer       │
│ Entities • Claims • Evidence│
│ Relationships • Provenance  │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│         Trust Layer         │
│ Verification • Reputation   │
│ Challenges • Confidence     │
└──────────────┬──────────────┘
               ▼
┌─────────────────────────────┐
│       Open Graph Chain      │
│ Storage • Consensus • Query │
│ Replication • Validation    │
└─────────────────────────────┘
```

### Application Layer

Applications such as search engines, research tools, AI assistants, autonomous agents, and enterprise systems interact with knowledge through OKP.

### Knowledge Layer

Defines how entities, claims, relationships, evidence, sources, and provenance form the **Open Knowledge Graph**.

### Trust Layer

Provides the signals needed to evaluate knowledge through provenance, verification, challenges, identity, reputation, and evidence.

The protocol does not decide what is true.

### Open Graph Chain

A decentralized graph-native network where independent nodes collectively store, replicate, validate, index, and serve the knowledge graph.

**The knowledge graph is the chain.**

---

## Whitepaper

The repository contains the evolving **Open Knowledge Protocol Whitepaper**.

The whitepaper explores:

- Knowledge representation
- Claims and conflicting knowledge
- Provenance
- Knowledge identity
- Verification
- Trust and reputation
- Decentralized graph storage
- Graph consensus
- Distributed queries
- Incentive models
- DAO governance
- Privacy
- AI and autonomous agents
- Security
- Protocol evolution

The whitepaper should currently be considered a **proposal and design exploration**, not a finalized specification.

Many technical and economic decisions remain intentionally open.

---

## We Want This Whitepaper to Be Challenged

OKP should not be designed by one person or one organization.

We actively invite researchers, engineers, graph database experts, distributed-systems engineers, cryptographers, AI researchers, economists, and anyone interested in open knowledge to challenge the ideas presented here.

If you think something will not work, **tell us why**.

If you know a better architecture, **propose it**.

If an assumption is wrong, **challenge it**.

If another project has already solved part of the problem, **point us to it**.

Strong disagreement backed by reasoning is as valuable as agreement.

---

## How to Suggest Changes

The easiest way to contribute is through **GitHub Issues**.

Create an issue if you want to:

- Challenge an assumption
- Suggest an architectural change
- Identify a technical problem
- Propose a new concept
- Improve an existing chapter
- Point out missing research
- Suggest relevant projects or papers
- Identify security or economic risks

When possible, mention the relevant chapter and explain the reasoning behind your suggestion.

A useful issue might look like:

```text
Title:
Chapter 12: Cross-shard graph traversal may become expensive

Chapter:
12 — Distributed Graph Storage

Problem:
The proposed design assumes queries can traverse multiple
graph shards efficiently. Highly connected entities could
require queries across a large number of shards.

Suggestion:
Consider...

References:
Relevant papers/projects/implementations...
```

---

## Proposing Changes to the Whitepaper

For concrete changes, you can also open a **Pull Request**.

1. Fork the repository.
2. Create a branch.
3. Update the relevant chapter.
4. Explain the reasoning behind the change.
5. Open a Pull Request.

Please avoid changing an architectural principle without explaining **why the change improves the protocol**.

Large architectural changes should preferably begin as an Issue so they can be discussed before modifying the whitepaper.

---

## Open Questions

Several important questions remain intentionally unresolved.

Examples include:

```text
How should graph sharding work?

What consensus model best fits graph-native state?

How should cross-shard traversal work?

How should knowledge reputation be calculated?

How should Sybil attacks be resisted?

Which operations should require economic cost?

Does OKP require a native token?

How should DAO governance evolve?

How should private graphs interact with the public graph?

How should AI-generated knowledge be identified and verified?
```

These are not implementation details hidden behind the whitepaper.

They are **open research and design problems**.

Contributions addressing them are especially welcome.

---

## Design Principles

While implementation details can change, OKP is built around several principles:

**Knowledge should be open.**

**Claims are not truth.**

**Evidence should be traceable.**

**Disagreement should be preserved.**

**History should not be silently rewritten.**

**Network consensus should not decide truth.**

**Trust should be transparent and plural.**

**Privacy must be preserved.**

**The protocol should remain permissionless.**

**No organization should own the global knowledge graph.**

---

## Governance

The long-term goal is for OKP to be governed by a DAO rather than controlled by its original creators.

The DAO may eventually govern protocol upgrades, network parameters, treasury resources, and ecosystem development.

However:

> **The DAO governs the protocol. It does not decide what is true.**

Knowledge remains governed by evidence, provenance, verification, disagreement, and the trust policies chosen by those consuming it.

---

## Status

🚧 **Early Design / Whitepaper Stage**

OKP is currently an evolving concept.

The architecture, protocol, graph chain, consensus mechanism, economic model, and governance system should not be considered finalized.

This repository exists partly to expose those ideas early enough for them to be challenged.

---

## License

The whitepaper and documentation are licensed under the **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)** license.

You may share and adapt the material, including for commercial purposes, provided appropriate attribution is given and derivative works are distributed under the same license.

Future software implementations, SDKs, node software, and developer tooling may be released separately under the **Apache License 2.0**.

---

## Contributing

You do not need permission to participate.

Read the whitepaper.

Question its assumptions.

Open an Issue.

Propose an alternative.

Submit a Pull Request.

Build an experiment.

Share relevant research.

The objective is not to defend the current design.

The objective is to discover whether an **open, decentralized knowledge infrastructure can actually be built**.

**If knowledge belongs to everyone, its architecture should be designed in the open.**