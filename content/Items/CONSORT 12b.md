---
id: consort-2025-item-12b
type: ChecklistItem
item_number: 12b
label: "Eligibility criteria for sites and intervention deliverers, if applicable"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-eligibility-criteria
status: reviewed
order: 15
requirement_count: 2
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 12b: Eligibility criteria for sites and intervention deliverers, if applicable

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand eligibility criteria for sites and intervention deliverers, if applicable. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "If applicable, eligibility criteria for sites and for individuals delivering the interventions" — CONSORT 2025 expanded checklist, item 12b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Eligibility criteria|Eligibility criteria]]
- **Domain classes:** [[TrialRole]]

## Atomic requirements

1. **Eligibility criteria for trial sites.** Report eligibility criteria for trial sites. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-item-12b-applicable`)
2. **Eligibility criteria for individuals delivering interventions.** Report eligibility criteria for individuals delivering interventions. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-item-12b-applicable`)

## Applicability

- **Site or intervention-deliverer criteria are applicable:** `{"any":[{"equals":true,"fact":"design.sites.have_eligibility_criteria"},{"equals":true,"fact":"intervention.deliverers.have_eligibility_criteria"}]}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 12a]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 12b applicability:** `{"implies":{"if":{"any":[{"equals":true,"fact":"design.sites.have_eligibility_criteria"},{"equals":true,"fact":"intervention.deliverers.have_eligibility_criteria"}]},"then":{"activate":{"ref":"consort-2025-item-12b"}}}}`
- **Item 12b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-12b-r01"}},{"require":{"ref":"consort-2025-item-12b-r02"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "contextual",
        "expression": {
          "any": [
            {
              "equals": true,
              "fact": "design.sites.have_eligibility_criteria"
            },
            {
              "equals": true,
              "fact": "intervention.deliverers.have_eligibility_criteria"
            }
          ]
        },
        "id": "consort-2025-condition-item-12b-applicable",
        "label": "Site or intervention-deliverer criteria are applicable",
        "source_references": [
          {
            "locator": {
              "item_number": "12b",
              "page": 4,
              "quoted_fragment": "If applicable, eligibility criteria for sites and for individuals delivering the interventions"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "If applicable, eligibility criteria for sites and for individuals delivering the interventions",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-12b",
    "item_number": "12b",
    "label": "Eligibility criteria for sites and intervention deliverers, if applicable",
    "order": 15,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand eligibility criteria for sites and intervention deliverers, if applicable. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-12a"
      ],
      "governed_by": [
        "consort-2025-rule-item-12b-applicability",
        "consort-2025-rule-item-12b-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-item-12b-applicable"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-12b-r01",
        "consort-2025-item-12b-r02"
      ],
      "targets_domain_class": [
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-item-12b-applicable",
        "id": "consort-2025-item-12b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Eligibility criteria for trial sites",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-12b",
        "requirement_text": "Report eligibility criteria for trial sites.",
        "source_references": [
          {
            "locator": {
              "item_number": "12b",
              "page": 4,
              "row_label": "Eligibility criteria for trial sites"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Eligibility criteria for trial sites",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-item-12b-applicable",
        "id": "consort-2025-item-12b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Eligibility criteria for individuals delivering interventions",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-12b",
        "requirement_text": "Report eligibility criteria for individuals delivering interventions.",
        "source_references": [
          {
            "locator": {
              "item_number": "12b",
              "page": 4,
              "row_label": "Eligibility criteria for individuals delivering interventions"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Eligibility criteria for individuals delivering interventions",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "implies": {
            "if": {
              "any": [
                {
                  "equals": true,
                  "fact": "design.sites.have_eligibility_criteria"
                },
                {
                  "equals": true,
                  "fact": "intervention.deliverers.have_eligibility_criteria"
                }
              ]
            },
            "then": {
              "activate": {
                "ref": "consort-2025-item-12b"
              }
            }
          }
        },
        "id": "consort-2025-rule-item-12b-applicability",
        "label": "Item 12b applicability",
        "rule_kind": "conditional_item",
        "status": "reviewed",
        "type": "NormativeRule"
      },
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-12b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-12b-r02"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-12b-completeness",
        "label": "Item 12b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "12b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "12b",
          "page": 4
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "If applicable, eligibility criteria for sites and for individuals delivering the interventions",
    "status": "reviewed",
    "topic": "consort-2025-topic-eligibility-criteria",
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
