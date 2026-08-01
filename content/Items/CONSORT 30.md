---
id: consort-2025-item-30
type: ChecklistItem
item_number: 30
label: "Trial limitations, bias, imprecision, generalisability, and multiplicity"
guideline_version: consort-2025
section: consort-2025-section-discussion
topic: consort-2025-topic-limitations
status: reviewed
order: 42
requirement_count: 4
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 30: Trial limitations, bias, imprecision, generalisability, and multiplicity

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand trial limitations, bias, imprecision, generalisability, and multiplicity. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Trial limitations, addressing sources of potential bias, imprecision, generalisability, and, if relevant, multiplicity of analyses" — CONSORT 2025 expanded checklist, item 30.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Discussion|Discussion]]
- **Topic:** [[Limitations|Limitations]]
- **Domain classes:** [[RandomisedTrial]], [[TrialDesign]], [[OutcomeResult]]

## Atomic requirements

1. **Methodological limitations and methods used to minimise or mitigate them.** Report methodological limitations and methods used to minimise or mitigate them. (`must`; expects `method_description`)
2. **Imprecision in the results.** Report imprecision in the results. (`must`; expects `free_text_description`)
3. **Generalisability of the results.** Report generalisability of the results. (`must`; expects `free_text_description`)
4. **Limitations related to multiplicity where relevant.** Report limitations related to multiplicity where relevant. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-multiplicity-relevant`)

## Applicability

- **Multiplicity is relevant to interpretation:** `{"equals":true,"fact":"analysis.multiplicity.applicable"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 30 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-30-r01"}},{"require":{"ref":"consort-2025-item-30-r02"}},{"require":{"ref":"consort-2025-item-30-r03"}},{"require":{"ref":"consort-2025-item-30-r04"}}]}`

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
          "fact": "analysis.multiplicity.applicable"
        },
        "id": "consort-2025-condition-multiplicity-relevant",
        "label": "Multiplicity is relevant to interpretation",
        "source_references": [
          {
            "locator": {
              "item_number": "30",
              "page": 12,
              "quoted_fragment": "Trial limitations, addressing sources of potential bias, imprecision, generalisability, and, if relevant, multiplicity of analyses"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Trial limitations, addressing sources of potential bias, imprecision, generalisability, and, if relevant, multiplicity of analyses",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-30",
    "item_number": "30",
    "label": "Trial limitations, bias, imprecision, generalisability, and multiplicity",
    "order": 42,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand trial limitations, bias, imprecision, generalisability, and multiplicity. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-30-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-multiplicity-relevant"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-30-r01",
        "consort-2025-item-30-r02",
        "consort-2025-item-30-r03",
        "consort-2025-item-30-r04"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-trial-design",
        "consort-class-outcome-result"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-30-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Methodological limitations and methods used to minimise or mitigate them",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-30",
        "requirement_text": "Report methodological limitations and methods used to minimise or mitigate them.",
        "source_references": [
          {
            "locator": {
              "item_number": "30",
              "page": 12,
              "row_label": "Methodological limitations and methods used to minimise or mitigate them"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Methodological limitations and methods used to minimise or mitigate them",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "id": "consort-2025-item-30-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Imprecision in the results",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-30",
        "requirement_text": "Report imprecision in the results.",
        "source_references": [
          {
            "locator": {
              "item_number": "30",
              "page": 12,
              "row_label": "Imprecision in the results"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Imprecision in the results",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-30-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Generalisability of the results",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-30",
        "requirement_text": "Report generalisability of the results.",
        "source_references": [
          {
            "locator": {
              "item_number": "30",
              "page": 12,
              "row_label": "Generalisability of the results"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Generalisability of the results",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-multiplicity-relevant",
        "id": "consort-2025-item-30-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Limitations related to multiplicity where relevant",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-30",
        "requirement_text": "Report limitations related to multiplicity where relevant.",
        "source_references": [
          {
            "locator": {
              "item_number": "30",
              "page": 12,
              "row_label": "Limitations related to multiplicity where relevant"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Limitations related to multiplicity where relevant",
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
                "ref": "consort-2025-item-30-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-30-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-30-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-30-r04"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-30-completeness",
        "label": "Item 30 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-discussion",
    "source_references": [
      {
        "locator": {
          "item_number": "30"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "30",
          "page": 12
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Trial limitations, addressing sources of potential bias, imprecision, generalisability, and, if relevant, multiplicity of analyses",
    "status": "reviewed",
    "topic": "consort-2025-topic-limitations",
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
