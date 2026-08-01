---
id: consort-class-intervention
type: OntologyClass
class_name: Intervention
kind: domain_class
status: reviewed
aliases:
  - Intervention
tags:
  - consort/2025
  - ontology/domain-class
---

# Intervention

> [!definition]
> A treatment, exposure, strategy, or care process assigned or delivered within a trial arm.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `description` | `string` | Replicable description of intervention components and delivery. |
| `name` | `string` | Name of the intervention. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[TrialArm]] → `has_intervention`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A treatment, exposure, strategy, or care process assigned or delivered within a trial arm.",
    "id": "consort-class-intervention",
    "kind": "domain_class",
    "label": "Intervention",
    "name": "Intervention",
    "parent": "OntologyEntity",
    "properties": {
      "description": {
        "definition": "Replicable description of intervention components and delivery.",
        "required": false,
        "value_type": "string"
      },
      "name": {
        "definition": "Name of the intervention.",
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
