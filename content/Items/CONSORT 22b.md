---
id: consort-2025-item-22b
type: ChecklistItem
item_number: 22b
label: "Post-randomisation losses and exclusions with reasons"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-participant-flow
status: reviewed
order: 32
requirement_count: 2
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 22b: Post-randomisation losses and exclusions with reasons

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand post-randomisation losses and exclusions with reasons. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "For each group, losses and exclusions after randomisation, together with reasons" — CONSORT 2025 expanded checklist, item 22b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Participant flow|Participant flow]]
- **Domain classes:** [[ParticipantFlowObservation]], [[Participant]], [[TrialArm]]

## Atomic requirements

1. **Number lost to follow-up.** Report number lost to follow-up. (`must`; expects `number`; scoped by `consort-2025-scope-item-22b-each-trial-group`)
2. **Number excluded from the main primary-outcome analysis with exact reasons.** Report number excluded from the main primary-outcome analysis with exact reasons. (`must`; expects `number`; scoped by `consort-2025-scope-item-22b-each-trial-group`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

- **Each trial group:** repeat over `trial.group`.

## Relations to other guideline elements

- [[CONSORT 22a]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 22b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-22b-r01"}},{"require":{"ref":"consort-2025-item-22b-r02"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "For each group, losses and exclusions after randomisation, together with reasons",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-22b",
    "item_number": "22b",
    "label": "Post-randomisation losses and exclusions with reasons",
    "order": 32,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand post-randomisation losses and exclusions with reasons. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-22a"
      ],
      "governed_by": [
        "consort-2025-rule-item-22b-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-22b-r01",
        "consort-2025-item-22b-r02"
      ],
      "targets_domain_class": [
        "consort-class-participant-flow-observation",
        "consort-class-participant",
        "consort-class-trial-arm"
      ]
    },
    "requirements": [
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number lost to follow-up",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22b",
        "requirement_text": "Report number lost to follow-up.",
        "scope": "consort-2025-scope-item-22b-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22b",
              "page": 10,
              "row_label": "Number lost to follow-up"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number lost to follow-up",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number excluded from the main primary-outcome analysis with exact reasons",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22b",
        "requirement_text": "Report number excluded from the main primary-outcome analysis with exact reasons.",
        "scope": "consort-2025-scope-item-22b-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22b",
              "page": 10,
              "row_label": "Number excluded from the main primary-outcome analysis with exact reasons"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number excluded from the main primary-outcome analysis with exact reasons",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-22b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22b-r02"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-22b-completeness",
        "label": "Item 22b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "trial.group",
        "id": "consort-2025-scope-item-22b-each-trial-group",
        "label": "Each trial group",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-results",
    "source_references": [
      {
        "locator": {
          "item_number": "22b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "22b",
          "page": 10
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "For each group, losses and exclusions after randomisation, together with reasons",
    "status": "reviewed",
    "topic": "consort-2025-topic-participant-flow",
    "type": "ChecklistItem"
  },
  "schema_version": "1.0"
}
```
<!-- END:CONSORT-ONTOLOGY -->

## Source provenance

> [!source]
> Formalized from the official CONSORT 2025 checklist and expanded checklist. Each atomic requirement contains an item-and-page locator. See [[10 Source and Licensing Notes]].

## Maintainer notes

Status is `reviewed`. This is a reporting requirement model, not a judgment of methodological quality.
