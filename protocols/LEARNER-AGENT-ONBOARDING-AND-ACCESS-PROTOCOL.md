# Learner Agent Onboarding and Access Protocol

## Purpose

This protocol defines how each learner creates and operates their own School repository while remaining connected to DadiSchool as the canonical learning hub.

DadiSchool owns shared doctrine, reusable templates, governance, quality standards, and infrastructure missions.

Each learner-owned School repository owns that learner's private notes, assignments, drafts, feedback, progress, and subject-specific study work.

## Core Model

```text
DadiSchool
  -> canonical doctrine, standards, templates, missions, reusable tools

Learner School
  -> learner-owned workspace, notes, assignments, drafts, progress

Learner Agent
  -> organises study work and raises structured requests

DadiSchool Team
  -> Director + ChatGPT + Codex review, design, govern, and build
```

## Ownership Rule

The learner must own their own GitHub account and repository.

The learner must remain repository owner. DadiSchool collaborators do not take ownership of learner content.

Recommended repository naming:

- `mummy-school`
- `son-school`
- `<name>-school`
- `<topic>-school` for self-directed programmes such as `dadi-culinary-school`

## Required Access

The learner must invite the agreed DadiSchool operators as collaborators.

Minimum recommended access:

- Director: Maintain or Admin
- Codex operating account: Write or Maintain
- Other agents: only through an authenticated operator account or approved GitHub integration

Do not share passwords, personal access tokens, recovery codes, SSH private keys, or agent secrets in repository files, issues, chat messages, or commits.

Access must be granted through GitHub collaborator invitations, GitHub Apps, deploy keys, or another formally approved mechanism.

## Learner Repository Foundation

The learner agent must create this minimum structure:

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
inbox/
```

## Required Control Files

### `README.md`

Explains the purpose of the School, repository ownership, relationship to DadiSchool, and navigation.

### `AGENTS.md`

Defines the learner agent's authority, restrictions, workflow, escalation rules, file locations, and academic-integrity obligations.

### `SCHOOL_PROFILE.md`

Records non-sensitive learning context:

- learner display name
- education level or self-study mode
- subjects
- preferred learning style
- accessibility needs supplied by the learner
- guardian requirements where applicable

Sensitive personal data must not be recorded unless necessary and explicitly approved.

### `LEARNING_GOALS.md`

Records current objectives, target dates, success criteria, and priorities.

### `MISSION_BOARD.md`

Tracks active, blocked, submitted, reviewed, and completed learning missions.

## Learner Agent Responsibilities

The learner agent may:

- organise notes and resources
- create study plans
- create revision questions and flashcards
- explain concepts
- produce essay outlines and supported drafts
- track deadlines and progress
- identify weak areas
- request infrastructure or doctrine improvements
- submit review packets to the DadiSchool team

The learner agent must not:

- impersonate the learner
- submit assessed work without learner review
- fabricate citations, sources, grades, feedback, or completion evidence
- expose private information
- silently overwrite substantial learner work
- change repository governance or collaborator access without explicit approval

## Escalation Path

The learner agent handles ordinary study activity locally.

Escalate to DadiSchool when the request requires:

- a new reusable study doctrine
- a new template or workflow
- difficult research design
- quality review of important work
- technical automation
- repository tooling
- dashboards, search, memory, or integrations
- safeguarding, privacy, or academic-integrity decisions

## Handoff Packet

Every escalation must create a Markdown packet under:

```text
inbox/to-dadischool/
```

Required packet fields:

```text
Title:
Learner School:
Requested by:
Date:
Priority:
Deadline:
Objective:
Context:
Files involved:
What the learner agent already tried:
Exact help required:
Constraints:
Academic-integrity status:
Sensitive-data status:
Done when:
```

The learner agent then opens a GitHub issue or pull request in the learner repository and links the packet.

DadiSchool operators review the request, convert technical work into a Codex mission where needed, and return decisions or reusable improvements.

## Improvement Flow

Learner-specific content remains in the learner repository.

A reusable improvement may be proposed to DadiSchool when it benefits multiple Schools.

Examples:

- essay planning doctrine
- language-learning workflow
- culinary practical assessment template
- revision timetable generator
- citation verification checklist

Reusable improvements must be stripped of personal information before being copied or proposed upstream.

## Minor Safeguarding

For a child learner:

- guardian retains Admin or Maintain access
- the child's agent operates under guardian-approved rules
- external communications and publishing require guardian approval
- personal identifiers, school details, addresses, schedules, and private feedback must remain protected
- agent actions must be visible and reviewable
- no autonomous purchasing, account creation, or external contact

## Initial Activation Sequence

1. Learner creates their GitHub account.
2. Learner creates their School repository.
3. Learner invites the approved DadiSchool collaborators.
4. Learner agent creates the required foundation files and directories.
5. Learner agent records the School profile and learning goals.
6. Learner agent creates the first mission board entry.
7. DadiSchool performs a foundation review.
8. The learner begins normal study operations.

## Acceptance Gate

A learner School is connected only when:

- learner ownership is confirmed
- collaborator access is confirmed
- required files exist
- agent authority and restrictions are documented
- escalation packets have a defined path
- academic-integrity rules are active
- privacy and safeguarding controls are active where applicable
- DadiSchool has completed an initial review
