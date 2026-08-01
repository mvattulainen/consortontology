---
id: consort-class-blinding-process
type: OntologyClass
class_name: BlindingProcess
kind: domain_class
status: reviewed
aliases:
  - Blinding Process
tags:
  - consort/2025
  - ontology/domain-class
---

# BlindingProcess

> [!definition]
> The process used to establish, maintain, evaluate, or break blinding to trial-arm assignment.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `mechanism` | `method_description` | Mechanism used to establish blinding. |
| `status` | `controlled_term` | Current or reported blinding status. |

## Relations

### Outgoing

- `performed_by_role` → [[TrialRole]]

### Incoming

- [[RandomisedTrial]] → `uses_blinding_process`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "The process used to establish, maintain, evaluate, or break blinding to trial-arm assignment.",
    "id": "consort-class-blinding-process",
    "kind": "domain_class",
    "label": "Blinding Process",
    "name": "BlindingProcess",
    "parent": "OntologyEntity",
    "properties": {
      "mechanism": {
        "definition": "Mechanism used to establish blinding.",
        "required": false,
        "value_type": "method_description"
      },
      "status": {
        "definition": "Current or reported blinding status.",
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
