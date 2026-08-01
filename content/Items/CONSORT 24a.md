---
id: consort-2025-item-24a
type: ChecklistItem
item_number: 24a
label: "Intervention and comparator as actually administered"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-intervention-and-comparator-delivery
status: reviewed
order: 35
requirement_count: 5
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 24a: Intervention and comparator as actually administered

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand intervention and comparator as actually administered. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Intervention and comparator as they were actually administered" — CONSORT 2025 expanded checklist, item 24a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Intervention and comparator delivery|Intervention and comparator delivery]]
- **Domain classes:** [[TrialArm]], [[Intervention]], [[Comparator]], [[Participant]]

## Atomic requirements

1. **Who actually delivered each intervention or comparator, including number and expertise.** Report who actually delivered each intervention or comparator, including number and expertise. (`must`; expects `number`; scoped by `consort-2025-scope-item-24a-each-intervention-comparator`)
2. **How each intervention or comparator was actually administered.** Report how each intervention or comparator was actually administered. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-24a-each-intervention-comparator`)
3. **What intervention or comparator was actually administered.** Report what intervention or comparator was actually administered. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-24a-each-intervention-comparator`)
4. **Participant adherence.** Report participant adherence. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-24a-each-intervention-comparator`)
5. **Care-provider fidelity where appropriate.** Report care-provider fidelity where appropriate. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-delivery-fidelity-applicable`; scoped by `consort-2025-scope-item-24a-each-intervention-comparator`)

## Applicability

- **Care-provider fidelity is appropriate to assess:** `{"equals":true,"fact":"intervention.delivery_fidelity.applicable"}`

## Scope and repetition

- **Each intervention and comparator:** repeat over `intervention.trial_group_intervention`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 24a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-24a-r01"}},{"require":{"ref":"consort-2025-item-24a-r02"}},{"require":{"ref":"consort-2025-item-24a-r03"}},{"require":{"ref":"consort-2025-item-24a-r04"}},{"require":{"ref":"consort-2025-item-24a-r05"}}]}`

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
          "fact": "intervention.delivery_fidelity.applicable"
        },
        "id": "consort-2025-condition-delivery-fidelity-applicable",
        "label": "Care-provider fidelity is appropriate to assess",
        "source_references": [
          {
            "locator": {
              "item_number": "24a",
              "page": 10,
              "quoted_fragment": "Intervention and comparator as they were actually administered"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Intervention and comparator as they were actually administered",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-24a",
    "item_number": "24a",
    "label": "Intervention and comparator as actually administered",
    "order": 35,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand intervention and comparator as actually administered. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-24a-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-delivery-fidelity-applicable"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-24a-r01",
        "consort-2025-item-24a-r02",
        "consort-2025-item-24a-r03",
        "consort-2025-item-24a-r04",
        "consort-2025-item-24a-r05"
      ],
      "targets_domain_class": [
        "consort-class-trial-arm",
        "consort-class-intervention",
        "consort-class-comparator",
        "consort-class-participant"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-24a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who actually delivered each intervention or comparator, including number and expertise",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-24a",
        "requirement_text": "Report who actually delivered each intervention or comparator, including number and expertise.",
        "scope": "consort-2025-scope-item-24a-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "24a",
              "page": 10,
              "row_label": "Who actually delivered each intervention or comparator, including number and expertise"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who actually delivered each intervention or comparator, including number and expertise",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "id": "consort-2025-item-24a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How each intervention or comparator was actually administered",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-24a",
        "requirement_text": "Report how each intervention or comparator was actually administered.",
        "scope": "consort-2025-scope-item-24a-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "24a",
              "page": 10,
              "row_label": "How each intervention or comparator was actually administered"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How each intervention or comparator was actually administered",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-24a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "What intervention or comparator was actually administered",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-24a",
        "requirement_text": "Report what intervention or comparator was actually administered.",
        "scope": "consort-2025-scope-item-24a-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "24a",
              "page": 10,
              "row_label": "What intervention or comparator was actually administered"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "What intervention or comparator was actually administered",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-24a-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Participant adherence",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-24a",
        "requirement_text": "Report participant adherence.",
        "scope": "consort-2025-scope-item-24a-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "24a",
              "page": 10,
              "row_label": "Participant adherence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Participant adherence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-delivery-fidelity-applicable",
        "id": "consort-2025-item-24a-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Care-provider fidelity where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-24a",
        "requirement_text": "Report care-provider fidelity where appropriate.",
        "scope": "consort-2025-scope-item-24a-each-intervention-comparator",
        "source_references": [
          {
            "locator": {
              "item_number": "24a",
              "page": 10,
              "row_label": "Care-provider fidelity where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Care-provider fidelity where appropriate",
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
                "ref": "consort-2025-item-24a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-24a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-24a-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-24a-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-24a-r05"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-24a-completeness",
        "label": "Item 24a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "intervention.trial_group_intervention",
        "id": "consort-2025-scope-item-24a-each-intervention-comparator",
        "label": "Each intervention and comparator",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-results",
    "source_references": [
      {
        "locator": {
          "item_number": "24a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "24a",
          "page": 10
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Intervention and comparator as they were actually administered",
    "status": "reviewed",
    "topic": "consort-2025-topic-intervention-and-comparator-delivery",
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
