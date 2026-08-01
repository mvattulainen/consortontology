---
id: consort-2025-item-8
type: ChecklistItem
item_number: 8
label: "Patient or public involvement"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-patient-and-public-involvement
status: reviewed
order: 10
requirement_count: 3
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 8: Patient or public involvement

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand patient or public involvement. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Details of patient or public involvement in the design, conduct and reporting of the trial" — CONSORT 2025 expanded checklist, item 8.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Patient and public involvement|Patient and public involvement]]
- **Domain classes:** [[TrialRole]]

## Atomic requirements

1. **How patients or the public were involved at different trial stages.** Report how patients or the public were involved at different trial stages. (`must`; expects `free_text_description`)
2. **Who was involved.** Report who was involved. (`must`; expects `person_or_role`)
3. **Explicit statement that there was no patient or public involvement.** Provide an explicit statement that there was no patient or public involvement. (`must`; expects `boolean_statement`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> - **Involvement details or explicit none:** `any_of` over `consort-2025-item-8-g02`, `consort-2025-item-8-r03`.
- **Involvement details branch:** `all_of` over `consort-2025-item-8-r01`, `consort-2025-item-8-r02`.

- **Item 8 completeness:** `{"satisfy_with":{"ref":"consort-2025-item-8-g01"}}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Details of patient or public involvement in the design, conduct and reporting of the trial",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-8",
    "item_number": "8",
    "label": "Patient or public involvement",
    "order": 10,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand patient or public involvement. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-8-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-8-r01",
        "consort-2025-item-8-r02",
        "consort-2025-item-8-r03"
      ],
      "has_requirement_group": [
        "consort-2025-item-8-g01",
        "consort-2025-item-8-g02"
      ],
      "targets_domain_class": [
        "consort-class-trial-role"
      ]
    },
    "requirement_groups": [
      {
        "id": "consort-2025-item-8-g01",
        "label": "Involvement details or explicit none",
        "members": [
          "consort-2025-item-8-g02",
          "consort-2025-item-8-r03"
        ],
        "operator": "any_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      },
      {
        "id": "consort-2025-item-8-g02",
        "label": "Involvement details branch",
        "members": [
          "consort-2025-item-8-r01",
          "consort-2025-item-8-r02"
        ],
        "operator": "all_of",
        "status": "reviewed",
        "type": "RequirementGroup"
      }
    ],
    "requirements": [
      {
        "id": "consort-2025-item-8-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How patients or the public were involved at different trial stages",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-8",
        "requirement_text": "Report how patients or the public were involved at different trial stages.",
        "source_references": [
          {
            "locator": {
              "item_number": "8",
              "page": 3,
              "row_label": "How patients or the public were involved at different trial stages"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How patients or the public were involved at different trial stages",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-8-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who was involved",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-8",
        "requirement_text": "Report who was involved.",
        "source_references": [
          {
            "locator": {
              "item_number": "8",
              "page": 3,
              "row_label": "Who was involved"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who was involved",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "id": "consort-2025-item-8-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Explicit statement that there was no patient or public involvement",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-8",
        "requirement_text": "Provide an explicit statement that there was no patient or public involvement.",
        "source_references": [
          {
            "locator": {
              "item_number": "8",
              "page": 3,
              "row_label": "Explicit statement that there was no patient or public involvement"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Explicit statement that there was no patient or public involvement",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      }
    ],
    "rules": [
      {
        "expression": {
          "satisfy_with": {
            "ref": "consort-2025-item-8-g01"
          }
        },
        "id": "consort-2025-rule-item-8-completeness",
        "label": "Item 8 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "8"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "8",
          "page": 3
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Details of patient or public involvement in the design, conduct and reporting of the trial",
    "status": "reviewed",
    "topic": "consort-2025-topic-patient-and-public-involvement",
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
