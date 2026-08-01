---
id: consort-2025-item-11
type: ChecklistItem
item_number: 11
label: "Trial settings and locations"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-trial-setting
status: reviewed
order: 13
requirement_count: 3
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 11: Trial settings and locations

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand trial settings and locations. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Settings (e.g., community, hospital) and locations (e.g., countries, sites) where the trial was conducted" — CONSORT 2025 expanded checklist, item 11.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Trial setting|Trial setting]]
- **Domain classes:** [[RandomisedTrial]]

## Atomic requirements

1. **Geographic locations where the trial was conducted.** Report geographic locations where the trial was conducted. (`must`; expects `free_text_description`)
2. **Participant recruitment settings.** Report participant recruitment settings. (`must`; expects `free_text_description`)
3. **Number of sites.** Report number of sites. (`must`; expects `number`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 11 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-11-r01"}},{"require":{"ref":"consort-2025-item-11-r02"}},{"require":{"ref":"consort-2025-item-11-r03"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Settings (e.g., community, hospital) and locations (e.g., countries, sites) where the trial was conducted",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-11",
    "item_number": "11",
    "label": "Trial settings and locations",
    "order": 13,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand trial settings and locations. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-11-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-11-r01",
        "consort-2025-item-11-r02",
        "consort-2025-item-11-r03"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-11-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Geographic locations where the trial was conducted",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-11",
        "requirement_text": "Report geographic locations where the trial was conducted.",
        "source_references": [
          {
            "locator": {
              "item_number": "11",
              "page": 4,
              "row_label": "Geographic locations where the trial was conducted"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Geographic locations where the trial was conducted",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-11-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Participant recruitment settings",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-11",
        "requirement_text": "Report participant recruitment settings.",
        "source_references": [
          {
            "locator": {
              "item_number": "11",
              "page": 4,
              "row_label": "Participant recruitment settings"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Participant recruitment settings",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-11-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number of sites",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-11",
        "requirement_text": "Report number of sites.",
        "source_references": [
          {
            "locator": {
              "item_number": "11",
              "page": 4,
              "row_label": "Number of sites"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number of sites",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-11-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-11-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-11-r03"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-11-completeness",
        "label": "Item 11 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "11"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "11",
          "page": 4
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Settings (e.g., community, hospital) and locations (e.g., countries, sites) where the trial was conducted",
    "status": "reviewed",
    "topic": "consort-2025-topic-trial-setting",
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
