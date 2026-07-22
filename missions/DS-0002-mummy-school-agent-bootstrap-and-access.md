# DS-0002 — Mummy School Agent Bootstrap and Access

## Status

READY

## Priority

HIGH

## Objective

Instruct the Mummy School learner agent to initialise its learner-owned GitHub environment, grant the approved DadiSchool team access, and connect its escalation workflow to DadiSchool without moving private learner content into the canonical hub.

## Operating Context

- Canonical hub: `Imperial-Leader/dadischool`
- Learner environment: learner-owned repository named `mummy-school`
- Repository owner: the learner
- DadiSchool operators: Director, ChatGPT, and Codex
- Governing protocol: `protocols/LEARNER-AGENT-ONBOARDING-AND-ACCESS-PROTOCOL.md`

## Preconditions

The learner must:

1. Own the GitHub account.
2. Create the `mummy-school` repository.
3. Invite the approved DadiSchool GitHub account or accounts as collaborators.
4. Confirm the repository URL and default branch.

Credentials, personal access tokens, passwords, recovery codes, and private keys must never be sent through chat or committed to GitHub.

## Mission Scope

The Mummy School learner agent must create:

```text
README.md
AGENTS.md
SCHOOL_PROFILE.md
LEARNING_GOALS.md
MISSION_BOARD.md

subjects/
assignments/
notes/
research/
essays/
feedback/
revision/
progress/
missions/
reports/
templates/
inbox/to-dadischool/
inbox/from-dadischool/
```

Because Git does not preserve empty directories, each initial directory may contain a `.gitkeep` or a concise `README.md` explaining its purpose.

## Required Agent Contract

`AGENTS.md` must state that the learner agent:

- serves the learner first
- organises and assists but does not impersonate the learner
- distinguishes teaching, outlining, drafting, review, and final submission
- never fabricates citations or evidence
- preserves substantial learner-authored work
- records meaningful changes through commits
- escalates reusable doctrine and technical requests through structured packets
- does not expose private or sensitive information
- cannot change collaborators, permissions, secrets, or repository governance without owner approval

## Access Gate

The environment is not considered connected until the DadiSchool team can:

- view the repository
- read its control files
- open or comment on issues where permitted
- contribute through commits or pull requests according to granted permissions

Do not weaken repository security merely to make agent access easier.

## Escalation Workflow

When Mummy School needs work from DadiSchool:

1. Create a packet under `inbox/to-dadischool/`.
2. Include objective, context, relevant file paths, attempts, constraints, deadline, integrity status, and acceptance criteria.
3. Open a GitHub issue in Mummy School linking the packet.
4. Label or title it clearly as `DADISCHOOL REQUEST`.
5. DadiSchool reviews the issue.
6. Technical work is converted into a Codex mission.
7. Decisions and deliverables are returned under `inbox/from-dadischool/` or through a pull request.

## First Required Output

The learner agent must produce a bootstrap report at:

```text
reports/MUMMY-SCHOOL-BOOTSTRAP-REPORT.md
```

The report must contain:

- repository full name
- owner confirmation
- default branch
- collaborator access confirmation without exposing secrets
- created file tree
- current subjects or intended learning tracks
- first three learning goals
- first active mission
- unresolved setup blockers
- confirmation that the onboarding protocol was read and applied

## Validation

Before reporting completion, verify:

- all required files exist
- all navigation links resolve
- no secrets are committed
- no fabricated learner information is inserted
- private content is not copied to DadiSchool
- `AGENTS.md` contains authority and restriction boundaries
- the handoff directories and packet format are ready
- the initial mission board contains at least one actionable learner mission

## Done When

Mummy School is learner-owned, accessible to the approved DadiSchool operators, governed by the canonical onboarding protocol, and capable of sending structured work requests to DadiSchool.

## Command for the Mummy School Agent

```text
Build the foundation of my learner-owned `mummy-school` GitHub repository according to the DadiSchool Learner Agent Onboarding and Access Protocol. Preserve my ownership, create the required control files and study directories, establish the `to-dadischool` and `from-dadischool` handoff paths, document your authority and restrictions in `AGENTS.md`, and produce `reports/MUMMY-SCHOOL-BOOTSTRAP-REPORT.md`. Do not request, reveal, or commit passwords, tokens, keys, recovery codes, or other secrets. Stop and report any missing repository permission as a blocker rather than bypassing it.
```
