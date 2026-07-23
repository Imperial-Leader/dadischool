# Learner Handoff Packet Specification

## Purpose

This specification defines the single canonical request and response format used between every learner-owned School repository and DadiSchool.

It applies to all learner environments regardless of learner name, subject, institution, age, or study mode.

## Core Rule

Learner-specific work remains inside the learner-owned repository.

Only the minimum context required to complete a request may be included in a handoff packet. Reusable doctrine may be proposed upstream only after personal, private, sensitive, and institution-specific information has been removed.

## Canonical Paths

Requests to DadiSchool:

```text
inbox/to-dadischool/
```

Responses from DadiSchool:

```text
inbox/from-dadischool/
```

## Packet Identifier

Each packet must use this identifier format:

```text
DSR-YYYYMMDD-NNN
```

Example:

```text
DSR-20260723-001
```

The numeric sequence resets each day within the learner repository.

## Request Filename

```text
DSR-YYYYMMDD-NNN-short-slug.md
```

Example:

```text
DSR-20260723-001-review-research-question.md
```

## Request Statuses

Use exactly one:

- `DRAFT`
- `READY`
- `IN-REVIEW`
- `BLOCKED`
- `ANSWERED`
- `CANCELLED`

## Priority Values

Use exactly one:

- `LOW`
- `NORMAL`
- `HIGH`
- `URGENT`

`URGENT` must be reserved for genuine deadline, safeguarding, privacy, access, or academic-integrity risk.

## Request Packet Contract

Every request must contain:

```markdown
# DadiSchool Request — <title>

## Packet ID

DSR-YYYYMMDD-NNN

## Status

READY

## Priority

NORMAL

## Learner Repository

owner/repository

## Requested By

Learner or learner agent display name

## Created

YYYY-MM-DD

## Deadline

YYYY-MM-DD, NONE, or UNKNOWN_REQUIRED

## Objective

One precise outcome.

## Academic Context

Course, module, subject, assessment type, or self-study context. Use UNKNOWN_REQUIRED when not supplied.

## Relevant Paths

- path/to/file

## Work Already Attempted

What has already been tried and what happened.

## Exact Help Required

The specific decision, review, explanation, doctrine, template, or technical work requested.

## Constraints

Time, format, word count, tools, marking criteria, accessibility, privacy, or other limits.

## Academic-Integrity Status

State whether the work is formative, assessed, submitted, awaiting submission, or UNKNOWN_REQUIRED. State what assistance is permitted when known.

## Sensitive-Data Status

Use one:

- NONE
- REDACTED
- PRESENT_WITH_OWNER_APPROVAL
- BLOCKED_PENDING_REDACTION

## Required Output

Exact deliverable and destination path.

## Acceptance Criteria

- measurable completion check

## Blockers

- NONE

## Owner Approval Required

YES or NO, followed by the exact action requiring approval.
```

## Issue Contract

After committing a `READY` request packet, the learner agent must open a linked issue in the learner repository.

Issue title:

```text
DADISCHOOL REQUEST: DSR-YYYYMMDD-NNN — <title>
```

Issue body must include:

- packet ID
- packet path
- objective
- priority
- deadline
- blocker status
- explicit statement that no secrets are included

The issue must not duplicate private learner material unnecessarily.

## Response Packet Contract

DadiSchool returns a response under:

```text
inbox/from-dadischool/
```

Recommended filename:

```text
DSR-YYYYMMDD-NNN-response.md
```

Every response must contain:

```markdown
# DadiSchool Response — <title>

## Packet ID

DSR-YYYYMMDD-NNN

## Response Status

COMPLETED, PARTIAL, BLOCKED, or REJECTED

## Reviewed By

Operator or agent role

## Decision

Clear result or ruling.

## Deliverables

- path, pull request, commit, doctrine, template, or explanation

## Learner Action Required

- exact next action, or NONE

## Integrity Notes

Any academic-integrity restrictions or required learner review.

## Privacy Notes

Any redaction, retention, or handling requirements.

## Acceptance Check

How the learner agent verifies the response.

## Remaining Blockers

- NONE
```

## Routing Rules

The learner agent handles ordinary study work locally.

Route to DadiSchool when work requires:

- reusable doctrine or templates
- important quality review
- complex research design
- citation or evidence verification
- technical automation or integrations
- repository tooling
- safeguarding or privacy decisions
- academic-integrity rulings
- cross-repository coordination

Technical requests may be converted into a Codex mission by DadiSchool.

## Secret and Access Rule

Packets, issues, commits, pull requests, and comments must never contain passwords, tokens, API keys, private keys, recovery codes, session cookies, authentication files, or other secrets.

Missing repository permission must be reported as `BLOCKED`. It must never be bypassed by weakening security, exposing the repository, or requesting credentials through chat.

## Privacy Rule

Before escalation, remove any information not required for the request.

Do not copy complete private notes, assessment drafts, feedback, personal identifiers, addresses, schedules, student numbers, or institutional credentials into DadiSchool.

Use file paths and concise summaries wherever possible.

## Academic-Integrity Rule

The packet must clearly distinguish:

- teaching
- explanation
- planning
- outlining
- drafting
- editing
- review
- final submission

The learner remains responsible for understanding, approving, and submitting assessed work.

DadiSchool agents must not impersonate the learner or fabricate citations, evidence, grades, feedback, research results, or completion records.

## Validation Gate

A request is valid only when:

- the packet ID and filename match
- every required field exists
- the objective is precise
- relevant paths are provided
- attempts and constraints are recorded
- integrity and sensitive-data statuses are declared
- acceptance criteria are measurable
- no secrets are present
- the linked issue references the committed packet

Invalid packets must be returned for correction rather than silently interpreted.
