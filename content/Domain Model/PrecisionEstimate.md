---
id: consort-class-precision-estimate
type: OntologyClass
class_name: PrecisionEstimate
kind: domain_class
status: reviewed
aliases:
  - Precision Estimate
tags:
  - consort/2025
  - ontology/domain-class
---

# PrecisionEstimate

> [!definition]
> A quantitative expression of uncertainty around an EffectEstimate, such as a confidence or credible interval.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `interval_type` | `controlled_term` | Confidence interval, credible interval, standard error, or another uncertainty representation. |
| `level` | `number` | Coverage level such as 0.95. |
| `lower_bound` | `number` | Lower interval bound. |
| `upper_bound` | `number` | Upper interval bound. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[EffectEstimate]] → `has_precision_estimate`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A quantitative expression of uncertainty around an EffectEstimate, such as a confidence or credible interval.",
    "id": "consort-class-precision-estimate",
    "kind": "domain_class",
    "label": "Precision Estimate",
    "name": "PrecisionEstimate",
    "parent": "OntologyEntity",
    "properties": {
      "interval_type": {
        "definition": "Confidence interval, credible interval, standard error, or another uncertainty representation.",
        "required": true,
        "value_type": "controlled_term"
      },
      "level": {
        "definition": "Coverage level such as 0.95.",
        "required": false,
        "value_type": "number"
      },
      "lower_bound": {
        "definition": "Lower interval bound.",
        "required": false,
        "value_type": "number"
      },
      "upper_bound": {
        "definition": "Upper interval bound.",
        "required": false,
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
