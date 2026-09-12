# Chapter 20 — Privacy and Private Knowledge

Not all knowledge should be public.

Organizations hold confidential information. Individuals have personal data. Governments and institutions may manage restricted information.

OKP must therefore separate **open knowledge infrastructure** from the assumption that all knowledge is publicly visible.

## Public and Private Knowledge

Knowledge can exist at different visibility levels.

```text id="3f4cq5"
Knowledge
   │
   ├── Public
   │
   ├── Restricted
   │
   └── Private
```

Public knowledge can be stored and queried through the Open Graph Chain.

Private knowledge can remain within systems controlled by its owner while still using OKP identities, schemas, and relationships.

## Private Knowledge Graphs

An organization may maintain its own private graph.

For example:

```text id="mqoznk"
Private Company Graph

Supplier A
   │
   ├── Internal Risk Score
   ├── Private Contract
   └── Investigation Notes
           │
           │ references
           ▼
     Public OKP Entity
```

The organization does not need to publish its contracts or investigation data to benefit from the public graph.

Public and private knowledge can reference the same globally identifiable entities.

## Selective Sharing

Sometimes knowledge should be shared only with specific participants.

A company may share information with an auditor.

A researcher may share a dataset with approved institutions.

A government agency may share information with another authorized agency.

Access controls can determine who is allowed to retrieve protected knowledge.

```text id="rg3h13"
Private Knowledge
       │
       ▼
Access Policy
   /        \
Allowed    Denied
   │
   ▼
Authorized User
```

## Proof Without Disclosure

In some cases, participants may need to prove something without revealing the underlying information.

For example, an organization might prove that a required verification was completed without publishing the confidential documents used during that process.

Cryptographic techniques such as commitments and zero-knowledge proofs may support these scenarios.

```text id="4i0fdq"
Private Evidence
      │
      ▼
Cryptographic Proof
      │
      ▼
Public Verification
```

The protocol can verify the proof without requiring the private evidence to become public.

## Privacy and Immutability

Immutable networks create a serious privacy challenge.

Sensitive personal information should generally **not be written directly into permanent public graph history**.

Encryption alone may not always be sufficient because encrypted data can remain permanently available and cryptographic assumptions can change over time.

OKP should therefore follow a simple principle:

**Do not put information on the public chain that may later need to be deleted.**

Sensitive data can remain off-chain or inside private graphs while the public network stores only appropriate references or proofs.

## Data Ownership

Using OKP should not require organizations to surrender control of their private knowledge.

```text id="p3cz24"
Public Knowledge ─────► Open Graph Chain

Private Knowledge ────► Owner-Controlled Storage
                              │
                              ▼
                         OKP Compatible
```

Organizations can choose what they publish, what they share selectively, and what remains private.

## One Protocol, Different Boundaries

The same knowledge standards can operate across public and private environments.

This makes it possible to connect knowledge without requiring all knowledge to live in the same database.

The Open Knowledge Graph can become the shared public layer, while organizations and individuals maintain private extensions around it.

**Open knowledge should mean that public knowledge is not controlled by a single organization—not that every piece of knowledge must become public.**