---
id: consort-2025-item-9
type: ChecklistItem
item_number: 9
label: "Trial design, allocation ratio, and framework"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-trial-design
status: reviewed
order: 11
requirement_count: 4
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 9: Trial design, allocation ratio, and framework

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand trial design, allocation ratio, and framework. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Description of trial design including type of trial, allocation ratio, and framework" — CONSORT 2025 expanded checklist, item 9.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Trial design|Trial design]]
- **Domain classes:** [[RandomisedTrial]], [[TrialDesign]], [[TrialArm]]

## Atomic requirements

1. **Type of trial design.** Report type of trial design. (`must`; expects `free_text_description`)
2. **Conceptual framework.** Report conceptual framework. (`must`; expects `free_text_description`)
3. **Unit of randomisation.** Report unit of randomisation. (`must`; expects `free_text_description`)
4. **Allocation ratio.** Report allocation ratio. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 9 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-9-r01"}},{"require":{"ref":"consort-2025-item-9-r02"}},{"require":{"ref":"consort-2025-item-9-r03"}},{"require":{"ref":"consort-2025-item-9-r04"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Description of trial design including type of trial, allocation ratio, and framework",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-9",
    "item_number": "9",
    "label": "Trial design, allocation ratio, and framework",
    "order": 11,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand trial design, allocation ratio, and framework. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-9-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-9-r01",
        "consort-2025-item-9-r02",
        "consort-2025-item-9-r03",
        "consort-2025-item-9-r04"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-trial-design",
        "consort-class-trial-arm"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-9-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Type of trial design",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-9",
        "requirement_text": "Report type of trial design.",
        "source_references": [
          {
            "locator": {
              "item_number": "9",
              "page": 3,
              "row_label": "Type of trial design"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Type of trial design",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-9-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Conceptual framework",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-9",
        "requirement_text": "Report conceptual framework.",
        "source_references": [
          {
            "locator": {
              "item_number": "9",
              "page": 3,
              "row_label": "Conceptual framework"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Conceptual framework",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-9-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Unit of randomisation",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-9",
        "requirement_text": "Report unit of randomisation.",
        "source_references": [
          {
            "locator": {
              "item_number": "9",
              "page": 3,
              "row_label": "Unit of randomisation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Unit of randomisation",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-9-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Allocation ratio",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-9",
        "requirement_text": "Report allocation ratio.",
        "source_references": [
          {
            "locator": {
              "item_number": "9",
              "page": 3,
              "row_label": "Allocation ratio"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Allocation ratio",
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
                "ref": "consort-2025-item-9-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-9-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-9-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-9-r04"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-9-completeness",
        "label": "Item 9 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "9"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "9",
          "page": 3
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Description of trial design including type of trial, allocation ratio, and framework",
    "status": "reviewed",
    "topic": "consort-2025-topic-trial-design",
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
