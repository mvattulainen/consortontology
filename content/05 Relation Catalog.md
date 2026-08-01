---
id: consort-2025-relation-catalog
type: OntologyEntity
label: "Relation Catalog"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# Relation Catalog

| Relation | Domain | Range | Inverse | Definition |
|---|---|---|---|---|
| `has_version` | ReportingGuideline | GuidelineVersion | `version_of` | Guideline has a released version |
| `version_of` | GuidelineVersion | ReportingGuideline | `has_version` | Inverse of has_version |
| `has_section` | GuidelineVersion | ChecklistSection | `section_of` | Version contains a top-level section |
| `section_of` | ChecklistSection | GuidelineVersion | `has_section` | Inverse of has_section |
| `has_topic` | ChecklistSection | ChecklistTopic | `topic_of` | Section contains a topic |
| `topic_of` | ChecklistTopic | ChecklistSection | `has_topic` | Inverse of has_topic |
| `contains_item` | ChecklistSection|ChecklistTopic | ChecklistItem | `item_of` | Organizational containment |
| `item_of` | ChecklistItem | ChecklistSection|ChecklistTopic | `contains_item` | Inverse containment |
| `has_atomic_requirement` | ChecklistItem | AtomicRequirement | `requirement_of` | Item decomposes into a requirement |
| `requirement_of` | AtomicRequirement | ChecklistItem | `has_atomic_requirement` | Inverse decomposition |
| `has_requirement_group` | ChecklistItem | RequirementGroup | — | Item contains a logical group |
| `has_member` | RequirementGroup | AtomicRequirement|RequirementGroup | — | Group membership |
| `has_applicability_condition` | ChecklistItem|RequirementGroup|AtomicRequirement | ApplicabilityCondition | — | Entity is active under a condition |
| `has_scope` | AtomicRequirement|RequirementGroup | ScopeDefinition | — | Requirement repeats over a domain |
| `governed_by` | ChecklistItem|AtomicRequirement | NormativeRule | — | Rule applies to entity |
| `references_requirement` | NormativeRule | AtomicRequirement | — | Rule operand refers to requirement |
| `cross_references` | OntologyEntity | OntologyEntity | — | Informative or semantic cross-reference |
| `precedes` | ChecklistItem | ChecklistItem | — | Ordering relation |
| `derived_from` | OntologyEntity | SourceReference | — | Entity was formalized from source |
| `has_source_locator` | OntologyEntity | SourceLocator | — | Precise source location |
| `supersedes` | OntologyEntity | OntologyEntity | — | New entity replaces older entity |
| `refines` | ExtensionHook|OntologyEntity | OntologyEntity | — | Adds specificity without replacing identity |
| `modifies` | ExtensionHook | OntologyEntity | — | Changes applicability or requirements |
| `subclass_of` | OntologyClass | OntologyClass | — | Class inherits the meaning and constraints of a parent class |
| `targets_domain_class` | ChecklistItem|AtomicRequirement | OntologyClass | — | Guideline element specifies reporting about a domain class |
| `has_trial_design` | RandomisedTrial | TrialDesign | `design_of_trial` | Trial has a structural design |
| `has_arm` | RandomisedTrial | TrialArm | `arm_of_trial` | Trial contains a trial arm |
| `enrols_participant` | RandomisedTrial | Participant | `participates_in_trial` | Trial enrols a participant |
| `assigned_to_arm` | Participant | TrialArm | `has_assigned_participant` | Participant is assigned to a trial arm |
| `has_intervention` | TrialArm | Intervention | `intervention_of_arm` | Trial arm specifies or receives an intervention |
| `has_comparator` | RandomisedTrial | Comparator | `comparator_of_trial` | Trial identifies a comparator condition |
| `specifies_outcome` | RandomisedTrial | OutcomeSpecification | `outcome_of_trial` | Trial prespecifies an outcome |
| `has_primary_outcome` | RandomisedTrial | PrimaryOutcome | `primary_outcome_of_trial` | Trial designates a primary outcome |
| `has_secondary_outcome` | RandomisedTrial | SecondaryOutcome | `secondary_outcome_of_trial` | Trial designates a secondary outcome |
| `has_harms_outcome` | RandomisedTrial | HarmsOutcome | `harms_outcome_of_trial` | Trial specifies a harms outcome |
| `uses_random_allocation_process` | RandomisedTrial | RandomAllocationProcess | `random_allocation_process_of` | Trial uses a random allocation process |
| `uses_allocation_concealment_process` | RandomisedTrial | AllocationConcealmentProcess | `allocation_concealment_process_of` | Trial uses an allocation concealment process |
| `uses_blinding_process` | RandomisedTrial | BlindingProcess | `blinding_process_of` | Trial uses or evaluates a blinding process |
| `has_trial_role` | RandomisedTrial | TrialRole | `role_in_trial` | Trial defines a responsibility performed by an actor |
| `has_flow_observation` | RandomisedTrial | ParticipantFlowObservation | `flow_observation_of_trial` | Trial has an observation at a participant-flow stage |
| `has_outcome_result` | RandomisedTrial | OutcomeResult | `outcome_result_of_trial` | Trial reports a result for an outcome |
| `result_for_outcome` | OutcomeResult | OutcomeSpecification | `has_result` | Outcome result instantiates an outcome specification |
| `has_group_result` | OutcomeResult | GroupResult | `group_result_of` | Outcome result contains a result for a trial arm |
| `result_for_arm` | GroupResult | TrialArm | `has_group_result_for_arm` | Group result describes one trial arm |
| `has_effect_estimate` | OutcomeResult | EffectEstimate | `effect_estimate_of` | Outcome result includes an effect estimate |
| `has_precision_estimate` | EffectEstimate | PrecisionEstimate | `precision_estimate_of` | Effect estimate includes a precision estimate |
| `performed_by_role` | RandomAllocationProcess|AllocationConcealmentProcess|BlindingProcess | TrialRole | `performs_process_role` | Process is performed or governed by a trial role |

The parseable catalog is `_data/relations.yaml`.
