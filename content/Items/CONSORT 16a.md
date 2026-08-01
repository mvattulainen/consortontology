---
id: consort-2025-item-16a
type: ChecklistItem
item_number: 16a
label: "Sample-size determination and assumptions"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-sample-size
status: reviewed
order: 19
requirement_count: 8
condition_count: 2
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 16a: Sample-size determination and assumptions

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand sample-size determination and assumptions. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "How sample size was determined, including all assumptions supporting the sample size calculation" — CONSORT 2025 expanded checklist, item 16a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Sample size|Sample size]]
- **Domain classes:** [[TrialDesign]], [[PrimaryOutcome]]

## Atomic requirements

1. **Primary outcome used for the calculation.** Report primary outcome used for the calculation. (`must`; expects `free_text_description`)
2. **Assumed outcome values for each group with rationale or references.** Report assumed outcome values for each group with rationale or references. (`must`; expects `reason`)
3. **Target difference and assumed standard deviation where applicable, with rationale.** Report target difference and assumed standard deviation where applicable, with rationale. (`must`; expects `reason`)
4. **Statistical significance level or type I error.** Report statistical significance level or type I error. (`must`; expects `number`)
5. **Statistical power or type II error.** Report statistical power or type II error. (`must`; expects `number`)
6. **Adjustments for missing data, non-adherence, or other factors.** Report adjustments for missing data, non-adherence, or other factors. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-sample-size-adjustment-used`)
7. **Target sample size per trial group.** Report target sample size per trial group. (`must`; expects `number`)
8. **Software used for the sample-size calculation.** Report software used for the sample-size calculation. (`conditional_must`; expects `number`; when `consort-2025-condition-sample-size-software-used`)

## Applicability

- **Sample-size adjustment was used:** `{"equals":true,"fact":"analysis.sample_size.adjustment_used"}`
- **Sample-size software was used:** `{"equals":true,"fact":"analysis.sample_size.software_used"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 16a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-16a-r01"}},{"require":{"ref":"consort-2025-item-16a-r02"}},{"require":{"ref":"consort-2025-item-16a-r03"}},{"require":{"ref":"consort-2025-item-16a-r04"}},{"require":{"ref":"consort-2025-item-16a-r05"}},{"require":{"ref":"consort-2025-item-16a-r06"}},{"require":{"ref":"consort-2025-item-16a-r07"}},{"require":{"ref":"consort-2025-item-16a-r08"}}]}`

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
          "fact": "analysis.sample_size.adjustment_used"
        },
        "id": "consort-2025-condition-sample-size-adjustment-used",
        "label": "Sample-size adjustment was used",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "quoted_fragment": "How sample size was determined, including all assumptions supporting the sample size calculation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      },
      {
        "condition_kind": "presence_dependent",
        "expression": {
          "equals": true,
          "fact": "analysis.sample_size.software_used"
        },
        "id": "consort-2025-condition-sample-size-software-used",
        "label": "Sample-size software was used",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "quoted_fragment": "How sample size was determined, including all assumptions supporting the sample size calculation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "How sample size was determined, including all assumptions supporting the sample size calculation",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-16a",
    "item_number": "16a",
    "label": "Sample-size determination and assumptions",
    "order": 19,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand sample-size determination and assumptions. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-16a-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-sample-size-adjustment-used",
        "consort-2025-condition-sample-size-software-used"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-16a-r01",
        "consort-2025-item-16a-r02",
        "consort-2025-item-16a-r03",
        "consort-2025-item-16a-r04",
        "consort-2025-item-16a-r05",
        "consort-2025-item-16a-r06",
        "consort-2025-item-16a-r07",
        "consort-2025-item-16a-r08"
      ],
      "targets_domain_class": [
        "consort-class-trial-design",
        "consort-class-primary-outcome"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-16a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Primary outcome used for the calculation",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report primary outcome used for the calculation.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Primary outcome used for the calculation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Primary outcome used for the calculation",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-16a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Assumed outcome values for each group with rationale or references",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report assumed outcome values for each group with rationale or references.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Assumed outcome values for each group with rationale or references"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Assumed outcome values for each group with rationale or references",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "id": "consort-2025-item-16a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Target difference and assumed standard deviation where applicable, with rationale",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report target difference and assumed standard deviation where applicable, with rationale.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Target difference and assumed standard deviation where applicable, with rationale"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Target difference and assumed standard deviation where applicable, with rationale",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "id": "consort-2025-item-16a-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Statistical significance level or type I error",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report statistical significance level or type I error.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Statistical significance level or type I error"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Statistical significance level or type I error",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "id": "consort-2025-item-16a-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Statistical power or type II error",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report statistical power or type II error.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Statistical power or type II error"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Statistical power or type II error",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-sample-size-adjustment-used",
        "id": "consort-2025-item-16a-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Adjustments for missing data, non-adherence, or other factors",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report adjustments for missing data, non-adherence, or other factors.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Adjustments for missing data, non-adherence, or other factors"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Adjustments for missing data, non-adherence, or other factors",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-16a-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Target sample size per trial group",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report target sample size per trial group.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Target sample size per trial group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Target sample size per trial group",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-sample-size-software-used",
        "id": "consort-2025-item-16a-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Software used for the sample-size calculation",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-16a",
        "requirement_text": "Report software used for the sample-size calculation.",
        "source_references": [
          {
            "locator": {
              "item_number": "16a",
              "page": 6,
              "row_label": "Software used for the sample-size calculation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Software used for the sample-size calculation",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-16a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16a-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16a-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16a-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16a-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16a-r07"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16a-r08"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-16a-completeness",
        "label": "Item 16a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "16a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "16a",
          "page": 6
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "How sample size was determined, including all assumptions supporting the sample size calculation",
    "status": "reviewed",
    "topic": "consort-2025-topic-sample-size",
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
