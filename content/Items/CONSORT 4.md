---
id: consort-2025-item-4
type: ChecklistItem
item_number: 4
label: "Access to participant data, data dictionary, statistical code, and other materials"
guideline_version: consort-2025
section: consort-2025-section-open-science
topic: consort-2025-topic-data-sharing
status: reviewed
order: 5
requirement_count: 5
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 4: Access to participant data, data dictionary, statistical code, and other materials

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand access to participant data, data dictionary, statistical code, and other materials. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Where and how the individual de-identified participant data (including data dictionary), statistical code and any other materials can be accessed" — CONSORT 2025 expanded checklist, item 4.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Open Science|Open science]]
- **Topic:** [[Data sharing|Data sharing]]
- **Domain classes:** [[RandomisedTrial]], [[Participant]]

## Atomic requirements

1. **What de-identified participant data and data dictionary are shared.** Report what de-identified participant data and data dictionary are shared. (`must`; expects `free_text_description`)
2. **Where the shared data, code, and materials are accessible.** Report where the shared data, code, and materials are accessible. (`must`; expects `url`)
3. **How access to the shared data, code, and materials is obtained.** Report how access to the shared data, code, and materials is obtained. (`must`; expects `free_text_description`)
4. **Explicit statement that no sharing is planned.** Provide an explicit statement that no sharing is planned. (`must`; expects `boolean_statement`)
5. **Explanation of why no sharing is planned.** Report explanation of why no sharing is planned. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> - **Sharing or explicit no-sharing alternative:** `any_of` over `consort-2025-item-4-g02`, `consort-2025-item-4-g03`.
- **Sharing information branch:** `all_of` over `consort-2025-item-4-r01`, `consort-2025-item-4-r02`, `consort-2025-item-4-r03`.
- **No sharing planned branch:** `all_of` over `consort-2025-item-4-r04`, `consort-2025-item-4-r05`.

- **Item 4 completeness:** `{"satisfy_with":{"ref":"consort-2025-item-4-g01"}}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Where and how the individual de-identified participant data (including data dictionary), statistical code and any other materials can be accessed",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-4",
    "item_number": "4",
    "label": "Access to participant data, data dictionary, statistical code, and other materials",
    "order": 5,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand access to participant data, data dictionary, statistical code, and other materials. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-4-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-4-r01",
        "consort-2025-item-4-r02",
        "consort-2025-item-4-r03",
        "consort-2025-item-4-r04",
        "consort-2025-item-4-r05"
      ],
      "has_requirement_group": [
        "consort-2025-item-4-g01",
        "consort-2025-item-4-g02",
        "consort-2025-item-4-g03"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-participant"
      ]
    },
    "requirement_groups": [
      {
        "id": "consort-2025-item-4-g01",
        "label": "Sharing or explicit no-sharing alternative",
        "members": [
          "consort-2025-item-4-g02",
          "consort-2025-item-4-g03"
        ],
        "operator": "any_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      },
      {
        "id": "consort-2025-item-4-g02",
        "label": "Sharing information branch",
        "members": [
          "consort-2025-item-4-r01",
          "consort-2025-item-4-r02",
          "consort-2025-item-4-r03"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      },
      {
        "id": "consort-2025-item-4-g03",
        "label": "No sharing planned branch",
        "members": [
          "consort-2025-item-4-r04",
          "consort-2025-item-4-r05"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      }
    ],
    "requirements": [
      {
        "id": "consort-2025-item-4-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "What de-identified participant data and data dictionary are shared",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-4",
        "requirement_text": "Report what de-identified participant data and data dictionary are shared.",
        "source_references": [
          {
            "locator": {
              "item_number": "4",
              "page": 2,
              "row_label": "What de-identified participant data and data dictionary are shared"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "What de-identified participant data and data dictionary are shared",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-4-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Where the shared data, code, and materials are accessible",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-4",
        "requirement_text": "Report where the shared data, code, and materials are accessible.",
        "source_references": [
          {
            "locator": {
              "item_number": "4",
              "page": 2,
              "row_label": "Where the shared data, code, and materials are accessible"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Where the shared data, code, and materials are accessible",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "url"
      },
      {
        "id": "consort-2025-item-4-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How access to the shared data, code, and materials is obtained",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-4",
        "requirement_text": "Report how access to the shared data, code, and materials is obtained.",
        "source_references": [
          {
            "locator": {
              "item_number": "4",
              "page": 2,
              "row_label": "How access to the shared data, code, and materials is obtained"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How access to the shared data, code, and materials is obtained",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-4-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Explicit statement that no sharing is planned",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-4",
        "requirement_text": "Provide an explicit statement that no sharing is planned.",
        "source_references": [
          {
            "locator": {
              "item_number": "4",
              "page": 2,
              "row_label": "Explicit statement that no sharing is planned"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Explicit statement that no sharing is planned",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "id": "consort-2025-item-4-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Explanation of why no sharing is planned",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-4",
        "requirement_text": "Report explanation of why no sharing is planned.",
        "source_references": [
          {
            "locator": {
              "item_number": "4",
              "page": 2,
              "row_label": "Explanation of why no sharing is planned"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Explanation of why no sharing is planned",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "satisfy_with": {
            "ref": "consort-2025-item-4-g01"
          }
        },
        "id": "consort-2025-rule-item-4-completeness",
        "label": "Item 4 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-open-science",
    "source_references": [
      {
        "locator": {
          "item_number": "4"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "4",
          "page": 2
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Where and how the individual de-identified participant data (including data dictionary), statistical code and any other materials can be accessed",
    "status": "reviewed",
    "topic": "consort-2025-topic-data-sharing",
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
