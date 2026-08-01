---
id: consort-2025-rule-catalog
type: OntologyEntity
label: "Rule Catalog"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# Rule Catalog

The ontology now contains **60 normative rules** in three scopes: one global reporting rule, 49 checklist-item rules, and 10 draft structural rules for future trial instances. The canonical machine-readable definitions are in [`_data/rules.yaml`](./_data/rules.yaml) for global and trial-domain rules and [`_data/items.yaml`](./_data/items.yaml) for item rules.

> [!rule] General completeness
> An item is complete when every applicable `must` or `conditional_must` atomic requirement is satisfied, subject to its requirement-group operators.

## Rule inventory

| Scope           | Rule kind                 | Count | Where the rules are listed                                                                                                                                                                                          |
| --------------- | ------------------------- | ----: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Global          | General item completeness |     1 | [[General item completeness]]                                                                                                                                                                                       |
| Checklist items | Item completeness         |    42 | [Checklist Index](./09-checklist-index), “Formal rules” column                                                                                                                                                      |
| Checklist items | Conditional applicability |     5 | [Items 12b](./items/consort-12b#formal-rules), [20b](./items/consort-20b#formal-rules), [21d](./items/consort-21d#formal-rules), [23b](./items/consort-23b#formal-rules), and [28](./items/consort-28#formal-rules) |
| Checklist items | Repeated scope            |     1 | [Item 26](./items/consort-26#formal-rules)                                                                                                                                                                          |
| Checklist items | Typed branching           |     1 | [Item 26](./items/consort-26#formal-rules)                                                                                                                                                                          |
| Trial domain    | Structural integrity      |    10 | [Trial Domain Model — Structural rules](./11-trial-domain-model#structural-rules)                                                                                                                                   |

The item-rule total is 49 because five conditionally applicable items have a second applicability rule, and item 26 has two additional rules for repeated scope and typed branching.

## Expression language

Supported expression operators are `all`, `any`, `not`, `implies`, `equals`, `in`, `exists`, `for_each`, `at_least`, `exactly_one`, `require`, `activate`, and `satisfy_with`.

The catalog supports unconditional requirements, conditional items, conditional subrequirements, repeated scopes, typed branches, alternative satisfaction, explicit negative statements, expected locations, cross-item conceptual dependencies, and trial-domain integrity constraints.

## Reusable rule patterns

See [[General item completeness]], [[Explicit negative alternatives]], [[Conditional applicability]], [[Repeated scope]], and [[Typed branching]].

> [!note]
> The 10 trial-domain rules are draft structural constraints authored for this ontology. They are not additional CONSORT 2025 reporting items and should be reviewed before they are used to validate populated trial data.
