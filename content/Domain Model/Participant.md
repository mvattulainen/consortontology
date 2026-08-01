---
id: consort-class-participant
type: OntologyClass
class_name: Participant
kind: domain_class
status: reviewed
aliases:
  - Participant
tags:
  - consort/2025
  - ontology/domain-class
---

# Participant

> [!definition]
> A person or other eligible unit enrolled in a randomised trial.

- **Parent class:** [[04 Class Catalog|OntologyEntity]]
- **Layer:** Trial-domain interface within the Layer A guideline ontology
- **Instance policy:** No trial-specific individuals are populated in this release.

## Properties

| Property | Value type | Definition |
|---|---|---|
| `participant_identifier` | `identifier` | Pseudonymous or external participant identifier. |

## Relations

### Outgoing

- `assigned_to_arm` → [[TrialArm]]

### Incoming

- [[RandomisedTrial]] → `enrols_participant`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "abstract": false,
    "definition": "A person or other eligible unit enrolled in a randomised trial.",
    "id": "consort-class-participant",
    "kind": "domain_class",
    "label": "Participant",
    "name": "Participant",
    "parent": "OntologyEntity",
    "properties": {
      "participant_identifier": {
        "definition": "Pseudonymous or external participant identifier.",
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
