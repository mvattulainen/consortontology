---
id: consort-class-trial-arm
type: OntologyClass
class_name: TrialArm
kind: domain_class
status: reviewed
aliases:
  - Trial Arm
tags:
  - consort/2025
  - ontology/domain-class
---

# TrialArm

> [!definition]
> A named group to which participants or other units can be assigned and for which an intervention or comparator is specified.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `arm_identifier` | `identifier` | Stable identifier for the trial arm. |
| `label` | `string` | Human-readable arm label. |

## Relations

### Outgoing

- `has_intervention` → [[Intervention]]

### Incoming

- [[RandomisedTrial]] → `has_arm`
- [[Participant]] → `assigned_to_arm`
- [[GroupResult]] → `result_for_arm`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A named group to which participants or other units can be assigned and for which an intervention or comparator is specified.",
    "id": "consort-class-trial-arm",
    "kind": "domain_class",
    "label": "Trial Arm",
    "name": "TrialArm",
    "parent": "OntologyEntity",
    "properties": {
      "arm_identifier": {
        "definition": "Stable identifier for the trial arm.",
        "required": true,
        "value_type": "identifier"
      },
      "label": {
        "definition": "Human-readable arm label.",
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
