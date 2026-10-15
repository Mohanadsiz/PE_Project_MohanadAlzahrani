# Library Guide

**Library:** Internal IT Help Desk — Prompt Library
**Owner:** Mohanad Alzahrani
**Version:** v1
**Date:** 2026_10_15

---

## What This Library Is

A small, tested set of prompt templates for the Internal IT Help Desk.
Each template turns one recurring task into a reliable draft that a duty
technician reviews before it is sent. The library follows the RACE method
(Role · Action · Context · Expectation) and the rules from Days 1 to 4.

Five approved templates live in `templates/`:

1. `IT-Reply-Ticket` — draft a polite reply to a ticket.
2. `IT-Summarize-Thread` — summarize a long ticket thread.
3. `IT-Route-Ticket` — label a ticket by category.
4. `IT-Notice-Maintenance` — write a planned-maintenance notice.
5. `IT-Steps-Fix` — turn a known fix into numbered steps.

The shared facts are in `blocks/IT-Facts-v1_2026_10_15.md`.
The rules are in `rules/IT-Rules-v1_2026_10_15.md`.

---

## How to Use the Library (in 5 steps)

1. **Pick** the right template from `library_index.md`.
2. **Copy** the template text into your AI assistant. Paste the IT Facts
   into `[FACTS]` or attach the block file.
3. **Fill** every `[VARIABLE]`. Mask personal data first: use codes such as
   `User-1`, `Ticket-X` or `Device-1`. Never type a real name, email,
   device code or phone number.
4. **Run** the prompt once and read the reply against the IT Help Desk
   Facts.
5. **Review**: the duty technician checks the reply, deletes any unsupported
   statement, and approves it before it is sent.

---

## How to Fill the Variables

| Variable | What to type | Example |
|---|---|---|
| `[INPUT_TEXT]` | The masked ticket, thread or issue | A ticket about a forgotten password |
| `[LANGUAGE]` | Arabic · English · Automated · Bilingual · Mixed | `English` or `Arabic` |
| `[TONE]` | Formal · Friendly · Calm · Neutral | `Friendly` |
| `[MAX_WORDS]` | A number in the allowed range | `60` |
| `[FOCUS]` | Only for `IT-Summarize-Thread` | `Hardware` |
| `[CATEGORIES]` | Only for `IT-Route-Ticket` | `Access, Hardware, Software, Network, Other` |
| `[FACTS]` | The IT Help Desk Facts block | The text of `blocks/IT-Facts-v1_2026_10_15.md` |

If a value is missing, the template uses its default. If a variable has no
default, the template asks for it — do not guess.

---

## How to Check an Output

Before sending, score the reply on the five-point verification checklist:

| Check | Pass means |
|---|---|
| Facts supported and current | Every fact is in the IT Facts block |
| Numbers, dates, names exact | They match the source exactly |
| No promises or actions | No promised date and no "I did this" |
| No sensitive data repeated | Only codes such as `User-1`; nothing personal |
| Complete and natural | Every question answered; a native reader approves |

A reply is ready only when it scores 5 out of 5. If a score is not full,
fix the template once and run again — or record the reason and move on.

---

## Who Owns What

| File | Owner | What the owner does |
|---|---|---|
| `blocks/IT-Facts-v1_2026_10_15.md` | Mohanad Alzahrani | Keeps the facts current (version, date, change log) |
| `rules/IT-Rules-v1_2026_10_15.md` | Mohanad Alzahrani | Reviews and updates the five rules |
| Each template file | Mohanad Alzahrani | Updates the template, tests it, and records the change |
| Every sent reply | The duty technician | Approves the reply before it is sent |

---

## Limits

- The help desk never asks for passwords or verification codes.
- The help desk cannot see the status of hardware orders — refer the employee
  to the procurement team.
- Urgent outages are reported by phone to the duty line, not by email.
- A person always reviews before anything is sent.

---

## Change Log

| Version | Date | Change |
|---|---|---|
| v1 | 2026_10_15 | First version of the IT Help Desk library guide. |