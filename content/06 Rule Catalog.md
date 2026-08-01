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

> [!rule] General completeness
> An item is complete when every applicable `must` or `conditional_must` atomic requirement is satisfied, subject to its requirement-group operators.

Supported expression operators are `all`, `any`, `not`, `implies`, `equals`, `in`, `exists`, `for_each`, `at_least`, `exactly_one`, `require`, `activate`, and `satisfy_with`.

The catalog supports unconditional requirements, conditional items, conditional subrequirements, repeated scopes, typed branches, alternative satisfaction, explicit negative statements, expected locations, and cross-item conceptual dependencies.

See [[General item completeness]], [[Explicit negative alternatives]], [[Conditional applicability]], [[Repeated scope]], and [[Typed branching]].
