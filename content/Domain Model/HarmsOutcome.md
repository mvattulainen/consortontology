---
id: consort-class-harms-outcome
type: OntologyClass
class_name: HarmsOutcome
kind: domain_class
status: reviewed
aliases:
  - Harms Outcome
tags:
  - consort/2025
  - ontology/domain-class
---

# HarmsOutcome

> [!definition]
> An OutcomeSpecification describing a harm or unintended effect and its assessment method.

- **Parent class:** [[OutcomeSpecification]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `severity_system` | `string` | System used to grade harm severity. |
| `surveillance_type` | `controlled_term` | Systematic or non-systematic harms surveillance. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[RandomisedTrial]] → `has_harms_outcome`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "An OutcomeSpecification describing a harm or unintended effect and its assessment method.",
    "id": "consort-class-harms-outcome",
    "kind": "domain_class",
    "label": "Harms Outcome",
    "name": "HarmsOutcome",
    "parent": "OutcomeSpecification",
    "properties": {
      "severity_system": {
        "definition": "System used to grade harm severity.",
        "required": false,
        "value_type": "string"
      },
      "surveillance_type": {
        "definition": "Systematic or non-systematic harms surveillance.",
        "required": false,
        "value_type": "controlled_term"
      }
    },
    "status": "reviewed",
    "type": "OntologyClass"
  },
  "schema_version": "1.0"
}
```
<!-- END:CONSORT-ONTOLOGY -->

## Guideline mappings

See [[11 Trial Domain Model]] and [[09 Checklist Index]]. Checklist-item notes identify which domain classes their reporting requirements concern.
