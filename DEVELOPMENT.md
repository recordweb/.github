# Development Workflow

This document describes the common workflow for making changes in RecordWeb repositories, in particular `recordweb/rwc` and `recordweb/rwp`.

## Principles

- A Call for Comments (CfC) in `recordweb/.github` provides the cross-repository, governance, and discussion context.
- Issues in `recordweb/rwc` and `recordweb/rwp` define concrete work items.
- Create a separate topic branch for each independent subject area or implementation unit.
- Open one pull request (PR) per repository and topic branch.
- Keep commits small, coherent, and traceable.
- Link PRs, issues, and the relevant CfC explicitly.
- Use `Refs` for contextual references and `Resolves` only for an issue that is fully completed by the PR.

A CfC can be implemented through multiple PRs, including PRs in different repositories and PRs authored by different contributors.

## Work hierarchy

| Level | Purpose | Example |
| --- | --- | --- |
| CfC in `.github` | Governance context, discussion, decision, and cross-repository coordination | `recordweb/.github#3` |
| Issue in RWC or RWP | A concrete technical, editorial, or conceptual work item | `recordweb/rwp#42` |
| Branch | Isolated work on a defined topic | `cfc3-conformance` |
| Commit | One coherent and reviewable change | `rwp: define conformance levels` |
| Pull request | Review and merge unit for one repository | `recordweb/rwp#...` |

## 1. Identify the work item

Before starting, record the following information:

- The parent CfC, for example `recordweb/.github#<CFC-NUMBER>`.
- The implementing issue, for example `recordweb/rwc#<ISSUE-NUMBER>` or `recordweb/rwp#<ISSUE-NUMBER>`.
- The repository in which the change belongs.
- The subject area, for example `conformance`, `security`, or `merkle-integrity`.
- The responsible contributor.
- Dependencies on other issues or PRs.

Use a distinct branch and PR where work can be reviewed, merged, or assigned independently. For example, Conformance, Security, and Merkle Integrity should normally be separate streams of work.

## 2. Update the local repository

Start from the current `main` branch:

```bash
cd <repository>
git switch main
git pull --ff-only origin main
```

If necessary, fetch the remote state first:

```bash
git fetch origin
git switch main
git pull --ff-only origin main
```

## 3. Create a topic branch

Use this branch naming convention:

```text
cfc<CFC-NUMBER>-<topic>
```

Examples:

```bash
git switch -c cfc3-conformance
git switch -c cfc3-security
git switch -c cfc3-merkle-integrity
```

When a topic contains independent work items, use a more specific name:

```bash
git switch -c cfc3-conformance-levels
git switch -c cfc3-conformance-assertions
```

Create branches from the current `main` branch unless a documented dependency requires a different base branch.

## 4. Make and inspect changes

Keep the branch limited to its stated topic. Do not include unrelated clean-ups or changes that belong to another issue.

For specification and documentation changes, check in particular:

- Terminology and definitions.
- Normative language and requirement levels.
- Internal and external references.
- Examples, diagrams, and identifiers.
- Consistency between RWC and RWP where applicable.

Inspect the working tree before committing:

```bash
git status
git diff
```

## 5. Create coherent commits

A commit should represent one coherent and understandable change. A branch may contain several commits where that improves traceability and reviewability.

```bash
git add <file-or-directory>
git commit -m "rwp: define conformance levels"
```

Suggested commit-message pattern:

```text
<repository-area>: <concise imperative description>
```

Examples:

```text
rwc: clarify the conformance concept
rwp: define conformance requirements
rwp: add security considerations
rwp: specify Merkle integrity verification
docs: align terminology with CfC 3
```

References may be included in the commit body when useful:

```text
Refs: recordweb/rwp#42
Refs: recordweb/.github#3
```

Do not use issue-closing keywords in commit messages. Issue closure should be controlled in the PR description, where the complete scope is visible during review.

## 6. Publish the branch

Push the new branch and configure its upstream:

```bash
git push -u origin cfc-3-conformance
```

For later updates:

```bash
git push
```

## 7. Open a pull request

Open a PR from the topic branch to `main` in the relevant repository.

- **Base branch:** `main`
- **Compare branch:** the topic branch, for example `cfc-3-conformance`
- Use a concise, descriptive title.
- Explain the scope and boundaries of the change.
- Request the appropriate review.
- Apply repository labels where available.

Example title:

```text
RWP: Specify conformance requirements
```

Example PR description:

```markdown
## Purpose

Implements the Conformance part of [CfC #3](https://github.com/recordweb/.github/issues/3).

## Related work

Resolves recordweb/rwp#42
Refs recordweb/.github#3

## Changes

- Defines the conformance levels.
- Clarifies verifiable requirements.
- Adds examples and references.

## Scope boundary

- Security is addressed in a separate PR.
- Merkle Integrity is addressed in a separate PR by another contributor.

## Checks

- [ ] Terminology reviewed
- [ ] References reviewed
- [ ] Examples reviewed
- [ ] RWC/RWP consistency considered
```

## 8. Use `Resolves` and `Refs` deliberately

RecordWeb repositories contain specifications and governance documents rather than executable code. Therefore, use only the following keywords in PR descriptions:

- `Resolves <owner>/<repository>#<number>`: The PR completely implements and closes the referenced issue when it is merged into `main`.
- `Refs <owner>/<repository>#<number>`: The issue or CfC provides context, is related, or remains open after this PR is merged.

Examples:

```markdown
Resolves recordweb/rwp#42
Refs recordweb/.github#3
```

A CfC normally remains open while several independent issues and PRs are being processed. Therefore, reference the CfC with `Refs`, not `Resolves`.

Use `Resolves` for a concrete RWC or RWP issue only when the PR fully completes that issue. If work is partial, shared across several PRs, or depends on follow-up work, use `Refs` instead.

Do not use `Fixes`, `Closes`, or other closing keywords. This terminology is intentionally avoided because the work concerns documents, concepts, and specifications.

## 9. Maintain the CfC and issues

After opening a PR:

- Add a link to the PR from the implementing issue.
- Add the PR to the relevant topic section of the CfC.
- Make the implementation status visible: proposed, in review, merged, or superseded.
- Keep substantive questions in the CfC or the appropriate issue, rather than only in PR review comments.

Example CfC tracking section:

```markdown
### Conformance

- [ ] RWC: [PR #...](...)
- [ ] RWP: [PR #...](...)

### Security

- [ ] RWP: [PR #...](...)

### Merkle Integrity

- [ ] RWP: [PR #...](...)
```

A CfC is ready to close only when its decision has been documented and all intended work items are either merged, explicitly deferred, or otherwise resolved.

## 10. Update a branch during review

If `main` advances while the PR is open, update the topic branch as needed:

```bash
git switch main
git pull --ff-only origin main
git switch cfc-3-conformance
git merge main
```

Resolve any conflicts, review the result, and push the updated branch:

```bash
git add <resolved-files>
git commit
git push
```

Do not rewrite shared branch history without agreement. In particular, avoid force-pushing branches that other contributors use as a basis for their work.

## 11. After merge

Once the PR is merged:

```bash
git switch main
git pull --ff-only origin main
git branch -d cfc-3-conformance
git push origin --delete cfc-3-conformance
```

Then:

- Verify that the intended issue was closed when `Resolves` was used.
- Update the status and links in the CfC.
- Update dependent branches or PRs if necessary.
- Leave the CfC open until all its planned work has been completed or explicitly handled.

## Example: a multi-repository CfC

A CfC may coordinate several independent PRs:

```text
CfC #3: Conformance, Security and Merkle Integrity
|
+-- Conformance
|   +-- RWC: cfc3-conformance -> PR in recordweb/rwc
|   +-- RWP: cfc3-conformance -> PR in recordweb/rwp
|
+-- Security
|   +-- RWP: cfc3-security -> PR in recordweb/rwp
|
+-- Merkle Integrity
    +-- RWP: cfc3-merkle-integrity -> PR in recordweb/rwp
        (maintained by the responsible contributor)
```

Each PR remains focused, independently reviewable, and attributable to its relevant issue. The CfC provides the shared rationale and records the overall decision across repositories.
