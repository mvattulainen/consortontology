---
id: consort-2025-item-14
type: ChecklistItem
item_number: 14
label: "Prespecified primary and secondary outcomes and defining components"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-outcomes
status: reviewed
order: 17
requirement_count: 7
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 14: Prespecified primary and secondary outcomes and defining components

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand prespecified primary and secondary outcomes and defining components. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Pre-specified primary and secondary outcomes, including the specific measurement variable, analysis metric, method of aggregation, and time point for each outcome" — CONSORT 2025 expanded checklist, item 14.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Outcomes|Outcomes]]
- **Domain classes:** [[OutcomeSpecification]], [[PrimaryOutcome]], [[SecondaryOutcome]], [[TrialRole]]

## Atomic requirements

1. **Outcome role as primary or secondary, as prespecified.** Report outcome role as primary or secondary, as prespecified. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-14-each-primary-secondary-outcome`)
2. **Specific measurement variable and definition where relevant.** Report specific measurement variable and definition where relevant. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-14-each-primary-secondary-outcome`)
3. **Analysis metric for each participant.** Report analysis metric for each participant. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-14-each-primary-secondary-outcome`)
4. **Method of aggregation for each trial group.** Report method of aggregation for each trial group. (`must`; expects `method_description`; scoped by `consort-2025-scope-item-14-each-primary-secondary-outcome`)
5. **Time point of interest for analysis.** Report time point of interest for analysis. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-14-each-primary-secondary-outcome`)
6. **Who assessed the outcome.** Report who assessed the outcome. (`must`; expects `person_or_role`; scoped by `consort-2025-scope-item-14-each-primary-secondary-outcome`)
7. **Rationale for outcome choice and whether it belongs to a core outcome set.** Report rationale for outcome choice and whether it belongs to a core outcome set. (`must`; expects `reason`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

- **Each primary and secondary outcome:** repeat over `outcome.primary_or_secondary`.

## Relations to other guideline elements

- [[CONSORT 16a]]
- [[CONSORT 21a]]
- [[CONSORT 26]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 14 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-14-r01"}},{"require":{"ref":"consort-2025-item-14-r02"}},{"require":{"ref":"consort-2025-item-14-r03"}},{"require":{"ref":"consort-2025-item-14-r04"}},{"require":{"ref":"consort-2025-item-14-r05"}},{"require":{"ref":"consort-2025-item-14-r06"}},{"require":{"ref":"consort-2025-item-14-r07"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Pre-specified primary and secondary outcomes, including the specific measurement variable, analysis metric, method of aggregation, and time point for each outcome",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-14",
    "item_number": "14",
    "label": "Prespecified primary and secondary outcomes and defining components",
    "order": 17,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand prespecified primary and secondary outcomes and defining components. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-16a",
        "consort-2025-item-21a",
        "consort-2025-item-26"
      ],
      "governed_by": [
        "consort-2025-rule-item-14-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-14-r01",
        "consort-2025-item-14-r02",
        "consort-2025-item-14-r03",
        "consort-2025-item-14-r04",
        "consort-2025-item-14-r05",
        "consort-2025-item-14-r06",
        "consort-2025-item-14-r07"
      ],
      "targets_domain_class": [
        "consort-class-outcome-specification",
        "consort-class-primary-outcome",
        "consort-class-secondary-outcome",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-14-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Outcome role as primary or secondary, as prespecified",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-14",
        "requirement_text": "Report outcome role as primary or secondary, as prespecified.",
        "scope": "consort-2025-scope-item-14-each-primary-secondary-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "14",
              "page": 5,
              "row_label": "Outcome role as primary or secondary, as prespecified"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Outcome role as primary or secondary, as prespecified",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-14-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Specific measurement variable and definition where relevant",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-14",
        "requirement_text": "Report specific measurement variable and definition where relevant.",
        "scope": "consort-2025-scope-item-14-each-primary-secondary-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "14",
              "page": 5,
              "row_label": "Specific measurement variable and definition where relevant"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Specific measurement variable and definition where relevant",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-14-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Analysis metric for each participant",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-14",
        "requirement_text": "Report analysis metric for each participant.",
        "scope": "consort-2025-scope-item-14-each-primary-secondary-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "14",
              "page": 5,
              "row_label": "Analysis metric for each participant"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Analysis metric for each participant",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-14-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Method of aggregation for each trial group",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-14",
        "requirement_text": "Report method of aggregation for each trial group.",
        "scope": "consort-2025-scope-item-14-each-primary-secondary-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "14",
              "page": 5,
              "row_label": "Method of aggregation for each trial group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Method of aggregation for each trial group",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "id": "consort-2025-item-14-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Time point of interest for analysis",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-14",
        "requirement_text": "Report time point of interest for analysis.",
        "scope": "consort-2025-scope-item-14-each-primary-secondary-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "14",
              "page": 5,
              "row_label": "Time point of interest for analysis"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Time point of interest for analysis",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-14-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who assessed the outcome",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-14",
        "requirement_text": "Report who assessed the outcome.",
        "scope": "consort-2025-scope-item-14-each-primary-secondary-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "14",
              "page": 5,
              "row_label": "Who assessed the outcome"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who assessed the outcome",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "id": "consort-2025-item-14-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Rationale for outcome choice and whether it belongs to a core outcome set",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-14",
        "requirement_text": "Report rationale for outcome choice and whether it belongs to a core outcome set.",
        "source_references": [
          {
            "locator": {
              "item_number": "14",
              "page": 5,
              "row_label": "Rationale for outcome choice and whether it belongs to a core outcome set"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Rationale for outcome choice and whether it belongs to a core outcome set",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-14-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-14-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-14-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-14-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-14-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-14-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-14-r07"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-14-completeness",
        "label": "Item 14 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "outcome.primary_or_secondary",
        "id": "consort-2025-scope-item-14-each-primary-secondary-outcome",
        "label": "Each primary and secondary outcome",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "14"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "14",
          "page": 5
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Pre-specified primary and secondary outcomes, including the specific measurement variable, analysis metric, method of aggregation, and time point for each outcome",
    "status": "reviewed",
    "topic": "consort-2025-topic-outcomes",
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
