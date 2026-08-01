---
id: consort-2025-item-21b
type: ChecklistItem
item_number: 21b
label: "Analysis populations and groups"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-statistical-methods
status: reviewed
order: 28
requirement_count: 3
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 21b: Analysis populations and groups

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand analysis populations and groups. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Definition of who is included in each analysis, and in which group" — CONSORT 2025 expanded checklist, item 21b.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Statistical methods|Statistical methods]]
- **Domain classes:** [[Participant]], [[TrialArm]]

## Atomic requirements

1. **Who was included in each primary and other analysis.** Report who was included in each primary and other analysis. (`must`; expects `person_or_role`; scoped by `consort-2025-scope-item-21b-each-analysis`)
2. **Exclusions due to missing data or other reasons.** Report exclusions due to missing data or other reasons. (`must`; expects `reason`; scoped by `consort-2025-scope-item-21b-each-analysis`)
3. **Trial group in which participants were analysed.** Report trial group in which participants were analysed. (`must`; expects `free_text_description`; scoped by `consort-2025-scope-item-21b-each-analysis`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

- **Each statistical analysis:** repeat over `analysis.declared`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 21b completeness:** `{"all":[{"require":{"ref":"consort-2025-item-21b-r01"}},{"require":{"ref":"consort-2025-item-21b-r02"}},{"require":{"ref":"consort-2025-item-21b-r03"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Definition of who is included in each analysis, and in which group",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-21b",
    "item_number": "21b",
    "label": "Analysis populations and groups",
    "order": 28,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand analysis populations and groups. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-21b-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-21b-r01",
        "consort-2025-item-21b-r02",
        "consort-2025-item-21b-r03"
      ],
      "targets_domain_class": [
        "consort-class-participant",
        "consort-class-trial-arm"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-21b-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who was included in each primary and other analysis",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21b",
        "requirement_text": "Report who was included in each primary and other analysis.",
        "scope": "consort-2025-scope-item-21b-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21b",
              "page": 8,
              "row_label": "Who was included in each primary and other analysis"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who was included in each primary and other analysis",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "id": "consort-2025-item-21b-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Exclusions due to missing data or other reasons",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21b",
        "requirement_text": "Report exclusions due to missing data or other reasons.",
        "scope": "consort-2025-scope-item-21b-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21b",
              "page": 8,
              "row_label": "Exclusions due to missing data or other reasons"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Exclusions due to missing data or other reasons",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "reason"
      },
      {
        "id": "consort-2025-item-21b-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Trial group in which participants were analysed",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-21b",
        "requirement_text": "Report trial group in which participants were analysed.",
        "scope": "consort-2025-scope-item-21b-each-analysis",
        "source_references": [
          {
            "locator": {
              "item_number": "21b",
              "page": 8,
              "row_label": "Trial group in which participants were analysed"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Trial group in which participants were analysed",
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
                "ref": "consort-2025-item-21b-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21b-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-21b-r03"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-21b-completeness",
        "label": "Item 21b completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "analysis.declared",
        "id": "consort-2025-scope-item-21b-each-analysis",
        "label": "Each statistical analysis",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "21b"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "21b",
          "page": 8
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Definition of who is included in each analysis, and in which group",
    "status": "reviewed",
    "topic": "consort-2025-topic-statistical-methods",
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
