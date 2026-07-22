# DS-0001 — Family Learning Operating System Foundation

## Status

READY FOR CODEX

## Priority

HIGH

## Objective

Turn DadiSchool into the canonical learning operating system used by multiple independent learner repositories.

The first learner repos will include Mummy School, a school environment for the Director's 12-year-old son, and personal self-school programmes such as culinary arts and language learning.

## Architectural rule

DadiSchool is the shared headquarters. It must contain reusable doctrine, standards, templates, schemas, mission protocols, and tooling.

Learner repositories must contain personal notes, assignments, essays, coursework, revision records, feedback, and learner-specific progress.

Do not centralise private learner content inside DadiSchool.

## Required repository structure

Create and document the following structure:

```text
/
├── README.md
├── MISSION_BOARD.md
├── docs/
│   ├── ARCHITECTURE.md
│   ├── REPOSITORY-BOUNDARIES.md
│   ├── AGENT-ROLES.md
│   └── LEARNER-REPO-STANDARD.md
├── operational_instinct/
│   ├── study_instinct/
│   ├── essay_instinct/
│   ├── research_instinct/
│   ├── revision_instinct/
│   ├── exam_instinct/
│   ├── citation_instinct/
│   ├── memory_instinct/
│   ├── safeguarding_instinct/
│   ├── academic_integrity_instinct/
│   └── handoff_instinct/
├── templates/
│   ├── learner-repository/
│   ├── course/
│   ├── lesson/
│   ├── study-note/
│   ├── essay/
│   ├── flashcards/
│   ├── revision-plan/
│   ├── assessment/
│   └── agent-handoff/
├── schemas/
├── utilities/
├── missions/
└── reports/
```

## Learner repository standard

Create a reusable learner-repository template with at least:

```text
PROFILE.md
LEARNING_GOALS.md
CURRICULUM.md
STUDY_BOARD.md
AGENT_INSTRUCTIONS.md

subjects/
assignments/
notes/
essays/
research/
revision/
assessments/
feedback/
progress/
missions/
reports/
```

The standard must support both:

1. Formal education, including school, college, and university work.
2. Self-school programmes, including culinary arts, language learning, professional skills, and hobbies.

## Agent collaboration protocol

Design a GitHub-native handoff protocol allowing learner agents to request support from the DadiSchool headquarters.

Minimum lifecycle:

```text
DISCOVERY
→ LEARNER WORK
→ SUPPORT REQUEST
→ DADISCHOOL TRIAGE
→ CODEX MISSION WHEN ENGINEERING IS REQUIRED
→ DIRECTOR REVIEW
→ RESPONSE OR REUSABLE DOCTRINE UPGRADE
```

Support requests must distinguish between:

- study guidance
- research assistance
- essay planning
- feedback and marking
- infrastructure request
- automation request
- doctrine improvement
- safeguarding escalation

Define a machine-readable front matter schema for requests and reports.

## Age adaptation and safeguarding

The system must distinguish adult learners from minors.

For minors:

- require age-band configuration
- avoid collecting unnecessary personal data
- establish parent or guardian governance
- preserve learner authorship
- prevent agents from impersonating the learner or completing assessed work deceptively
- define escalation rules for sensitive or unsafe content
- make instructions developmentally appropriate

Do not build surveillance mechanics.

## Academic integrity

Create doctrine that separates:

- teaching
- explaining
- brainstorming
- outlining
- formative feedback
- proofreading
- citation support
- model answers clearly labelled for study
- prohibited deceptive submission of agent-written assessed work

The system should help the learner produce better work without replacing the learner's thinking.

## Personal curriculum support

The learner template must support modular curricula. Initial example tracks:

- Culinary Arts: steak fundamentals, heat control, seasoning, sauces, food safety, plating, and reflective practice.
- Language Learning: pronunciation, vocabulary, grammar, listening, speaking, reading, writing, spaced repetition, and cultural context.
- Age-appropriate school subjects for a 12-year-old, configured only after the learner's actual curriculum and needs are supplied.

Do not hard-code a specific school curriculum without Director-provided requirements.

## Technical foundation

Implement only lightweight, repository-first foundations in this mission.

Required:

- Markdown-first content
- YAML front matter schemas
- validation script for required learner-repo files and front matter
- issue templates for learner support requests
- pull-request template for reusable doctrine contributions
- CODEOWNERS or documented review ownership where supported
- clear setup guide for creating a new learner repo from the template

Do not add databases, embeddings, dashboards, or external services until the content model and doctrine are approved.

## Deliverables

1. Canonical architecture documents.
2. Learner repository template.
3. Initial empty doctrine index with purpose statements and extension rules.
4. GitHub issue and PR templates.
5. Validation utility and usage documentation.
6. Example configuration for:
   - adult formal learner
   - minor learner under guardian governance
   - self-school culinary course
   - self-school language course
7. Completion report in `reports/`.
8. Updated `MISSION_BOARD.md`.

## Acceptance criteria

- A new learner repo can be created from the template without guessing its folder structure.
- Personal learner content remains outside DadiSchool.
- Adult, minor, formal, and self-school modes are represented.
- Agent handoffs have a documented lifecycle and machine-readable format.
- Academic integrity and safeguarding boundaries are explicit.
- Validation catches missing required files and malformed front matter.
- No unnecessary application stack is introduced.
- Documentation explains exactly when Codex should and should not be involved.

## Codex operating constraint

Codex builds the rails, validators, templates, and automation. Codex does not act as the learner and does not author final assessed submissions on the learner's behalf.

## Director command

Catch DS-0001 in `Imperial-Leader/dadischool` and build the family learning operating system foundation exactly to mission scope.
