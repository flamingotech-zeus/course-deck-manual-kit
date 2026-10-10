# Course Deck and Instructor Manual Kit

[English](README.md) | [简体中文](README.zh-CN.md)

> Batch-produce Chinese course decks with speaker notes and minute markers, plus matching instructor manuals.

## What this is

> **Note on de-identification.** This README is written generically. The skill file itself may still reference internal domains, host names or local absolute paths. Run a scan pass (see `opensource-preflight-audit`) and replace them before publishing.

This is not a slide template. The requirement it is built around is a practical one that templates do not address: the deck has to fill the allotted session time.

That means every page carries a time allocation and the speaker notes explain what to say, so a session can be checked against its duration before anyone stands up.

## Why we open-sourced it

We run training sessions and produce courses in batches. The recurring failure was a deck that looked complete and ran out of material twenty minutes early.

Attaching time to each page turned that into something checkable. It is a production workflow with generic structure and no business content.

## What it does

- **Minute markers per page.** Each page states its expected duration, so the total can be reconciled against the session length before delivery.
- **Speaker notes.** The deck carries what to say, not just what to show, so it can be handed to a different instructor.
- **A matching instructor manual.** The Word companion expands the notes into something readable away from the screen.
- **Batch production.** A course of N sessions is generated as a set, so formatting and structure stay consistent across the whole course instead of drifting session by session.

## Requirements

Python 3 · python-pptx · python-docx

## Installation

```bash
git clone https://github.com/<your-username>/course-deck-manual-kit.git
```

Then place the folder into your agent skills directory:

| OS | Path |
|---|---|
| Windows | `C:\Users\<you>\.workbuddy\skills\course-deck-manual-kit\` |
| macOS / Linux | `~/.workbuddy/skills/course-deck-manual-kit/` |

There is no build step. Restart the session and it takes effect.

## How to use

Describe the course:

- "Ten sessions, sixty minutes each"
- "Every lesson needs its own deck and manual"
- "Generate the whole course at once"

The skill produces a deck per session plus the matching manual, with times reconciled.

## Files

```
└── SKILL.md
```

## Notes and limits

1. **Minute markers are estimates.** They are a planning aid that makes overrun visible early; they are not a timing guarantee.
2. **Speaker notes need a human pass.** Notes written for completeness read differently from notes written for speaking.
3. **Course content is an input, not an output.** The tool structures and formats; the substance comes from the material you supply.
4. **The example course is a placeholder** and should be replaced.

## License

MIT
