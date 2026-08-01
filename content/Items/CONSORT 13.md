---
id: consort-2025-item-13
type: ChecklistItem
item_number: 13
label: "Replicable intervention and comparator details"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-intervention-and-comparator
status: reviewed
order: 16
requirement_count: 12
condition_count: 7
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 13: Replicable intervention and comparator details

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand replicable intervention and comparator details. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed" — CONSORT 2025 expanded checklist, item 13.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Intervention and comparator|Intervention and comparator]]
- **Domain classes:** [[TrialArm]], [[Intervention]], [[Comparator]]

## Atomic requirements

1. **Components of each intervention and comparator.** Report components of each intervention and comparator. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-13-each-intervention-comparator`)
2. **How each intervention and comparator was administered.** Report how each intervention and comparator was administered. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-13-each-intervention-comparator`)
3. **When and for how long each intervention and comparator was administered.** Report when and for how long each intervention and comparator was administered. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-13-each-intervention-comparator`)
4. **Procedures for tailoring to individual participants.** Report procedures for tailoring to individual participants. (`must`; expects `method_description`; scoped by `consort-2025-scope-item-13-each-intervention-comparator`)
5. **Physical or informational materials used and where they can be accessed.** Report physical or informational materials used and where they can be accessed. (`conditional_must`; expects `url`; when `consort-2025-condition-additional-materials-relevant`; scoped by `consort-2025-scope-item-13-each-intervention-comparator`)
6. **Allowed or prohibited concomitant care where appropriate.** Report allowed or prohibited concomitant care where appropriate. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-concomitant-care-applicable`; scoped by `consort-2025-scope-item-13-each-intervention-comparator`)
7. **Criteria for intervention or comparator modifications and discontinuations where appropriate.** Report criteria for intervention or comparator modifications and discontinuations where appropriate. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-modification-criteria-applicable`; scoped by `consort-2025-scope-item-13-each-intervention-comparator`)
8. **Description of usual care when it is the comparator.** Report description of usual care when it is the comparator. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-usual-care-comparator`)
9. **Whether intervention groups also received usual care.** State whether intervention groups also received usual care. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-usual-care-comparator`)
10. **When and how care-provider fidelity and participant adherence were assessed, if applicable.** Report when and how care-provider fidelity and participant adherence were assessed, if applicable. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-fidelity-assessment-applicable`)
11. **Strategies for improving fidelity and adherence.** Report strategies for improving fidelity and adherence. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-fidelity-improvement-used`)
12. **Prespecified classification of treatment as planned, where appropriate.** Report prespecified classification of treatment as planned, where appropriate. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-treated-as-planned-classification-applicable`)

## Applicability

- **Additional intervention materials are relevant:** `{"equals":true,"fact":"intervention.additional_materials.relevant"}`
- **Concomitant-care guidance is applicable:** `{"equals":true,"fact":"intervention.concomitant_care.applicable"}`
- **Modification criteria are applicable:** `{"equals":true,"fact":"intervention.modification_criteria.applicable"}`
- **Comparator is usual care:** `{"equals":"usual_care","fact":"intervention.comparator.type"}`
- **Fidelity or adherence assessment is applicable:** `{"equals":true,"fact":"intervention.fidelity_assessment.applicable"}`
- **A fidelity or adherence improvement strategy was used:** `{"equals":true,"fact":"intervention.fidelity_improvement_strategy.used"}`
- **Treated-as-planned classification is applicable:** `{"equals":true,"fact":"intervention.treated_as_planned_classification.applicable"}`

## Scope and repetition

- **Each intervention and comparator:** repeat over `intervention.trial_group_intervention`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 13 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-13-r01"}},{"require":{"ref":"consort-2025-item-13-r02"}},{"require":{"ref":"consort-2025-item-13-r03"}},{"require":{"ref":"consort-2025-item-13-r04"}},{"require":{"ref":"consort-2025-item-13-r05"}},{"require":{"ref":"consort-2025-item-13-r06"}},{"require":{"ref":"consort-2025-item-13-r07"}},{"require":{"ref":"consort-2025-item-13-r08"}},{"require":{"ref":"consort-2025-item-13-r09"}},{"require":{"ref":"consort-2025-item-13-r10"}},{"require":{"ref":"consort-2025-item-13-r11"}},{"require":{"ref":"consort-2025-item-13-r12"}}]}`

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
          "fact": "intervention.additional_materials.relevant"
        },
        "id": "consort-2025-condition-additional-materials-relevant",
        "label": "Additional intervention materials are relevant",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "quoted_fragment": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed"
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
          "fact": "intervention.concomitant_care.applicable"
        },
        "id": "consort-2025-condition-concomitant-care-applicable",
        "label": "Concomitant-care guidance is applicable",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "quoted_fragment": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed"
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
          "fact": "intervention.modification_criteria.applicable"
        },
        "id": "consort-2025-condition-modification-criteria-applicable",
        "label": "Modification criteria are applicable",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "quoted_fragment": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed"
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
          "equals": "usual_care",
          "fact": "intervention.comparator.type"
        },
        "id": "consort-2025-condition-usual-care-comparator",
        "label": "Comparator is usual care",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "quoted_fragment": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed"
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
          "fact": "intervention.fidelity_assessment.applicable"
        },
        "id": "consort-2025-condition-fidelity-assessment-applicable",
        "label": "Fidelity or adherence assessment is applicable",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "quoted_fragment": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed"
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
          "fact": "intervention.fidelity_improvement_strategy.used"
        },
        "id": "consort-2025-condition-fidelity-improvement-used",
        "label": "A fidelity or adherence improvement strategy was used",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "quoted_fragment": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed"
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
          "fact": "intervention.treated_as_planned_classification.applicable"
        },
        "id": "consort-2025-condition-treated-as-planned-classification-applicable",
        "label": "Treated-as-planned classification is applicable",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "quoted_fragment": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-13",
    "item_number": "13",
    "label": "Replicable intervention and comparator details",
    "order": 16,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand replicable intervention and comparator details. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-13-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-additional-materials-relevant",
        "consort-2025-condition-concomitant-care-applicable",
        "consort-2025-condition-modification-criteria-applicable",
        "consort-2025-condition-usual-care-comparator",
        "consort-2025-condition-fidelity-assessment-applicable",
        "consort-2025-condition-fidelity-improvement-used",
        "consort-2025-condition-treated-as-planned-classification-applicable"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-13-r01",
        "consort-2025-item-13-r02",
        "consort-2025-item-13-r03",
        "consort-2025-item-13-r04",
        "consort-2025-item-13-r05",
        "consort-2025-item-13-r06",
        "consort-2025-item-13-r07",
        "consort-2025-item-13-r08",
        "consort-2025-item-13-r09",
        "consort-2025-item-13-r10",
        "consort-2025-item-13-r11",
        "consort-2025-item-13-r12"
      ],
      "targets_domain_class": [
        "consort-class-trial-arm",
        "consort-class-intervention",
        "consort-class-comparator"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-13-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Components of each intervention and comparator",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report components of each intervention and comparator.",
        "scope": "consort-2025-scope-item-13-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Components of each intervention and comparator"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Components of each intervention and comparator",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-13-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How each intervention and comparator was administered",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report how each intervention and comparator was administered.",
        "scope": "consort-2025-scope-item-13-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "How each intervention and comparator was administered"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How each intervention and comparator was administered",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-13-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "When and for how long each intervention and comparator was administered",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report when and for how long each intervention and comparator was administered.",
        "scope": "consort-2025-scope-item-13-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "When and for how long each intervention and comparator was administered"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "When and for how long each intervention and comparator was administered",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-13-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Procedures for tailoring to individual participants",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report procedures for tailoring to individual participants.",
        "scope": "consort-2025-scope-item-13-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Procedures for tailoring to individual participants"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Procedures for tailoring to individual participants",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-additional-materials-relevant",
        "id": "consort-2025-item-13-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Physical or informational materials used and where they can be accessed",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report physical or informational materials used and where they can be accessed.",
        "scope": "consort-2025-scope-item-13-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Physical or informational materials used and where they can be accessed"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Physical or informational materials used and where they can be accessed",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "url"
      },
      {
        "applicability_condition": "consort-2025-condition-concomitant-care-applicable",
        "id": "consort-2025-item-13-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Allowed or prohibited concomitant care where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report allowed or prohibited concomitant care where appropriate.",
        "scope": "consort-2025-scope-item-13-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Allowed or prohibited concomitant care where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Allowed or prohibited concomitant care where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-modification-criteria-applicable",
        "id": "consort-2025-item-13-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Criteria for intervention or comparator modifications and discontinuations where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report criteria for intervention or comparator modifications and discontinuations where appropriate.",
        "scope": "consort-2025-scope-item-13-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Criteria for intervention or comparator modifications and discontinuations where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Criteria for intervention or comparator modifications and discontinuations where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-usual-care-comparator",
        "id": "consort-2025-item-13-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Description of usual care when it is the comparator",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report description of usual care when it is the comparator.",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Description of usual care when it is the comparator"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Description of usual care when it is the comparator",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-usual-care-comparator",
        "id": "consort-2025-item-13-r09",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether intervention groups also received usual care",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "State whether intervention groups also received usual care.",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Whether intervention groups also received usual care"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether intervention groups also received usual care",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-fidelity-assessment-applicable",
        "id": "consort-2025-item-13-r10",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "When and how care-provider fidelity and participant adherence were assessed, if applicable",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report when and how care-provider fidelity and participant adherence were assessed, if applicable.",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "When and how care-provider fidelity and participant adherence were assessed, if applicable"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "When and how care-provider fidelity and participant adherence were assessed, if applicable",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-fidelity-improvement-used",
        "id": "consort-2025-item-13-r11",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Strategies for improving fidelity and adherence",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report strategies for improving fidelity and adherence.",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Strategies for improving fidelity and adherence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Strategies for improving fidelity and adherence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-treated-as-planned-classification-applicable",
        "id": "consort-2025-item-13-r12",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Prespecified classification of treatment as planned, where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-13",
        "requirement_text": "Report prespecified classification of treatment as planned, where appropriate.",
        "source_references": [
          {
            "locator": {
              "item_number": "13",
              "page": 4,
              "row_label": "Prespecified classification of treatment as planned, where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Prespecified classification of treatment as planned, where appropriate",
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
                "ref": "consort-2025-item-13-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r07"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r08"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r09"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r10"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r11"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-13-r12"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-13-completeness",
        "label": "Item 13 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "intervention.trial_group_intervention",
        "id": "consort-2025-scope-item-13-each-intervention-comparator",
        "label": "Each intervention and comparator",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "13"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "13",
          "page": 4
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Intervention and comparator with sufficient details to allow replication; if relevant, where additional materials can be accessed",
    "status": "reviewed",
    "topic": "consort-2025-topic-intervention-and-comparator",
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
