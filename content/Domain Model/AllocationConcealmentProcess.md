---
id: consort-class-allocation-concealment-process
type: OntologyClass
class_name: AllocationConcealmentProcess
kind: domain_class
status: reviewed
aliases:
  - Allocation Concealment Process
tags:
  - consort/2025
  - ontology/domain-class
---

# AllocationConcealmentProcess

> [!definition]
> The process used to prevent foreknowledge of upcoming trial-arm assignments before allocation.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `concealment_mechanism` | `method_description` | Mechanism that prevents foreknowledge of assignment. |

## Relations

### Outgoing

- `performed_by_role` → [[TrialRole]]

### Incoming

- [[RandomisedTrial]] → `uses_allocation_concealment_process`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "The process used to prevent foreknowledge of upcoming trial-arm assignments before allocation.",
    "id": "consort-class-allocation-concealment-process",
    "kind": "domain_class",
    "label": "Allocation Concealment Process",
    "name": "AllocationConcealmentProcess",
    "parent": "OntologyEntity",
    "properties": {
      "concealment_mechanism": {
        "definition": "Mechanism that prevents foreknowledge of assignment.",
        "required": true,
        "value_type": "method_description"
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
