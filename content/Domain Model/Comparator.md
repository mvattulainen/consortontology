---
id: consort-class-comparator
type: OntologyClass
class_name: Comparator
kind: domain_class
status: reviewed
aliases:
  - Comparator
tags:
  - consort/2025
  - ontology/domain-class
---

# Comparator

> [!definition]
> The intervention, usual care, placebo, or other condition against which another intervention is evaluated.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `comparator_type` | `controlled_term` | Comparator category such as placebo, usual care, or active comparator. |
| `name` | `string` | Name of the comparator. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[RandomisedTrial]] → `has_comparator`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "The intervention, usual care, placebo, or other condition against which another intervention is evaluated.",
    "id": "consort-class-comparator",
    "kind": "domain_class",
    "label": "Comparator",
    "name": "Comparator",
    "parent": "OntologyEntity",
    "properties": {
      "comparator_type": {
        "definition": "Comparator category such as placebo, usual care, or active comparator.",
        "required": false,
        "value_type": "controlled_term"
      },
      "name": {
        "definition": "Name of the comparator.",
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
