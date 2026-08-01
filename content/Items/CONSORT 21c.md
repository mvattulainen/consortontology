---
id: consort-2025-item-21c
type: ChecklistItem
item_number: 21c
label: "Handling of missing data"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-statistical-methods
status: reviewed
order: 29
requirement_count: 3
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 21c: Handling of missing data

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand handling of missing data. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "How missing data were handled in the analysis" — CONSORT 2025 expanded checklist, item 21c.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Statistical methods|Statistical methods]]
- **Domain classes:** [[OutcomeResult]]

## Atomic requirements

1. **Assumption about the missing-data mechanism, with justification.** Report assumption about the missing-data mechanism, with justification. (`must`; expects `method_description`; scoped by `consort-2025-scope-item-21c-each-analysis`)
2. **Method used to handle missing data, with justification.** Report method used to handle missing data, with justification. (`must`; expects `method_description`; scoped by `consort-2025-scope-item-21c-each-analysis`)
3. **Whether sensitivity analyses for missing data were conducted.** State whether sensitivity analyses for missing data were conducted. (`must`; expects `boolean_statement`; scoped by `consort-2025-scope-item-21c-each-analysis`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

- **Each statistical analysis:** repeat over `analysis.declared`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 21c completeness:** `{"all":[{"require":{"ref":"consort-2025-item-21c-r01"}},{"require":{"ref":"consort-2025-item-21c-r02"}},{"require":{"ref":"consort-2025-item-21c-r03"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "How missing data were handled in the analysis",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-21c",
    "item_number": "21c",
    "label": "Handling of missing data",
    "order": 29,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand handling of missing data. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-21c-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-21c-r01",
        "consort-2025-item-21c-r02",
        "consort-2025-item-21c-r03"
      ],
      "targets_domain_class": [
        "consort-class-outcome-result"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-21c-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Assumption about the missing-data mechanism, with justification",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21c",
        "requirement_text": "Report assumption about the missing-data mechanism, with justification.",
        "scope": "consort-2025-scope-item-21c-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21c",
              "page": 9,
              "row_label": "Assumption about the missing-data mechanism, with justification"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Assumption about the missing-data mechanism, with justification",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "id": "consort-2025-item-21c-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Method used to handle missing data, with justification",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21c",
        "requirement_text": "Report method used to handle missing data, with justification.",
        "scope": "consort-2025-scope-item-21c-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21c",
              "page": 9,
              "row_label": "Method used to handle missing data, with justification"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Method used to handle missing data, with justification",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "id": "consort-2025-item-21c-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether sensitivity analyses for missing data were conducted",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21c",
        "requirement_text": "State whether sensitivity analyses for missing data were conducted.",
        "scope": "consort-2025-scope-item-21c-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21c",
              "page": 9,
              "row_label": "Whether sensitivity analyses for missing data were conducted"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether sensitivity analyses for missing data were conducted",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-21c-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21c-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21c-r03"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-21c-completeness",
        "label": "Item 21c completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "analysis.declared",
        "id": "consort-2025-scope-item-21c-each-analysis",
        "label": "Each statistical analysis",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "21c"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "21c",
          "page": 9
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "How missing data were handled in the analysis",
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
