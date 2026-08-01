---
id: consort-2025-item-10
type: ChecklistItem
item_number: 10
label: "Important changes after trial commencement"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-changes-to-trial-protocol
status: reviewed
order: 12
requirement_count: 4
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 10: Important changes after trial commencement

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand important changes after trial commencement. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Important changes to the trial after it commenced including any outcomes or analyses that were not prespecified, with reason" — CONSORT 2025 expanded checklist, item 10.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Changes to trial protocol|Changes to trial protocol]]
- **Domain classes:** [[RandomisedTrial]], [[TrialDesign]], [[OutcomeSpecification]]

## Atomic requirements

1. **Changes to the original protocol after commencement, with timing.** Report changes to the original protocol after commencement, with timing. (`must`; expects `free_text_description`)
2. **Reasons for each important protocol change.** Report reasons for each important protocol change. (`must`; expects `reason`)
3. **Outcomes that were not prespecified.** Report outcomes that were not prespecified. (`must`; expects `free_text_description`)
4. **Analyses that were not prespecified.** Report analyses that were not prespecified. (`must`; expects `free_text_description`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 10 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-10-r01"}},{"require":{"ref":"consort-2025-item-10-r02"}},{"require":{"ref":"consort-2025-item-10-r03"}},{"require":{"ref":"consort-2025-item-10-r04"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Important changes to the trial after it commenced including any outcomes or analyses that were not prespecified, with reason",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-10",
    "item_number": "10",
    "label": "Important changes after trial commencement",
    "order": 12,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand important changes after trial commencement. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-10-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-10-r01",
        "consort-2025-item-10-r02",
        "consort-2025-item-10-r03",
        "consort-2025-item-10-r04"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-trial-design",
        "consort-class-outcome-specification"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-10-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Changes to the original protocol after commencement, with timing",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-10",
        "requirement_text": "Report changes to the original protocol after commencement, with timing.",
        "source_references": [
          {
            "locator": {
              "item_number": "10",
              "page": 3,
              "row_label": "Changes to the original protocol after commencement, with timing"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Changes to the original protocol after commencement, with timing",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-10-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Reasons for each important protocol change",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-10",
        "requirement_text": "Report reasons for each important protocol change.",
        "source_references": [
          {
            "locator": {
              "item_number": "10",
              "page": 3,
              "row_label": "Reasons for each important protocol change"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Reasons for each important protocol change",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "id": "consort-2025-item-10-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Outcomes that were not prespecified",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-10",
        "requirement_text": "Report outcomes that were not prespecified.",
        "source_references": [
          {
            "locator": {
              "item_number": "10",
              "page": 3,
              "row_label": "Outcomes that were not prespecified"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Outcomes that were not prespecified",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-10-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Analyses that were not prespecified",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-10",
        "requirement_text": "Report analyses that were not prespecified.",
        "source_references": [
          {
            "locator": {
              "item_number": "10",
              "page": 3,
              "row_label": "Analyses that were not prespecified"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Analyses that were not prespecified",
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
                "ref": "consort-2025-item-10-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-10-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-10-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-10-r04"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-10-completeness",
        "label": "Item 10 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "10"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "10",
          "page": 3
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Important changes to the trial after it commenced including any outcomes or analyses that were not prespecified, with reason",
    "status": "reviewed",
    "topic": "consort-2025-topic-changes-to-trial-protocol",
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
