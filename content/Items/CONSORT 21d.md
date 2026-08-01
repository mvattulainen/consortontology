---
id: consort-2025-item-21d
type: ChecklistItem
item_number: 21d
label: "Methods for additional analyses"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-statistical-methods
status: reviewed
order: 30
requirement_count: 7
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 21d: Methods for additional analyses

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand methods for additional analyses. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Methods for any additional analyses, distinguishing prespecified from post-hoc" — CONSORT 2025 expanded checklist, item 21d.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Statistical methods|Statistical methods]]
- **Domain classes:** [[OutcomeResult]]

## Atomic requirements

1. **Whether additional analyses were prespecified or post hoc.** State whether additional analyses were prespecified or post hoc. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-additional-analysis-performed`; scoped by `consort-2025-scope-item-21d-each-additional-analysis`)
2. **Whether all additional analyses conducted are reported.** State whether all additional analyses conducted are reported. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-additional-analysis-performed`; scoped by `consort-2025-scope-item-21d-each-additional-analysis`)
3. **Rationale for sensitivity analyses.** Report rationale for sensitivity analyses. (`conditional_must`; expects `reason`; when `consort-2025-condition-additional-analysis-performed`; scoped by `consort-2025-scope-item-21d-each-additional-analysis`)
4. **Methods for sensitivity analyses.** Report methods for sensitivity analyses. (`conditional_must`; expects `method_description`; when `consort-2025-condition-additional-analysis-performed`; scoped by `consort-2025-scope-item-21d-each-additional-analysis`)
5. **Baseline variables explored in subgroup analyses.** Report baseline variables explored in subgroup analyses. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-additional-analysis-performed`; scoped by `consort-2025-scope-item-21d-each-additional-analysis`)
6. **Rationale for subgroup analyses.** Report rationale for subgroup analyses. (`conditional_must`; expects `reason`; when `consort-2025-condition-additional-analysis-performed`; scoped by `consort-2025-scope-item-21d-each-additional-analysis`)
7. **Methods for subgroup analyses.** Report methods for subgroup analyses. (`conditional_must`; expects `method_description`; when `consort-2025-condition-additional-analysis-performed`; scoped by `consort-2025-scope-item-21d-each-additional-analysis`)

## Applicability

- **An additional analysis was performed:** `{"equals":true,"fact":"analysis.additional.performed"}`

## Scope and repetition

- **Each additional analysis:** repeat over `analysis.additional`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 21d applicability:** `{"implies":{"if":{"equals":true,"fact":"analysis.additional.performed"},"then":{"activate":{"ref":"consort-2025-item-21d"}}}}`
- **Item 21d completeness:** `{"all":[{"require":{"ref":"consort-2025-item-21d-r01"}},{"require":{"ref":"consort-2025-item-21d-r02"}},{"require":{"ref":"consort-2025-item-21d-r03"}},{"require":{"ref":"consort-2025-item-21d-r04"}},{"require":{"ref":"consort-2025-item-21d-r05"}},{"require":{"ref":"consort-2025-item-21d-r06"}},{"require":{"ref":"consort-2025-item-21d-r07"}}]}`

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
          "fact": "analysis.additional.performed"
        },
        "id": "consort-2025-condition-additional-analysis-performed",
        "label": "An additional analysis was performed",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "quoted_fragment": "Methods for any additional analyses, distinguishing prespecified from post-hoc"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Methods for any additional analyses, distinguishing prespecified from post-hoc",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-21d",
    "item_number": "21d",
    "label": "Methods for additional analyses",
    "order": 30,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand methods for additional analyses. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-21d-applicability",
        "consort-2025-rule-item-21d-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-additional-analysis-performed"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-21d-r01",
        "consort-2025-item-21d-r02",
        "consort-2025-item-21d-r03",
        "consort-2025-item-21d-r04",
        "consort-2025-item-21d-r05",
        "consort-2025-item-21d-r06",
        "consort-2025-item-21d-r07"
      ],
      "targets_domain_class": [
        "consort-class-outcome-result"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-additional-analysis-performed",
        "id": "consort-2025-item-21d-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether additional analyses were prespecified or post hoc",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21d",
        "requirement_text": "State whether additional analyses were prespecified or post hoc.",
        "scope": "consort-2025-scope-item-21d-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "row_label": "Whether additional analyses were prespecified or post hoc"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether additional analyses were prespecified or post hoc",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-additional-analysis-performed",
        "id": "consort-2025-item-21d-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether all additional analyses conducted are reported",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21d",
        "requirement_text": "State whether all additional analyses conducted are reported.",
        "scope": "consort-2025-scope-item-21d-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "row_label": "Whether all additional analyses conducted are reported"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether all additional analyses conducted are reported",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-additional-analysis-performed",
        "id": "consort-2025-item-21d-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Rationale for sensitivity analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21d",
        "requirement_text": "Report rationale for sensitivity analyses.",
        "scope": "consort-2025-scope-item-21d-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "row_label": "Rationale for sensitivity analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Rationale for sensitivity analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "applicability_condition": "consort-2025-condition-additional-analysis-performed",
        "id": "consort-2025-item-21d-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Methods for sensitivity analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21d",
        "requirement_text": "Report methods for sensitivity analyses.",
        "scope": "consort-2025-scope-item-21d-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "row_label": "Methods for sensitivity analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Methods for sensitivity analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-additional-analysis-performed",
        "id": "consort-2025-item-21d-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Baseline variables explored in subgroup analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21d",
        "requirement_text": "Report baseline variables explored in subgroup analyses.",
        "scope": "consort-2025-scope-item-21d-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "row_label": "Baseline variables explored in subgroup analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Baseline variables explored in subgroup analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-additional-analysis-performed",
        "id": "consort-2025-item-21d-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Rationale for subgroup analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21d",
        "requirement_text": "Report rationale for subgroup analyses.",
        "scope": "consort-2025-scope-item-21d-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "row_label": "Rationale for subgroup analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Rationale for subgroup analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "applicability_condition": "consort-2025-condition-additional-analysis-performed",
        "id": "consort-2025-item-21d-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Methods for subgroup analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21d",
        "requirement_text": "Report methods for subgroup analyses.",
        "scope": "consort-2025-scope-item-21d-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21d",
              "page": 9,
              "row_label": "Methods for subgroup analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Methods for subgroup analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "implies": {
            "if": {
              "equals": true,
              "fact": "analysis.additional.performed"
            },
            "then": {
              "activate": {
                "ref": "consort-2025-item-21d"
              }
            }
          }
        },
        "id": "consort-2025-rule-item-21d-applicability",
        "label": "Item 21d applicability",
        "rule_kind": "conditional_item",
        "status": "reviewed",
        "type": "NormativeRule"
      },
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-21d-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21d-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21d-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21d-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21d-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21d-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21d-r07"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-21d-completeness",
        "label": "Item 21d completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "analysis.additional",
        "id": "consort-2025-scope-item-21d-each-additional-analysis",
        "label": "Each additional analysis",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "21d"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "21d",
          "page": 9
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Methods for any additional analyses, distinguishing prespecified from post-hoc",
    "status": "reviewed",
    "topic": "consort-2025-topic-statistical-methods",
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
