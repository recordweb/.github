# [DRAFT] RecordWeb Community Group Charter

{TBD: remove next sentence before submitting for approval}  
This Charter is a work in progress. To submit feedback, please use [RecordWeb GitHub organisation Issues](https://github.com/recordweb/.github) where the Charter is being developed.

* **This Charter:** https://github.com/recordweb/.github/blob/main/CGCharter.md  
* **Previous Charter:** None  
* **Start Date:** TBD  
* **Last Modified:** 2026-07-03

## Goals

The RecordWeb Community Group develops an open, royalty-free application and profile layer for institutionally provable information on the Web.

Its purpose is to define how existing Web standards (in particular DID Core, PROV-O, Verifiable Credentials, and related technologies) can be composed into an interoperable architecture for institutional records management across public authorities, regulated organisations, and other institutional contexts.

The group aims to produce both:
- explanatory material that makes the RecordWeb model understandable and discussable across disciplines; and
- normative specifications that can be implemented by software systems and referenced by institutions in procurement, implementation, and interoperability requirements.

## Scope of Work

The scope of the group is the development of RecordWeb as an application and interoperability layer for institutional records on the Web.

In scope are:
- the conceptual model of the Record as the smallest semantically autonomous unit of institutional information;
- versioned, attributable, and cryptographically verifiable institutional records;
- the composition of existing standards such as DID Core, PROV-O, VC Data Model, JSON-LD, and related technologies into RecordWeb application profiles;
- the RecordWeb Protocol (RWP) as a normative implementation profile;
- the `did:rwp` DID method specification and related resolver/profile work;
- use cases, implementation guidance, examples, proof-of-concept work, and interoperability considerations for public authorities and institutional adopters;
- liaison with other relevant groups and standards communities where appropriate.

The group does not aim to replace or redefine the underlying W3C standards it builds on. Instead, it defines how these standards are applied together in the institutional records domain.

Key use cases include:
- public administration processes such as permits and case handling;
- inter-organisational exchange of accountable records;
- long-term traceability and proof of institutional information states;
- procurement and implementation of interoperable records-management systems.

### Out of Scope

The following topics are out of scope for the current charter:
- redefining the core data models or normative requirements of underlying W3C standards such as DID Core, PROV-O, or VC Data Model;
- creating a general-purpose records management standard outside the RecordWeb application/profile context;
- defining proprietary or royalty-bearing technologies;
- private or non-public governance processes for technical decision-making.

## Deliverables

### Specifications

The group expects to produce the following Specification deliverables:

1. **RecordWeb Protocol (RWP)**  
   A normative implementation profile describing how RecordWeb applies existing Web standards to create, manage, version, link, and verify institutional records in an interoperable and royalty-free manner.

2. **`did:rwp` DID Method Specification**  
   A DID method specification for RecordWeb identifiers, including method-specific resolution and interoperability considerations, with the intent of eventual submission to the W3C DID Specification Registries.

Additional specification deliverables may be added by charter update if the group later identifies a clear need for further normative profiles or companion specifications.

### Non-Normative Reports

The group may produce other Community Group Reports within the scope of this charter that are not Specifications, such as use cases, requirements, or white papers.

### Test Suites and Other Software

The group may produce test suites, schemas, examples, prototypes, and other software artifacts to support the specifications. See the relevant GitHub repository `LICENSE` file for software contribution licensing information.

The group **may** produce test suites to support the specifications. See the GitHub `LICENSE` file for test suite contribution licensing information.

## Dependencies or Liaisons

The group expects to coordinate, where appropriate, with:
- W3C Credentials Community Group;
- W3C DID-related communities and the DID Specification Registries process;
- Solid community work;
- relevant archival, records-management, and public-sector interoperability communities, including eCH and related initiatives.

The group depends conceptually on existing standards including DID Core, PROV-O, Verifiable Credentials, JSON-LD, and related Web architecture components.

## Community and Business Group Process

The group operates under the [Community and Business Group Process](https://www.w3.org/community/about/process). Terms in this Charter that conflict with those of the Community and Business Group Process are void.

As with other Community Groups, W3C seeks organizational licensing commitments under the [W3C Community Contributor License Agreement (CLA)](https://www.w3.org/community/about/process/cla/). When people request to participate without representing their organization’s legal interests, W3C will in general approve those requests, with the following understanding: W3C will seek and expect an organizational commitment under the CLA starting with the individual's first request to make a contribution to a group [Deliverable](#deliverable). The section on [Contribution Mechanics](#contrib) describes how W3C expects to monitor these contribution requests.

The [W3C Code of Conduct](https://www.w3.org/policies/code-of-conduct/) and [W3C Antitrust and competition policy] https://www.w3.org/policies/antitrust-2024/) apply to participation in this group.

## Work Limited to Charter Scope

The group will not publish specifications on topics other than those listed under [Specifications](#specifications). See below for [how to modify the charter](charter_change).

## Contribution Mechanics

Substantive contributions to specifications can only be made by Community Group Participants who have agreed to the [W3C Community Contributor License Agreement (CLA)](https://www.w3.org/community/about/process/cla/).

Reports other than Specifications published by this group should use the [W3C Software and Document License](https://www.w3.org/copyright/software-license-2023/) where possible.

Community Group participants agree to make all contributions in the GitHub repository the group is using for the particular document — e.g., via pull requests, issues, or comments on existing issues. 

All GitHub repositories attached to the Community Group must contain a copy of the [CONTRIBUTING](https://github.com/w3c/licenses/blob/main/CG-CONTRIBUTING.md) and [LICENSE](https://github.com/w3c/licenses/blob/main/CG-LICENSE.md) files.

## Transparency

The group will conduct all technical work in public. Technical discussions, issue tracking, pull requests, and editorial work will occur in public GitHub repositories (and not privately on mailing lists).

Meetings may be restricted to Community Group participants, but a public summary or minutes must be posted as an issue on GitHub.

## Decision Process

The group seeks to make decisions by consensus.

The detailed decision-making model, role definitions, and governance practices are described in the RecordWeb [`GOVERNANCE.md`](https://github.com/recordweb/.github/blob/main/GOVERNANCE.md) document. In summary:
- technical decisions are discussed publicly in GitHub issues and pull requests;
- editors and chairs summarise outcomes;
- where consensus cannot be reached, the Chairs may decide with reasoning documented in public;
- governance and scope changes follow an extended public discussion period.

Any decisions reached at meetings are tentative until publicly recorded. Any group participant may object within 7 days of publication of a decision, provided that they include clear technical or procedural reasons for the objection.

## Chair Selection

Participants in this group choose their Chair(s) and can replace their Chair(s) at any time using whatever means they prefer. However, if 5 participants, no two from the same organization, call for an election, the group must use the following process to replace any current Chair(s) with a new Chair, consulting the Community Development Lead on election operations (e.g., voting infrastructure and using [RFC 3797](https://datatracker.ietf.org/doc/html/rfc3797)).

Participants dissatisfied with the outcome of an election may ask the Community Development Lead to intervene. The Community Development Lead, after evaluating the election, may take any action including no action.

## Amendments to This Charter

The group can decide to work on a proposed amended charter, editing the text using the [Decision Process](#decision) described above. The decision on whether to adopt the amended charter is made by conducting a 30-day vote on the proposed new charter. The new charter, if approved, takes effect on either the proposed date in the charter itself, or 7 days after the result of the election is announced, whichever is later. A new charter must receive 2/3 of the votes cast in the approval vote to pass. The group may make simple corrections to the charter such as deliverable dates by the simpler group decision process rather than this charter amendment process. The group will use the amendment process for any substantive changes to the goals, scope, deliverables, decision process or rules for amending the charter.
