---
id: consort-2025-item-22a
type: ChecklistItem
item_number: 22a
label: "Participant numbers assigned, receiving intervention, and analysed"
guideline_version: consort-2025
section: consort-2025-section-results
topic: consort-2025-topic-participant-flow
status: reviewed
order: 31
requirement_count: 9
condition_count: 2
source_complete: true
tags:
  - consort/2025
  - ontology/checklist-item
---

# CONSORT 22a: Participant numbers assigned, receiving intervention, and analysed

## Plain-language meaning

Authors should provide the information represented by the atomic requirements below so readers can understand participant numbers assigned, receiving intervention, and analysed. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.

> [!source] Official concise checklist wording
> "For each group, the numbers randomly assigned, receiving intended intervention, and analysed for the primary outcome" — CONSORT 2025 expanded checklist, item 22a.

## Place in the ontology

- **Class:** [[04 Class Catalog|ChecklistItem]]
- **Section:** [[Results|Results]]
- **Topic:** [[Participant flow|Participant flow]]
- **Domain classes:** [[ParticipantFlowObservation]], [[Participant]], [[TrialArm]]

## Atomic requirements

1. **Number evaluated for potential enrolment, if recorded.** Report number evaluated for potential enrolment, if recorded. (`conditional_must`; expects `number`; when `consort-2025-condition-potential-enrolment-recorded`)
2. **Number excluded before randomisation with exact reasons.** Report number excluded before randomisation with exact reasons. (`must`; expects `number`)
3. **Number randomly assigned.** Report number randomly assigned. (`must`; expects `number`; scoped by `consort-2025-scope-item-22a-each-trial-group`)
4. **Number receiving the intervention as allocated.** Report number receiving the intervention as allocated. (`must`; expects `number`; scoped by `consort-2025-scope-item-22a-each-trial-group`)
5. **Number completing the intervention as allocated.** Report number completing the intervention as allocated. (`must`; expects `number`; scoped by `consort-2025-scope-item-22a-each-trial-group`)
6. **Number completing follow-up as planned.** Report number completing follow-up as planned. (`must`; expects `number`; scoped by `consort-2025-scope-item-22a-each-trial-group`)
7. **Number included in the main primary-outcome analysis.** Report number included in the main primary-outcome analysis. (`must`; expects `number`; scoped by `consort-2025-scope-item-22a-each-trial-group`)
8. **Number of care providers or centres performing the intervention where appropriate.** Report number of care providers or centres performing the intervention where appropriate. (`conditional_must`; expects `number`; when `consort-2025-condition-provider-centre-flow-applicable`; scoped by `consort-2025-scope-item-22a-each-trial-group`)
9. **Number treated by each provider or centre where appropriate.** Report number treated by each provider or centre where appropriate. (`conditional_must`; expects `number`; when `consort-2025-condition-provider-centre-flow-applicable`; scoped by `consort-2025-scope-item-22a-each-trial-group`)

## Applicability

- **Potential enrolment was recorded:** `{"equals":true,"fact":"trial.flow.potential_enrolment_recorded"}`
- **Provider or centre flow is appropriate:** `{"equals":true,"fact":"reporting_context.provider_centre_flow.applicable"}`

## Scope and repetition

- **Each trial group:** repeat over `trial.group`.

## Relations to other guideline elements

- [[09 Checklist Index]]

## Formal rules

> [!rule] Logical composition
> All applicable `must` and `conditional_must` requirements are conjunctive.

- **Item 22a completeness:** `{"all":[{"require":{"ref":"consort-2025-item-22a-r01"}},{"require":{"ref":"consort-2025-item-22a-r02"}},{"require":{"ref":"consort-2025-item-22a-r03"}},{"require":{"ref":"consort-2025-item-22a-r04"}},{"require":{"ref":"consort-2025-item-22a-r05"}},{"require":{"ref":"consort-2025-item-22a-r06"}},{"require":{"ref":"consort-2025-item-22a-r07"}},{"require":{"ref":"consort-2025-item-22a-r08"}},{"require":{"ref":"consort-2025-item-22a-r09"}}]}`

## Machine-readable specification

<!-- BEGIN:CONSORT-ONTOLOGY -->
```yaml
{
  "entity": {
    "applicability_conditions": [
      {
        "condition_kind": "presence_dependent",
        "expression": {
          "equals": true,
          "fact": "trial.flow.potential_enrolment_recorded"
        },
        "id": "consort-2025-condition-potential-enrolment-recorded",
        "label": "Potential enrolment was recorded",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "quoted_fragment": "For each group, the numbers randomly assigned, receiving intended intervention, and analysed for the primary outcome"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      },
      {
        "condition_kind": "contextual",
        "expression": {
          "equals": true,
          "fact": "reporting_context.provider_centre_flow.applicable"
        },
        "id": "consort-2025-condition-provider-centre-flow-applicable",
        "label": "Provider or centre flow is appropriate",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "quoted_fragment": "For each group, the numbers randomly assigned, receiving intended intervention, and analysed for the primary outcome"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "status": "reviewed",
        "type": "ApplicabilityCondition"
      }
    ],
    "concise_description": "For each group, the numbers randomly assigned, receiving intended intervention, and analysed for the primary outcome",
    "guideline_version": "consort-2025",
    "id": "consort-2025-item-22a",
    "item_number": "22a",
    "label": "Participant numbers assigned, receiving intervention, and analysed",
    "order": 31,
    "plain_language": "Authors should provide the information represented by the atomic requirements below so readers can understand participant numbers assigned, receiving intervention, and analysed. The model separates independently reportable details and makes any conditions, alternatives, and repetition explicit.",
    "relations": {
      "cross_references": [],
      "governed_by": [
        "consort-2025-rule-item-22a-completeness"
      ],
      "has_applicability_condition": [
        "consort-2025-condition-potential-enrolment-recorded",
        "consort-2025-condition-provider-centre-flow-applicable"
      ],
      "has_atomic_requirement": [
        "consort-2025-item-22a-r01",
        "consort-2025-item-22a-r02",
        "consort-2025-item-22a-r03",
        "consort-2025-item-22a-r04",
        "consort-2025-item-22a-r05",
        "consort-2025-item-22a-r06",
        "consort-2025-item-22a-r07",
        "consort-2025-item-22a-r08",
        "consort-2025-item-22a-r09"
      ],
      "targets_domain_class": [
        "consort-class-participant-flow-observation",
        "consort-class-participant",
        "consort-class-trial-arm"
      ]
    },
    "requirements": [
      {
        "applicability_condition": "consort-2025-condition-potential-enrolment-recorded",
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r01",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number evaluated for potential enrolment, if recorded",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number evaluated for potential enrolment, if recorded.",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number evaluated for potential enrolment, if recorded"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number evaluated for potential enrolment, if recorded",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r02",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number excluded before randomisation with exact reasons",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number excluded before randomisation with exact reasons.",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number excluded before randomisation with exact reasons"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number excluded before randomisation with exact reasons",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r03",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number randomly assigned",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number randomly assigned.",
        "scope": "consort-2025-scope-item-22a-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number randomly assigned"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number randomly assigned",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r04",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number receiving the intervention as allocated",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number receiving the intervention as allocated.",
        "scope": "consort-2025-scope-item-22a-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number receiving the intervention as allocated"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number receiving the intervention as allocated",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r05",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number completing the intervention as allocated",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number completing the intervention as allocated.",
        "scope": "consort-2025-scope-item-22a-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number completing the intervention as allocated"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number completing the intervention as allocated",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r06",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number completing follow-up as planned",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number completing follow-up as planned.",
        "scope": "consort-2025-scope-item-22a-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number completing follow-up as planned"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number completing follow-up as planned",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r07",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number included in the main primary-outcome analysis",
        "normative_strength": "must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number included in the main primary-outcome analysis.",
        "scope": "consort-2025-scope-item-22a-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number included in the main primary-outcome analysis"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number included in the main primary-outcome analysis",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-provider-centre-flow-applicable",
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r08",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number of care providers or centres performing the intervention where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number of care providers or centres performing the intervention where appropriate.",
        "scope": "consort-2025-scope-item-22a-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number of care providers or centres performing the intervention where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number of care providers or centres performing the intervention where appropriate",
        "status": "reviewed",
        "type": "AtomicRequirement",
        "value_expectation": "number"
      },
      {
        "applicability_condition": "consort-2025-condition-provider-centre-flow-applicable",
        "expected_location": "flow_diagram",
        "id": "consort-2025-item-22a-r09",
        "interpretation_note": "Formalized as an independently evaluable reporting obligation from the expanded-checklist detail.",
        "label": "Number treated by each provider or centre where appropriate",
        "normative_strength": "conditional_must",
        "parent_item": "consort-2025-item-22a",
        "requirement_text": "Report number treated by each provider or centre where appropriate.",
        "scope": "consort-2025-scope-item-22a-each-trial-group",
        "source_references": [
          {
            "locator": {
              "item_number": "22a",
              "page": 9,
              "row_label": "Number treated by each provider or centre where appropriate"
            },
            "source": "consort-2025-expanded-checklist"
          }
        ],
        "source_text": "Number treated by each provider or centre where appropriate",
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
                "ref": "consort-2025-item-22a-r01"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r02"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r03"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r04"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r05"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r06"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r07"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r08"
              }
            },
            {
              "require": {
                "ref": "consort-2025-item-22a-r09"
              }
            }
          ]
        },
        "id": "consort-2025-rule-item-22a-completeness",
        "label": "Item 22a completeness",
        "rule_kind": "completeness",
        "status": "reviewed",
        "type": "NormativeRule"
      }
    ],
    "scopes": [
      {
        "domain": "trial.group",
        "id": "consort-2025-scope-item-22a-each-trial-group",
        "label": "Each trial group",
        "scope_type": "for_each",
        "status": "reviewed",
        "type": "ScopeDefinition"
      }
    ],
    "section": "consort-2025-section-results",
    "source_references": [
      {
        "locator": {
          "item_number": "22a"
        },
        "source": "consort-2025-statement"
      },
      {
        "locator": {
          "item_number": "22a",
          "page": 9
        },
        "source": "consort-2025-expanded-checklist"
      }
    ],
    "source_text": "For each group, the numbers randomly assigned, receiving intended intervention, and analysed for the primary outcome",
    "status": "reviewed",
    "topic": "consort-2025-topic-participant-flow",
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
