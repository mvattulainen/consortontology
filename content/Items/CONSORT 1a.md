---
id: consort-2025-item-1a
type: ChecklistItem
item_number: 1a
label: "Identification as a randomised trial"
guideline_version: consort-2025
section: consort-2025-section-title-and-abstract
topic: consort-2025-topic-title-and-structured-abstract
status: reviewed
order: 1
requirement_count: 1
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 1a: Identification as a randomised trial

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand identification as a randomised trial. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Identification as a randomised trial" — CONSORT 2025 expanded checklist, item 1a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Title and Abstract|Title and abstract]]
- **Topic:** [[Title and structured abstract|Title and structured abstract]]
- **Domain classes:** [[RandomisedTrial]]

## Atomic requirements

1. **Use the word “randomised” in the title.** Report use the word “randomised” in the title. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 1a completeness:** `{"require":{"ref":"consort-2025-item-1a-r01"}}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Identification as a randomised trial",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-1a",
    "item_number": "1a",
    "label": "Identification as a randomised trial",
    "order": 1,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand identification as a randomised trial. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-1a-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-1a-r01"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial"
      ]
    },
    "requirements": [
      {
        "expected_location": "title",
        "id": "consort-2025-item-1a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Use the word “randomised” in the title",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1a",
        "requirement_text": "Report use the word “randomised” in the title.",
        "source_references": [
          {
            "locator": {
              "item_number": "1a",
              "page": 1,
              "row_label": "Use the word “randomised” in the title"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Use the word “randomised” in the title",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "require": {
            "ref": "consort-2025-item-1a-r01"
          }
        },
        "id": "consort-2025-rule-item-1a-completeness",
        "label": "Item 1a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-title-and-abstract",
    "source_references": [
      {
        "locator": {
          "item_number": "1a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "1a",
          "page": 1
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Identification as a randomised trial",
    "status": "reviewed",
    "topic": "consort-2025-topic-title-and-structured-abstract",
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
