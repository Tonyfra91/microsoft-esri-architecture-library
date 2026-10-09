# Ground Truth Conceptual Pattern

## Purpose

Ground Truth is a conceptual pattern for grounding agent reasoning in authoritative business, spatial, domain, and operational context.

> **IMPORTANT**
>
> Ground Truth is not an existing Microsoft or Esri product. It is not a committed roadmap item. It must not be presented as a supported integration or packaged solution.

## Concept

The pattern asks an agent to reason from traceable context rather than from an unqualified collection of data:

```text
Authoritative sources
    → Governed context
    → Spatial and domain grounding
    → Agent reasoning and tool use
    → Attributed answer or proposed action
    → Human review when required
```

## Grounding Dimensions

| Dimension | Question |
|---|---|
| Authority | Which system or owner defines the fact? |
| Identity | Which user or workload is requesting access? |
| Authorization | Is that identity allowed to read or act on the source? |
| Semantics | What do the entity, property, measure, and relationship mean? |
| Spatial context | Where is the entity, and which geographic relationships apply? |
| Domain context | Which industry or operational rules constrain interpretation? |
| Time | When was the fact valid, observed, or updated? |
| Lineage | How was the fact produced or transformed? |
| Confidence | What uncertainty or quality limitations apply? |
| Actionability | May the agent answer, recommend, or change state? |

## Candidate Sources

Candidate sources may include:

- Governed Fabric data
- Power BI semantic models
- Validated Fabric IQ context
- Supported Data Agent responses
- ArcGIS Online or ArcGIS Enterprise content
- Validated Esri domain definitions
- Supported spatial tools and analytical outputs
- Customer policies and operational systems

Each source requires independent validation. Inclusion in this list does not establish integration support.

## Ground Truth Contract

A future implementation should define:

1. Source identity and owner.
2. Scope and authority.
3. Version and freshness.
4. Semantic definitions.
5. Spatial reference and scale.
6. Access-control behavior.
7. Retrieval or tool contract.
8. Citation and lineage format.
9. Conflict-resolution policy.
10. Human-approval policy.

## Human Role

Human interaction should be matched to consequence:

| Outcome | Candidate control |
|---|---|
| Informational answer | Source attribution and user verification |
| Analytical recommendation | Review of assumptions, evidence, and uncertainty |
| Operational proposal | Named approver and recorded decision |
| External or irreversible action | Strong authorization, explicit approval, audit, and recovery plan |

## Validation Questions

- [ ] Are all sources authoritative for the claim they support?
- [ ] Are semantics consistent across Microsoft, Esri, and customer systems?
- [ ] Is location represented at the correct scale and spatial reference?
- [ ] Is temporal validity included?
- [ ] Does identity propagate to every data and tool boundary?
- [ ] Are citations and lineage returned with the answer?
- [ ] Are conflicting sources visible rather than silently merged?
- [ ] Are consequential actions gated by policy and human approval?
- [ ] Can the system fail safely when grounding is incomplete?

## Relationship to the Reference Pattern

Ground Truth provides the grounding objective for [Microsoft + Esri Agentic Reference Pattern](README.md). The reference pattern must remain conceptual until each component, connection, and boundary is supported by evidence.
