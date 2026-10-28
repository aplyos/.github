# APLYOS Repository Governance — Idea Intake and Assignment Policy

**Version:** 1.1.0  
**Status:** Active organizational policy  
**Scope:** All repositories under the `aplyos` GitHub organization  
**Language:** English  
**Effective date:** 2026-10-28

## 1. Purpose

Prevent premature implementation, misplaced issues, duplicated documentation, and accidental changes to product roadmaps. The repository destination must be determined **before** creating or editing an issue, document, or development task.

## 2. Authoritative destinations

| Information type | Primary destination |
| --- | --- |
| New ideas, external inspirations, unapproved feature proposals, early research | `aplyos/ideapool` |
| Approved and scoped product development tasks | Relevant product repository (e.g. `hibase`, `vibase`, `installer`, `cms`, `ntp`) |
| Approved cross-product technical specifications and conventions | `aplyos/standards` |
| Organization-wide repository governance and GitHub conventions | `aplyos/.github` |
| Historical or superseded project material | Existing designated archive; do not recreate it in active product backlogs |

The product mentioned in an idea does **not** determine the destination. Until approval, the default destination is `aplyos/ideapool`.

## 3. Mandatory pre-write checks

Before any GitHub write action:

1. Identify whether the content is an **idea**, **approved implementation task**, **binding standard**, **organizational rule**, or **archive record**.
2. Inspect the existing repositories and relevant conventions rather than assuming a destination.
3. Search the intended destination for equivalent issues or documents; update or link existing material where appropriate.
4. Confirm that implementation or roadmap changes were explicitly authorized. Discussion, enthusiasm, or a request to “save this” is **not** implementation approval.
5. Preserve the original source, decision status, language preference, and relevant links.
6. Make the smallest justified change and report the exact repository and resulting URL.

When destination or authorization remains genuinely ambiguous, ask before writing. Never interpret an unapproved idea as an implementation request.

## 4. Idea lifecycle

**Captured → Reviewed → Approved or Rejected/Deferred → Scoped → Implemented**

- **Captured:** Create a concise, searchable issue in `aplyos/ideapool`. Record purpose, source, potential relevance, risks, and “not approved for implementation”.
- **Reviewed:** Check architectural fit, maintenance burden, security, dependencies, licensing, duplication, and practical value.
- **Approved:** Require an explicit decision identifying the product, scope, and priority.
- **Scoped:** Only then create a linked implementation issue in the relevant product repository. Keep the original idea as the decision record; avoid copying entire discussions.
- **Rejected/Deferred:** Retain rationale in the ideapool without polluting product backlogs.

No idea may silently become a release commitment.

## 5. External open-source references

Record the upstream project URL and, when relevant, its license and version. Distinguish between studying concepts and copying code. Do not imply license compatibility or adopt dependencies without review. Do not claim technical capabilities that have not been verified.

## 6. Wrong-repository correction

If an issue is created in the wrong repository:

1. Stop further changes to that issue.
2. Check for an existing equivalent in the correct repository.
3. Create or update the canonical record in the correct destination.
4. Close the misplaced issue with a short link to the canonical record, using an appropriate reason.
5. Report both URLs and confirm that no product roadmap was modified.

Do not silently delete history or maintain two active canonical copies.

## 7. Language and documentation discipline

Use English for this organization-wide policy. For project content, respect the established language preference of the project or the user's explicit request. Do not translate existing records without authorization. Avoid redundant documents and unnecessary architecture expansions.

## 8. Labels and assignee discipline

Before creating or updating an issue, inspect existing labels and assignment conventions in the destination repository. Prefer existing labels with established meaning; do not invent or proliferate near-duplicate labels. Apply only labels that accurately describe the issue's type, lifecycle state or domain. Do not use a priority, implementation, release or approval label to imply a decision that has not been made. If an appropriate label is unavailable, leave the issue unlabeled and propose a deliberate taxonomy change rather than silently creating a new label.

Assignees represent an actual accountable owner of the next action, not the person who suggested or captured an idea. Unapproved reference ideas should normally remain unassigned. Assign only a valid GitHub account with a known, agreed responsibility; never infer ownership from repository membership, issue authorship or a potential product consumer. If assignment is unclear, leave it empty.

Before changing labels or assignees on an existing issue, preserve unrelated metadata and verify the resulting state. Report applied labels, assignment (including none) and any unavailable convention. Do not equate an open issue with an active development task.

## 9. Chat-to-GitHub archival rule

Before declaring a chat safe to delete, verify that its durable decisions, relevant sources, unresolved items, and authoritative links are actually recorded in GitHub or another designated durable destination. A summary alone is not proof of a completed transfer. Report what was verified and what remains uncertain.

## 10. Enforcement and limitations

This document is the authoritative organizational routing policy. It guides contributors and assistants but is **not an automated enforcement mechanism**. Future sessions or tools must consult it before writing; its existence alone does not guarantee automatic compliance. Stronger enforcement requires separate technical controls or workflow validation.

## 11. Example: Cyberdrop-DL

Cyberdrop-DL is an external reference for possible download management concepts, not an approved Hibase feature.

- Canonical idea: https://github.com/aplyos/ideapool/issues/83
- Misplaced issue (closed): https://github.com/aplyos/hibase/issues/171

**Decision:** Retain the idea in the ideapool; do not add it to the Hibase roadmap without explicit approval.
