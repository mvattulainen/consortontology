---
id: consort-class-trial-role
type: OntologyClass
class_name: TrialRole
kind: domain_class
status: reviewed
aliases:
  - Trial Role
tags:
  - consort/2025
  - ontology/domain-class
---

# TrialRole

> [!definition]
> A defined responsibility performed by a person, group, or organization in trial design, conduct, analysis, or reporting.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `actor_label` | `string` | Human-readable person, group, or organization label. |
| `role_type` | `controlled_term` | Responsibility such as sequence generator, enroler, assessor, analyst, or funder. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[RandomisedTrial]] → `has_trial_role`
- [[RandomAllocationProcess]] or [[AllocationConcealmentProcess]] or [[BlindingProcess]] → `performed_by_role`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A defined responsibility performed by a person, group, or organization in trial design, conduct, analysis, or reporting.",
    "id": "consort-class-trial-role",
    "kind": "domain_class",
    "label": "Trial Role",
    "name": "TrialRole",
    "parent": "OntologyEntity",
    "properties": {
      "actor_label": {
        "definition": "Human-readable person, group, or organization label.",
        "required": false,
        "value_type": "string"
      },
      "role_type": {
        "definition": "Responsibility such as sequence generator, enroler, assessor, analyst, or funder.",
        "required": true,
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
