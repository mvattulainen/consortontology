---
id: consort-2025-item-27
type: ChecklistItem
item_number: 27
label: "Harms or unintended events in each group"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-harms
status: reviewed
order: 39
requirement_count: 7
condition_count: 3
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 27: Harms or unintended events in each group

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand harms or unintended events in each group. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "All harms or unintended events in each group" — CONSORT 2025 expanded checklist, item 27.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Harms|Harms]]
- **Domain classes:** [[HarmsOutcome]], [[OutcomeResult]], [[GroupResult]], [[EffectEstimate]], [[PrecisionEstimate]], [[TrialArm]]

## Atomic requirements

1. **Number of deaths.** Report number of deaths. (`must`; expects `number`; scoped by `consort-2025-scope-item-27-each-trial-group`)
2. **Number withdrawn due to harms.** Report number withdrawn due to harms. (`must`; expects `number`; scoped by `consort-2025-scope-item-27-each-trial-group`)
3. **Number with at least one systematically assessed, non-systematically assessed, or serious harm.** Report number with at least one systematically assessed, non-systematically assessed, or serious harm. (`must`; expects `number`; scoped by `consort-2025-scope-item-27-each-trial-group`)
4. **Number of harm events where appropriate.** Report number of harm events where appropriate. (`conditional_must`; expects `number`; when `consort-2025-condition-harm-event-count-appropriate`; scoped by `consort-2025-scope-item-27-each-trial-group`)
5. **Effect estimate and precision for harms where appropriate.** Report effect estimate and precision for harms where appropriate. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-harm-effect-estimate-appropriate`; scoped by `consort-2025-scope-item-27-each-trial-group`)
6. **Absolute and relative effects for binary or time-to-event harms where appropriate.** Report absolute and relative effects for binary or time-to-event harms where appropriate. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-harm-binary-time-event-effect-appropriate`; scoped by `consort-2025-scope-item-27-each-trial-group`)
7. **Explicit statement that no adverse events were identified.** Provide an explicit statement that no adverse events were identified. (`must`; expects `boolean_statement`)

## Applicability

- **A harm event count is appropriate:** `{"equals":true,"fact":"harm.event_count.applicable"}`
- **A comparative harm effect estimate is appropriate:** `{"equals":true,"fact":"harm.effect_estimate.applicable"}`
- **Binary or time-to-event harm effects are appropriate:** `{"all":[{"equals":true,"fact":"harm.effect_estimate.applicable"},{"fact":"harm.outcome.type","in":["binary","time_to_event"]}]}`

## Scope and repetition

- **Each trial group:** repeat over `trial.group`.

## Relations to other guideline elements

- [[CONSORT 15]]
- [[CONSORT 21a]]

## Formal rules

> [!rule] Logical composition
> - **Harms reported or explicit none:** `any_of` over `consort-2025-item-27-g-harms-reported`, `consort-2025-item-27-r07`.
- **Harms reporting branch:** `all_of` over `consort-2025-item-27-r01`, `consort-2025-item-27-r02`, `consort-2025-item-27-r03`, `consort-2025-item-27-r04`, `consort-2025-item-27-r05`, `consort-2025-item-27-r06`.

- **Item 27 completeness:** `{"satisfy_with":{"ref":"consort-2025-item-27-g-harms-or-explicit-none"}}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "contextual",
        "expression": {
          "equals": true,
          "fact": "harm.event_count.applicable"
        },
        "id": "consort-2025-condition-harm-event-count-appropriate",
        "label": "A harm event count is appropriate",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "quoted_fragment": "All harms or unintended events in each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      },
      {
        "condition_kind": "contextual",
        "expression": {
          "equals": true,
          "fact": "harm.effect_estimate.applicable"
        },
        "id": "consort-2025-condition-harm-effect-estimate-appropriate",
        "label": "A comparative harm effect estimate is appropriate",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "quoted_fragment": "All harms or unintended events in each group"
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
          "all": [
            {
              "equals": true,
              "fact": "harm.effect_estimate.applicable"
            },
            {
              "fact": "harm.outcome.type",
              "in": [
                "binary",
                "time_to_event"
              ]
            }
          ]
        },
        "id": "consort-2025-condition-harm-binary-time-event-effect-appropriate",
        "label": "Binary or time-to-event harm effects are appropriate",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "quoted_fragment": "All harms or unintended events in each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "All harms or unintended events in each group",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-27",
    "item_number": "27",
    "label": "Harms or unintended events in each group",
    "order": 39,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand harms or unintended events in each group. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-15",
        "consort-2025-item-21a"
      ],
      "governed_by": [
        "consort-2025-rule-item-27-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-harm-event-count-appropriate",
        "consort-2025-condition-harm-effect-estimate-appropriate",
        "consort-2025-condition-harm-binary-time-event-effect-appropriate"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-27-r01",
        "consort-2025-item-27-r02",
        "consort-2025-item-27-r03",
        "consort-2025-item-27-r04",
        "consort-2025-item-27-r05",
        "consort-2025-item-27-r06",
        "consort-2025-item-27-r07"
      ],
      "has_requirement_group": [
        "consort-2025-item-27-g-harms-or-explicit-none",
        "consort-2025-item-27-g-harms-reported"
      ],
      "targets_domain_class": [
        "consort-class-harms-outcome",
        "consort-class-outcome-result",
        "consort-class-group-result",
        "consort-class-effect-estimate",
        "consort-class-precision-estimate",
        "consort-class-trial-arm"
      ]
    },
    "requirement_groups": [
      {
        "id": "consort-2025-item-27-g-harms-or-explicit-none",
        "label": "Harms reported or explicit none",
        "members": [
          "consort-2025-item-27-g-harms-reported",
          "consort-2025-item-27-r07"
        ],
        "operator": "any_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      },
      {
        "id": "consort-2025-item-27-g-harms-reported",
        "label": "Harms reporting branch",
        "members": [
          "consort-2025-item-27-r01",
          "consort-2025-item-27-r02",
          "consort-2025-item-27-r03",
          "consort-2025-item-27-r04",
          "consort-2025-item-27-r05",
          "consort-2025-item-27-r06"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      }
    ],
    "requirements": [
      {
        "id": "consort-2025-item-27-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number of deaths",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-27",
        "requirement_text": "Report number of deaths.",
        "scope": "consort-2025-scope-item-27-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "row_label": "Number of deaths"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number of deaths",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "id": "consort-2025-item-27-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number withdrawn due to harms",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-27",
        "requirement_text": "Report number withdrawn due to harms.",
        "scope": "consort-2025-scope-item-27-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "row_label": "Number withdrawn due to harms"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number withdrawn due to harms",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "id": "consort-2025-item-27-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number with at least one systematically assessed, non-systematically assessed, or serious harm",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-27",
        "requirement_text": "Report number with at least one systematically assessed, non-systematically assessed, or serious harm.",
        "scope": "consort-2025-scope-item-27-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "row_label": "Number with at least one systematically assessed, non-systematically assessed, or serious harm"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number with at least one systematically assessed, non-systematically assessed, or serious harm",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-harm-event-count-appropriate",
        "id": "consort-2025-item-27-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number of harm events where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-27",
        "requirement_text": "Report number of harm events where appropriate.",
        "scope": "consort-2025-scope-item-27-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "row_label": "Number of harm events where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number of harm events where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-harm-effect-estimate-appropriate",
        "id": "consort-2025-item-27-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Effect estimate and precision for harms where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-27",
        "requirement_text": "Report effect estimate and precision for harms where appropriate.",
        "scope": "consort-2025-scope-item-27-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "row_label": "Effect estimate and precision for harms where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Effect estimate and precision for harms where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-harm-binary-time-event-effect-appropriate",
        "id": "consort-2025-item-27-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Absolute and relative effects for binary or time-to-event harms where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-27",
        "requirement_text": "Report absolute and relative effects for binary or time-to-event harms where appropriate.",
        "scope": "consort-2025-scope-item-27-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "row_label": "Absolute and relative effects for binary or time-to-event harms where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Absolute and relative effects for binary or time-to-event harms where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-27-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Explicit statement that no adverse events were identified",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-27",
        "requirement_text": "Provide an explicit statement that no adverse events were identified.",
        "source_references": [
          {
            "locator": {
              "item_number": "27",
              "page": 11,
              "row_label": "Explicit statement that no adverse events were identified"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Explicit statement that no adverse events were identified",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      }
    ],
    "rules": [
      {
        "expression": {
          "satisfy_with": {
            "ref": "consort-2025-item-27-g-harms-or-explicit-none"
          }
        },
        "id": "consort-2025-rule-item-27-completeness",
        "label": "Item 27 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "trial.group",
        "id": "consort-2025-scope-item-27-each-trial-group",
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
          "item_number": "27"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "27",
          "page": 11
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "All harms or unintended events in each group",
    "status": "reviewed",
    "topic": "consort-2025-topic-harms",
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
