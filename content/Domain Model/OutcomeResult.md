---
id: consort-class-outcome-result
type: OntologyClass
class_name: OutcomeResult
kind: domain_class
status: reviewed
aliases:
  - Outcome Result
tags:
  - consort/2025
  - ontology/domain-class
---

# OutcomeResult

> [!definition]
> A result for an OutcomeSpecification from a defined analysis population and time point.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `analysis_population` | `string` | Definition of participants included in the result. |
| `time_point` | `string` | Outcome time point represented by the result. |

## Relations

### Outgoing

- `result_for_outcome` → [[OutcomeSpecification]]
- `has_group_result` → [[GroupResult]]
- `has_effect_estimate` → [[EffectEstimate]]

### Incoming

- [[RandomisedTrial]] → `has_outcome_result`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A result for an OutcomeSpecification from a defined analysis population and time point.",
    "id": "consort-class-outcome-result",
    "kind": "domain_class",
    "label": "Outcome Result",
    "name": "OutcomeResult",
    "parent": "OntologyEntity",
    "properties": {
      "analysis_population": {
        "definition": "Definition of participants included in the result.",
        "required": true,
        "value_type": "string"
      },
      "time_point": {
        "definition": "Outcome time point represented by the result.",
        "required": true,
        "value_type": "string"
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
