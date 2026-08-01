---
id: consort-class-effect-estimate
type: OntologyClass
class_name: EffectEstimate
kind: domain_class
status: reviewed
aliases:
  - Effect Estimate
tags:
  - consort/2025
  - ontology/domain-class
---

# EffectEstimate

> [!definition]
> A quantitative estimate comparing results between trial arms or otherwise summarizing an intervention effect.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `measure_type` | `controlled_term` | Effect measure such as mean difference, risk ratio, or hazard ratio. |
| `scale` | `string` | Scale on which the estimate is expressed. |
| `value` | `number` | Numerical effect estimate. |

## Relations

### Outgoing

- `has_precision_estimate` → [[PrecisionEstimate]]

### Incoming

- [[OutcomeResult]] → `has_effect_estimate`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A quantitative estimate comparing results between trial arms or otherwise summarizing an intervention effect.",
    "id": "consort-class-effect-estimate",
    "kind": "domain_class",
    "label": "Effect Estimate",
    "name": "EffectEstimate",
    "parent": "OntologyEntity",
    "properties": {
      "measure_type": {
        "definition": "Effect measure such as mean difference, risk ratio, or hazard ratio.",
        "required": true,
        "value_type": "controlled_term"
      },
      "scale": {
        "definition": "Scale on which the estimate is expressed.",
        "required": false,
        "value_type": "string"
      },
      "value": {
        "definition": "Numerical effect estimate.",
        "required": true,
        "value_type": "number"
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
