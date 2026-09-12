# Chapter 16 — Incentive Model and Knowledge Economy

A decentralized knowledge network cannot depend on a single organization to pay for its infrastructure.

Participants who store knowledge, process queries, verify claims, and maintain the network need reasons to contribute resources.

OKP therefore requires an incentive model aligned with useful work.

## Who Contributes Value?

Different participants contribute different forms of value.

### Knowledge Contributors

People, organizations, and AI agents publish claims, sources, evidence, and relationships.

### Storage Nodes

Storage nodes provide disk space, bandwidth, and availability to keep portions of the graph accessible.

### Query and Index Nodes

These nodes make the distributed graph searchable and execute queries for applications.

### Validators

Validators protect the integrity of the graph by validating protocol operations.

### Verifiers

Verifiers examine claims, provide evidence, and challenge incorrect or misleading knowledge.

Each role contributes to the health of the network in a different way.

## Who Pays?

Applications that consume network resources may pay for operations such as:

```text id="8kb4ic"
Publish Knowledge
       │
       ▼
Store / Replicate
       │
       ▼
Index
       │
       ▼
Query
```

Simple public access may eventually be subsidized or extremely inexpensive, while resource-intensive operations can carry higher costs.

Organizations may also fund specific datasets, domains, or public knowledge as a shared resource.

## Reward Useful Work

Network rewards should correspond to measurable contributions.

For example:

```text id="g4kk9j"
Storage Node
     │
     └── Stores + Serves Data ──► Reward

Query Node
     │
     └── Executes Queries ──────► Reward

Verifier
     │
     └── Useful Verification ───► Reputation / Reward
```

Simply adding more data should not automatically produce rewards.

Otherwise, the easiest way to earn from the network would be to generate enormous amounts of low-quality knowledge.

## Economic Cost as Spam Protection

An open graph is vulnerable to spam.

Attackers or automated agents could create millions of meaningless entities, claims, and relationships.

Small economic costs can make large-scale abuse expensive.

```text id="u4x48u"
Publish Claim
     │
     ├── Network Cost
     └── Identity / Reputation
             │
             ▼
        Spam Resistance
```

The goal is not to make knowledge expensive to publish.

The goal is to ensure that abusing shared network resources has a cost.

## Incentives Should Improve Knowledge

Economic rewards can easily create unintended behaviour.

For example, directly rewarding every verification could encourage participants to generate meaningless verification activity.

OKP should therefore reward outcomes that improve the network rather than simple activity.

Reputation, independent agreement, successful challenges, usage, and long-term contribution quality may all become useful signals.

## The Role of a Network Token

A native token may eventually provide a common economic mechanism for:

- Paying network fees
- Rewarding infrastructure providers
- Staking
- Spam prevention
- DAO governance
- Ecosystem funding

However, a token should serve the protocol rather than define it.

The economic model should first determine **what behaviour the network needs to encourage and what resources need to be paid for**.

Token mechanics can then be designed around those requirements.

## A Sustainable Knowledge Network

The long-term goal is a self-sustaining network where value flows between those who consume knowledge and those who help maintain it.

```text id="0wlh5d"
Knowledge Consumers
        │
        ▼
   Network Economy
   /      |       \
  ▼       ▼        ▼
Storage  Query   Knowledge
 Nodes   Nodes   Ecosystem
```

No single company should need to finance the world's knowledge infrastructure.

**The network should reward participants for keeping knowledge available, useful, verifiable, and open.**