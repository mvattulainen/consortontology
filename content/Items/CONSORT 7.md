---
id: consort-2025-item-7
type: ChecklistItem
item_number: 7
label: "Specific objectives related to benefits and harms"
guideline_version: consort-2025
section: consort-2025-section-introduction
topic: consort-2025-topic-objectives
status: reviewed
order: 9
requirement_count: 7
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 7: Specific objectives related to benefits and harms

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand specific objectives related to benefits and harms. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Specific objectives related to benefits and harms" — CONSORT 2025 expanded checklist, item 7.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Introduction|Introduction]]
- **Topic:** [[Objectives|Objectives]]
- **Domain classes:** [[RandomisedTrial]], [[Participant]], [[Intervention]], [[Comparator]], [[PrimaryOutcome]]

## Atomic requirements

1. **Trial objectives related to benefits and harms.** Report trial objectives related to benefits and harms. (`must`; expects `free_text_description`)
2. **Participants addressed by the objectives.** Report participants addressed by the objectives. (`must`; expects `free_text_description`)
3. **Interventions addressed by the objectives.** Report interventions addressed by the objectives. (`must`; expects `free_text_description`)
4. **Comparators addressed by the objectives.** Report comparators addressed by the objectives. (`must`; expects `free_text_description`)
5. **Primary outcomes addressed by the objectives.** Report primary outcomes addressed by the objectives. (`must`; expects `free_text_description`)
6. **Primary-outcome time point addressed by the objectives.** Report primary-outcome time point addressed by the objectives. (`must`; expects `free_text_description`)
7. **Objectives expressed using the estimands framework when that framework was used.** Report objectives expressed using the estimands framework when that framework was used. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-estimands-framework-used`)

## Applicability

- **Estimands framework used:** `{"equals":true,"fact":"design.estimands_framework.used"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 7 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-7-r01"}},{"require":{"ref":"consort-2025-item-7-r02"}},{"require":{"ref":"consort-2025-item-7-r03"}},{"require":{"ref":"consort-2025-item-7-r04"}},{"require":{"ref":"consort-2025-item-7-r05"}},{"require":{"ref":"consort-2025-item-7-r06"}},{"require":{"ref":"consort-2025-item-7-r07"}}]}`

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
          "fact": "design.estimands_framework.used"
        },
        "id": "consort-2025-condition-estimands-framework-used",
        "label": "Estimands framework used",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "quoted_fragment": "Specific objectives related to benefits and harms"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Specific objectives related to benefits and harms",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-7",
    "item_number": "7",
    "label": "Specific objectives related to benefits and harms",
    "order": 9,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand specific objectives related to benefits and harms. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-7-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-estimands-framework-used"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-7-r01",
        "consort-2025-item-7-r02",
        "consort-2025-item-7-r03",
        "consort-2025-item-7-r04",
        "consort-2025-item-7-r05",
        "consort-2025-item-7-r06",
        "consort-2025-item-7-r07"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-participant",
        "consort-class-intervention",
        "consort-class-comparator",
        "consort-class-primary-outcome"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-7-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Trial objectives related to benefits and harms",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-7",
        "requirement_text": "Report trial objectives related to benefits and harms.",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "row_label": "Trial objectives related to benefits and harms"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Trial objectives related to benefits and harms",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-7-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Participants addressed by the objectives",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-7",
        "requirement_text": "Report participants addressed by the objectives.",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "row_label": "Participants addressed by the objectives"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Participants addressed by the objectives",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-7-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Interventions addressed by the objectives",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-7",
        "requirement_text": "Report interventions addressed by the objectives.",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "row_label": "Interventions addressed by the objectives"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Interventions addressed by the objectives",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-7-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Comparators addressed by the objectives",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-7",
        "requirement_text": "Report comparators addressed by the objectives.",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "row_label": "Comparators addressed by the objectives"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Comparators addressed by the objectives",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-7-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Primary outcomes addressed by the objectives",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-7",
        "requirement_text": "Report primary outcomes addressed by the objectives.",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "row_label": "Primary outcomes addressed by the objectives"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Primary outcomes addressed by the objectives",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-7-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Primary-outcome time point addressed by the objectives",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-7",
        "requirement_text": "Report primary-outcome time point addressed by the objectives.",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "row_label": "Primary-outcome time point addressed by the objectives"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Primary-outcome time point addressed by the objectives",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-estimands-framework-used",
        "id": "consort-2025-item-7-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Objectives expressed using the estimands framework when that framework was used",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-7",
        "requirement_text": "Report objectives expressed using the estimands framework when that framework was used.",
        "source_references": [
          {
            "locator": {
              "item_number": "7",
              "page": 3,
              "row_label": "Objectives expressed using the estimands framework when that framework was used"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Objectives expressed using the estimands framework when that framework was used",
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
                "ref": "consort-2025-item-7-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-7-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-7-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-7-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-7-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-7-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-7-r07"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-7-completeness",
        "label": "Item 7 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-introduction",
    "source_references": [
      {
        "locator": {
          "item_number": "7"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "7",
          "page": 3
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Specific objectives related to benefits and harms",
    "status": "reviewed",
    "topic": "consort-2025-topic-objectives",
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
