---
id: consort-2025-item-3
type: ChecklistItem
item_number: 3
label: "Access to the trial protocol and statistical analysis plan"
guideline_version: consort-2025
section: consort-2025-section-open-science
topic: consort-2025-topic-protocol-and-statistical-analysis-plan
status: reviewed
order: 4
requirement_count: 2
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 3: Access to the trial protocol and statistical analysis plan

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand access to the trial protocol and statistical analysis plan. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Where the trial protocol and statistical analysis plan can be accessed" — CONSORT 2025 expanded checklist, item 3.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Open Science|Open science]]
- **Topic:** [[Protocol and statistical analysis plan|Protocol and statistical analysis plan]]
- **Domain classes:** [[RandomisedTrial]], [[TrialDesign]]

## Atomic requirements

1. **Location of the protocol with a URL, DOI, repository, registry, or supplement locator.** Report location of the protocol with a URL, DOI, repository, registry, or supplement locator. (`must`; expects `url`)
2. **Location of the full statistical analysis plan with a URL, DOI, repository, registry, or supplement locator.** Report location of the full statistical analysis plan with a URL, DOI, repository, registry, or supplement locator. (`must`; expects `url`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 3 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-3-r01"}},{"require":{"ref":"consort-2025-item-3-r02"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Where the trial protocol and statistical analysis plan can be accessed",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-3",
    "item_number": "3",
    "label": "Access to the trial protocol and statistical analysis plan",
    "order": 4,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand access to the trial protocol and statistical analysis plan. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-3-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-3-r01",
        "consort-2025-item-3-r02"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial",
        "consort-class-trial-design"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-3-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Location of the protocol with a URL, DOI, repository, registry, or supplement locator",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-3",
        "requirement_text": "Report location of the protocol with a URL, DOI, repository, registry, or supplement locator.",
        "source_references": [
          {
            "locator": {
              "item_number": "3",
              "page": 2,
              "row_label": "Location of the protocol with a URL, DOI, repository, registry, or supplement locator"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Location of the protocol with a URL, DOI, repository, registry, or supplement locator",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "url"
      },
      {
        "id": "consort-2025-item-3-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Location of the full statistical analysis plan with a URL, DOI, repository, registry, or supplement locator",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-3",
        "requirement_text": "Report location of the full statistical analysis plan with a URL, DOI, repository, registry, or supplement locator.",
        "source_references": [
          {
            "locator": {
              "item_number": "3",
              "page": 2,
              "row_label": "Location of the full statistical analysis plan with a URL, DOI, repository, registry, or supplement locator"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Location of the full statistical analysis plan with a URL, DOI, repository, registry, or supplement locator",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "url"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-3-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-3-r02"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-3-completeness",
        "label": "Item 3 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-open-science",
    "source_references": [
      {
        "locator": {
          "item_number": "3"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "3",
          "page": 2
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Where the trial protocol and statistical analysis plan can be accessed",
    "status": "reviewed",
    "topic": "consort-2025-topic-protocol-and-statistical-analysis-plan",
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
