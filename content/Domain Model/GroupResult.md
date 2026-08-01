---
id: consort-class-group-result
type: OntologyClass
class_name: GroupResult
kind: domain_class
status: reviewed
aliases:
  - Group Result
tags:
  - consort/2025
  - ontology/domain-class
---

# GroupResult

> [!definition]
> The result observed for a particular TrialArm within an OutcomeResult.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `unit` | `string` | Unit or scale of the result. |
| `value` | `number|string` | Observed or summarized result value. |

## Relations

### Outgoing

- `result_for_arm` → [[TrialArm]]

### Incoming

- [[OutcomeResult]] → `has_group_result`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "The result observed for a particular TrialArm within an OutcomeResult.",
    "id": "consort-class-group-result",
    "kind": "domain_class",
    "label": "Group Result",
    "name": "GroupResult",
    "parent": "OntologyEntity",
    "properties": {
      "unit": {
        "definition": "Unit or scale of the result.",
        "required": false,
        "value_type": "string"
      },
      "value": {
        "definition": "Observed or summarized result value.",
        "required": true,
        "value_type": "number|string"
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
