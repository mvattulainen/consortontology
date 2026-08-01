---
id: consort-2025-item-25
type: ChecklistItem
item_number: 25
label: "Baseline demographic and clinical characteristics by group"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-baseline-data
status: reviewed
order: 37
requirement_count: 2
condition_count: 2
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 25: Baseline demographic and clinical characteristics by group

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand baseline demographic and clinical characteristics by group. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "A table showing baseline demographic and clinical characteristics for each group" — CONSORT 2025 expanded checklist, item 25.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Baseline data|Baseline data]]
- **Domain classes:** [[Participant]], [[TrialArm]], [[GroupResult]]

## Atomic requirements

1. **Continuous baseline variables as mean and standard deviation or median and percentiles, as appropriate.** Report continuous baseline variables as mean and standard deviation or median and percentiles, as appropriate. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-continuous-baseline-variable-present`; scoped by `consort-2025-scope-item-25-each-trial-group`)
2. **Binary and categorical baseline variables as numbers and percentages.** Report binary and categorical baseline variables as numbers and percentages. (`conditional_must`; expects `number`; when `consort-2025-condition-categorical-baseline-variable-present`; scoped by `consort-2025-scope-item-25-each-trial-group`)

## Applicability

- **Continuous baseline variables are reported:** `{"equals":true,"fact":"reporting_context.baseline.continuous_variable_present"}`
- **Binary or categorical baseline variables are reported:** `{"equals":true,"fact":"reporting_context.baseline.categorical_variable_present"}`

## Scope and repetition

- **Each trial group:** repeat over `trial.group`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 25 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-25-r01"}},{"require":{"ref":"consort-2025-item-25-r02"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "type_dependent",
        "expression": {
          "equals": true,
          "fact": "reporting_context.baseline.continuous_variable_present"
        },
        "id": "consort-2025-condition-continuous-baseline-variable-present",
        "label": "Continuous baseline variables are reported",
        "source_references": [
          {
            "locator": {
              "item_number": "25",
              "page": 10,
              "quoted_fragment": "A table showing baseline demographic and clinical characteristics for each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      },
      {
        "condition_kind": "type_dependent",
        "expression": {
          "equals": true,
          "fact": "reporting_context.baseline.categorical_variable_present"
        },
        "id": "consort-2025-condition-categorical-baseline-variable-present",
        "label": "Binary or categorical baseline variables are reported",
        "source_references": [
          {
            "locator": {
              "item_number": "25",
              "page": 10,
              "quoted_fragment": "A table showing baseline demographic and clinical characteristics for each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "A table showing baseline demographic and clinical characteristics for each group",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-25",
    "item_number": "25",
    "label": "Baseline demographic and clinical characteristics by group",
    "order": 37,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand baseline demographic and clinical characteristics by group. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-25-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-continuous-baseline-variable-present",
        "consort-2025-condition-categorical-baseline-variable-present"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-25-r01",
        "consort-2025-item-25-r02"
      ],
      "targets_domain_class": [
        "consort-class-participant",
        "consort-class-trial-arm",
        "consort-class-group-result"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-continuous-baseline-variable-present",
        "expected_location": "table",
        "id": "consort-2025-item-25-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Continuous baseline variables as mean and standard deviation or median and percentiles, as appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-25",
        "requirement_text": "Report continuous baseline variables as mean and standard deviation or median and percentiles, as appropriate.",
        "scope": "consort-2025-scope-item-25-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "25",
              "page": 10,
              "row_label": "Continuous baseline variables as mean and standard deviation or median and percentiles, as appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Continuous baseline variables as mean and standard deviation or median and percentiles, as appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-categorical-baseline-variable-present",
        "expected_location": "table",
        "id": "consort-2025-item-25-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Binary and categorical baseline variables as numbers and percentages",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-25",
        "requirement_text": "Report binary and categorical baseline variables as numbers and percentages.",
        "scope": "consort-2025-scope-item-25-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "25",
              "page": 10,
              "row_label": "Binary and categorical baseline variables as numbers and percentages"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Binary and categorical baseline variables as numbers and percentages",
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
                "ref": "consort-2025-item-25-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-25-r02"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-25-completeness",
        "label": "Item 25 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "trial.group",
        "id": "consort-2025-scope-item-25-each-trial-group",
        "label": "Each trial group",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-results",
    "source_references": [
      {
        "locator": {
          "item_number": "25"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "25",
          "page": 10
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "A table showing baseline demographic and clinical characteristics for each group",
    "status": "reviewed",
    "topic": "consort-2025-topic-baseline-data",
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
