---
id: consort-2025-item-23a
type: ChecklistItem
item_number: 23a
label: "Recruitment and follow-up dates"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-recruitment
status: reviewed
order: 33
requirement_count: 4
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 23a: Recruitment and follow-up dates

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand recruitment and follow-up dates. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Dates defining the periods of recruitment and follow-up for outcomes of benefits and harms" — CONSORT 2025 expanded checklist, item 23a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Recruitment|Recruitment]]
- **Domain classes:** [[ParticipantFlowObservation]]

## Atomic requirements

1. **Recruitment start date.** Report recruitment start date. (`must`; expects `date`)
2. **Recruitment completion date.** Report recruitment completion date. (`must`; expects `date`)
3. **Date when follow-up ended.** Report date when follow-up ended. (`must`; expects `date`)
4. **Duration of follow-up.** Report duration of follow-up. (`must`; expects `duration`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 23a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-23a-r01"}},{"require":{"ref":"consort-2025-item-23a-r02"}},{"require":{"ref":"consort-2025-item-23a-r03"}},{"require":{"ref":"consort-2025-item-23a-r04"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Dates defining the periods of recruitment and follow-up for outcomes of benefits and harms",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-23a",
    "item_number": "23a",
    "label": "Recruitment and follow-up dates",
    "order": 33,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand recruitment and follow-up dates. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-23a-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-23a-r01",
        "consort-2025-item-23a-r02",
        "consort-2025-item-23a-r03",
        "consort-2025-item-23a-r04"
      ],
      "targets_domain_class": [
        "consort-class-participant-flow-observation"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-23a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Recruitment start date",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-23a",
        "requirement_text": "Report recruitment start date.",
        "source_references": [
          {
            "locator": {
              "item_number": "23a",
              "page": 10,
              "row_label": "Recruitment start date"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Recruitment start date",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "date"
      },
      {
        "id": "consort-2025-item-23a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Recruitment completion date",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-23a",
        "requirement_text": "Report recruitment completion date.",
        "source_references": [
          {
            "locator": {
              "item_number": "23a",
              "page": 10,
              "row_label": "Recruitment completion date"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Recruitment completion date",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "date"
      },
      {
        "id": "consort-2025-item-23a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Date when follow-up ended",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-23a",
        "requirement_text": "Report date when follow-up ended.",
        "source_references": [
          {
            "locator": {
              "item_number": "23a",
              "page": 10,
              "row_label": "Date when follow-up ended"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Date when follow-up ended",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "date"
      },
      {
        "id": "consort-2025-item-23a-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Duration of follow-up",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-23a",
        "requirement_text": "Report duration of follow-up.",
        "source_references": [
          {
            "locator": {
              "item_number": "23a",
              "page": 10,
              "row_label": "Duration of follow-up"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Duration of follow-up",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "duration"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-23a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-23a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-23a-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-23a-r04"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-23a-completeness",
        "label": "Item 23a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-results",
    "source_references": [
      {
        "locator": {
          "item_number": "23a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "23a",
          "page": 10
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Dates defining the periods of recruitment and follow-up for outcomes of benefits and harms",
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
