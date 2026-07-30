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

## Governance & How Decisions Are Made

RecordWeb is governed by the RecordWeb Community Group under a minimal, consensus-based process. Start here if you want to understand or join how the specification actually gets changed:

- [`CGCharter.md`](https://github.com/recordweb/.github/blob/main/CGCharter.md) — the Community Group charter
- [`GOVERNANCE.md`](https://github.com/recordweb/.github/blob/main/GOVERNANCE.md) — roles (Chairs, Editors, Contributors, Members) and the decision-making process

Substantive changes to the specification go through a **Call for Consensus (CfC)**: a batch of related issues is opened for a minimum 14-day discussion and comment period, tracked as a dedicated issue labeled [`cfc`](https://github.com/recordweb/.github/issues?q=is%3Aissue+label%3Acfc) in this repository, cross-linked from the individual issues under discussion in `rwc` and `rwp`. Anyone can follow along or comment — no membership required to participate in discussion.

---

## Repositories

| Repository | Description | Status |
|---|---|---|
| [`rwc`](https://github.com/recordweb/rwc) | RecordWeb Concept (RWC) — the conceptual report | Initial Editor's Draft — baseline from DOI 10.5281/zenodo.20475343 |
| [`rwp`](https://github.com/recordweb/rwp) | RecordWeb Protocol (RWP) — the normative specification | Initial Editor's Draft — baseline from DOI 10.5281/zenodo.20475345 |
| [`poc-fragestunde`](https://github.com/recordweb/poc-fragestunde) | Proof of Concept — RecordWeb applied to the Swiss Parliament's Question Time | In development |
| `did-rwp` | `did:rwp` DID Method Specification | Planned W3C CG deliverable |

---

## Foundational Documents

The RecordWeb specification was developed in two foundational documents, both published as defensive prior art on Zenodo:

| Document | Description | DOI |
|---|---|---|
| **RWC — RecordWeb Concept** | Conceptual foundations, design principles, relationship to archival science | [10.5281/zenodo.20475343](https://doi.org/10.5281/zenodo.20475343) |
| **RWP v0.1 — RecordWeb Protocol** | Normative technical specification: DID format, snapshot structure, version graph, Cases, federation, payload deletion | [10.5281/zenodo.20475345](https://doi.org/10.5281/zenodo.20475345) |

These documents are the single-author initial contribution by [Nik Jenzer](https://github.com/nikjenzer). They are explicitly intended as the foundation for a community-developed v1.0 — not as the conclusion of the specification process.

---

## Community Structure

RecordWeb distinguishes two forms of participation:

### Contributors
Individuals who materially co-develop the RecordWeb specification — writing, reviewing, prototyping, and editing the technical documents. Contributors engage at the level of protocol design and implementation, and must agree to the [W3C Community Contributor License Agreement](https://www.w3.org/community/about/agreements/cla/).

**How to contribute:** open a substantive issue or pull request in the relevant repository (`rwc` or `rwp`) — that alone constitutes participation as a Contributor. See [`CONTRIBUTING.md`](CONTRIBUTING.md) where available.

### Members
Institutions with a professional stake in RecordWeb — public administrations, hospitals, regulated organisations, universities, software vendors, and standards bodies. Members provide use cases, validate the specification against real-world requirements, participate in pilots, and adopt RecordWeb in their domain. Membership does not require the CLA unless normative specification text is contributed.

**Becoming a member:** open an issue using the Member Registration template ([`GOVERNANCE.md` §3.4](https://github.com/recordweb/.github/blob/main/GOVERNANCE.md)).

---

## W3C Community Group

RecordWeb is being developed as a W3C Community Group — the open, international forum for collaborative specification development.

- **Chairs:** Nik Jenzer · Melvin Carvalho
- **Status:** Formation phase — founding members welcome

The `did:rwp` DID method will be submitted to the [W3C DID Specification Registries](https://www.w3.org/TR/did-spec-registries/) as a Community Group deliverable.

---

## License

All specifications in this organisation are published under the [W3C Software and Document License](https://www.w3.org/Consortium/Legal/copyright-software). Code is licensed under [Apache 2.0](LICENSE).

---

## Contact

- **GitHub Issues:** preferred for all technical and community questions
- **Chairs:** open an issue tagged `[chairs]` for governance questions
