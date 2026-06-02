# Australian Maths Tutor (Johno)

Johno is an AI maths tutor for Australian students in Years 3 to 10, built for parents who want to support their child's learning at home. All content is anchored to the Australian Curriculum v9.0. No teaching background is required to use it.

Johno is built using the [Interpretable Context Methodology](https://arxiv.org/abs/2603.16021) by Van Clief and McDermott (2026). Folders and markdown files tell Claude who it is, what it knows, and how to behave. No orchestration frameworks, no coordination code. The folders are the architecture.

## Who it is for

Parents of maths students in Years 3 to 10 who want a patient, curriculum-aligned tutor available at home. Johno works best as a complement to school, not a replacement for it. Johno is not an answer machine or shortcut for homework. Johno is a tutor that supports learning.

## What Johno does

- Explains concepts in plain language with worked examples
- Gives one practice problem at a time and coaches the student through it
- Anchors every topic to the relevant ACARA content description and code
- Adjusts explanations when a student does not understand the first time
- Tracks session progress so each conversation picks up where the last one left off (Option 2 only)

## How to use it

There are two ways to use Johno depending on your comfort with technology.

### Option 1 — Claude.ai Projects (simple)

Best for parents who want to get started quickly with no setup.

1. In this repository, open `01_claude-project/` and find your child's year level folder
2. Download all three files from that folder: `CLAUDE.md`, `curriculum-year-X.md`, and `examples-year-X.md`
3. Go to [claude.ai](https://claude.ai), create a new Project, and upload those three files to the project knowledge
4. Start a conversation — Claude will read the files and become Johno

**Session continuity:** at the end of a session, ask Johno to summarise what was covered. Copy the summary and save it somewhere. Paste it at the start of your next session to resume where you left off.

### Option 2 — Claude Code (full)

Best for parents comfortable with VS Code who want automatic session tracking and a more structured experience.

1. Clone this repository locally
2. Open the repository root folder in VS Code with the Claude Code extension installed
3. Start a conversation — Claude reads the files and becomes Johno
4. At first use, Johno will ask your child's year level and what they want to work on

**Session continuity:** Johno automatically updates `session.md` at the end of each session and resumes from the right point next time. No manual copying required.

## Folder structure

```
australian-maths-tutor/
├── README.md                        — this file
├── CLAUDE.md                        — session routing for Claude Code
├── identity.md                      — who Johno is (shared across all year levels)
├── rules.md                         — how Johno behaves (shared across all year levels)
├── session.md                       — current state: year level, intake complete, last session date, last topic, pick up next
│
├── 01_claude-project/               — Option 1: Claude.ai Projects
│   ├── year-3/
│   │   ├── CLAUDE.md                — identity, context, pedagogy, rules, session flow, and examples
│   │   ├── curriculum-year-3.md     — ACARA Year 3 content descriptions
│   │   └── examples-year-3.md       — worked examples of good sessions
│   └── ... (year-4 through year-10, same structure)
│
└── 02_claude-code/                  — Option 2: Claude Code
    ├── year-3/
    │   ├── CLAUDE.md                — year-level session flow and curriculum scope
    │   ├── session-log.md           — dated history of all sessions for this year level
    │   ├── examples/
    │   │   └── examples.md          — worked examples of good sessions
    │   └── references/
    │       └── curriculum-year-3.md — ACARA Year 3 content descriptions
    └── ... (year-4 through year-10, same structure)
```

## Pedagogy

Johno is not one tutor wearing eight name tags. Each year level pitches its teaching (language, abstraction, scaffolding, and who leads the thinking) to the age of the learner. Years are grouped into four developmental bands, aligned to how students develop and how the Australian Curriculum groups its content:

| Band | Years | Register | Representation | Lead |
|------|-------|----------|----------------|------|
| Lower primary | 3–4 | Everyday words, define every term | Concrete — count, draw, picture | Tutor leads |
| Upper primary | 5–6 | Plain words plus correct terms | Bridging concrete to symbols | Shared lead |
| Lower secondary | 7–8 | Proper maths vocabulary | Mostly symbols and algebra | Tilts to student |
| Upper secondary | 9–10 | Precise and concise | Symbolic, general forms, justification | Student leads |

Within a band, the two years share the same pedagogical pitch but differ in curriculum scope and example complexity. This is what makes a Year 3 session feel genuinely different from a Year 10 one.