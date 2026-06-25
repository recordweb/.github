# RecordWeb — GOVERNANCE.md

> Version: 0.0.1 Draft — Formation Phase  
> Status: In effect from the date of W3C Community Group charter adoption  
> Maintained by: RecordWeb Community Group Chairs

---

## 1. Purpose

This document describes the governance of the RecordWeb GitHub organisation and the RecordWeb W3C Community Group. It defines roles, decision-making processes, and the principles under which the community operates.

Governance is kept minimal in the formation phase. This document will be extended as the Community Group grows.

---

## 2. Principles

RecordWeb governance is guided by four principles:

1. **Openness.** All substantive decisions are made in public, documented in GitHub issues or pull requests. There are no closed governance channels.
2. **Consensus.** The community seeks consensus before taking decisions. Where consensus cannot be reached, the Chairs decide, with reasoning documented.
3. **Separation of roles.** Technical decisions (protocol design) and community decisions (membership, scope, process) are kept explicitly separate.
4. **Institutional inclusivity.** Public institutions, government bodies, and regulated organisations are explicitly welcomed as full participants, not merely as users of the specification.

---

## 3. Roles

### 3.1 Chairs

The Chairs are responsible for:

- Facilitating community calls and decision-making processes
- Maintaining this governance document
- Resolving disputes when consensus cannot be reached
- Representing the Community Group to the W3C and to external stakeholders

**Current Chairs:**

| Name | Affiliation | Responsibilities |
|---|---|---|
| Nik Jenzer | (Swiss) Federal Chancellery and TRIEBWERKSTATT GmbH | Founding chair, specification lead, eCH liaison |
| Melvin Carvalho | — | W3C process, `did:rwp` method spec, prototyping |

Chairs serve until they resign or until the Community Group votes to change the chair composition (simple majority of Contributors, documented in a GitHub issue).

### 3.2 Editors

Editors are responsible for the editorial quality and consistency of a specific document. They:

- Review and merge pull requests on their document
- Maintain the document's conformance with W3C Community Group Note conventions
- Propose version increments

Each repository lists its editors in the document's front matter or `README.md`.

### 3.3 Contributors

Contributors are individuals who materially participate in the development of the RecordWeb specification. Contribution includes:

- Authoring or reviewing specification text
- Submitting or reviewing pull requests
- Participating in substantive GitHub issue discussions
- Prototyping and reporting implementation results

All Contributors must agree to the [W3C Community Contributor License Agreement (CLA)](https://www.w3.org/community/about/agreements/cla/) before their contributions can be merged.

**Registration:** No formal registration required. Opening a pull request or substantive issue constitutes participation as a Contributor.

### 3.4 Members

Members are institutions with a professional interest in RecordWeb. Membership is not a legal relationship — it is a declaration of engagement. Members:

- Provide use cases, test scenarios, and domain requirements
- Participate in pilot implementations
- Review specification drafts from an institutional perspective
- Are listed in the [`MEMBERS.md`](MEMBERS.md) file of this organisation

**Registration:** Open an issue using the [Member Registration template](.github/ISSUE_TEMPLATE/member-registration.md). A Chair confirms registration within 10 working days.

Member organisations do not have voting rights on technical decisions. Their input is documented and explicitly considered in specification development.

> **Note on future legal structure:** RecordWeb anticipates forming a legal entity (association / Verein under Swiss law or equivalent) as the community grows and institutional members require formal membership structures. This legal entity will be governed by statutes developed with input from the community. This document will be updated at that time.

---

## 4. Decision-Making

### 4.1 Technical Decisions (specification content)

Technical decisions are made by the Contributors who are active on the relevant repository, under the facilitation of the Editors and Chairs.

**Process:**
1. A proposal is opened as a GitHub issue with the label `proposal`.
2. A minimum of **14 days** of open discussion follows.
3. The Editor (or Chair, if no Editor is assigned) summarises the outcome.
4. If consensus is reached: the Editor merges the change.
5. If no consensus: the Chairs decide, with reasoning documented in the issue.

### 4.2 Community Decisions (governance, scope, membership)

Community decisions (changes to this document, scope changes, chair nominations) follow the same process as technical decisions, with the discussion period extended to **21 days** for significant changes.

### 4.3 What Does Not Require a Decision

- Editorial corrections (spelling, formatting, broken links)
- Adding examples that do not change normative text
- Member registrations (Chair confirms, no vote required)

---

## 5. Versioning and Publication

RecordWeb documents follow [Semantic Versioning](https://semver.org/):

- `MAJOR`: incompatible changes to normative requirements
- `MINOR`: backward-compatible additions
- `PATCH`: corrections without substantive change

Version increments are proposed by the Editor and confirmed by the Chairs. Publication as a W3C Community Group Note requires Chair sign-off.

---

## 6. Code of Conduct

RecordWeb adopts the [W3C Code of Ethics and Professional Conduct](https://www.w3.org/Consortium/cepc/) as its community standard. All participants — Contributors and Members alike — are expected to adhere to it.

Reports of conduct issues should be sent to the Chairs directly via GitHub issue tagged `[conduct]` (visible only to Chairs).

---

## 7. Intellectual Property

All specification contributions are made under the [W3C Community Contributor License Agreement](https://www.w3.org/community/about/agreements/cla/). This ensures that the specification can be implemented royalty-free.

Software contributions (reference implementations, tooling) are licensed under [Apache 2.0](LICENSE) unless otherwise stated in the repository.

---

## 8. Amendments

This document may be amended by the Chairs following the community decision process described in Section 4.2. The change history is maintained in the Git history of this file.

---

*RecordWeb is an open community. If you have questions about this governance document, open an issue tagged `[governance]`.*
