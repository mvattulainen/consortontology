---
id: consort-2025-item-5a
type: ChecklistItem
item_number: 5a
label: "Funding and support, including funder roles"
guideline_version: consort-2025
section: consort-2025-section-open-science
topic: consort-2025-topic-funding-and-conflicts-of-interest
status: reviewed
order: 6
requirement_count: 4
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 5a: Funding and support, including funder roles

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand funding and support, including funder roles. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Sources of funding and other support (e.g., supply of drugs), and role of funders in the design, conduct, analysis and reporting of the trial" — CONSORT 2025 expanded checklist, item 5a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Open Science|Open science]]
- **Topic:** [[Funding and conflicts of interest|Funding and conflicts of interest]]
- **Domain classes:** [[RandomisedTrial]], [[TrialRole]]

## Atomic requirements

1. **Name of each funder.** Report name of each funder. (`must`; expects `free_text_description`)
2. **Direct monetary support.** Report direct monetary support. (`must`; expects `free_text_description`)
3. **Indirect support such as free drugs, equipment, services, statistical analysis, or medical writing.** Report indirect support such as free drugs, equipment, services, statistical analysis, or medical writing. (`must`; expects `free_text_description`)
4. **Role of funders in trial design, conduct, data analysis, and reporting.** Report role of funders in trial design, conduct, data analysis, and reporting. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 5a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-5a-r01"}},{"require":{"ref":"consort-2025-item-5a-r02"}},{"require":{"ref":"consort-2025-item-5a-r03"}},{"require":{"ref":"consort-2025-item-5a-r04"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Sources of funding and other support (e.g., supply of drugs), and role of funders in the design, conduct, analysis and reporting of the trial",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-5a",
    "item_number": "5a",
    "label": "Funding and support, including funder roles",
    "order": 6,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand funding and support, including funder roles. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-5a-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-5a-r01",
        "consort-2025-item-5a-r02",
        "consort-2025-item-5a-r03",
        "consort-2025-item-5a-r04"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-5a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Name of each funder",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5a",
        "requirement_text": "Report name of each funder.",
        "source_references": [
          {
            "locator": {
              "item_number": "5a",
              "page": 2,
              "row_label": "Name of each funder"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Name of each funder",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-5a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Direct monetary support",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5a",
        "requirement_text": "Report direct monetary support.",
        "source_references": [
          {
            "locator": {
              "item_number": "5a",
              "page": 2,
              "row_label": "Direct monetary support"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Direct monetary support",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-5a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Indirect support such as free drugs, equipment, services, statistical analysis, or medical writing",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5a",
        "requirement_text": "Report indirect support such as free drugs, equipment, services, statistical analysis, or medical writing.",
        "source_references": [
          {
            "locator": {
              "item_number": "5a",
              "page": 2,
              "row_label": "Indirect support such as free drugs, equipment, services, statistical analysis, or medical writing"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Indirect support such as free drugs, equipment, services, statistical analysis, or medical writing",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-5a-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Role of funders in trial design, conduct, data analysis, and reporting",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-5a",
        "requirement_text": "Report role of funders in trial design, conduct, data analysis, and reporting.",
        "source_references": [
          {
            "locator": {
              "item_number": "5a",
              "page": 2,
              "row_label": "Role of funders in trial design, conduct, data analysis, and reporting"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Role of funders in trial design, conduct, data analysis, and reporting",
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
                "ref": "consort-2025-item-5a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-5a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-5a-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-5a-r04"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-5a-completeness",
        "label": "Item 5a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-open-science",
    "source_references": [
      {
        "locator": {
          "item_number": "5a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "5a",
          "page": 2
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Sources of funding and other support (e.g., supply of drugs), and role of funders in the design, conduct, analysis and reporting of the trial",
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
