---
id: consort-class-trial-design
type: OntologyClass
class_name: TrialDesign
kind: domain_class
status: reviewed
aliases:
  - Trial Design
tags:
  - consort/2025
  - ontology/domain-class
---

# TrialDesign

> [!definition]
> The structural design of a randomised trial, including design type, framework, unit of randomisation, and allocation ratio.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `allocation_ratio` | `string` | Planned ratio of allocation across trial arms. |
| `design_type` | `controlled_term` | Structural design such as parallel-group, crossover, or cluster. |
| `framework` | `controlled_term` | Inferential framework such as superiority, equivalence, or non-inferiority. |
| `unit_of_randomisation` | `controlled_term` | Type of unit assigned by randomisation. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[RandomisedTrial]] → `has_trial_design`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "The structural design of a randomised trial, including design type, framework, unit of randomisation, and allocation ratio.",
    "id": "consort-class-trial-design",
    "kind": "domain_class",
    "label": "Trial Design",
    "name": "TrialDesign",
    "parent": "OntologyEntity",
    "properties": {
      "allocation_ratio": {
        "definition": "Planned ratio of allocation across trial arms.",
        "required": false,
        "value_type": "string"
      },
      "design_type": {
        "definition": "Structural design such as parallel-group, crossover, or cluster.",
        "required": false,
        "value_type": "controlled_term"
      },
      "framework": {
        "definition": "Inferential framework such as superiority, equivalence, or non-inferiority.",
        "required": false,
        "value_type": "controlled_term"
      },
      "unit_of_randomisation": {
        "definition": "Type of unit assigned by randomisation.",
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
