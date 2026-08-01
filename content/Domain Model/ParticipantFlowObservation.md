---
id: consort-class-participant-flow-observation
type: OntologyClass
class_name: ParticipantFlowObservation
kind: domain_class
status: reviewed
aliases:
  - Participant Flow Observation
tags:
  - consort/2025
  - ontology/domain-class
---

# ParticipantFlowObservation

> [!definition]
> A count or status observation about participants at a defined trial-flow stage, optionally with reasons.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `count` | `number` | Number of participants observed at the stage. |
| `reason` | `string` | Reason associated with an exclusion, loss, or discontinuation. |
| `stage` | `controlled_term` | Trial-flow stage such as assessed, randomised, treated, followed up, or analysed. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[RandomisedTrial]] → `has_flow_observation`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A count or status observation about participants at a defined trial-flow stage, optionally with reasons.",
    "id": "consort-class-participant-flow-observation",
    "kind": "domain_class",
    "label": "Participant Flow Observation",
    "name": "ParticipantFlowObservation",
    "parent": "OntologyEntity",
    "properties": {
      "count": {
        "definition": "Number of participants observed at the stage.",
        "required": true,
        "value_type": "number"
      },
      "reason": {
        "definition": "Reason associated with an exclusion, loss, or discontinuation.",
        "required": false,
        "value_type": "string"
      },
      "stage": {
        "definition": "Trial-flow stage such as assessed, randomised, treated, followed up, or analysed.",
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
