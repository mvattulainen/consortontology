---
id: consort-class-outcome-specification
type: OntologyClass
class_name: OutcomeSpecification
kind: domain_class
status: reviewed
aliases:
  - Outcome Specification
tags:
  - consort/2025
  - ontology/domain-class
---

# OutcomeSpecification

> [!definition]
> A prespecified definition of an outcome, including role, variable, metric, aggregation method, time point, and assessor.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `aggregation_method` | `controlled_term` | Group-level aggregation method. |
| `analysis_metric` | `controlled_term` | Participant-level metric such as change from baseline. |
| `assessor_role` | `TrialRole` | Role responsible for outcome assessment. |
| `measurement_variable` | `string` | Specific variable measured. |
| `outcome_identifier` | `identifier` | Stable identifier for the outcome. |
| `role` | `controlled_term` | Primary, secondary, or other outcome role. |
| `time_point` | `string` | Time point of interest. |

## Relations

### Outgoing

- None defined.

### Incoming

- [[RandomisedTrial]] → `specifies_outcome`
- [[OutcomeResult]] → `result_for_outcome`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A prespecified definition of an outcome, including role, variable, metric, aggregation method, time point, and assessor.",
    "id": "consort-class-outcome-specification",
    "kind": "domain_class",
    "label": "Outcome Specification",
    "name": "OutcomeSpecification",
    "parent": "OntologyEntity",
    "properties": {
      "aggregation_method": {
        "definition": "Group-level aggregation method.",
        "required": true,
        "value_type": "controlled_term"
      },
      "analysis_metric": {
        "definition": "Participant-level metric such as change from baseline.",
        "required": true,
        "value_type": "controlled_term"
      },
      "assessor_role": {
        "definition": "Role responsible for outcome assessment.",
        "required": false,
        "value_type": "TrialRole"
      },
      "measurement_variable": {
        "definition": "Specific variable measured.",
        "required": true,
        "value_type": "string"
      },
      "outcome_identifier": {
        "definition": "Stable identifier for the outcome.",
        "required": true,
        "value_type": "identifier"
      },
      "role": {
        "definition": "Primary, secondary, or other outcome role.",
        "required": true,
        "value_type": "controlled_term"
      },
      "time_point": {
        "definition": "Time point of interest.",
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
