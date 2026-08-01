---
id: consort-2025-item-16b
type: ChecklistItem
item_number: 16b
label: "Interim analyses and stopping guidelines"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-sample-size
status: reviewed
order: 20
requirement_count: 8
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 16b: Interim analyses and stopping guidelines

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand interim analyses and stopping guidelines. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Explanation of any interim analyses and stopping guidelines" — CONSORT 2025 expanded checklist, item 16b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Sample size|Sample size]]
- **Domain classes:** [[TrialDesign]], [[TrialRole]]

## Atomic requirements

1. **Whether interim analyses were conducted.** State whether interim analyses were conducted. (`must`; expects `boolean_statement`)
2. **Whether interim analyses were pre-planned.** State whether interim analyses were pre-planned. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-interim-analysis-conducted`)
3. **Timing, indications, and responsible role for interim analyses.** Report timing, indications, and responsible role for interim analyses. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-interim-analysis-conducted`)
4. **Statistical methods for interim analyses.** Report statistical methods for interim analyses. (`conditional_must`; expects `method_description`; when `consort-2025-condition-interim-analysis-conducted`)
5. **Who accessed interim results and whether they were blinded.** Report who accessed interim results and whether they were blinded. (`conditional_must`; expects `person_or_role`; when `consort-2025-condition-interim-analysis-conducted`)
6. **Whether an independent Data Monitoring Committee was involved.** State whether an independent Data Monitoring Committee was involved. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-interim-analysis-conducted`)
7. **Criteria used to inform early stopping or other adaptations.** Report criteria used to inform early stopping or other adaptations. (`must`; expects `free_text_description`)
8. **Who decided whether to continue, stop, or modify the trial.** Report who decided whether to continue, stop, or modify the trial. (`must`; expects `person_or_role`)

## Applicability

- **Interim analysis conducted:** `{"equals":true,"fact":"analysis.interim_analysis.conducted"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 23b]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 16b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-16b-r01"}},{"require":{"ref":"consort-2025-item-16b-r02"}},{"require":{"ref":"consort-2025-item-16b-r03"}},{"require":{"ref":"consort-2025-item-16b-r04"}},{"require":{"ref":"consort-2025-item-16b-r05"}},{"require":{"ref":"consort-2025-item-16b-r06"}},{"require":{"ref":"consort-2025-item-16b-r07"}},{"require":{"ref":"consort-2025-item-16b-r08"}}]}`

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
          "fact": "analysis.interim_analysis.conducted"
        },
        "id": "consort-2025-condition-interim-analysis-conducted",
        "label": "Interim analysis conducted",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "quoted_fragment": "Explanation of any interim analyses and stopping guidelines"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Explanation of any interim analyses and stopping guidelines",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-16b",
    "item_number": "16b",
    "label": "Interim analyses and stopping guidelines",
    "order": 20,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand interim analyses and stopping guidelines. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-23b"
      ],
      "governed_by": [
        "consort-2025-rule-item-16b-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-interim-analysis-conducted"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-16b-r01",
        "consort-2025-item-16b-r02",
        "consort-2025-item-16b-r03",
        "consort-2025-item-16b-r04",
        "consort-2025-item-16b-r05",
        "consort-2025-item-16b-r06",
        "consort-2025-item-16b-r07",
        "consort-2025-item-16b-r08"
      ],
      "targets_domain_class": [
        "consort-class-trial-design",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-16b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether interim analyses were conducted",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "State whether interim analyses were conducted.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Whether interim analyses were conducted"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether interim analyses were conducted",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-interim-analysis-conducted",
        "id": "consort-2025-item-16b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether interim analyses were pre-planned",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "State whether interim analyses were pre-planned.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Whether interim analyses were pre-planned"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether interim analyses were pre-planned",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-interim-analysis-conducted",
        "id": "consort-2025-item-16b-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Timing, indications, and responsible role for interim analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "Report timing, indications, and responsible role for interim analyses.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Timing, indications, and responsible role for interim analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Timing, indications, and responsible role for interim analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-interim-analysis-conducted",
        "id": "consort-2025-item-16b-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Statistical methods for interim analyses",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "Report statistical methods for interim analyses.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Statistical methods for interim analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Statistical methods for interim analyses",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-interim-analysis-conducted",
        "id": "consort-2025-item-16b-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who accessed interim results and whether they were blinded",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "Report who accessed interim results and whether they were blinded.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Who accessed interim results and whether they were blinded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who accessed interim results and whether they were blinded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "applicability_condition": "consort-2025-condition-interim-analysis-conducted",
        "id": "consort-2025-item-16b-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether an independent Data Monitoring Committee was involved",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "State whether an independent Data Monitoring Committee was involved.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Whether an independent Data Monitoring Committee was involved"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether an independent Data Monitoring Committee was involved",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "id": "consort-2025-item-16b-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Criteria used to inform early stopping or other adaptations",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "Report criteria used to inform early stopping or other adaptations.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Criteria used to inform early stopping or other adaptations"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Criteria used to inform early stopping or other adaptations",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-16b-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who decided whether to continue, stop, or modify the trial",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-16b",
        "requirement_text": "Report who decided whether to continue, stop, or modify the trial.",
        "source_references": [
          {
            "locator": {
              "item_number": "16b",
              "page": 6,
              "row_label": "Who decided whether to continue, stop, or modify the trial"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who decided whether to continue, stop, or modify the trial",
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
                "ref": "consort-2025-item-16b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16b-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16b-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16b-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16b-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16b-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16b-r07"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-16b-r08"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-16b-completeness",
        "label": "Item 16b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "16b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "16b",
          "page": 6
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Explanation of any interim analyses and stopping guidelines",
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
