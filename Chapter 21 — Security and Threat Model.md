# Chapter 21 — Security and Threat Model

An open knowledge network will attract both useful contributions and attempts to manipulate it.

OKP must therefore protect two things:

**the integrity of the network and the integrity of knowledge history.**

It cannot guarantee that every claim is correct, but it should make manipulation difficult, visible, and traceable.

## False Knowledge

Anyone may attempt to publish incorrect or misleading claims.

OKP does not solve this by preventing controversial claims from entering the graph.

Instead, claims remain connected to their publisher, evidence, provenance, verification, and challenges.

```text id="sg4l5b"
Claim
  │
  ├── Publisher
  ├── Evidence
  ├── Provenance
  ├── Support
  └── Challenges
```

Applications can then decide how much confidence to place in them.

## Spam Attacks

Attackers could create millions of meaningless entities, claims, or relationships.

Defences may include:

- Publishing costs
- Rate limits
- Reputation
- Staking
- Storage costs
- Application-level filtering

The objective is to keep participation open while making large-scale abuse expensive.

## Sybil Attacks

One attacker could create thousands of identities and make them appear to independently support the same claim.

```text id="kdrdxu"
          Attacker
        /    |    \
       ▼     ▼     ▼
     ID A  ID B   ID C
       \     |     /
        ▼    ▼    ▼
           Claim
```

OKP should therefore not treat the number of supporters as equivalent to credibility.

Identity history, reputation, relationships, economic stake, and truly independent evidence can help detect coordinated behaviour.

## Fake Evidence

An attacker may publish real-looking claims supported by fabricated documents or manipulated evidence.

Cryptographic hashes can prove that evidence has not changed after publication.

They cannot prove that the evidence was genuine in the first place.

Verification must therefore consider the origin and credibility of the evidence itself.

**Cryptography can prove integrity. It cannot prove truth.**

## AI-Generated Knowledge Pollution

AI agents can generate knowledge much faster than humans.

A malicious or poorly configured agent could produce millions of plausible but incorrect claims.

AI-generated contributions should therefore remain identifiable.

Applications may apply different policies to human, institutional, and AI-generated knowledge.

Automation should increase the speed of knowledge creation without removing accountability.

## Node Attacks

Malicious nodes may attempt to:

- Reject valid operations
- Return incomplete query results
- Serve incorrect graph data
- Hide particular claims
- Manipulate indexes
- Go offline intentionally

Replication, cryptographic verification, independent query paths, and decentralized validation reduce dependence on any individual node.

## Censorship Resistance

A government, corporation, or powerful participant may attempt to remove or suppress knowledge.

Because graph data is distributed and replicated across independent nodes, no single operator should be able to erase valid public history.

Applications may choose not to display particular content, but that is different from deleting it from the protocol.

## Protocol Attacks

Attackers may also target the protocol itself through software vulnerabilities, compromised keys, validator attacks, or governance manipulation.

OKP should use established security practices including independent audits, secure key management, upgrade procedures, monitoring, and responsible vulnerability disclosure.

Critical protocol components should remain open to public inspection.

## Governance Attacks

Control of the DAO could become another attack vector.

An attacker acquiring enough governance power might attempt to change network rules for their benefit.

Governance protections discussed in Chapter 17 therefore form part of the security model.

The protocol should make capture difficult and make governance actions transparent.

## Assume Some Participants Are Malicious

OKP should not depend on every participant behaving honestly.

Its security model should assume that some publishers, nodes, verifiers, applications, and AI agents will eventually behave incorrectly or maliciously.

```text id="4fb6lr"
Untrusted Participants
        │
        ▼
Signatures + Validation
        │
        ▼
Replication + Consensus
        │
        ▼
Provenance + Verification
        │
        ▼
Transparent History
```

No single mechanism solves every threat.

Security comes from combining cryptography, decentralization, economic incentives, provenance, reputation, verification, and transparent history.

**OKP cannot guarantee that false knowledge will never enter the graph. It should guarantee that knowledge has a traceable history and that no single participant can silently rewrite what the network knows.**