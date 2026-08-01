---
id: consort-2025-item-15
type: ChecklistItem
item_number: 15
label: "Definition and assessment of harms"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-harms
status: reviewed
order: 18
requirement_count: 8
condition_count: 4
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 15: Definition and assessment of harms

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand definition and assessment of harms. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "How harms were defined and assessed (e.g., systematically, non-systematically)" — CONSORT 2025 expanded checklist, item 15.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Harms|Harms]]
- **Domain classes:** [[HarmsOutcome]], [[BlindingProcess]], [[TrialRole]]

## Atomic requirements

1. **Definition and measurement for each systematically assessed harm.** Report definition and measurement for each systematically assessed harm. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-systematic-harms-assessed`; scoped by `consort-2025-scope-item-15-each-systematic-harm`)
2. **Metrics, aggregation method, and analysis time point for systematically assessed harms where appropriate.** Report metrics, aggregation method, and analysis time point for systematically assessed harms where appropriate. (`conditional_must`; expects `method_description`; when `consort-2025-condition-systematic-harm-metrics-applicable`; scoped by `consort-2025-scope-item-15-each-systematic-harm`)
3. **Assessor, assessor blinding, assessment time points, and recording period for systematic harms assessment.** Report assessor, assessor blinding, assessment time points, and recording period for systematic harms assessment. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-systematic-harms-assessed`; scoped by `consort-2025-scope-item-15-each-systematic-harm`)
4. **Collection method for each non-systematically assessed harm.** Report collection method for each non-systematically assessed harm. (`conditional_must`; expects `method_description`; when `consort-2025-condition-nonsystematic-harms-assessed`; scoped by `consort-2025-scope-item-15-each-nonsystematic-harm`)
5. **Assessment time points and recording period for non-systematic harms assessment.** Report assessment time points and recording period for non-systematic harms assessment. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-nonsystematic-harms-assessed`; scoped by `consort-2025-scope-item-15-each-nonsystematic-harm`)
6. **Coding and severity-grading process, responsible role, blinding, and systems used.** Report coding and severity-grading process, responsible role, blinding, and systems used. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-nonsystematic-harms-assessed`; scoped by `consort-2025-scope-item-15-each-nonsystematic-harm`)
7. **Definitions used to group harms by seriousness, severity, body system, withdrawals, and causality.** Report definitions used to group harms by seriousness, severity, body system, withdrawals, and causality. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-harm-grouping-used`)
8. **Who grouped harms and whether that person was blinded.** Report who grouped harms and whether that person was blinded. (`conditional_must`; expects `person_or_role`; when `consort-2025-condition-harm-grouping-used`)

## Applicability

- **Systematic harms assessment was used:** `{"equals":true,"fact":"harm.systematic_assessment.used"}`
- **Systematic harm metrics are appropriate:** `{"all":[{"equals":true,"fact":"harm.systematic_assessment.used"},{"equals":true,"fact":"harm.metrics.applicable"}]}`
- **Non-systematic harms assessment was used:** `{"equals":true,"fact":"harm.nonsystematic_assessment.used"}`
- **Harms were grouped:** `{"equals":true,"fact":"harm.grouping.used"}`

## Scope and repetition

- **Each systematically assessed harm:** repeat over `harm.systematically_assessed`.
- **Each non-systematically assessed harm:** repeat over `harm.non_systematically_assessed`.

## Relations to other guideline elements

- [[CONSORT 27]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 15 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-15-r01"}},{"require":{"ref":"consort-2025-item-15-r02"}},{"require":{"ref":"consort-2025-item-15-r03"}},{"require":{"ref":"consort-2025-item-15-r04"}},{"require":{"ref":"consort-2025-item-15-r05"}},{"require":{"ref":"consort-2025-item-15-r06"}},{"require":{"ref":"consort-2025-item-15-r07"}},{"require":{"ref":"consort-2025-item-15-r08"}}]}`

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
          "fact": "harm.systematic_assessment.used"
        },
        "id": "consort-2025-condition-systematic-harms-assessed",
        "label": "Systematic harms assessment was used",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "quoted_fragment": "How harms were defined and assessed (e.g., systematically, non-systematically)"
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
          "all": [
            {
              "equals": true,
              "fact": "harm.systematic_assessment.used"
            },
            {
              "equals": true,
              "fact": "harm.metrics.applicable"
            }
          ]
        },
        "id": "consort-2025-condition-systematic-harm-metrics-applicable",
        "label": "Systematic harm metrics are appropriate",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "quoted_fragment": "How harms were defined and assessed (e.g., systematically, non-systematically)"
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
          "fact": "harm.nonsystematic_assessment.used"
        },
        "id": "consort-2025-condition-nonsystematic-harms-assessed",
        "label": "Non-systematic harms assessment was used",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "quoted_fragment": "How harms were defined and assessed (e.g., systematically, non-systematically)"
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
          "fact": "harm.grouping.used"
        },
        "id": "consort-2025-condition-harm-grouping-used",
        "label": "Harms were grouped",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "quoted_fragment": "How harms were defined and assessed (e.g., systematically, non-systematically)"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "How harms were defined and assessed (e.g., systematically, non-systematically)",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-15",
    "item_number": "15",
    "label": "Definition and assessment of harms",
    "order": 18,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand definition and assessment of harms. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-27"
      ],
      "governed_by": [
        "consort-2025-rule-item-15-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-systematic-harms-assessed",
        "consort-2025-condition-systematic-harm-metrics-applicable",
        "consort-2025-condition-nonsystematic-harms-assessed",
        "consort-2025-condition-harm-grouping-used"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-15-r01",
        "consort-2025-item-15-r02",
        "consort-2025-item-15-r03",
        "consort-2025-item-15-r04",
        "consort-2025-item-15-r05",
        "consort-2025-item-15-r06",
        "consort-2025-item-15-r07",
        "consort-2025-item-15-r08"
      ],
      "targets_domain_class": [
        "consort-class-harms-outcome",
        "consort-class-blinding-process",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-systematic-harms-assessed",
        "id": "consort-2025-item-15-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Definition and measurement for each systematically assessed harm",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report definition and measurement for each systematically assessed harm.",
        "scope": "consort-2025-scope-item-15-each-systematic-harm",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Definition and measurement for each systematically assessed harm"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Definition and measurement for each systematically assessed harm",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-systematic-harm-metrics-applicable",
        "id": "consort-2025-item-15-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Metrics, aggregation method, and analysis time point for systematically assessed harms where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report metrics, aggregation method, and analysis time point for systematically assessed harms where appropriate.",
        "scope": "consort-2025-scope-item-15-each-systematic-harm",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Metrics, aggregation method, and analysis time point for systematically assessed harms where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Metrics, aggregation method, and analysis time point for systematically assessed harms where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-systematic-harms-assessed",
        "id": "consort-2025-item-15-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Assessor, assessor blinding, assessment time points, and recording period for systematic harms assessment",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report assessor, assessor blinding, assessment time points, and recording period for systematic harms assessment.",
        "scope": "consort-2025-scope-item-15-each-systematic-harm",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Assessor, assessor blinding, assessment time points, and recording period for systematic harms assessment"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Assessor, assessor blinding, assessment time points, and recording period for systematic harms assessment",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-nonsystematic-harms-assessed",
        "id": "consort-2025-item-15-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Collection method for each non-systematically assessed harm",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report collection method for each non-systematically assessed harm.",
        "scope": "consort-2025-scope-item-15-each-nonsystematic-harm",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Collection method for each non-systematically assessed harm"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Collection method for each non-systematically assessed harm",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-nonsystematic-harms-assessed",
        "id": "consort-2025-item-15-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Assessment time points and recording period for non-systematic harms assessment",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report assessment time points and recording period for non-systematic harms assessment.",
        "scope": "consort-2025-scope-item-15-each-nonsystematic-harm",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Assessment time points and recording period for non-systematic harms assessment"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Assessment time points and recording period for non-systematic harms assessment",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-nonsystematic-harms-assessed",
        "id": "consort-2025-item-15-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Coding and severity-grading process, responsible role, blinding, and systems used",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report coding and severity-grading process, responsible role, blinding, and systems used.",
        "scope": "consort-2025-scope-item-15-each-nonsystematic-harm",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Coding and severity-grading process, responsible role, blinding, and systems used"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Coding and severity-grading process, responsible role, blinding, and systems used",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-harm-grouping-used",
        "id": "consort-2025-item-15-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Definitions used to group harms by seriousness, severity, body system, withdrawals, and causality",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report definitions used to group harms by seriousness, severity, body system, withdrawals, and causality.",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Definitions used to group harms by seriousness, severity, body system, withdrawals, and causality"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Definitions used to group harms by seriousness, severity, body system, withdrawals, and causality",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-harm-grouping-used",
        "id": "consort-2025-item-15-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who grouped harms and whether that person was blinded",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-15",
        "requirement_text": "Report who grouped harms and whether that person was blinded.",
        "source_references": [
          {
            "locator": {
              "item_number": "15",
              "page": 5,
              "row_label": "Who grouped harms and whether that person was blinded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who grouped harms and whether that person was blinded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-15-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-15-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-15-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-15-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-15-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-15-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-15-r07"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-15-r08"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-15-completeness",
        "label": "Item 15 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "harm.systematically_assessed",
        "id": "consort-2025-scope-item-15-each-systematic-harm",
        "label": "Each systematically assessed harm",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      },
      {
        "domain": "harm.non_systematically_assessed",
        "id": "consort-2025-scope-item-15-each-nonsystematic-harm",
        "label": "Each non-systematically assessed harm",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "15"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "15",
          "page": 5
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "How harms were defined and assessed (e.g., systematically, non-systematically)",
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
