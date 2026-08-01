---
id: consort-2025-item-19
type: ChecklistItem
item_number: 19
label: "Access to the allocation sequence during enrolment and assignment"
guideline_version: consort-2025
section: consort-2025-section-methods
topic: consort-2025-topic-implementation
status: reviewed
order: 24
requirement_count: 6
condition_count: 1
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 19: Access to the allocation sequence during enrolment and assignment

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand access to the allocation sequence during enrolment and assignment. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "Whether personnel who enrolled and those who assigned participants had access to the random allocation sequence" — CONSORT 2025 expanded checklist, item 19.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Methods|Methods]]
- **Topic:** [[Implementation|Implementation]]
- **Domain classes:** [[RandomAllocationProcess]], [[AllocationConcealmentProcess]], [[TrialRole]]

## Atomic requirements

1. **Who had access to the random allocation sequence.** Report who had access to the random allocation sequence. (`must`; expects `person_or_role`)
2. **Who enrolled participants.** Report who enrolled participants. (`must`; expects `person_or_role`)
3. **Who assigned participants to interventions.** Report who assigned participants to interventions. (`must`; expects `person_or_role`)
4. **Whether enrolling and assigning personnel had access to the sequence.** State whether enrolling and assigning personnel had access to the sequence. (`must`; expects `boolean_statement`)
5. **How and where the allocation list was stored when roles overlapped.** Report how and where the allocation list was stored when roles overlapped. (`conditional_must`; expects `free_text_description`; when `consort-2025-condition-allocation-roles-overlap`)
6. **Mechanisms preventing enrolling and assigning personnel from accessing the list.** Report mechanisms preventing enrolling and assigning personnel from accessing the list. (`conditional_must`; expects `method_description`; when `consort-2025-condition-allocation-roles-overlap`)

## Applicability

- **Sequence or concealment roles overlap with assignment implementation:** `{"equals":true,"fact":"design.allocation.roles_overlap"}`

## Scope and repetition

No explicit repetition scope is defined; each requirement is evaluated once.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 19 completeness:** `{"all":[{"require":{"ref":"consort-2025-item-19-r01"}},{"require":{"ref":"consort-2025-item-19-r02"}},{"require":{"ref":"consort-2025-item-19-r03"}},{"require":{"ref":"consort-2025-item-19-r04"}},{"require":{"ref":"consort-2025-item-19-r05"}},{"require":{"ref":"consort-2025-item-19-r06"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "objective",
        "expression": {
          "equals": true,
          "fact": "design.allocation.roles_overlap"
        },
        "id": "consort-2025-condition-allocation-roles-overlap",
        "label": "Sequence or concealment roles overlap with assignment implementation",
        "source_references": [
          {
            "locator": {
              "item_number": "19",
              "page": 7,
              "quoted_fragment": "Whether personnel who enrolled and those who assigned participants had access to the random allocation sequence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "Whether personnel who enrolled and those who assigned participants had access to the random allocation sequence",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-19",
    "item_number": "19",
    "label": "Access to the allocation sequence during enrolment and assignment",
    "order": 24,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand access to the allocation sequence during enrolment and assignment. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-19-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-allocation-roles-overlap"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-19-r01",
        "consort-2025-item-19-r02",
        "consort-2025-item-19-r03",
        "consort-2025-item-19-r04",
        "consort-2025-item-19-r05",
        "consort-2025-item-19-r06"
      ],
      "targets_domain_class": [
        "consort-class-random-allocation-process",
        "consort-class-allocation-concealment-process",
        "consort-class-trial-role"
      ]
    },
    "requirements": [
      {
        "id": "consort-2025-item-19-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who had access to the random allocation sequence",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-19",
        "requirement_text": "Report who had access to the random allocation sequence.",
        "source_references": [
          {
            "locator": {
              "item_number": "19",
              "page": 7,
              "row_label": "Who had access to the random allocation sequence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who had access to the random allocation sequence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "id": "consort-2025-item-19-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who enrolled participants",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-19",
        "requirement_text": "Report who enrolled participants.",
        "source_references": [
          {
            "locator": {
              "item_number": "19",
              "page": 7,
              "row_label": "Who enrolled participants"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who enrolled participants",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "id": "consort-2025-item-19-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Who assigned participants to interventions",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-19",
        "requirement_text": "Report who assigned participants to interventions.",
        "source_references": [
          {
            "locator": {
              "item_number": "19",
              "page": 7,
              "row_label": "Who assigned participants to interventions"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Who assigned participants to interventions",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "person_or_role"
      },
      {
        "id": "consort-2025-item-19-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Whether enrolling and assigning personnel had access to the sequence",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-19",
        "requirement_text": "State whether enrolling and assigning personnel had access to the sequence.",
        "source_references": [
          {
            "locator": {
              "item_number": "19",
              "page": 7,
              "row_label": "Whether enrolling and assigning personnel had access to the sequence"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Whether enrolling and assigning personnel had access to the sequence",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "boolean_statement"
      },
      {
        "applicability_condition": "consort-2025-condition-allocation-roles-overlap",
        "id": "consort-2025-item-19-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "How and where the allocation list was stored when roles overlapped",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-19",
        "requirement_text": "Report how and where the allocation list was stored when roles overlapped.",
        "source_references": [
          {
            "locator": {
              "item_number": "19",
              "page": 7,
              "row_label": "How and where the allocation list was stored when roles overlapped"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "How and where the allocation list was stored when roles overlapped",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "free_text_description"
      },
      {
        "applicability_condition": "consort-2025-condition-allocation-roles-overlap",
        "id": "consort-2025-item-19-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Mechanisms preventing enrolling and assigning personnel from accessing the list",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-19",
        "requirement_text": "Report mechanisms preventing enrolling and assigning personnel from accessing the list.",
        "source_references": [
          {
            "locator": {
              "item_number": "19",
              "page": 7,
              "row_label": "Mechanisms preventing enrolling and assigning personnel from accessing the list"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Mechanisms preventing enrolling and assigning personnel from accessing the list",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "method_description"
      }
    ],
    "rules": [
      {
        "expression": {
          "all": [
            {
              "require": {
                "ref": "consort-2025-item-19-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-19-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-19-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-19-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-19-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-19-r06"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-19-completeness",
        "label": "Item 19 completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "section": "consort-2025-section-methods",
    "source_references": [
      {
        "locator": {
          "item_number": "19"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "19",
          "page": 7
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "Whether personnel who enrolled and those who assigned participants had access to the random allocation sequence",
    "status": "reviewed",
    "topic": "consort-2025-topic-implementation",
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
