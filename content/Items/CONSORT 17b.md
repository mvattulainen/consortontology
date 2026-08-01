---
id: consort-2025-item-17b
type: ChecklistItem
item_number: 17b
label: "Type of randomisation and restrictions"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-randomisation-sequence-generation
status: reviewed
order: 22
requirement_count: 8
condition_count: 3
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 17b: Type of randomisation and restrictions

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand type of randomisation and restrictions. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Type of randomisation and details of any restriction (e.g., stratification, blocking and block size)" — CONSORT 2025 expanded checklist, item 17b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Randomisation - sequence generation|Randomisation: sequence generation]]
- **Domain classes:** [[RandomAllocationProcess]], [[TrialDesign]]

## Atomic requirements

1. **Type of randomisation and rationale where relevant.** Report type of randomisation and rationale where relevant. (`must`; expects `reason`)
2. **How randomisation blocks were generated.** Report how randomisation blocks were generated. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-blocked-randomisation`)
3. **Block sizes.** Report block sizes. (`conditional_must`; expects `number`; when `consort-2025-condition-blocked-randomisation`)
4. **Whether block sizes were fixed or randomly varied.** State whether block sizes were fixed or randomly varied. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-blocked-randomisation`)
5. **Whether trialists knew or became aware of block sizes.** State whether trialists knew or became aware of block sizes. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-blocked-randomisation`)
6. **Stratification factors.** Report stratification factors. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-stratified-randomisation`)
7. **Factors used in minimisation.** Report factors used in minimisation. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-minimisation-used`)
8. **Whether minimisation included a random element and its details.** State whether minimisation included a random element and its details. (`conditional_must`; expects `boolean_statement`; when `consort-2025-condition-minimisation-used`)

## Applicability

- **Blocked randomisation was used:** `{"equals":true,"fact":"design.randomisation.blocked"}`
- **Stratified randomisation was used:** `{"equals":true,"fact":"design.randomisation.stratified"}`
- **Minimisation was used:** `{"equals":true,"fact":"design.randomisation.minimisation"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 17a]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 17b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-17b-r01"}},{"require":{"ref":"consort-2025-item-17b-r02"}},{"require":{"ref":"consort-2025-item-17b-r03"}},{"require":{"ref":"consort-2025-item-17b-r04"}},{"require":{"ref":"consort-2025-item-17b-r05"}},{"require":{"ref":"consort-2025-item-17b-r06"}},{"require":{"ref":"consort-2025-item-17b-r07"}},{"require":{"ref":"consort-2025-item-17b-r08"}}]}`

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
          "fact": "design.randomisation.blocked"
        },
        "id": "consort-2025-condition-blocked-randomisation",
        "label": "Blocked randomisation was used",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "quoted_fragment": "Type of randomisation and details of any restriction (e.g., stratification, blocking and block size)"
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
          "equals": true,
          "fact": "design.randomisation.stratified"
        },
        "id": "consort-2025-condition-stratified-randomisation",
        "label": "Stratified randomisation was used",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "quoted_fragment": "Type of randomisation and details of any restriction (e.g., stratification, blocking and block size)"
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
          "equals": true,
          "fact": "design.randomisation.minimisation"
        },
        "id": "consort-2025-condition-minimisation-used",
        "label": "Minimisation was used",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "quoted_fragment": "Type of randomisation and details of any restriction (e.g., stratification, blocking and block size)"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Type of randomisation and details of any restriction (e.g., stratification, blocking and block size)",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-17b",
    "item_number": "17b",
    "label": "Type of randomisation and restrictions",
    "order": 22,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand type of randomisation and restrictions. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-17a"
      ],
      "governed_by": [
        "consort-2025-rule-item-17b-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-blocked-randomisation",
        "consort-2025-condition-stratified-randomisation",
        "consort-2025-condition-minimisation-used"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-17b-r01",
        "consort-2025-item-17b-r02",
        "consort-2025-item-17b-r03",
        "consort-2025-item-17b-r04",
        "consort-2025-item-17b-r05",
        "consort-2025-item-17b-r06",
        "consort-2025-item-17b-r07",
        "consort-2025-item-17b-r08"
      ],
      "targets_domain_class": [
        "consort-class-random-allocation-process",
        "consort-class-trial-design"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-17b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Type of randomisation and rationale where relevant",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "Report type of randomisation and rationale where relevant.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "Type of randomisation and rationale where relevant"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Type of randomisation and rationale where relevant",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "applicability_condition": "consort-2025-condition-blocked-randomisation",
        "id": "consort-2025-item-17b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How randomisation blocks were generated",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "Report how randomisation blocks were generated.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "How randomisation blocks were generated"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How randomisation blocks were generated",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-blocked-randomisation",
        "id": "consort-2025-item-17b-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Block sizes",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "Report block sizes.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "Block sizes"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Block sizes",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-blocked-randomisation",
        "id": "consort-2025-item-17b-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether block sizes were fixed or randomly varied",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "State whether block sizes were fixed or randomly varied.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "Whether block sizes were fixed or randomly varied"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether block sizes were fixed or randomly varied",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-blocked-randomisation",
        "id": "consort-2025-item-17b-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether trialists knew or became aware of block sizes",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "State whether trialists knew or became aware of block sizes.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "Whether trialists knew or became aware of block sizes"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether trialists knew or became aware of block sizes",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-stratified-randomisation",
        "id": "consort-2025-item-17b-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Stratification factors",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "Report stratification factors.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "Stratification factors"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Stratification factors",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-minimisation-used",
        "id": "consort-2025-item-17b-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Factors used in minimisation",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "Report factors used in minimisation.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "Factors used in minimisation"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Factors used in minimisation",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-minimisation-used",
        "id": "consort-2025-item-17b-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether minimisation included a random element and its details",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-17b",
        "requirement_text": "State whether minimisation included a random element and its details.",
        "source_references": [
          {
            "locator": {
              "item_number": "17b",
              "page": 6,
              "row_label": "Whether minimisation included a random element and its details"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether minimisation included a random element and its details",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-17b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17b-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17b-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17b-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17b-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17b-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17b-r07"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-17b-r08"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-17b-completeness",
        "label": "Item 17b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "17b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "17b",
          "page": 6
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Type of randomisation and details of any restriction (e.g., stratification, blocking and block size)",
    "status": "reviewed",
    "topic": "consort-2025-topic-randomisation-sequence-generation",
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
