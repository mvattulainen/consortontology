---
id: consort-2025-item-20a
type: ChecklistItem
item_number: 20a
label: "Roles blinded after assignment"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-blinding
status: reviewed
order: 25
requirement_count: 5
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 20a: Roles blinded after assignment

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand roles blinded after assignment. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Who was blinded after assignment to interventions" — CONSORT 2025 expanded checklist, item 20a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Blinding|Blinding]]
- **Domain classes:** [[BlindingProcess]], [[TrialRole]]

## Atomic requirements

1. **Whether trial participants were blinded.** State whether trial participants were blinded. (`must`; expects `boolean_statement`)
2. **Whether care providers were blinded.** State whether care providers were blinded. (`must`; expects `boolean_statement`)
3. **Whether data collectors were blinded.** State whether data collectors were blinded. (`must`; expects `boolean_statement`)
4. **Whether outcome assessors were blinded.** State whether outcome assessors were blinded. (`must`; expects `boolean_statement`)
5. **Whether data analysts were blinded.** State whether data analysts were blinded. (`must`; expects `boolean_statement`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 20a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-20a-r01"}},{"require":{"ref":"consort-2025-item-20a-r02"}},{"require":{"ref":"consort-2025-item-20a-r03"}},{"require":{"ref":"consort-2025-item-20a-r04"}},{"require":{"ref":"consort-2025-item-20a-r05"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Who was blinded after assignment to interventions",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-20a",
    "item_number": "20a",
    "label": "Roles blinded after assignment",
    "order": 25,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand roles blinded after assignment. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-20a-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-20a-r01",
        "consort-2025-item-20a-r02",
        "consort-2025-item-20a-r03",
        "consort-2025-item-20a-r04",
        "consort-2025-item-20a-r05"
      ],
      "targets_domain_class": [
        "consort-class-blinding-process",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-20a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether trial participants were blinded",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-20a",
        "requirement_text": "State whether trial participants were blinded.",
        "source_references": [
          {
            "locator": {
              "item_number": "20a",
              "page": 7,
              "row_label": "Whether trial participants were blinded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether trial participants were blinded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "id": "consort-2025-item-20a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether care providers were blinded",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-20a",
        "requirement_text": "State whether care providers were blinded.",
        "source_references": [
          {
            "locator": {
              "item_number": "20a",
              "page": 7,
              "row_label": "Whether care providers were blinded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether care providers were blinded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "id": "consort-2025-item-20a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether data collectors were blinded",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-20a",
        "requirement_text": "State whether data collectors were blinded.",
        "source_references": [
          {
            "locator": {
              "item_number": "20a",
              "page": 7,
              "row_label": "Whether data collectors were blinded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether data collectors were blinded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "id": "consort-2025-item-20a-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether outcome assessors were blinded",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-20a",
        "requirement_text": "State whether outcome assessors were blinded.",
        "source_references": [
          {
            "locator": {
              "item_number": "20a",
              "page": 7,
              "row_label": "Whether outcome assessors were blinded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether outcome assessors were blinded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "id": "consort-2025-item-20a-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether data analysts were blinded",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-20a",
        "requirement_text": "State whether data analysts were blinded.",
        "source_references": [
          {
            "locator": {
              "item_number": "20a",
              "page": 7,
              "row_label": "Whether data analysts were blinded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether data analysts were blinded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-20a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20a-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20a-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20a-r05"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-20a-completeness",
        "label": "Item 20a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "20a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "20a",
          "page": 7
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Who was blinded after assignment to interventions",
    "status": "reviewed",
    "topic": "consort-2025-topic-blinding",
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
