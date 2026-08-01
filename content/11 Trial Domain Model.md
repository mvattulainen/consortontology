---
id: consort-2025-trial-domain-model
type: OntologyEntity
label: "Trial Domain Model"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# Trial Domain Model

The following 19 concepts are first-class ontology classes with stable IDs, definitions, properties, relations, graph nodes, and individual Obsidian notes. They describe the information interface required by future evidence and validation layers. No trial-specific individuals are populated in Layer A.

## Classes

| Class | Parent | Stable ID |
|---|---|---|
| [[RandomisedTrial]] | `OntologyEntity` | `consort-class-randomised-trial` |
| [[TrialDesign]] | `OntologyEntity` | `consort-class-trial-design` |
| [[TrialArm]] | `OntologyEntity` | `consort-class-trial-arm` |
| [[Participant]] | `OntologyEntity` | `consort-class-participant` |
| [[Intervention]] | `OntologyEntity` | `consort-class-intervention` |
| [[Comparator]] | `OntologyEntity` | `consort-class-comparator` |
| [[OutcomeSpecification]] | `OntologyEntity` | `consort-class-outcome-specification` |
| [[PrimaryOutcome]] | [[OutcomeSpecification]] | `consort-class-primary-outcome` |
| [[SecondaryOutcome]] | [[OutcomeSpecification]] | `consort-class-secondary-outcome` |
| [[HarmsOutcome]] | [[OutcomeSpecification]] | `consort-class-harms-outcome` |
| [[RandomAllocationProcess]] | `OntologyEntity` | `consort-class-random-allocation-process` |
| [[AllocationConcealmentProcess]] | `OntologyEntity` | `consort-class-allocation-concealment-process` |
| [[BlindingProcess]] | `OntologyEntity` | `consort-class-blinding-process` |
| [[TrialRole]] | `OntologyEntity` | `consort-class-trial-role` |
| [[ParticipantFlowObservation]] | `OntologyEntity` | `consort-class-participant-flow-observation` |
| [[OutcomeResult]] | `OntologyEntity` | `consort-class-outcome-result` |
| [[GroupResult]] | `OntologyEntity` | `consort-class-group-result` |
| [[EffectEstimate]] | `OntologyEntity` | `consort-class-effect-estimate` |
| [[PrecisionEstimate]] | `OntologyEntity` | `consort-class-precision-estimate` |

## Core relationships

```mermaid
classDiagram
  RandomisedTrial --> TrialDesign : has_trial_design
  RandomisedTrial --> TrialArm : has_arm
  RandomisedTrial --> Participant : enrols_participant
  TrialArm --> Intervention : has_intervention
  RandomisedTrial --> Comparator : has_comparator
  RandomisedTrial --> OutcomeSpecification : specifies_outcome
  OutcomeSpecification <|-- PrimaryOutcome
  OutcomeSpecification <|-- SecondaryOutcome
  OutcomeSpecification <|-- HarmsOutcome
  RandomisedTrial --> RandomAllocationProcess : uses
  RandomisedTrial --> AllocationConcealmentProcess : uses
  RandomisedTrial --> BlindingProcess : uses
  RandomisedTrial --> TrialRole : has_trial_role
  RandomisedTrial --> ParticipantFlowObservation : has_flow_observation
  RandomisedTrial --> OutcomeResult : has_outcome_result
  OutcomeResult --> GroupResult : has_group_result
  OutcomeResult --> EffectEstimate : has_effect_estimate
  EffectEstimate --> PrecisionEstimate : has_precision_estimate
```

## Layer boundary

> [!warning]
> These are class definitions, not populated trial facts. Article evidence, extracted trial individuals, and validation results remain deferred to later layers.
