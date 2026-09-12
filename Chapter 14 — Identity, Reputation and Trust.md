# Chapter 14 — Identity, Reputation and Trust

In an open network, anyone can contribute knowledge.

This openness is important, but it creates a challenge: not every source, publisher, or verifier should automatically be trusted equally.

OKP therefore provides signals that applications can use to build their own trust models.

## Identity

Participants can have verifiable identities on the network.

A participant may represent:

- A person
- An organization
- A research institution
- A government agency
- An AI agent
- An anonymous or pseudonymous contributor

Contributions can be cryptographically signed, allowing the network to verify which identity published them.

Identity proves **who made a contribution**. It does not prove that the contribution is correct.

## Reputation

Reputation can develop from a participant's history on the graph.

Signals may include:

- Previous contributions
- Quality of supporting evidence
- Independent verification
- Successful challenges
- Corrections and retractions
- Citations by other trusted participants

For example:

```text id="z8gn61"
Publisher
    │
    ├── Published 120 claims
    ├── 90 independently supported
    ├── 8 disputed
    └── 3 retracted
```

These signals allow applications to evaluate the publisher's history rather than relying only on their identity.

## Reputation Is Contextual

Trust should not be represented by one universal score.

A researcher may be highly trusted in molecular biology but have no special authority in economics.

```text id="tvrtuo"
                  Researcher
                 /          \
                ▼            ▼
        Molecular Biology   Economics
           High Trust       No Special Trust
```

Reputation can therefore be associated with domains, topics, and types of contribution.

## Trust Is Application-Specific

OKP should provide the underlying trust signals, but applications decide how to use them.

A scientific application may prioritize peer-reviewed research.

A news application may prioritize primary sources and independent confirmation.

An AI agent may combine provenance, source reputation, evidence quality, recency, and independent verification.

Two applications can therefore evaluate the same claim differently while using the same Open Knowledge Graph.

## A Practical Trust Flow

Consider an AI agent trying to answer:

**“Does Drug X reduce the risk of Disease Y?”**

The agent first discovers relevant claims in the graph.

```text id="k00e76"
Question
   │
   ▼
Relevant Claims
   │
   ├── Claim A: Supports
   ├── Claim B: Supports
   └── Claim C: Challenges
```

For each claim, it can inspect the available trust signals:

```text id="hz0j7l"
Claim
  │
  ├── Who published it?
  ├── What is the source?
  ├── What evidence supports it?
  ├── Who verified it?
  ├── Who challenged it?
  ├── What is the publisher's reputation?
  └── How recent is the evidence?
```

The application then applies its own trust policy.

For example, a medical application may give greater weight to clinical trials and peer-reviewed research, while giving less weight to unsupported individual claims.

```text id="5ms7g4"
Claims
   │
   ▼
Trust Policy
   │
   ├── Provenance
   ├── Evidence Quality
   ├── Publisher Reputation
   ├── Independent Verification
   ├── Contradicting Evidence
   └── Recency
   │
   ▼
Confidence
```

The result is not simply **trusted** or **untrusted**.

The application can produce a confidence level and explain which evidence contributed to that decision.

Another application may use a different trust policy and reach a different confidence level using the same underlying graph.

This is an important property of OKP:

**the network provides trust signals; the consumer decides how to interpret them.**

## Resistance to Manipulation

Reputation must be difficult to manufacture.

Creating thousands of identities should not automatically create thousands of trusted participants.

Trust models may therefore consider signals such as contribution history, independent attestations, network relationships, evidence quality, and economic stake where appropriate.

The protocol should make these signals available without forcing every application to use the same formula.

## Trust Without a Central Authority

OKP does not maintain an official list of trusted people or organizations.

Instead, it creates an open graph of identities, contributions, evidence, verification, challenges, and reputation signals.

Applications can then decide whom and what they trust.

**OKP does not tell participants whom to trust. It provides the evidence needed to make trust transparent, explainable, and open to challenge.**