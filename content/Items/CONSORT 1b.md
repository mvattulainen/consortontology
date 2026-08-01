---
id: consort-2025-item-1b
type: ChecklistItem
item_number: 1b
label: "Structured summary of trial design, methods, results, and conclusions"
guideline_version: consort-2025
section: consort-2025-section-title-and-abstract
topic: consort-2025-topic-title-and-structured-abstract
status: reviewed
order: 2
requirement_count: 15
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 1b: Structured summary of trial design, methods, results, and conclusions

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand structured summary of trial design, methods, results, and conclusions. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Structured summary of the trial design, methods, results, and conclusions" — CONSORT 2025 expanded checklist, item 1b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Title and Abstract|Title and abstract]]
- **Topic:** [[Title and structured abstract|Title and structured abstract]]
- **Domain classes:** [[RandomisedTrial]], [[TrialDesign]], [[TrialArm]], [[Participant]], [[Intervention]], [[Comparator]], [[PrimaryOutcome]], [[HarmsOutcome]], [[OutcomeResult]], [[GroupResult]], [[EffectEstimate]], [[PrecisionEstimate]]

## Atomic requirements

1. **Specific objectives.** Report specific objectives. (`must`; expects `free_text_description`)
2. **Trial design and framework.** Report trial design and framework. (`must`; expects `free_text_description`)
3. **Eligibility criteria for participants and settings.** Report eligibility criteria for participants and settings. (`must`; expects `free_text_description`)
4. **Interventions and comparators intended for each group.** Report interventions and comparators intended for each group. (`must`; expects `free_text_description`)
5. **Primary outcomes.** Report primary outcomes. (`must`; expects `free_text_description`)
6. **Method used to allocate participants to interventions.** Report method used to allocate participants to interventions. (`must`; expects `method_description`)
7. **Roles blinded after assignment.** Report roles blinded after assignment. (`must`; expects `free_text_description`)
8. **Number of participants randomised to each group.** Report number of participants randomised to each group. (`must`; expects `number`)
9. **For the primary outcome, number analysed in each group.** Report for the primary outcome, number analysed in each group. (`must`; expects `number`)
10. **For the primary outcome, result for each group, estimated effect size, and precision.** Report for the primary outcome, result for each group, estimated effect size, and precision. (`must`; expects `number`)
11. **Important harms or unintended events for each group.** Report important harms or unintended events for each group. (`must`; expects `free_text_description`)
12. **General interpretation of the results.** Report general interpretation of the results. (`must`; expects `free_text_description`)
13. **Trial registry name and identification number.** Report trial registry name and identification number. (`must`; expects `number`)
14. **Sources of funding.** Report sources of funding. (`must`; expects `free_text_description`)
15. **Exclude information that does not appear in the body of the report.** Report exclude information that does not appear in the body of the report. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 1a]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 1b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-1b-r01"}},{"require":{"ref":"consort-2025-item-1b-r02"}},{"require":{"ref":"consort-2025-item-1b-r03"}},{"require":{"ref":"consort-2025-item-1b-r04"}},{"require":{"ref":"consort-2025-item-1b-r05"}},{"require":{"ref":"consort-2025-item-1b-r06"}},{"require":{"ref":"consort-2025-item-1b-r07"}},{"require":{"ref":"consort-2025-item-1b-r08"}},{"require":{"ref":"consort-2025-item-1b-r09"}},{"require":{"ref":"consort-2025-item-1b-r10"}},{"require":{"ref":"consort-2025-item-1b-r11"}},{"require":{"ref":"consort-2025-item-1b-r12"}},{"require":{"ref":"consort-2025-item-1b-r13"}},{"require":{"ref":"consort-2025-item-1b-r14"}},{"require":{"ref":"consort-2025-item-1b-r15"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Structured summary of the trial design, methods, results, and conclusions",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-1b",
    "item_number": "1b",
    "label": "Structured summary of trial design, methods, results, and conclusions",
    "order": 2,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand structured summary of trial design, methods, results, and conclusions. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-1a"
      ],
      "governed_by": [
        "consort-2025-rule-item-1b-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-1b-r01",
        "consort-2025-item-1b-r02",
        "consort-2025-item-1b-r03",
        "consort-2025-item-1b-r04",
        "consort-2025-item-1b-r05",
        "consort-2025-item-1b-r06",
        "consort-2025-item-1b-r07",
        "consort-2025-item-1b-r08",
        "consort-2025-item-1b-r09",
        "consort-2025-item-1b-r10",
        "consort-2025-item-1b-r11",
        "consort-2025-item-1b-r12",
        "consort-2025-item-1b-r13",
        "consort-2025-item-1b-r14",
        "consort-2025-item-1b-r15"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-trial-design",
        "consort-class-trial-arm",
        "consort-class-participant",
        "consort-class-intervention",
        "consort-class-comparator",
        "consort-class-primary-outcome",
        "consort-class-harms-outcome",
        "consort-class-outcome-result",
        "consort-class-group-result",
        "consort-class-effect-estimate",
        "consort-class-precision-estimate"
      ]
    },
    "requirements": [
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Specific objectives",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report specific objectives.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Specific objectives"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Specific objectives",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Trial design and framework",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report trial design and framework.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Trial design and framework"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Trial design and framework",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Eligibility criteria for participants and settings",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report eligibility criteria for participants and settings.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Eligibility criteria for participants and settings"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Eligibility criteria for participants and settings",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Interventions and comparators intended for each group",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report interventions and comparators intended for each group.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Interventions and comparators intended for each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Interventions and comparators intended for each group",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Primary outcomes",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report primary outcomes.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Primary outcomes"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Primary outcomes",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Method used to allocate participants to interventions",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report method used to allocate participants to interventions.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Method used to allocate participants to interventions"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Method used to allocate participants to interventions",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Roles blinded after assignment",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report roles blinded after assignment.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Roles blinded after assignment"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Roles blinded after assignment",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number of participants randomised to each group",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report number of participants randomised to each group.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Number of participants randomised to each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number of participants randomised to each group",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r09",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "For the primary outcome, number analysed in each group",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report for the primary outcome, number analysed in each group.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "For the primary outcome, number analysed in each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "For the primary outcome, number analysed in each group",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r10",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "For the primary outcome, result for each group, estimated effect size, and precision",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report for the primary outcome, result for each group, estimated effect size, and precision.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "For the primary outcome, result for each group, estimated effect size, and precision"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "For the primary outcome, result for each group, estimated effect size, and precision",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r11",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Important harms or unintended events for each group",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report important harms or unintended events for each group.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Important harms or unintended events for each group"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Important harms or unintended events for each group",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r12",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "General interpretation of the results",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report general interpretation of the results.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "General interpretation of the results"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "General interpretation of the results",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r13",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Trial registry name and identification number",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report trial registry name and identification number.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Trial registry name and identification number"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Trial registry name and identification number",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r14",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Sources of funding",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report sources of funding.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Sources of funding"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Sources of funding",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "expected_location": "abstract",
        "id": "consort-2025-item-1b-r15",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Exclude information that does not appear in the body of the report",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-1b",
        "requirement_text": "Report exclude information that does not appear in the body of the report.",
        "source_references": [
          {
            "locator": {
              "item_number": "1b",
              "page": 1,
              "row_label": "Exclude information that does not appear in the body of the report"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Exclude information that does not appear in the body of the report",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-1b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r07"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r08"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r09"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r10"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r11"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r12"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r13"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r14"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-1b-r15"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-1b-completeness",
        "label": "Item 1b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-title-and-abstract",
    "source_references": [
      {
        "locator": {
          "item_number": "1b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "1b",
          "page": 1
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Structured summary of the trial design, methods, results, and conclusions",
    "status": "reviewed",
    "topic": "consort-2025-topic-title-and-structured-abstract",
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
