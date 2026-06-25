# RecordWeb

**RecordWeb** is an open composition architecture for institutionally provable information on the Web.

It assembles three W3C standards — [DID](https://www.w3.org/TR/did-core/), [PROV-O](https://www.w3.org/TR/prov-o/), and [VC](https://www.w3.org/TR/vc-data-model-2.0/) — into a coherent protocol layer that makes institutional information **attributable, versioned, and cryptographically verifiable**, independent of the systems in which it is stored.

The Web made documents findable. Linked Data made facts linkable. **RecordWeb makes institutional information provable.**

---

## What is RecordWeb?

RecordWeb defines a **Record** as the smallest semantically autonomous unit of institutional information — a building permit decision, a medical examination result, a parliamentary submission, a contract. Every Record in RecordWeb has:

- A **permanent decentralised identity** (`did:rwp`) that survives system migrations
- An **immutable version graph** in which every change creates a new cryptographically secured snapshot
- A **provenance layer** (PROV-O) that structurally encodes who produced what, when, and on the basis of what
- A **tamper-evident proof** (VC Data Model 2.0) that makes the Record verifiable without a central authority

RecordWeb is not a replacement for existing W3C standards. It is the missing composition — the protocol layer that connects DID, PROV-O, and VC into a deployable architecture for institutional information.

---

## Foundational Documents

The RecordWeb specification was developed in two foundational documents, both published as defensive prior art on Zenodo:

| Document | Description | DOI |
|---|---|---|
| **RWC — RecordWeb Concept** | Conceptual foundations, design principles, relationship to archival science | [10.5281/zenodo.20475343](https://doi.org/10.5281/zenodo.20475343) |
| **RWP v0.1 — RecordWeb Protocol** | Normative technical specification: DID format, snapshot structure, version graph, Cases, federation, payload deletion | [10.5281/zenodo.20475345](https://doi.org/10.5281/zenodo.20475345) |

These documents are the single-author initial contribution by [Nik Jenzer](https://github.com/nikjenzer). They are explicitly intended as the foundation for a community-developed v1.0 — not as the conclusion of the specification process.

---

## Repositories

| Repository | Description | Status |
|---|---|---|
| [`w3c-cg-note`](https://github.com/recordweb/w3c-cg-note) | W3C Community Group Note — the primary specification document | Active, v0.0.1 draft |
| `did-rwp` | `did:rwp` DID Method Specification | Planned W3C CG deliverable |
| `poc-xyz` | Proof-of-Concept: several demonstrator, mocup, proofs, ... | Planned |

---

## Community Structure

RecordWeb distinguishes two forms of participation:

### Contributors
Individuals who materially co-develop the RecordWeb specification — writing, reviewing, prototyping, and editing the technical documents. Contributors engage at the level of protocol design and implementation.

**How to contribute:** contact the chairs (planned: open an issue or pull request in the relevant repository. See [`CONTRIBUTING.md`](CONTRIBUTING.md)).

### Members
Institutions with a professional stake in RecordWeb — public administrations, hospitals, regulated organisations, universities, software vendors, and standards bodies. Members provide use cases, validate the specification against real-world requirements, participate in pilots, and adopt RecordWeb in their domain.

Members do not need to engage at the technical protocol level. Their expertise is **domain knowledge**: what institutional provability must achieve in practice.

**Becoming a member:** contact the chairs (planned: pen an issue in this repository using the [Member Registration template](.github/ISSUE_TEMPLATE/member-registration.md)).

---

## W3C Community Group

RecordWeb is being developed as a W3C Community Group. The Community Group provides the open, international forum for collaborative specification development.

- **W3C CG proposal:** submitted to the W3C Credentials Community Group
- **Chairs:** Nik Jenzer · Melvin Carvalho
- **Status:** Formation phase — founding members welcome

The `did:rwp` DID method will be submitted to the [W3C DID Specification Registries](https://www.w3.org/TR/did-spec-registries/) as a Community Group deliverable.

---

## Governance

This organisation is governed by the RecordWeb Community Group. See [`GOVERNANCE.md`](GOVERNANCE.md) for the decision-making model, roles, and process.

---

## License

All specifications in this organisation are published under the [W3C Software and Document License](https://www.w3.org/Consortium/Legal/copyright-software). Code is licensed under [Apache 2.0](LICENSE).

---

## Contact

- **GitHub Issues:** preferred for all technical and community questions
- **Chairs:** open an issue tagged `[chairs]` for governance questions
