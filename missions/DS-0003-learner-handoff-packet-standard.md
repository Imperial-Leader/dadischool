# DS-0003 — Learner Handoff Packet Standard

## Status

COMPLETE

## Priority

HIGH

## Objective

Create one canonical request and response contract for communication between every learner-owned School repository and DadiSchool.

## Scope

This mission establishes:

- one packet identifier format
- one request filename convention
- one request field contract
- one linked GitHub issue contract
- one DadiSchool response contract
- shared privacy, secret, access, and academic-integrity gates
- a reusable request template

## Canonical Outputs

- `protocols/LEARNER-HANDOFF-PACKET-SPECIFICATION.md`
- `templates/LEARNER-HANDOFF-REQUEST-TEMPLATE.md`

## Operating Rule

Every learner-owned repository must use:

```text
inbox/to-dadischool/
inbox/from-dadischool/
```

Requests must use packet IDs formatted as:

```text
DSR-YYYYMMDD-NNN
```

## Acceptance Checks

- packet fields are explicit and reusable
- request and response contracts are both defined
- issue-title and issue-body requirements are defined
- privacy and redaction rules are active
- secret handling and permission blockers are explicit
- academic-integrity status is mandatory
- learner ownership remains unchanged
- technical requests can be routed into Codex missions
- a copy-ready template exists

## Result

DadiSchool now has one reusable handoff standard for current and future learner repositories.
