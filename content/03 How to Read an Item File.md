---
id: consort-2025-how-to-read-item
type: OntologyEntity
label: "How to Read an Item File"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# How to Read an Item File

Each item starts with discovery metadata and an attributed concise source statement. The atomic-requirement list separates independently assessable obligations. Applicability explains activation conditions, scope explains repetition, and requirement groups express `all_of` or alternative branches.

The embedded JSON object is valid YAML and is an exact copy of the canonical record. Stable IDs—not labels or filenames—carry identity.

The “Domain classes” row connects the checklist item to the first-class concepts it reports about. Follow those links to [[11 Trial Domain Model]].

> [!warning]
> `conditional_must` never means “optional.” It is required when its explicit condition is true.

Try [[CONSORT 4]], [[CONSORT 14]], [[CONSORT 20b]], [[CONSORT 26]], and [[CONSORT 27]] as worked patterns.
