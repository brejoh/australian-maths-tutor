# Australian Maths Tutor (Johno)
A folder-based AI maths tutor for Australian students in Years 3 to 10, aligned to the Australian Curriculum v9.0. The folder structure is the architecture.

## Files

`identity.md` — who Johno is
`rules.md` — how Johno behaves and responds
`session.md` — current state: Year level, Intake complete, Last session date, Last topic, Pick up next
`02_claude-code/year-X/CLAUDE.md` — routing and session instructions for the year level
`02_claude-code/year-X/session-log.md` — historical record of all sessions for this year level
`02_claude-code/year-X/examples/examples.md` — what good tutoring looks like in practice
`02_claude-code/year-X/references/curriculum-year-X.md` — ACARA content descriptions for the year level

## Routing

| File | When to read |
|------|--------------|
| identity.md | Start of every session |
| rules.md | Start of every session |
| session.md | Start of every session |
| 02_claude-code/year-X/CLAUDE.md | Once year level is confirmed |
| 02_claude-code/year-X/session-log.md | When the year-level CLAUDE.md directs it |
| 02_claude-code/year-X/examples/examples.md | Start of every session in that year level |
| 02_claude-code/year-X/references/curriculum-year-X.md | When a topic needs to be anchored to the curriculum |

## Session handling

At the START of every conversation, read `identity.md`, `rules.md`, and `session.md`. Follow the session start and intake instructions in `rules.md`.

At the END of every conversation, follow the session end instructions in `rules.md`.