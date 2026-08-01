---
id: consort-2025-item-2
type: ChecklistItem
item_number: 2
label: "Trial registry name, identifier with URL, and registration date"
guideline_version: consort-2025
section: consort-2025-section-open-science
topic: consort-2025-topic-trial-registration
status: reviewed
order: 3
requirement_count: 5
condition_count: 0
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 2: Trial registry name, identifier with URL, and registration date

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand trial registry name, identifier with url, and registration date. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Name of trial registry, identifying number (with URL) and date of registration" — CONSORT 2025 expanded checklist, item 2.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Open Science|Open science]]
- **Topic:** [[Trial registration|Trial registration]]
- **Domain classes:** [[RandomisedTrial]]

## Atomic requirements

1. **Name of registry.** Report name of registry. (`must`; expects `free_text_description`)
2. **Trial registry identifying number.** Report trial registry identifying number. (`must`; expects `identifier`)
3. **URL to registry record.** Report uRL to registry record. (`must`; expects `url`)
4. **Date of registration.** Report date of registration. (`must`; expects `date`)
5. **Whether results are publicly posted to the registry, available as a preprint with URL, or published with citations.** State whether results are publicly posted to the registry, available as a preprint with URL, or published with citations. (`must`; expects `boolean_statement`)

## Applicability

This item is always active for reports within the guideline's scope.

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 2 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-2-r01"}},{"require":{"ref":"consort-2025-item-2-r02"}},{"require":{"ref":"consort-2025-item-2-r03"}},{"require":{"ref":"consort-2025-item-2-r04"}},{"require":{"ref":"consort-2025-item-2-r05"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "concise_description": "Name of trial registry, identifying number (with URL) and date of registration",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-2",
    "item_number": "2",
    "label": "Trial registry name, identifier with URL, and registration date",
    "order": 3,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand trial registry name, identifier with url, and registration date. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-2-completeness"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-2-r01",
        "consort-2025-item-2-r02",
        "consort-2025-item-2-r03",
        "consort-2025-item-2-r04",
        "consort-2025-item-2-r05"
      ],
      "targets_domain_class": [
        "consort-class-randomised-trial"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-2-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Name of registry",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-2",
        "requirement_text": "Report name of registry.",
        "source_references": [
          {
            "locator": {
              "item_number": "2",
              "page": 2,
              "row_label": "Name of registry"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Name of registry",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "id": "consort-2025-item-2-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Trial registry identifying number",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-2",
        "requirement_text": "Report trial registry identifying number.",
        "source_references": [
          {
            "locator": {
              "item_number": "2",
              "page": 2,
              "row_label": "Trial registry identifying number"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Trial registry identifying number",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "identifier"
      },
      {
        "id": "consort-2025-item-2-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "URL to registry record",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-2",
        "requirement_text": "Report uRL to registry record.",
        "source_references": [
          {
            "locator": {
              "item_number": "2",
              "page": 2,
              "row_label": "URL to registry record"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "URL to registry record",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "url"
      },
      {
        "id": "consort-2025-item-2-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Date of registration",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-2",
        "requirement_text": "Report date of registration.",
        "source_references": [
          {
            "locator": {
              "item_number": "2",
              "page": 2,
              "row_label": "Date of registration"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Date of registration",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "date"
      },
      {
        "id": "consort-2025-item-2-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether results are publicly posted to the registry, available as a preprint with URL, or published with citations",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-2",
        "requirement_text": "State whether results are publicly posted to the registry, available as a preprint with URL, or published with citations.",
        "source_references": [
          {
            "locator": {
              "item_number": "2",
              "page": 2,
              "row_label": "Whether results are publicly posted to the registry, available as a preprint with URL, or published with citations"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether results are publicly posted to the registry, available as a preprint with URL, or published with citations",
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
                "ref": "consort-2025-item-2-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-2-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-2-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-2-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-2-r05"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-2-completeness",
        "label": "Item 2 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-open-science",
    "source_references": [
      {
        "locator": {
          "item_number": "2"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "2",
          "page": 2
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Name of trial registry, identifying number (with URL) and date of registration",
    "status": "reviewed",
    "topic": "consort-2025-topic-trial-registration",
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
