---
id: consort-2025-item-6
type: ChecklistItem
item_number: 6
label: "Scientific background and rationale"
guideline_version: consort-2025
section: consort-2025-section-introduction
topic: consort-2025-topic-background-and-rationale
status: reviewed
order: 8
requirement_count: 6
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 6: Scientific background and rationale

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand scientific background and rationale. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Scientific background and rationale" — CONSORT 2025 expanded checklist, item 6.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Introduction|Introduction]]
- **Topic:** [[Background and rationale|Background and rationale]]
- **Domain classes:** [[RandomisedTrial]], [[Intervention]], [[Comparator]]

## Atomic requirements

1. **Importance of the research question.** Report importance of the research question. (`must`; expects `free_text_description`)
2. **Why a new trial is needed in the context of available evidence.** Report why a new trial is needed in the context of available evidence. (`must`; expects `free_text_description`)
3. **How the intervention might work.** Report how the intervention might work. (`must`; expects `free_text_description`)
4. **Justification for the comparator.** Report justification for the comparator. (`must`; expects `reason`)
5. **Existing evidence about benefits and harms.** Report existing evidence about benefits and harms. (`must`; expects `free_text_description`)
6. **Relevant systematic reviews where available.** Report relevant systematic reviews where available. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-relevant-systematic-review-available`)

## Applicability

- **Relevant systematic review is available:** `{"equals":true,"fact":"reporting_context.relevant_systematic_review.available"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 6 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-6-r01"}},{"require":{"ref":"consort-2025-item-6-r02"}},{"require":{"ref":"consort-2025-item-6-r03"}},{"require":{"ref":"consort-2025-item-6-r04"}},{"require":{"ref":"consort-2025-item-6-r05"}},{"require":{"ref":"consort-2025-item-6-r06"}}]}`

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
          "fact": "reporting_context.relevant_systematic_review.available"
        },
        "id": "consort-2025-condition-relevant-systematic-review-available",
        "label": "Relevant systematic review is available",
        "source_references": [
          {
            "locator": {
              "item_number": "6",
              "page": 3,
              "quoted_fragment": "Scientific background and rationale"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Scientific background and rationale",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-6",
    "item_number": "6",
    "label": "Scientific background and rationale",
    "order": 8,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand scientific background and rationale. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-6-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-relevant-systematic-review-available"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-6-r01",
        "consort-2025-item-6-r02",
        "consort-2025-item-6-r03",
        "consort-2025-item-6-r04",
        "consort-2025-item-6-r05",
        "consort-2025-item-6-r06"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-intervention",
        "consort-class-comparator"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-6-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Importance of the research question",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-6",
        "requirement_text": "Report importance of the research question.",
        "source_references": [
          {
            "locator": {
              "item_number": "6",
              "page": 3,
              "row_label": "Importance of the research question"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Importance of the research question",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-6-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Why a new trial is needed in the context of available evidence",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-6",
        "requirement_text": "Report why a new trial is needed in the context of available evidence.",
        "source_references": [
          {
            "locator": {
              "item_number": "6",
              "page": 3,
              "row_label": "Why a new trial is needed in the context of available evidence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Why a new trial is needed in the context of available evidence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-6-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How the intervention might work",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-6",
        "requirement_text": "Report how the intervention might work.",
        "source_references": [
          {
            "locator": {
              "item_number": "6",
              "page": 3,
              "row_label": "How the intervention might work"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How the intervention might work",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-6-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Justification for the comparator",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-6",
        "requirement_text": "Report justification for the comparator.",
        "source_references": [
          {
            "locator": {
              "item_number": "6",
              "page": 3,
              "row_label": "Justification for the comparator"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Justification for the comparator",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "id": "consort-2025-item-6-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Existing evidence about benefits and harms",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-6",
        "requirement_text": "Report existing evidence about benefits and harms.",
        "source_references": [
          {
            "locator": {
              "item_number": "6",
              "page": 3,
              "row_label": "Existing evidence about benefits and harms"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Existing evidence about benefits and harms",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-relevant-systematic-review-available",
        "id": "consort-2025-item-6-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Relevant systematic reviews where available",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-6",
        "requirement_text": "Report relevant systematic reviews where available.",
        "source_references": [
          {
            "locator": {
              "item_number": "6",
              "page": 3,
              "row_label": "Relevant systematic reviews where available"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Relevant systematic reviews where available",
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
                "ref": "consort-2025-item-6-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-6-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-6-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-6-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-6-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-6-r06"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-6-completeness",
        "label": "Item 6 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-introduction",
    "source_references": [
      {
        "locator": {
          "item_number": "6"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "6",
          "page": 3
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Scientific background and rationale",
    "status": "reviewed",
    "topic": "consort-2025-topic-background-and-rationale",
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
