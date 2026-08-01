---
id: consort-2025-controlled-vocabularies
type: OntologyEntity
label: "Controlled Vocabularies"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# Controlled Vocabularies

## normative_strength

| Value | Meaning |
|---|---|
| `must` | Unconditional minimum reporting requirement |
| `conditional_must` | Required when its applicability condition is satisfied |
| `should` | Recommended but excluded from strict minimum completeness by default |
| `may` | Optional information |
| `explanatory` | Clarification, rationale, or example |

## condition_kind

| Value | Meaning |
|---|---|
| `objective` | Determined from a factual condition |
| `type_dependent` | Determined by an entity type |
| `presence_dependent` | Triggered when a procedure or analysis was done |
| `contextual` | Requires an explicit relevance or appropriateness interpretation |
| `alternative` | One of several reporting patterns may satisfy the source |

## logical_operator

| Value | Meaning |
|---|---|
| `all_of` | Every member is required |
| `any_of` | At least one member is required |
| `one_of` | Exactly one member is required |
| `at_least` | A minimum count is required |
| `sequence` | Members form an ordered sequence |

## scope_type

| Value | Meaning |
|---|---|
| `single` | Evaluate once |
| `for_each` | Evaluate for every member of the domain |
| `at_least_one` | Evaluate for at least one member |
| `all_declared` | Evaluate over every declared member |

## value_expectation

| Value | Meaning |
|---|---|
| `boolean_statement` | An explicit yes/no or occurred/did-not-occur statement |
| `identifier` | A stable identifier |
| `url` | A resolvable web location |
| `date` | A date |
| `number` | A numeric value |
| `percentage` | A percentage |
| `duration` | A duration |
| `controlled_term` | A value from an enumerated vocabulary |
| `free_text_description` | A narrative description |
| `person_or_role` | A named person or functional role |
| `method_description` | A reproducible method description |
| `reason` | A reason or justification |
| `citation` | A bibliographic citation |
| `software_name` | The name and, where relevant, version of software |

## entity_status

| Value | Meaning |
|---|---|
| `draft` | Not yet reviewed |
| `reviewed` | Ontology and source mapping reviewed internally |
| `approved` | Approved after ontology and CONSORT content review |
| `deprecated` | Retained for identity but no longer current |

## source_type

| Value | Meaning |
|---|---|
| `guideline_statement` | Published normative statement |
| `expanded_checklist` | Official detailed checklist |
| `explanation_and_elaboration` | Interpretive companion publication |
| `official_website` | Official website |

The parseable catalog is `_data/controlled-vocabularies.yaml`.
