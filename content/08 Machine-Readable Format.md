---
id: consort-2025-machine-format
type: OntologyEntity
label: "Machine-Readable Format"
status: reviewed
tags:
  - consort/2025
  - ontology
---

# Machine-Readable Format

Canonical data lives in `_data/*.yaml`. These files deliberately use JSON syntax, which is valid YAML 1.2 and lets the dependency-free Node.js reference implementation parse them deterministically.

`_data/classes.yaml` defines the guideline metamodel and 19 first-class trial-domain classes. Each domain class has a stable ID, parent, properties, and relations. Checklist items map to them through `targets_domain_class`.

Each item note embeds exactly one record between stable `BEGIN:CONSORT-ONTOLOGY` and `END:CONSORT-ONTOLOGY` comments. The build rejects divergence between embedded and canonical records.

Rules form a closed declarative language. Fact paths are interface contracts under the namespaces `trial.*`, `design.*`, `outcome.*`, `analysis.*`, `intervention.*`, `harm.*`, `registration.*`, and `reporting_context.*`. No executable code is allowed in ontology data.

Generated interchange artifacts live in `_generated`; they never replace canonical data.
