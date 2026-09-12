# Chapter 6 — Knowledge Identity

For a global knowledge graph to work, the same knowledge must be identifiable across different applications and nodes.

Consider:

**“Microsoft”**  
**“Microsoft Corporation”**  
**“MSFT”**

These names may all refer to the same organization. If every contributor creates a separate entity, the graph quickly becomes fragmented.

## Global Identity

Open Knowledge Protocol assigns a unique identity to every object in the graph.

This includes:

- Entities
- Claims
- Sources
- Evidence
- Documents

The identifier remains stable even when the information describing that object changes.

For example:

```text
Entity ID: okp://entity/abc123

Name: Microsoft Corporation
Aliases: Microsoft, MSFT
Type: Organization
```

Applications can use the identifier instead of relying only on names.

## Entity Resolution

Sometimes it will not be clear whether two entities are the same.

Instead of silently merging them, OKP can record a relationship such as:

```text
Entity A ─── SAME_AS ─── Entity B
```

Evidence supporting the match can also be attached.

This allows entity resolution to improve over time without losing the original records.

## Content Identity

Documents, evidence, and other content can also be identified using cryptographic hashes.

If the content changes, its hash changes.

This makes it possible to verify that the evidence being referenced today is the same evidence that was originally attached to a claim.

## A Common Address for Knowledge

A shared identity system allows knowledge created by different participants to connect without requiring a central organization to maintain a master database of IDs.

Just as URLs provide addresses for information on the web, OKP identifiers provide **stable addresses for knowledge in the Open Knowledge Graph.**