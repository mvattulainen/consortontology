---
id: consort-2025-item-24b
type: ChecklistItem
item_number: 24b
label: "Concomitant care received by each group"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-intervention-and-comparator-delivery
status: reviewed
order: 36
requirement_count: 2
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 24b: Concomitant care received by each group

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand concomitant care received by each group. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Concomitant care received during the trial for each group" — CONSORT 2025 expanded checklist, item 24b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Intervention and comparator delivery|Intervention and comparator delivery]]
- **Domain classes:** [[TrialArm]], [[Intervention]]

## Atomic requirements

1. **Number and percentage receiving each relevant concomitant intervention.** Report number and percentage receiving each relevant concomitant intervention. (`must`; expects `number`; scoped by `consort-2025-scope-item-24b-each-trial-group`)
2. **Cumulative or average exposure for each concomitant intervention where relevant.** Report cumulative or average exposure for each concomitant intervention where relevant. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-concomitant-exposure-summary-relevant`; scoped by `consort-2025-scope-item-24b-each-trial-group`)

## Applicability

- **Cumulative or average concomitant exposure is relevant:** `{"equals":true,"fact":"intervention.concomitant_exposure_summary.relevant"}`

## Scope and repetition

- **Each trial group:** repeat over `trial.group`.

## Relations to other guideline elements

- [[CONSORT 24a]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 24b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-24b-r01"}},{"require":{"ref":"consort-2025-item-24b-r02"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "contextual",
        "expression": {
          "equals": true,
          "fact": "intervention.concomitant_exposure_summary.relevant"
        },
        "id": "consort-2025-condition-concomitant-exposure-summary-relevant",
        "label": "Cumulative or average concomitant exposure is relevant",
        "source_references": [
          {
            "locator": {
              "item_number": "24b",
              "page": 10,
              "quoted_fragment": "Concomitant care received during the trial for each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Concomitant care received during the trial for each group",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-24b",
    "item_number": "24b",
    "label": "Concomitant care received by each group",
    "order": 36,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand concomitant care received by each group. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-24a"
      ],
      "governed_by": [
        "consort-2025-rule-item-24b-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-concomitant-exposure-summary-relevant"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-24b-r01",
        "consort-2025-item-24b-r02"
      ],
      "targets_domain_class": [
        "consort-class-trial-arm",
        "consort-class-intervention"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-24b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number and percentage receiving each relevant concomitant intervention",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-24b",
        "requirement_text": "Report number and percentage receiving each relevant concomitant intervention.",
        "scope": "consort-2025-scope-item-24b-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "24b",
              "page": 10,
              "row_label": "Number and percentage receiving each relevant concomitant intervention"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number and percentage receiving each relevant concomitant intervention",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-concomitant-exposure-summary-relevant",
        "id": "consort-2025-item-24b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Cumulative or average exposure for each concomitant intervention where relevant",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-24b",
        "requirement_text": "Report cumulative or average exposure for each concomitant intervention where relevant.",
        "scope": "consort-2025-scope-item-24b-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "24b",
              "page": 10,
              "row_label": "Cumulative or average exposure for each concomitant intervention where relevant"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Cumulative or average exposure for each concomitant intervention where relevant",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-24b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-24b-r02"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-24b-completeness",
        "label": "Item 24b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "trial.group",
        "id": "consort-2025-scope-item-24b-each-trial-group",
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
          "item_number": "24b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "24b",
          "page": 10
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Concomitant care received during the trial for each group",
    "status": "reviewed",
    "topic": "consort-2025-topic-intervention-and-comparator-delivery",
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
