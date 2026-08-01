---
id: consort-2025-class-catalog
type: OntologyEntity
label: "Class Catalog"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# Class Catalog

## Guideline metamodel classes

### OntologyEntity

Abstract superclass for every machine-readable entity. Stable ID: `consort-class-ontology-entity`.

### OntologyClass

A first-class definition of a category of ontology entity. Parent: `OntologyEntity`. Stable ID: `consort-class-ontology-class`.

### ReportingGuideline

A maintained reporting standard with one or more released versions. Parent: `OntologyEntity`. Stable ID: `consort-class-reporting-guideline`.

### GuidelineVersion

A released version of a reporting guideline. Parent: `OntologyEntity`. Stable ID: `consort-class-guideline-version`.

### ChecklistSection

A top-level organizational section of a guideline version. Parent: `OntologyEntity`. Stable ID: `consort-class-checklist-section`.

### ChecklistTopic

A named topic grouping checklist items within a section. Parent: `OntologyEntity`. Stable ID: `consort-class-checklist-topic`.

### ChecklistItem

An independently addressable checklist entry, including lettered subitems. Parent: `OntologyEntity`. Stable ID: `consort-class-checklist-item`.

### AtomicRequirement

The smallest independently evaluable reporting requirement. Parent: `OntologyEntity`. Stable ID: `consort-class-atomic-requirement`.

### RequirementGroup

A logical grouping of atomic requirements or other groups. Parent: `OntologyEntity`. Stable ID: `consort-class-requirement-group`.

### ApplicabilityCondition

A formal condition determining whether an entity is active. Parent: `OntologyEntity`. Stable ID: `consort-class-applicability-condition`.

### ScopeDefinition

A definition of the entities over which a requirement repeats. Parent: `OntologyEntity`. Stable ID: `consort-class-scope-definition`.

### NormativeRule

A declarative rule for applicability, composition, scope, or completeness. Parent: `OntologyEntity`. Stable ID: `consort-class-normative-rule`.

### ControlledTerm

A managed vocabulary value. Parent: `OntologyEntity`. Stable ID: `consort-class-controlled-term`.

### SourceReference

A bibliographic or web source supporting an ontology entity. Parent: `OntologyEntity`. Stable ID: `consort-class-source-reference`.

### SourceLocator

A precise location within a source. Parent: `OntologyEntity`. Stable ID: `consort-class-source-locator`.

### ExtensionHook

A placeholder through which a CONSORT extension may refine or modify an element. Parent: `OntologyEntity`. Stable ID: `consort-class-extension-hook`.

## Trial-domain classes

### [[RandomisedTrial]]

A study in which participants or other units are assigned to trial arms using a random allocation process. Parent: `OntologyEntity`. Stable ID: `consort-class-randomised-trial`.

### [[TrialDesign]]

The structural design of a randomised trial, including design type, framework, unit of randomisation, and allocation ratio. Parent: `OntologyEntity`. Stable ID: `consort-class-trial-design`.

### [[TrialArm]]

A named group to which participants or other units can be assigned and for which an intervention or comparator is specified. Parent: `OntologyEntity`. Stable ID: `consort-class-trial-arm`.

### [[Participant]]

A person or other eligible unit enrolled in a randomised trial. Parent: `OntologyEntity`. Stable ID: `consort-class-participant`.

### [[Intervention]]

A treatment, exposure, strategy, or care process assigned or delivered within a trial arm. Parent: `OntologyEntity`. Stable ID: `consort-class-intervention`.

### [[Comparator]]

The intervention, usual care, placebo, or other condition against which another intervention is evaluated. Parent: `OntologyEntity`. Stable ID: `consort-class-comparator`.

### [[OutcomeSpecification]]

A prespecified definition of an outcome, including role, variable, metric, aggregation method, time point, and assessor. Parent: `OntologyEntity`. Stable ID: `consort-class-outcome-specification`.

### [[PrimaryOutcome]]

An OutcomeSpecification designated as primary in the trial protocol. Parent: `OutcomeSpecification`. Stable ID: `consort-class-primary-outcome`.

### [[SecondaryOutcome]]

An OutcomeSpecification designated as secondary in the trial protocol. Parent: `OutcomeSpecification`. Stable ID: `consort-class-secondary-outcome`.

### [[HarmsOutcome]]

An OutcomeSpecification describing a harm or unintended effect and its assessment method. Parent: `OutcomeSpecification`. Stable ID: `consort-class-harms-outcome`.

### [[RandomAllocationProcess]]

The process used to generate and implement a random allocation sequence. Parent: `OntologyEntity`. Stable ID: `consort-class-random-allocation-process`.

### [[AllocationConcealmentProcess]]

The process used to prevent foreknowledge of upcoming trial-arm assignments before allocation. Parent: `OntologyEntity`. Stable ID: `consort-class-allocation-concealment-process`.

### [[BlindingProcess]]

The process used to establish, maintain, evaluate, or break blinding to trial-arm assignment. Parent: `OntologyEntity`. Stable ID: `consort-class-blinding-process`.

### [[TrialRole]]

A defined responsibility performed by a person, group, or organization in trial design, conduct, analysis, or reporting. Parent: `OntologyEntity`. Stable ID: `consort-class-trial-role`.

### [[ParticipantFlowObservation]]

A count or status observation about participants at a defined trial-flow stage, optionally with reasons. Parent: `OntologyEntity`. Stable ID: `consort-class-participant-flow-observation`.

### [[OutcomeResult]]

A result for an OutcomeSpecification from a defined analysis population and time point. Parent: `OntologyEntity`. Stable ID: `consort-class-outcome-result`.

### [[GroupResult]]

The result observed for a particular TrialArm within an OutcomeResult. Parent: `OntologyEntity`. Stable ID: `consort-class-group-result`.

### [[EffectEstimate]]

A quantitative estimate comparing results between trial arms or otherwise summarizing an intervention effect. Parent: `OntologyEntity`. Stable ID: `consort-class-effect-estimate`.

### [[PrecisionEstimate]]

A quantitative expression of uncertainty around an EffectEstimate, such as a confidence or credible interval. Parent: `OntologyEntity`. Stable ID: `consort-class-precision-estimate`.

The parseable catalog is `_data/classes.yaml`.
