---
id: consort-2025-item-18
type: ChecklistItem
item_number: 18
label: "Allocation concealment mechanism"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-allocation-concealment-mechanism
status: reviewed
order: 23
requirement_count: 1
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 18: Allocation concealment mechanism

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand allocation concealment mechanism. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Mechanism used to implement the random allocation sequence, describing steps to conceal the sequence until interventions were assigned" — CONSORT 2025 expanded checklist, item 18.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Allocation concealment mechanism|Allocation concealment mechanism]]
- **Domain classes:** [[AllocationConcealmentProcess]], [[TrialRole]]

## Atomic requirements

1. **How individuals enrolling participants were kept unaware of the next assignment in the random sequence.** Report how individuals enrolling participants were kept unaware of the next assignment in the random sequence. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 19]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 18 completeness:** `{"require":{"ref":"consort-2025-item-18-r01"}}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Mechanism used to implement the random allocation sequence, describing steps to conceal the sequence until interventions were assigned",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-18",
    "item_number": "18",
    "label": "Allocation concealment mechanism",
    "order": 23,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand allocation concealment mechanism. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-19"
      ],
      "governed_by": [
        "consort-2025-rule-item-18-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-18-r01"
      ],
      "targets_domain_class": [
        "consort-class-allocation-concealment-process",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-18-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How individuals enrolling participants were kept unaware of the next assignment in the random sequence",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-18",
        "requirement_text": "Report how individuals enrolling participants were kept unaware of the next assignment in the random sequence.",
        "source_references": [
          {
            "locator": {
              "item_number": "18",
              "page": 7,
              "row_label": "How individuals enrolling participants were kept unaware of the next assignment in the random sequence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How individuals enrolling participants were kept unaware of the next assignment in the random sequence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "require": {
            "ref": "consort-2025-item-18-r01"
          }
        },
        "id": "consort-2025-rule-item-18-completeness",
        "label": "Item 18 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "18"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "18",
          "page": 7
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Mechanism used to implement the random allocation sequence, describing steps to conceal the sequence until interventions were assigned",
    "status": "reviewed",
    "topic": "consort-2025-topic-allocation-concealment-mechanism",
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
