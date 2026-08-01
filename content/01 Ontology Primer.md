---
id: consort-2025-ontology-primer
type: OntologyEntity
label: "Ontology Primer"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# Ontology Primer

> [!definition] Ontology
> An ontology is an explicit, structured specification of concepts in a domain, their relationships, and the constraints and rules that organize them.

| Term | Meaning here | Example |
|---|---|---|
| Class | Category of entity | `ChecklistItem` |
| Individual | Particular member of a class | `consort-2025-item-20b` |
| Attribute | Literal property | `item_number: 20b` |
| Relation | Typed connection | `has_atomic_requirement` |
| Constraint | Structural restriction | Every item has a source |
| Rule | Conditional or compositional logic | Item 20b activates if blinding occurred |
| Controlled term | Permitted vocabulary value | `conditional_must` |
| Taxonomy | Mainly a broader/narrower hierarchy | Guideline element hierarchy |
| Ontology | Taxonomy plus relations, constraints, and rules | This complete CONSORT model |

> [!example]
> `ChecklistItem` is a class. `consort-2025-item-20b` is an individual. `consort-2025-item-20b-r01` is a different individual of class `AtomicRequirement`.

```mermaid
classDiagram
  ReportingGuideline "1" --> "1..*" GuidelineVersion : has_version
  GuidelineVersion "1" --> "1..*" ChecklistSection : has_section
  ChecklistSection "1" --> "1..*" ChecklistItem : contains_item
  ChecklistItem "1" --> "1..*" AtomicRequirement : has_atomic_requirement
  ChecklistItem "0..*" --> "0..*" ApplicabilityCondition : applies_when
  NormativeRule --> AtomicRequirement : references
```

See [[04 Class Catalog]], [[05 Relation Catalog]], and [[06 Rule Catalog]].
