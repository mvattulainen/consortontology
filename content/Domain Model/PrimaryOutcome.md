---
id: consort-class-primary-outcome
type: OntologyClass
class_name: PrimaryOutcome
kind: domain_class
status: reviewed
aliases:
  - Primary Outcome
tags:
  - consort/2025
  - ontology/domain-class
---

# PrimaryOutcome

> [!definition]
> An OutcomeSpecification designated as primary in the trial protocol.

- **Parent class:** [[OutcomeSpecification]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| — | — | No class-specific properties; inherited properties apply. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[RandomisedTrial]] → `has_primary_outcome`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "An OutcomeSpecification designated as primary in the trial protocol.",
    "id": "consort-class-primary-outcome",
    "kind": "domain_class",
    "label": "Primary Outcome",
    "name": "PrimaryOutcome",
    "parent": "OutcomeSpecification",
    "properties": {},
    "status": "reviewed",
    "type": "OntologyClass"
  },
  "schema_version": "1.0"
}
```
<!-- END:CONSORT-ONTOLOGY -->

## Guideline mappings

See [[11 Trial Domain Model]] and [[09 Checklist Index]]. Checklist-item notes identify which domain classes their reporting requirements concern.
