# Contributing to RecordWeb

Thank you for your interest in RecordWeb. This document explains the two ways to get involved and how specification changes actually happen.

RecordWeb is developed as a [W3C Community Group](https://www.w3.org/community/recordweb/). Everything that matters technically happens in the open, on GitHub — see [`GOVERNANCE.md`](GOVERNANCE.md) for the full decision-making model. This document is the practical "how do I actually participate" companion to it.

---

## Two ways to participate

### 1. Contributor — you help write the specification

Contributors author or review specification text, submit or review pull requests, and participate in substantive issue discussions on [`rwc`](https://github.com/recordweb/rwc) (RecordWeb Concept) or [`rwp`](https://github.com/recordweb/rwp) (RecordWeb Protocol).

**To become a Contributor:**

1. **Join the W3C Community Group** at [w3.org/community/recordweb](https://www.w3.org/community/recordweb/) with a W3C account (free, no W3C Membership required). Joining the group is also how you sign the [W3C Community Contributor License Agreement (CLA)](https://www.w3.org/community/about/agreements/cla/) — this happens automatically as part of the join flow, there is no separate GitHub CLA bot to deal with.
2. Open an issue or pull request on `rwc` or `rwp`. That alone constitutes participation as a Contributor per [`GOVERNANCE.md` §3.3](GOVERNANCE.md) — no additional registration on GitHub is required.

**Note:** only contributions that become normative specification text are CLA-governed. Prototyping, test reports, and review comments are welcome from anyone, CLA or not.

### 2. Member — your institution has a stake in RecordWeb

Members are institutions — public administrations, hospitals, regulated organisations, universities, vendors, standards bodies — with a professional interest in RecordWeb. Members provide use cases, test scenarios, and pilot feedback. They do not need to engage at the technical protocol level, and do not need the CLA unless they contribute normative text directly (see [`GOVERNANCE.md` §3.4](GOVERNANCE.md)).

**To register as a Member:**

[Open a Member Registration issue](https://github.com/recordweb/.github/issues/new?template=member-registration.md) in this repository. A Chair confirms registration within 10 working days and adds your institution to [`MEMBERS.md`](MEMBERS.md).

---

## How specification changes happen

1. Open a proposal issue on `rwc` or `rwp`, labelled `proposal`.
2. A minimum 14-day open discussion period follows (per [`GOVERNANCE.md` §4.1](GOVERNANCE.md)).
3. Substantive batches are formally opened as a **Call for Consensus (CfC)** — tracked as a dedicated issue labelled [`cfc`](https://github.com/recordweb/.github/issues?q=is%3Aissue+label%3Acfc) in this repository, cross-linked from the issues under discussion. React with 👍 on the CfC issue if you support the current text; if you object, say so in a comment with your rationale before the deadline — a reaction alone isn't enough.
4. After the deadline, the Editor (or a Chair) summarises the outcome on the CfC issue. If consensus is reached, the change is merged. If not, the Chairs decide and document their reasoning.

## Code of Conduct

All participants — Contributors and Members alike — are expected to follow the [W3C Code of Ethics and Professional Conduct](https://www.w3.org/Consortium/cepc/). See [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).

## Questions

Open an issue tagged `[governance]` for process questions, or `[chairs]` to reach the Chairs directly.
