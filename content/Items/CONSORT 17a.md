---
id: consort-2025-item-17a
type: ChecklistItem
item_number: 17a
label: "Generator and method of random allocation sequence"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-randomisation-sequence-generation
status: reviewed
order: 21
requirement_count: 3
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 17a: Generator and method of random allocation sequence

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand generator and method of random allocation sequence. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Who generated the random allocation sequence and the method used" — CONSORT 2025 expanded checklist, item 17a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Randomisation - sequence generation|Randomisation: sequence generation]]
- **Domain classes:** [[RandomAllocationProcess]], [[TrialRole]]

## Atomic requirements

1. **Who generated the allocation sequence.** Report who generated the allocation sequence. (`must`; expects `person_or_role`)
2. **Method of sequence generation.** Report method of sequence generation. (`must`; expects `method_description`)
3. **Software used for random sequence generation.** Report software used for random sequence generation. (`conditional_must`; expects `software_name`; when `consort-2025-condition-randomisation-software-used`)

## Applicability

- **Randomisation software was used:** `{"equals":true,"fact":"design.randomisation.software_used"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 17a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-17a-r01"}},{"require":{"ref":"consort-2025-item-17a-r02"}},{"require":{"ref":"consort-2025-item-17a-r03"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "presence_dependent",
        "expression": {
          "equals": true,
          "fact": "design.randomisation.software_used"
        },
        "id": "consort-2025-condition-randomisation-software-used",
        "label": "Randomisation software was used",
        "source_references": [
          {
            "locator": {
              "item_number": "17a",
              "page": 6,
              "quoted_fragment": "Who generated the random allocation sequence and the method used"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Who generated the random allocation sequence and the method used",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-17a",
    "item_number": "17a",
    "label": "Generator and method of random allocation sequence",
    "order": 21,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand generator and method of random allocation sequence. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-17a-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-randomisation-software-used"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-17a-r01",
        "consort-2025-item-17a-r02",
        "consort-2025-item-17a-r03"
      ],
      "targets_domain_class": [
        "consort-class-random-allocation-process",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-17a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who generated the allocation sequence",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-17a",
        "requirement_text": "Report who generated the allocation sequence.",
        "source_references": [
          {
            "locator": {
              "item_number": "17a",
              "page": 6,
              "row_label": "Who generated the allocation sequence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who generated the allocation sequence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "id": "consort-2025-item-17a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Method of sequence generation",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-17a",
        "requirement_text": "Report method of sequence generation.",
        "source_references": [
          {
            "locator": {
              "item_number": "17a",
              "page": 6,
              "row_label": "Method of sequence generation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Method of sequence generation",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-randomisation-software-used",
        "id": "consort-2025-item-17a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Software used for random sequence generation",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17a",
        "requirement_text": "Report software used for random sequence generation.",
        "source_references": [
          {
            "locator": {
              "item_number": "17a",
              "page": 6,
              "row_label": "Software used for random sequence generation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Software used for random sequence generation",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "software_name"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-17a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17a-r03"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-17a-completeness",
        "label": "Item 17a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "17a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "17a",
          "page": 6
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Who generated the random allocation sequence and the method used",
    "status": "reviewed",
    "topic": "consort-2025-topic-randomisation-sequence-generation",
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
