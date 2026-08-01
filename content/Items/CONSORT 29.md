---
id: consort-2025-item-29
type: ChecklistItem
item_number: 29
label: "Interpretation consistent with results and relevant evidence"
guideline_version: consort-2025
section: consort-2025-section-discussion
topic: consort-2025-topic-interpretation
status: reviewed
order: 41
requirement_count: 3
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 29: Interpretation consistent with results and relevant evidence

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand interpretation consistent with results and relevant evidence. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Interpretation consistent with results, balancing benefits and harms, and considering other relevant evidence" — CONSORT 2025 expanded checklist, item 29.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Discussion|Discussion]]
- **Topic:** [[Interpretation|Interpretation]]
- **Domain classes:** [[RandomisedTrial]], [[OutcomeResult]], [[HarmsOutcome]]

## Atomic requirements

1. **Brief summary balancing benefits and harms.** Report brief summary balancing benefits and harms. (`must`; expects `free_text_description`)
2. **Relationship of trial results to existing evidence.** Report relationship of trial results to existing evidence. (`must`; expects `free_text_description`)
3. **Interpretation without unsupported spin.** Report interpretation without unsupported spin. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 29 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-29-r01"}},{"require":{"ref":"consort-2025-item-29-r02"}},{"require":{"ref":"consort-2025-item-29-r03"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Interpretation consistent with results, balancing benefits and harms, and considering other relevant evidence",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-29",
    "item_number": "29",
    "label": "Interpretation consistent with results and relevant evidence",
    "order": 41,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand interpretation consistent with results and relevant evidence. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-29-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-29-r01",
        "consort-2025-item-29-r02",
        "consort-2025-item-29-r03"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-outcome-result",
        "consort-class-harms-outcome"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-29-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Brief summary balancing benefits and harms",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-29",
        "requirement_text": "Report brief summary balancing benefits and harms.",
        "source_references": [
          {
            "locator": {
              "item_number": "29",
              "page": 11,
              "row_label": "Brief summary balancing benefits and harms"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Brief summary balancing benefits and harms",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-29-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Relationship of trial results to existing evidence",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-29",
        "requirement_text": "Report relationship of trial results to existing evidence.",
        "source_references": [
          {
            "locator": {
              "item_number": "29",
              "page": 11,
              "row_label": "Relationship of trial results to existing evidence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Relationship of trial results to existing evidence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-29-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Interpretation without unsupported spin",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-29",
        "requirement_text": "Report interpretation without unsupported spin.",
        "source_references": [
          {
            "locator": {
              "item_number": "29",
              "page": 11,
              "row_label": "Interpretation without unsupported spin"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Interpretation without unsupported spin",
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
                "ref": "consort-2025-item-29-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-29-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-29-r03"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-29-completeness",
        "label": "Item 29 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-discussion",
    "source_references": [
      {
        "locator": {
          "item_number": "29"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "29",
          "page": 11
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Interpretation consistent with results, balancing benefits and harms, and considering other relevant evidence",
    "status": "reviewed",
    "topic": "consort-2025-topic-interpretation",
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
