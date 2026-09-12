# Chapter 15 — Knowledge Verification

Publishing a claim does not make it true.

Open Knowledge Protocol allows independent participants to examine claims, support them, challenge them, and contribute new evidence.

Verification therefore becomes an ongoing process rather than a one-time approval.

## Claim Lifecycle

A claim may move through several stages:

```text id="r17s87"
Publish Claim
     │
     ▼
  Unverified
     │
     ├──── Supporting Evidence
     │
     ▼
  Supported
     │
     ├──── Contradicting Evidence
     │
     ▼
   Disputed
```

These states describe what has happened around a claim. They do not represent an absolute judgment of truth.

## Verification

A verifier can examine a claim and publish a verification record.

For example:

```text id="d9w9tf"
Verifier
   │
   ▼
Verification
   │
   ├── Claim
   ├── Position: SUPPORT
   ├── Evidence
   ├── Reason
   ├── Timestamp
   └── Signature
```

The verification becomes part of the graph and can itself be inspected by others.

## Challenges

Participants can also challenge a claim.

A challenge should ideally explain why the claim is being disputed and provide supporting evidence.

```text id="ndb6ej"
Evidence A
    │
 SUPPORTS
    ▼
  Claim
    ▲
 CHALLENGES
    │
Evidence B
```

The original claim is not removed.

Instead, the disagreement becomes visible within the graph.

## Verification Workflow

Consider a new claim being submitted to OKP.

### 1. Publish

A publisher submits the claim with its source, evidence, provenance, and digital signature.

```text id="88aknk"
Publisher
    │
    ▼
Claim + Evidence + Provenance
```

The network validates that the submission follows protocol rules and records it in the graph.

The claim initially has no independent verification.

### 2. Discover

Verifiers discover claims relevant to their domain.

A verifier may be a person, organization, research institution, or AI agent.

```text id="gw86nw"
New Claim
   │
   ▼
Relevant Verifiers
```

### 3. Evaluate

A verifier examines the claim and its provenance.

They may inspect:

- Original sources
- Supporting evidence
- Methodology
- Related claims
- Existing challenges
- Publisher identity

### 4. Respond

The verifier publishes a signed response.

```text id="rc43i1"
               Claim
              /     \
             ▼       ▼
          SUPPORT  CHALLENGE
             │       │
             ▼       ▼
         Evidence  Evidence
```

The response becomes another object in the graph.

### 5. Re-evaluate

New evidence or challenges may appear later.

Other participants can verify the new evidence, challenge previous verification, or contribute additional information.

```text id="i3z98j"
Claim
  │
  ├── Verification A
  ├── Verification B
  ├── Challenge C
  ├── Evidence D
  └── Evidence E
```

The verification process therefore does not have a final step.

Knowledge can continue to be examined as new information becomes available.

### 6. Interpret

Applications evaluate the resulting graph using their own trust models.

```text id="bypz5l"
Claim
 + Evidence
 + Verifications
 + Challenges
 + Reputation
 + Provenance
       │
       ▼
Application Trust Model
       │
       ▼
Confidence
```

The protocol provides the verification history. The application determines what that history means.

## Verification Can Be Challenged

Verification itself should not become an authority.

A verifier may misunderstand evidence, have a conflict of interest, or simply be wrong.

Other participants can therefore challenge a verification or provide additional evidence.

This creates a chain of reasoning that remains open to inspection.

## Humans, Organizations, and AI Agents

Verification can come from different participants.

A research institution may verify scientific claims. A government agency may verify an official record. An individual may contribute evidence. AI agents may analyze sources and identify supporting or conflicting information.

Each contribution carries its own identity, provenance, and reputation signals.

Applications decide how much weight to give each one.

## Verification Changes Confidence

As verification accumulates, the confidence around a claim can change.

```text id="s8d83x"
                Claim
             /    |    \
            ▼     ▼     ▼
         Support Support Challenge
            │     │       │
            └─────┼───────┘
                  ▼
          Confidence Signal
```

Confidence is therefore derived from the evidence and verification surrounding a claim rather than being permanently assigned when the claim is created.

## An Open Verification Process

OKP does not create a central fact-checking authority.

Instead, it makes verification part of the knowledge graph itself.

Anyone can inspect the claim, its evidence, who supported it, who challenged it, and why.

**Claims are published openly. Evidence strengthens or weakens them. Verification makes that process visible and accountable.**