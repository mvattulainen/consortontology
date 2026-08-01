---
id: consort-2025-item-28
type: ChecklistItem
item_number: 28
label: "Other analyses and prespecified versus post-hoc status"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-ancillary-analyses
status: reviewed
order: 40
requirement_count: 2
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 28: Other analyses and prespecified versus post-hoc status

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand other analyses and prespecified versus post-hoc status. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Any other analyses performed, including subgroup and sensitivity analyses, distinguishing pre-specified from post-hoc" — CONSORT 2025 expanded checklist, item 28.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Ancillary analyses|Ancillary analyses]]
- **Domain classes:** [[OutcomeResult]]

## Atomic requirements

1. **Results for every other analysis performed.** Report results for every other analysis performed. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-other-analysis-performed`; scoped by `consort-2025-scope-item-28-each-additional-analysis`)
2. **Whether each analysis was prespecified or post hoc.** State whether each analysis was prespecified or post hoc. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-other-analysis-performed`; scoped by `consort-2025-scope-item-28-each-additional-analysis`)

## Applicability

- **Another analysis was performed:** `{"equals":true,"fact":"analysis.additional.performed"}`

## Scope and repetition

- **Each additional analysis:** repeat over `analysis.additional`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 28 applicability:** `{"implies":{"if":{"equals":true,"fact":"analysis.additional.performed"},"then":{"activate":{"ref":"consort-2025-item-28"}}}}`
- **Item 28 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-28-r01"}},{"require":{"ref":"consort-2025-item-28-r02"}}]}`

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
        "id": "consort-2025-condition-other-analysis-performed",
        "label": "Another analysis was performed",
        "source_references": [
          {
            "locator": {
              "item_number": "28",
              "page": 11,
              "quoted_fragment": "Any other analyses performed, including subgroup and sensitivity analyses, distinguishing pre-specified from post-hoc"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Any other analyses performed, including subgroup and sensitivity analyses, distinguishing pre-specified from post-hoc",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-28",
    "item_number": "28",
    "label": "Other analyses and prespecified versus post-hoc status",
    "order": 40,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand other analyses and prespecified versus post-hoc status. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-28-applicability",
        "consort-2025-rule-item-28-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-other-analysis-performed"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-28-r01",
        "consort-2025-item-28-r02"
      ],
      "targets_domain_class": [
        "consort-class-outcome-result"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-other-analysis-performed",
        "id": "consort-2025-item-28-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Results for every other analysis performed",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-28",
        "requirement_text": "Report results for every other analysis performed.",
        "scope": "consort-2025-scope-item-28-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "28",
              "page": 11,
              "row_label": "Results for every other analysis performed"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Results for every other analysis performed",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-other-analysis-performed",
        "id": "consort-2025-item-28-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether each analysis was prespecified or post hoc",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-28",
        "requirement_text": "State whether each analysis was prespecified or post hoc.",
        "scope": "consort-2025-scope-item-28-each-additional-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "28",
              "page": 11,
              "row_label": "Whether each analysis was prespecified or post hoc"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether each analysis was prespecified or post hoc",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
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
                "ref": "consort-2025-item-28"
              }
            }
          }
        },
        "id": "consort-2025-rule-item-28-applicability",
        "label": "Item 28 applicability",
        "rule_kind": "conditional_item",
        "status": "reviewed",
        "type": "NormativeRule"
      },
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-28-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-28-r02"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-28-completeness",
        "label": "Item 28 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "analysis.additional",
        "id": "consort-2025-scope-item-28-each-additional-analysis",
        "label": "Each additional analysis",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-results",
    "source_references": [
      {
        "locator": {
          "item_number": "28"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "28",
          "page": 11
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Any other analyses performed, including subgroup and sensitivity analyses, distinguishing pre-specified from post-hoc",
    "status": "reviewed",
    "topic": "consort-2025-topic-ancillary-analyses",
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
