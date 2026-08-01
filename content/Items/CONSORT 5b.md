---
id: consort-2025-item-5b
type: ChecklistItem
item_number: 5b
label: "Financial and other conflicts of interest"
guideline_version: consort-2025
section: consort-2025-section-open-science
topic: consort-2025-topic-funding-and-conflicts-of-interest
status: reviewed
order: 7
requirement_count: 4
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 5b: Financial and other conflicts of interest

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand financial and other conflicts of interest. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Financial and other conflicts of interest of the manuscript authors" — CONSORT 2025 expanded checklist, item 5b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Open Science|Open science]]
- **Topic:** [[Funding and conflicts of interest|Funding and conflicts of interest]]
- **Domain classes:** [[TrialRole]]

## Atomic requirements

1. **Financial conflicts of interest of manuscript authors.** Report financial conflicts of interest of manuscript authors. (`must`; expects `free_text_description`)
2. **Non-financial conflicts of interest of manuscript authors.** Report non-financial conflicts of interest of manuscript authors. (`must`; expects `free_text_description`)
3. **Procedures used to reduce the influence of conflicts on design, conduct, analysis, or reporting.** Report procedures used to reduce the influence of conflicts on design, conduct, analysis, or reporting. (`must`; expects `method_description`)
4. **Explicit statement that there are no conflicts of interest.** Provide an explicit statement that there are no conflicts of interest. (`must`; expects `boolean_statement`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[CONSORT 5a]]

## Formal rules

> [!rule] Logical composition
> - **Conflict disclosure or explicit none:** `any_of` over `consort-2025-item-5b-g02`, `consort-2025-item-5b-r04`.
- **Conflict disclosure branch:** `all_of` over `consort-2025-item-5b-r01`, `consort-2025-item-5b-r02`, `consort-2025-item-5b-r03`.

- **Item 5b completeness:** `{"satisfy_with":{"ref":"consort-2025-item-5b-g01"}}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Financial and other conflicts of interest of the manuscript authors",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-5b",
    "item_number": "5b",
    "label": "Financial and other conflicts of interest",
    "order": 7,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand financial and other conflicts of interest. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [
        "consort-2025-item-5a"
      ],
      "governed_by": [
        "consort-2025-rule-item-5b-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-5b-r01",
        "consort-2025-item-5b-r02",
        "consort-2025-item-5b-r03",
        "consort-2025-item-5b-r04"
      ],
      "has_requirement_group": [
        "consort-2025-item-5b-g01",
        "consort-2025-item-5b-g02"
      ],
      "targets_domain_class": [
        "consort-class-trial-role"
      ]
    },
    "requirement_groups": [
      {
        "id": "consort-2025-item-5b-g01",
        "label": "Conflict disclosure or explicit none",
        "members": [
          "consort-2025-item-5b-g02",
          "consort-2025-item-5b-r04"
        ],
        "operator": "any_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      },
      {
        "id": "consort-2025-item-5b-g02",
        "label": "Conflict disclosure branch",
        "members": [
          "consort-2025-item-5b-r01",
          "consort-2025-item-5b-r02",
          "consort-2025-item-5b-r03"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      }
    ],
    "requirements": [
      {
        "id": "consort-2025-item-5b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Financial conflicts of interest of manuscript authors",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5b",
        "requirement_text": "Report financial conflicts of interest of manuscript authors.",
        "source_references": [
          {
            "locator": {
              "item_number": "5b",
              "page": 2,
              "row_label": "Financial conflicts of interest of manuscript authors"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Financial conflicts of interest of manuscript authors",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-5b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Non-financial conflicts of interest of manuscript authors",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5b",
        "requirement_text": "Report non-financial conflicts of interest of manuscript authors.",
        "source_references": [
          {
            "locator": {
              "item_number": "5b",
              "page": 2,
              "row_label": "Non-financial conflicts of interest of manuscript authors"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Non-financial conflicts of interest of manuscript authors",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-5b-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Procedures used to reduce the influence of conflicts on design, conduct, analysis, or reporting",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5b",
        "requirement_text": "Report procedures used to reduce the influence of conflicts on design, conduct, analysis, or reporting.",
        "source_references": [
          {
            "locator": {
              "item_number": "5b",
              "page": 2,
              "row_label": "Procedures used to reduce the influence of conflicts on design, conduct, analysis, or reporting"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Procedures used to reduce the influence of conflicts on design, conduct, analysis, or reporting",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      },
      {
        "id": "consort-2025-item-5b-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Explicit statement that there are no conflicts of interest",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5b",
        "requirement_text": "Provide an explicit statement that there are no conflicts of interest.",
        "source_references": [
          {
            "locator": {
              "item_number": "5b",
              "page": 2,
              "row_label": "Explicit statement that there are no conflicts of interest"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Explicit statement that there are no conflicts of interest",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      }
    ],
    "rules": [
      {
        "expression": {
          "satisfy_with": {
            "ref": "consort-2025-item-5b-g01"
          }
        },
        "id": "consort-2025-rule-item-5b-completeness",
        "label": "Item 5b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-open-science",
    "source_references": [
      {
        "locator": {
          "item_number": "5b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "5b",
          "page": 2
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Financial and other conflicts of interest of the manuscript authors",
    "status": "reviewed",
    "topic": "consort-2025-topic-funding-and-conflicts-of-interest",
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
