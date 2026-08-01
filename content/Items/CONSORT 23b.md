---
id: consort-2025-item-23b
type: ChecklistItem
item_number: 23b
label: "Reason the trial ended or stopped, if relevant"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-recruitment
status: reviewed
order: 34
requirement_count: 3
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 23b: Reason the trial ended or stopped, if relevant

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand reason the trial ended or stopped, if relevant. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "If relevant, why the trial ended or was stopped" — CONSORT 2025 expanded checklist, item 23b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Recruitment|Recruitment]]
- **Domain classes:** [[RandomisedTrial]], [[TrialRole]]

## Atomic requirements

1. **Reason for stopping before planned completion.** Report reason for stopping before planned completion. (`conditional_must`; expects `reason`; when `consort-2025-condition-trial-stopped-early`)
2. **Who decided to stop.** Report who decided to stop. (`conditional_must`; expects `person_or_role`; when `consort-2025-condition-trial-stopped-early`)
3. **Funder's role in the stopping decision.** Report funder's role in the stopping decision. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-trial-stopped-early`)

## Applicability

- **Trial stopped before planned completion:** `{"equals":true,"fact":"trial.stopped_early"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 16b]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 23b applicability:** `{"implies":{"if":{"equals":true,"fact":"trial.stopped_early"},"then":{"activate":{"ref":"consort-2025-item-23b"}}}}`
- **Item 23b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-23b-r01"}},{"require":{"ref":"consort-2025-item-23b-r02"}},{"require":{"ref":"consort-2025-item-23b-r03"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "objective",
        "expression": {
          "equals": true,
          "fact": "trial.stopped_early"
        },
        "id": "consort-2025-condition-trial-stopped-early",
        "label": "Trial stopped before planned completion",
        "source_references": [
          {
            "locator": {
              "item_number": "23b",
              "page": 10,
              "quoted_fragment": "If relevant, why the trial ended or was stopped"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "If relevant, why the trial ended or was stopped",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-23b",
    "item_number": "23b",
    "label": "Reason the trial ended or stopped, if relevant",
    "order": 34,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand reason the trial ended or stopped, if relevant. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-16b"
      ],
      "governed_by": [
        "consort-2025-rule-item-23b-applicability",
        "consort-2025-rule-item-23b-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-trial-stopped-early"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-23b-r01",
        "consort-2025-item-23b-r02",
        "consort-2025-item-23b-r03"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-trial-stopped-early",
        "id": "consort-2025-item-23b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Reason for stopping before planned completion",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-23b",
        "requirement_text": "Report reason for stopping before planned completion.",
        "source_references": [
          {
            "locator": {
              "item_number": "23b",
              "page": 10,
              "row_label": "Reason for stopping before planned completion"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Reason for stopping before planned completion",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "applicability_condition": "consort-2025-condition-trial-stopped-early",
        "id": "consort-2025-item-23b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who decided to stop",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-23b",
        "requirement_text": "Report who decided to stop.",
        "source_references": [
          {
            "locator": {
              "item_number": "23b",
              "page": 10,
              "row_label": "Who decided to stop"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who decided to stop",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "applicability_condition": "consort-2025-condition-trial-stopped-early",
        "id": "consort-2025-item-23b-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Funder's role in the stopping decision",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-23b",
        "requirement_text": "Report funder's role in the stopping decision.",
        "source_references": [
          {
            "locator": {
              "item_number": "23b",
              "page": 10,
              "row_label": "Funder's role in the stopping decision"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Funder's role in the stopping decision",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "implies": {
            "if": {
              "equals": true,
              "fact": "trial.stopped_early"
            },
            "then": {
              "activate": {
                "ref": "consort-2025-item-23b"
              }
            }
          }
        },
        "id": "consort-2025-rule-item-23b-applicability",
        "label": "Item 23b applicability",
        "rule_kind": "conditional_item",
        "status": "reviewed",
        "type": "NormativeRule"
      },
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-23b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-23b-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-23b-r03"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-23b-completeness",
        "label": "Item 23b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-results",
    "source_references": [
      {
        "locator": {
          "item_number": "23b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "23b",
          "page": 10
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "If relevant, why the trial ended or was stopped",
    "status": "reviewed",
    "topic": "consort-2025-topic-recruitment",
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
