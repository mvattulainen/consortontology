---
id: consort-2025-item-12a
type: ChecklistItem
item_number: 12a
label: "Eligibility criteria for participants"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-eligibility-criteria
status: reviewed
order: 14
requirement_count: 3
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 12a: Eligibility criteria for participants

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand eligibility criteria for participants. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Eligibility criteria for participants" — CONSORT 2025 expanded checklist, item 12a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Eligibility criteria|Eligibility criteria]]
- **Domain classes:** [[Participant]]

## Atomic requirements

1. **All participant inclusion criteria.** Report all participant inclusion criteria. (`must`; expects `free_text_description`)
2. **All participant exclusion criteria.** Report all participant exclusion criteria. (`must`; expects `free_text_description`)
3. **Methods of recruitment.** Report methods of recruitment. (`must`; expects `method_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 12a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-12a-r01"}},{"require":{"ref":"consort-2025-item-12a-r02"}},{"require":{"ref":"consort-2025-item-12a-r03"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Eligibility criteria for participants",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-12a",
    "item_number": "12a",
    "label": "Eligibility criteria for participants",
    "order": 14,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand eligibility criteria for participants. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-12a-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-12a-r01",
        "consort-2025-item-12a-r02",
        "consort-2025-item-12a-r03"
      ],
      "targets_domain_class": [
        "consort-class-participant"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-12a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "All participant inclusion criteria",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-12a",
        "requirement_text": "Report all participant inclusion criteria.",
        "source_references": [
          {
            "locator": {
              "item_number": "12a",
              "page": 4,
              "row_label": "All participant inclusion criteria"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "All participant inclusion criteria",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-12a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "All participant exclusion criteria",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-12a",
        "requirement_text": "Report all participant exclusion criteria.",
        "source_references": [
          {
            "locator": {
              "item_number": "12a",
              "page": 4,
              "row_label": "All participant exclusion criteria"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "All participant exclusion criteria",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-12a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Methods of recruitment",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-12a",
        "requirement_text": "Report methods of recruitment.",
        "source_references": [
          {
            "locator": {
              "item_number": "12a",
              "page": 4,
              "row_label": "Methods of recruitment"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Methods of recruitment",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-12a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-12a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-12a-r03"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-12a-completeness",
        "label": "Item 12a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "12a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "12a",
          "page": 4
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Eligibility criteria for participants",
    "status": "reviewed",
    "topic": "consort-2025-topic-eligibility-criteria",
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
