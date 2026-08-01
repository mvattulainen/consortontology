---
id: consort-class-randomised-trial
type: OntologyClass
class_name: RandomisedTrial
kind: domain_class
status: reviewed
aliases:
  - Randomised Trial
tags:
  - consort/2025
  - ontology/domain-class
---

# RandomisedTrial

> [!definition]
> A study in which participants or other units are assigned to trial arms using a random allocation process.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `public_title` | `string` | Public title of the trial. |
| `trial_identifier` | `identifier` | Stable identifier for the trial. |

## Relations

### Outgoing

- `has_trial_design` → [[TrialDesign]]
- `has_arm` → [[TrialArm]]
- `enrols_participant` → [[Participant]]
- `has_comparator` → [[Comparator]]
- `specifies_outcome` → [[OutcomeSpecification]]
- `has_primary_outcome` → [[PrimaryOutcome]]
- `has_secondary_outcome` → [[SecondaryOutcome]]
- `has_harms_outcome` → [[HarmsOutcome]]
- `uses_random_allocation_process` → [[RandomAllocationProcess]]
- `uses_allocation_concealment_process` → [[AllocationConcealmentProcess]]
- `uses_blinding_process` → [[BlindingProcess]]
- `has_trial_role` → [[TrialRole]]
- `has_flow_observation` → [[ParticipantFlowObservation]]
- `has_outcome_result` → [[OutcomeResult]]

### Incoming

- None defined.

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A study in which participants or other units are assigned to trial arms using a random allocation process.",
    "id": "consort-class-randomised-trial",
    "kind": "domain_class",
    "label": "Randomised Trial",
    "name": "RandomisedTrial",
    "parent": "OntologyEntity",
    "properties": {
      "public_title": {
        "definition": "Public title of the trial.",
        "required": false,
        "value_type": "string"
      },
      "trial_identifier": {
        "definition": "Stable identifier for the trial.",
        "required": false,
        "value_type": "identifier"
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
