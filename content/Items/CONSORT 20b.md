---
id: consort-2025-item-20b
type: ChecklistItem
item_number: 20b
label: "Blinding mechanism and intervention similarity, if blinded"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-blinding
status: reviewed
order: 26
requirement_count: 6
condition_count: 5
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 20b: Blinding mechanism and intervention similarity, if blinded

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand blinding mechanism and intervention similarity, if blinded. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "If blinded, how blinding was achieved and description of the similarity of interventions" — CONSORT 2025 expanded checklist, item 20b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Blinding|Blinding]]
- **Domain classes:** [[BlindingProcess]], [[Intervention]], [[Comparator]]

## Atomic requirements

1. **Mechanism used to establish blinding.** Report mechanism used to establish blinding. (`conditional_must`; expects `method_description`; when `consort-2025-condition-if-blinded`)
2. **Similarities or differences between compared interventions.** Report similarities or differences between compared interventions. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-if-blinded`)
3. **Procedures intended to maintain blinding and reduce unblinding risk, where appropriate.** Report procedures intended to maintain blinding and reduce unblinding risk, where appropriate. (`conditional_must`; expects `method_description`; when `consort-2025-condition-blinding-maintenance-applicable`)
4. **Procedures used to evaluate blinding procedures.** Report procedures used to evaluate blinding procedures. (`conditional_must`; expects `method_description`; when `consort-2025-condition-blinding-evaluation-done`)
5. **Known compromises in blinding.** Report known compromises in blinding. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-blinding-compromised`)
6. **Emergency unblinding, with reasons and procedure, if done.** Report emergency unblinding, with reasons and procedure, if done. (`conditional_must`; expects `method_description`; when `consort-2025-condition-emergency-unblinding-done`)

## Applicability

- **Blinding occurred:** `{"equals":true,"fact":"trial.blinding.any_role_blinded"}`
- **Blinding maintenance procedures are appropriate:** `{"all":[{"equals":true,"fact":"trial.blinding.any_role_blinded"},{"equals":true,"fact":"trial.blinding.maintenance_procedures.applicable"}]}`
- **Blinding procedures were evaluated:** `{"equals":true,"fact":"trial.blinding.evaluation_performed"}`
- **A known compromise in blinding occurred:** `{"equals":true,"fact":"trial.blinding.compromised"}`
- **Emergency unblinding was performed:** `{"equals":true,"fact":"trial.blinding.emergency_unblinding_performed"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 20a]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 20b applicability:** `{"implies":{"if":{"equals":true,"fact":"trial.blinding.any_role_blinded"},"then":{"activate":{"ref":"consort-2025-item-20b"}}}}`
- **Item 20b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-20b-r01"}},{"require":{"ref":"consort-2025-item-20b-r02"}},{"require":{"ref":"consort-2025-item-20b-r03"}},{"require":{"ref":"consort-2025-item-20b-r04"}},{"require":{"ref":"consort-2025-item-20b-r05"}},{"require":{"ref":"consort-2025-item-20b-r06"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "objective",
        "expression": {
          "equals": true,
          "fact": "trial.blinding.any_role_blinded"
        },
        "id": "consort-2025-condition-if-blinded",
        "label": "Blinding occurred",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "quoted_fragment": "If blinded, how blinding was achieved and description of the similarity of interventions"
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
              "fact": "trial.blinding.any_role_blinded"
            },
            {
              "equals": true,
              "fact": "trial.blinding.maintenance_procedures.applicable"
            }
          ]
        },
        "id": "consort-2025-condition-blinding-maintenance-applicable",
        "label": "Blinding maintenance procedures are appropriate",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "quoted_fragment": "If blinded, how blinding was achieved and description of the similarity of interventions"
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
          "fact": "trial.blinding.evaluation_performed"
        },
        "id": "consort-2025-condition-blinding-evaluation-done",
        "label": "Blinding procedures were evaluated",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "quoted_fragment": "If blinded, how blinding was achieved and description of the similarity of interventions"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      },
      {
        "condition_kind": "objective",
        "expression": {
          "equals": true,
          "fact": "trial.blinding.compromised"
        },
        "id": "consort-2025-condition-blinding-compromised",
        "label": "A known compromise in blinding occurred",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "quoted_fragment": "If blinded, how blinding was achieved and description of the similarity of interventions"
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
          "fact": "trial.blinding.emergency_unblinding_performed"
        },
        "id": "consort-2025-condition-emergency-unblinding-done",
        "label": "Emergency unblinding was performed",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "quoted_fragment": "If blinded, how blinding was achieved and description of the similarity of interventions"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "If blinded, how blinding was achieved and description of the similarity of interventions",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-20b",
    "item_number": "20b",
    "label": "Blinding mechanism and intervention similarity, if blinded",
    "order": 26,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand blinding mechanism and intervention similarity, if blinded. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-20a"
      ],
      "governed_by": [
        "consort-2025-rule-item-20b-applicability",
        "consort-2025-rule-item-20b-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-if-blinded",
        "consort-2025-condition-blinding-maintenance-applicable",
        "consort-2025-condition-blinding-evaluation-done",
        "consort-2025-condition-blinding-compromised",
        "consort-2025-condition-emergency-unblinding-done"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-20b-r01",
        "consort-2025-item-20b-r02",
        "consort-2025-item-20b-r03",
        "consort-2025-item-20b-r04",
        "consort-2025-item-20b-r05",
        "consort-2025-item-20b-r06"
      ],
      "targets_domain_class": [
        "consort-class-blinding-process",
        "consort-class-intervention",
        "consort-class-comparator"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-if-blinded",
        "id": "consort-2025-item-20b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Mechanism used to establish blinding",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-20b",
        "requirement_text": "Report mechanism used to establish blinding.",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "row_label": "Mechanism used to establish blinding"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Mechanism used to establish blinding",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-if-blinded",
        "id": "consort-2025-item-20b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Similarities or differences between compared interventions",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-20b",
        "requirement_text": "Report similarities or differences between compared interventions.",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "row_label": "Similarities or differences between compared interventions"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Similarities or differences between compared interventions",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-blinding-maintenance-applicable",
        "id": "consort-2025-item-20b-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Procedures intended to maintain blinding and reduce unblinding risk, where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-20b",
        "requirement_text": "Report procedures intended to maintain blinding and reduce unblinding risk, where appropriate.",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "row_label": "Procedures intended to maintain blinding and reduce unblinding risk, where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Procedures intended to maintain blinding and reduce unblinding risk, where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-blinding-evaluation-done",
        "id": "consort-2025-item-20b-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Procedures used to evaluate blinding procedures",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-20b",
        "requirement_text": "Report procedures used to evaluate blinding procedures.",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "row_label": "Procedures used to evaluate blinding procedures"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Procedures used to evaluate blinding procedures",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "applicability_condition": "consort-2025-condition-blinding-compromised",
        "id": "consort-2025-item-20b-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Known compromises in blinding",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-20b",
        "requirement_text": "Report known compromises in blinding.",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "row_label": "Known compromises in blinding"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Known compromises in blinding",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-emergency-unblinding-done",
        "id": "consort-2025-item-20b-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Emergency unblinding, with reasons and procedure, if done",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-20b",
        "requirement_text": "Report emergency unblinding, with reasons and procedure, if done.",
        "source_references": [
          {
            "locator": {
              "item_number": "20b",
              "page": 8,
              "row_label": "Emergency unblinding, with reasons and procedure, if done"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Emergency unblinding, with reasons and procedure, if done",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "implies": {
            "if": {
              "equals": true,
              "fact": "trial.blinding.any_role_blinded"
            },
            "then": {
              "activate": {
                "ref": "consort-2025-item-20b"
              }
            }
          }
        },
        "id": "consort-2025-rule-item-20b-applicability",
        "label": "Item 20b applicability",
        "rule_kind": "conditional_item",
        "status": "reviewed",
        "type": "NormativeRule"
      },
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-20b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20b-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20b-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20b-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20b-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-20b-r06"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-20b-completeness",
        "label": "Item 20b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "20b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "20b",
          "page": 8
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "If blinded, how blinding was achieved and description of the similarity of interventions",
    "status": "reviewed",
    "topic": "consort-2025-topic-blinding",
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
