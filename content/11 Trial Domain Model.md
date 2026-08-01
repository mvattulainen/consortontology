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

| Class                            | Parent                   | Stable ID                                      |
| -------------------------------- | ------------------------ | ---------------------------------------------- |
| [[RandomisedTrial]]              | `OntologyEntity`         | `consort-class-randomised-trial`               |
| [[TrialDesign]]                  | `OntologyEntity`         | `consort-class-trial-design`                   |
| [[TrialArm]]                     | `OntologyEntity`         | `consort-class-trial-arm`                      |
| [[Participant]]                  | `OntologyEntity`         | `consort-class-participant`                    |
| [[Intervention]]                 | `OntologyEntity`         | `consort-class-intervention`                   |
| [[Comparator]]                   | `OntologyEntity`         | `consort-class-comparator`                     |
| [[OutcomeSpecification]]         | `OntologyEntity`         | `consort-class-outcome-specification`          |
| [[PrimaryOutcome]]               | [[OutcomeSpecification]] | `consort-class-primary-outcome`                |
| [[SecondaryOutcome]]             | [[OutcomeSpecification]] | `consort-class-secondary-outcome`              |
| [[HarmsOutcome]]                 | [[OutcomeSpecification]] | `consort-class-harms-outcome`                  |
| [[RandomAllocationProcess]]      | `OntologyEntity`         | `consort-class-random-allocation-process`      |
| [[AllocationConcealmentProcess]] | `OntologyEntity`         | `consort-class-allocation-concealment-process` |
| [[BlindingProcess]]              | `OntologyEntity`         | `consort-class-blinding-process`               |
| [[TrialRole]]                    | `OntologyEntity`         | `consort-class-trial-role`                     |
| [[ParticipantFlowObservation]]   | `OntologyEntity`         | `consort-class-participant-flow-observation`   |
| [[OutcomeResult]]                | `OntologyEntity`         | `consort-class-outcome-result`                 |
| [[GroupResult]]                  | `OntologyEntity`         | `consort-class-group-result`                   |
| [[EffectEstimate]]               | `OntologyEntity`         | `consort-class-effect-estimate`                |
| [[PrecisionEstimate]]            | `OntologyEntity`         | `consort-class-precision-estimate`             |

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

## Structural rules

These rules validate future populated trial instances against the domain model. They are ontology-authored structural constraints, not additional CONSORT 2025 reporting items. All are initially `draft` pending review against concrete implementation use cases.

| ID       | Rule                         | Structural constraint                                                                                                                                                     |
| -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `TDM-01` | Trial structure              | Every [[RandomisedTrial]] has exactly one [[TrialDesign]] and at least two [[TrialArm\|trial arms]].                                                                      |
| `TDM-02` | Arm identification           | Every [[TrialArm]] has one `arm_identifier` and one human-readable `label`.                                                                                               |
| `TDM-03` | Participant assignment       | Every enrolled [[Participant]] is assigned to exactly one arm belonging to the same trial.                                                                                |
| `TDM-04` | Arm intervention             | Every trial arm has at least one [[Intervention]], and every intervention has a `name`.                                                                                   |
| `TDM-05` | Outcome definition           | Every [[OutcomeSpecification]] has an identifier, measurement variable, role, analysis metric, aggregation method, and time point.                                        |
| `TDM-06` | Primary outcome designation  | Every randomised trial has at least one [[PrimaryOutcome]], and each primary outcome is also one of the trial's outcome specifications.                                   |
| `TDM-07` | Randomisation processes      | Every randomised trial has exactly one [[RandomAllocationProcess]] and exactly one [[AllocationConcealmentProcess]], each with its required method description.           |
| `TDM-08` | Result linkage               | Every [[OutcomeResult]] refers to exactly one outcome specification and has at least one [[GroupResult]]; every group result refers to exactly one arm of the same trial. |
| `TDM-09` | Effect and precision         | Every [[EffectEstimate]] has a measure type and numeric value; every attached [[PrecisionEstimate]] states its interval type.                                             |
| `TDM-10` | Participant-flow observation | Every [[ParticipantFlowObservation]] has a stage and a non-negative count.                                                                                                |

The machine-readable expressions and stable IDs are maintained in [`_data/rules.yaml`](./_data/rules.yaml) and indexed in the [[06 Rule Catalog|Rule Catalog]].

## Layer boundary

> [!warning]
> These are class definitions, not populated trial facts. Article evidence, extracted trial individuals, and validation results remain deferred to later layers.
