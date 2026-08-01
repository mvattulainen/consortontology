---
id: consort-class-random-allocation-process
type: OntologyClass
class_name: RandomAllocationProcess
kind: domain_class
status: reviewed
aliases:
  - Random Allocation Process
tags:
  - consort/2025
  - ontology/domain-class
---

# RandomAllocationProcess

> [!definition]
> The process used to generate and implement a random allocation sequence.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `restriction_type` | `controlled_term` | Restriction such as blocking, stratification, or minimisation. |
| `sequence_generation_method` | `method_description` | Method used to generate the random allocation sequence. |

## Relations

### Outgoing

- `performed_by_role` → [[TrialRole]]

### Incoming

- [[RandomisedTrial]] → `uses_random_allocation_process`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "The process used to generate and implement a random allocation sequence.",
    "id": "consort-class-random-allocation-process",
    "kind": "domain_class",
    "label": "Random Allocation Process",
    "name": "RandomAllocationProcess",
    "parent": "OntologyEntity",
    "properties": {
      "restriction_type": {
        "definition": "Restriction such as blocking, stratification, or minimisation.",
        "required": false,
        "value_type": "controlled_term"
      },
      "sequence_generation_method": {
        "definition": "Method used to generate the random allocation sequence.",
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
