---
id: consort-2025-item-26
type: ChecklistItem
item_number: 26
label: "Analysis numbers, outcome results, effect estimates, and precision"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-numbers-analysed-outcomes-and-estimation
status: reviewed
order: 38
requirement_count: 10
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 26: Analysis numbers, outcome results, effect estimates, and precision

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand analysis numbers, outcome results, effect estimates, and precision. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "For each primary and secondary outcome, by group: analysis numbers, available data, results, effect size, precision, and absolute and relative effects for binary outcomes" — CONSORT 2025 expanded checklist, item 26.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Numbers analysed, outcomes and estimation|Numbers analysed, outcomes and estimation]]
- **Domain classes:** [[OutcomeSpecification]], [[PrimaryOutcome]], [[SecondaryOutcome]], [[OutcomeResult]], [[GroupResult]], [[EffectEstimate]], [[PrecisionEstimate]], [[TrialArm]], [[Participant]]

## Atomic requirements

1. **Number of participants included in the analysis.** Report number of participants included in the analysis. (`must`; expects `number`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
2. **Number of participants with available data at the outcome time point.** Report number of participants with available data at the outcome time point. (`must`; expects `number`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
3. **Reasons for missing data.** Report reasons for missing data. (`must`; expects `reason`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
4. **Outcome summary for each group.** Report outcome summary for each group. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
5. **Estimated effect size.** Report estimated effect size. (`must`; expects `number`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
6. **Precision of the effect estimate.** Report precision of the effect estimate. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
7. **Continuous-outcome summary and effect measure where applicable.** Report continuous-outcome summary and effect measure where applicable. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
8. **Absolute effect for binary or time-to-event outcomes.** Report absolute effect for binary or time-to-event outcomes. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-binary-or-time-to-event`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
9. **Relative effect for binary or time-to-event outcomes.** Report relative effect for binary or time-to-event outcomes. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-binary-or-time-to-event`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)
10. **Precision for binary or time-to-event effect estimates.** Report precision for binary or time-to-event effect estimates. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-binary-or-time-to-event`; scoped by `consort-2025-scope-item-26-each-planned-outcome`)

## Applicability

- **Binary or time-to-event outcome:** `{"fact":"outcome.type","in":["binary","time_to_event"]}`

## Scope and repetition

- **Each planned primary and secondary outcome:** repeat over `outcome.planned_primary_or_secondary`.
- **Each trial group:** repeat over `trial.group`.

## Relations to other guideline elements

- [[CONSORT 14]]
- [[CONSORT 21a]]

## Formal rules

> [!rule] Logical composition
> - **Absolute and relative effect branch:** `all_of` over `consort-2025-item-26-r08`, `consort-2025-item-26-r09`, `consort-2025-item-26-r10`.

- **Item 26 repeats by outcome and trial group:** `{"for_each":{"domain":"outcome.planned_primary_or_secondary","then":{"for_each":{"domain":"trial.group","then":{"all":[{"require":{"ref":"consort-2025-item-26-r01"}},{"require":{"ref":"consort-2025-item-26-r02"}},{"require":{"ref":"consort-2025-item-26-r03"}}]}}}}}`
- **Binary and time-to-event effects:** `{"implies":{"if":{"fact":"outcome.type","in":["binary","time_to_event"]},"then":{"all":[{"require":{"ref":"consort-2025-item-26-r08"}},{"require":{"ref":"consort-2025-item-26-r09"}},{"require":{"ref":"consort-2025-item-26-r10"}}]}}}`
- **Item 26 completeness:** `{"satisfy_with":{"ref":"consort-2025-item-26-g-binary-time-event-effects"}}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "type_dependent",
        "expression": {
          "fact": "outcome.type",
          "in": [
            "binary",
            "time_to_event"
          ]
        },
        "id": "consort-2025-condition-binary-or-time-to-event",
        "label": "Binary or time-to-event outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "quoted_fragment": "For each primary and secondary outcome, by group: analysis numbers, available data, results, effect size, precision, and absolute and relative effects for binary outcomes"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "For each primary and secondary outcome, by group: analysis numbers, available data, results, effect size, precision, and absolute and relative effects for binary outcomes",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-26",
    "item_number": "26",
    "label": "Analysis numbers, outcome results, effect estimates, and precision",
    "order": 38,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand analysis numbers, outcome results, effect estimates, and precision. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-14",
        "consort-2025-item-21a"
      ],
      "governed_by": [
        "consort-2025-rule-item-26-outcome-group-scope",
        "consort-2025-rule-item-26-binary-time-event",
        "consort-2025-rule-item-26-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-binary-or-time-to-event"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-26-r01",
        "consort-2025-item-26-r02",
        "consort-2025-item-26-r03",
        "consort-2025-item-26-r04",
        "consort-2025-item-26-r05",
        "consort-2025-item-26-r06",
        "consort-2025-item-26-r07",
        "consort-2025-item-26-r08",
        "consort-2025-item-26-r09",
        "consort-2025-item-26-r10"
      ],
      "has_requirement_group": [
        "consort-2025-item-26-g-binary-time-event-effects"
      ],
      "targets_domain_class": [
        "consort-class-outcome-specification",
        "consort-class-primary-outcome",
        "consort-class-secondary-outcome",
        "consort-class-outcome-result",
        "consort-class-group-result",
        "consort-class-effect-estimate",
        "consort-class-precision-estimate",
        "consort-class-trial-arm",
        "consort-class-participant"
      ]
    },
    "requirement_groups": [
      {
        "applicability_condition": "consort-2025-condition-binary-or-time-to-event",
        "id": "consort-2025-item-26-g-binary-time-event-effects",
        "label": "Absolute and relative effect branch",
        "members": [
          "consort-2025-item-26-r08",
          "consort-2025-item-26-r09",
          "consort-2025-item-26-r10"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      }
    ],
    "requirements": [
      {
        "id": "consort-2025-item-26-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number of participants included in the analysis",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report number of participants included in the analysis.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Number of participants included in the analysis"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number of participants included in the analysis",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "id": "consort-2025-item-26-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number of participants with available data at the outcome time point",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report number of participants with available data at the outcome time point.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Number of participants with available data at the outcome time point"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number of participants with available data at the outcome time point",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "id": "consort-2025-item-26-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Reasons for missing data",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report reasons for missing data.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Reasons for missing data"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Reasons for missing data",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "id": "consort-2025-item-26-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Outcome summary for each group",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report outcome summary for each group.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Outcome summary for each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Outcome summary for each group",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-26-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Estimated effect size",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report estimated effect size.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Estimated effect size"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Estimated effect size",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "id": "consort-2025-item-26-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Precision of the effect estimate",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report precision of the effect estimate.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Precision of the effect estimate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Precision of the effect estimate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-26-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Continuous-outcome summary and effect measure where applicable",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report continuous-outcome summary and effect measure where applicable.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Continuous-outcome summary and effect measure where applicable"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Continuous-outcome summary and effect measure where applicable",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-binary-or-time-to-event",
        "id": "consort-2025-item-26-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Absolute effect for binary or time-to-event outcomes",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report absolute effect for binary or time-to-event outcomes.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Absolute effect for binary or time-to-event outcomes"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Absolute effect for binary or time-to-event outcomes",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-binary-or-time-to-event",
        "id": "consort-2025-item-26-r09",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Relative effect for binary or time-to-event outcomes",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report relative effect for binary or time-to-event outcomes.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Relative effect for binary or time-to-event outcomes"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Relative effect for binary or time-to-event outcomes",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-binary-or-time-to-event",
        "id": "consort-2025-item-26-r10",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Precision for binary or time-to-event effect estimates",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-26",
        "requirement_text": "Report precision for binary or time-to-event effect estimates.",
        "scope": "consort-2025-scope-item-26-each-planned-outcome",
        "source_references": [
          {
            "locator": {
              "item_number": "26",
              "page": 11,
              "row_label": "Precision for binary or time-to-event effect estimates"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Precision for binary or time-to-event effect estimates",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "for_each": {
            "domain": "outcome.planned_primary_or_secondary",
            "then": {
              "for_each": {
                "domain": "trial.group",
                "then": {
                  "all": [
                    {
                      "require": {
                        "ref": "consort-2025-item-26-r01"
                      }
                    },
                    {
                      "require": {
                        "ref": "consort-2025-item-26-r02"
                      }
                    },
                    {
                      "require": {
                        "ref": "consort-2025-item-26-r03"
                      }
                    }
                  ]
                }
              }
            }
          }
        },
        "id": "consort-2025-rule-item-26-outcome-group-scope",
        "label": "Item 26 repeats by outcome and trial group",
        "rule_kind": "repeated_scope",
        "status": "reviewed",
        "type": "NormativeRule"
      },
      {
        "expression": {
          "implies": {
            "if": {
              "fact": "outcome.type",
              "in": [
                "binary",
                "time_to_event"
              ]
            },
            "then": {
              "all": [
                {
                  "require": {
                    "ref": "consort-2025-item-26-r08"
                  }
                },
                {
                  "require": {
                    "ref": "consort-2025-item-26-r09"
                  }
                },
                {
                  "require": {
                    "ref": "consort-2025-item-26-r10"
                  }
                }
              ]
            }
          }
        },
        "id": "consort-2025-rule-item-26-binary-time-event",
        "label": "Binary and time-to-event effects",
        "rule_kind": "typed_branching",
        "status": "reviewed",
        "type": "NormativeRule"
      },
      {
        "expression": {
          "satisfy_with": {
            "ref": "consort-2025-item-26-g-binary-time-event-effects"
          }
        },
        "id": "consort-2025-rule-item-26-completeness",
        "label": "Item 26 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "outcome.planned_primary_or_secondary",
        "id": "consort-2025-scope-item-26-each-planned-outcome",
        "label": "Each planned primary and secondary outcome",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      },
      {
        "domain": "trial.group",
        "id": "consort-2025-scope-item-26-each-trial-group",
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
          "item_number": "26"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "26",
          "page": 11
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "For each primary and secondary outcome, by group: analysis numbers, available data, results, effect size, precision, and absolute and relative effects for binary outcomes",
    "status": "reviewed",
    "topic": "consort-2025-topic-numbers-analysed-outcomes-and-estimation",
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
