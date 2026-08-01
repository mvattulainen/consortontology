---
id: consort-2025-item-21a
type: ChecklistItem
item_number: 21a
label: "Statistical comparison methods for outcomes and harms"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-statistical-methods
status: reviewed
order: 27
requirement_count: 14
condition_count: 3
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 21a: Statistical comparison methods for outcomes and harms

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand statistical comparison methods for outcomes and harms. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Statistical methods used to compare groups for primary and secondary outcomes, including harms" — CONSORT 2025 expanded checklist, item 21a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Statistical methods|Statistical methods]]
- **Domain classes:** [[OutcomeSpecification]], [[HarmsOutcome]], [[EffectEstimate]], [[PrecisionEstimate]]

## Atomic requirements

1. **Main statistical comparison method for each analysis.** Report main statistical comparison method for each analysis. (`must`; expects `method_description`; scoped by `consort-2025-scope-item-21a-each-analysis`)
2. **Deviations from the statistical analysis plan.** Report deviations from the statistical analysis plan. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-21a-each-analysis`)
3. **Distinction between prespecified and post-hoc analyses.** Report distinction between prespecified and post-hoc analyses. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-21a-each-analysis`)
4. **Effect measure with interval estimates.** Report effect measure with interval estimates. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-21a-each-analysis`)
5. **Statistical significance level.** Report statistical significance level. (`must`; expects `number`; scoped by `consort-2025-scope-item-21a-each-analysis`)
6. **Bayesian priors.** Report bayesian priors. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-bayesian-analysis`)
7. **Bayesian computational and modelling choices.** Report bayesian computational and modelling choices. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-bayesian-analysis`)
8. **Bayesian effect measures with credible intervals.** Report bayesian effect measures with credible intervals. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-bayesian-analysis`)
9. **Rationale for adjusted analyses.** Report rationale for adjusted analyses. (`conditional_must`; expects `reason`; when `consort-2025-condition-adjusted-analysis`)
10. **Whether adjusted analyses were prespecified or post hoc.** State whether adjusted analyses were prespecified or post hoc. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-adjusted-analysis`)
11. **Covariates used for adjustment.** Report covariates used for adjustment. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-adjusted-analysis`)
12. **Adjusted-analysis methods, including handling of continuous covariates.** Report adjusted-analysis methods, including handling of continuous covariates. (`conditional_must`; expects `method_description`; when `consort-2025-condition-adjusted-analysis`)
13. **Methods used to account for multiplicity.** Report methods used to account for multiplicity. (`conditional_must`; expects `method_description`; when `consort-2025-condition-multiplicity-addressed`)
14. **Software used for analyses.** Report software used for analyses. (`must`; expects `software_name`; scoped by `consort-2025-scope-item-21a-each-analysis`)

## Applicability

- **Bayesian analysis used:** `{"equals":true,"fact":"analysis.method.bayesian"}`
- **Adjusted analysis used:** `{"equals":true,"fact":"analysis.adjusted.performed"}`
- **Multiplicity is applicable:** `{"equals":true,"fact":"analysis.multiplicity.applicable"}`

## Scope and repetition

- **Each statistical analysis:** repeat over `analysis.declared`.

## Relations to other guideline elements

- [[CONSORT 14]]
- [[CONSORT 26]]

## Formal rules

> [!rule] Logical composition
> - **Base statistical methods:** `all_of` over `consort-2025-item-21a-r01`, `consort-2025-item-21a-r02`, `consort-2025-item-21a-r03`, `consort-2025-item-21a-r04`, `consort-2025-item-21a-r05`.
- **Bayesian details:** `all_of` over `consort-2025-item-21a-r06`, `consort-2025-item-21a-r07`, `consort-2025-item-21a-r08`.
- **Adjusted-analysis details:** `all_of` over `consort-2025-item-21a-r09`, `consort-2025-item-21a-r10`, `consort-2025-item-21a-r11`, `consort-2025-item-21a-r12`.

- **Item 21a completeness:** `{"satisfy_with":{"ref":"consort-2025-item-21a-g-base"}}`

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
          "fact": "analysis.method.bayesian"
        },
        "id": "consort-2025-condition-bayesian-analysis",
        "label": "Bayesian analysis used",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "quoted_fragment": "Statistical methods used to compare groups for primary and secondary outcomes, including harms"
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
          "fact": "analysis.adjusted.performed"
        },
        "id": "consort-2025-condition-adjusted-analysis",
        "label": "Adjusted analysis used",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "quoted_fragment": "Statistical methods used to compare groups for primary and secondary outcomes, including harms"
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
          "fact": "analysis.multiplicity.applicable"
        },
        "id": "consort-2025-condition-multiplicity-addressed",
        "label": "Multiplicity is applicable",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "quoted_fragment": "Statistical methods used to compare groups for primary and secondary outcomes, including harms"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Statistical methods used to compare groups for primary and secondary outcomes, including harms",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-21a",
    "item_number": "21a",
    "label": "Statistical comparison methods for outcomes and harms",
    "order": 27,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand statistical comparison methods for outcomes and harms. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-14",
        "consort-2025-item-26"
      ],
      "governed_by": [
        "consort-2025-rule-item-21a-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-bayesian-analysis",
        "consort-2025-condition-adjusted-analysis",
        "consort-2025-condition-multiplicity-addressed"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-21a-r01",
        "consort-2025-item-21a-r02",
        "consort-2025-item-21a-r03",
        "consort-2025-item-21a-r04",
        "consort-2025-item-21a-r05",
        "consort-2025-item-21a-r06",
        "consort-2025-item-21a-r07",
        "consort-2025-item-21a-r08",
        "consort-2025-item-21a-r09",
        "consort-2025-item-21a-r10",
        "consort-2025-item-21a-r11",
        "consort-2025-item-21a-r12",
        "consort-2025-item-21a-r13",
        "consort-2025-item-21a-r14"
      ],
      "has_requirement_group": [
        "consort-2025-item-21a-g-base",
        "consort-2025-item-21a-g-bayesian",
        "consort-2025-item-21a-g-adjusted"
      ],
      "targets_domain_class": [
        "consort-class-outcome-specification",
        "consort-class-harms-outcome",
        "consort-class-effect-estimate",
        "consort-class-precision-estimate"
      ]
    },
    "requirement_groups": [
      {
        "id": "consort-2025-item-21a-g-base",
        "label": "Base statistical methods",
        "members": [
          "consort-2025-item-21a-r01",
          "consort-2025-item-21a-r02",
          "consort-2025-item-21a-r03",
          "consort-2025-item-21a-r04",
          "consort-2025-item-21a-r05"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      },
      {
        "applicability_condition": "consort-2025-condition-bayesian-analysis",
        "id": "consort-2025-item-21a-g-bayesian",
        "label": "Bayesian details",
        "members": [
          "consort-2025-item-21a-r06",
          "consort-2025-item-21a-r07",
          "consort-2025-item-21a-r08"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      },
      {
        "applicability_condition": "consort-2025-condition-adjusted-analysis",
        "id": "consort-2025-item-21a-g-adjusted",
        "label": "Adjusted-analysis details",
        "members": [
          "consort-2025-item-21a-r09",
          "consort-2025-item-21a-r10",
          "consort-2025-item-21a-r11",
          "consort-2025-item-21a-r12"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      }
    ],
    "requirements": [
      {
        "id": "consort-2025-item-21a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Main statistical comparison method for each analysis",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report main statistical comparison method for each analysis.",
        "scope": "consort-2025-scope-item-21a-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Main statistical comparison method for each analysis"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Main statistical comparison method for each analysis",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "id": "consort-2025-item-21a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Deviations from the statistical analysis plan",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report deviations from the statistical analysis plan.",
        "scope": "consort-2025-scope-item-21a-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Deviations from the statistical analysis plan"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Deviations from the statistical analysis plan",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-21a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Distinction between prespecified and post-hoc analyses",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report distinction between prespecified and post-hoc analyses.",
        "scope": "consort-2025-scope-item-21a-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Distinction between prespecified and post-hoc analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Distinction between prespecified and post-hoc analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-21a-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Effect measure with interval estimates",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report effect measure with interval estimates.",
        "scope": "consort-2025-scope-item-21a-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Effect measure with interval estimates"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Effect measure with interval estimates",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-21a-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Statistical significance level",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report statistical significance level.",
        "scope": "consort-2025-scope-item-21a-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Statistical significance level"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Statistical significance level",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-bayesian-analysis",
        "id": "consort-2025-item-21a-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Bayesian priors",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report bayesian priors.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Bayesian priors"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Bayesian priors",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-bayesian-analysis",
        "id": "consort-2025-item-21a-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Bayesian computational and modelling choices",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report bayesian computational and modelling choices.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Bayesian computational and modelling choices"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Bayesian computational and modelling choices",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-bayesian-analysis",
        "id": "consort-2025-item-21a-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Bayesian effect measures with credible intervals",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report bayesian effect measures with credible intervals.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Bayesian effect measures with credible intervals"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Bayesian effect measures with credible intervals",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-adjusted-analysis",
        "id": "consort-2025-item-21a-r09",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Rationale for adjusted analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report rationale for adjusted analyses.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Rationale for adjusted analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Rationale for adjusted analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "applicability_condition": "consort-2025-condition-adjusted-analysis",
        "id": "consort-2025-item-21a-r10",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether adjusted analyses were prespecified or post hoc",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "State whether adjusted analyses were prespecified or post hoc.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Whether adjusted analyses were prespecified or post hoc"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether adjusted analyses were prespecified or post hoc",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-adjusted-analysis",
        "id": "consort-2025-item-21a-r11",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Covariates used for adjustment",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report covariates used for adjustment.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Covariates used for adjustment"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Covariates used for adjustment",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-adjusted-analysis",
        "id": "consort-2025-item-21a-r12",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Adjusted-analysis methods, including handling of continuous covariates",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report adjusted-analysis methods, including handling of continuous covariates.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Adjusted-analysis methods, including handling of continuous covariates"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Adjusted-analysis methods, including handling of continuous covariates",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-multiplicity-addressed",
        "id": "consort-2025-item-21a-r13",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Methods used to account for multiplicity",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report methods used to account for multiplicity.",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Methods used to account for multiplicity"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Methods used to account for multiplicity",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "id": "consort-2025-item-21a-r14",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Software used for analyses",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21a",
        "requirement_text": "Report software used for analyses.",
        "scope": "consort-2025-scope-item-21a-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21a",
              "page": 8,
              "row_label": "Software used for analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Software used for analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "software_name"
      }
    ],
    "rules": [
      {
        "expression": {
          "satisfy_with": {
            "ref": "consort-2025-item-21a-g-base"
          }
        },
        "id": "consort-2025-rule-item-21a-completeness",
        "label": "Item 21a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "analysis.declared",
        "id": "consort-2025-scope-item-21a-each-analysis",
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
          "item_number": "21a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "21a",
          "page": 8
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Statistical methods used to compare groups for primary and secondary outcomes, including harms",
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
