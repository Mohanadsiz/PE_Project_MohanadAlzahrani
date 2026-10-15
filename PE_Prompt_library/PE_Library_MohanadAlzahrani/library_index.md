# Library Index

**Library:** Internal IT Help Desk — Prompt Library
**Owner:** Mohanad Alzahrani
**Version:** v1
**Date:** 2026_10_15
**Status:** Ready to demo

---

## Templates

| Template | Task | Variables | Version | Status |
|---|---|---|---|---|
| [IT-Reply-Ticket](templates/IT-Reply-Ticket-v1_2026_10_15.md) | Reply to an employee's IT support ticket | `[INPUT_TEXT]` `[LANGUAGE]` `[TONE]` `[MAX_WORDS]` `[FACTS]` | v1 | Approved |
| [IT-Summarize-Thread](templates/IT-Summarize-Thread-v1_2026_10_15.md) | Summarize a long ticket thread for the next technician | `[INPUT_TEXT]` `[LANGUAGE]` `[MAX_WORDS]` `[FOCUS]` `[FACTS]` | v1 | Approved |
| [IT-Route-Ticket](templates/IT-Route-Ticket-v1_2026_10_15.md) | Label a ticket as Access, Hardware, Software, Network or Other | `[INPUT_TEXT]` `[CATEGORIES]` `[LANGUAGE]` `[FACTS]` | v1 | Approved |
| [IT-Notice-Maintenance](templates/IT-Notice-Maintenance-v1_2026_10_15.md) | Write a planned-maintenance notice with date, time and actions | `[INPUT_TEXT]` `[LANGUAGE]` `[TONE]` `[MAX_WORDS]` `[FACTS]` | v1 | Approved |
| [IT-Steps-Fix](templates/IT-Steps-Fix-v1_2026_10_15.md) | Turn a known fix into short numbered steps for the employee | `[INPUT_TEXT]` `[LANGUAGE]` `[TONE]` `[MAX_WORDS]` `[FACTS]` | v1 | Approved |

---

## Shared Blocks

| Block | Used by | File |
|---|---|---|
| IT Help Desk Facts | All 5 templates | `blocks/IT-Facts-v1_2026_10_15.md` |

---

## Rules

| File | What it is |
|---|---|
| `rules/IT-Rules-v1_2026_10_15.md` | Five responsible-use rules for the IT Help Desk (Data, Verification, Fairness, Policy, Human decision) |

---

## `[LANGUAGE]` Values (same in every template)

| Value | Meaning |
|---|---|
| Arabic | Answer in Arabic only |
| English | Answer in English only |
| Automated (default) | Reply in the main language of the input |
| Bilingual | Two separate versions: Arabic, then English |
| Mixed | One reply that merges Arabic and English |

---

## The Daily Habit: Pick, Fill, Run, Review, Verify

1. **Pick** the right template from the index.
2. **Fill** every `[VARIABLE]`. **Mask first**: use codes such as `User-1`, `Ticket-X`, `Device-1`. Never type real names, device codes, emails or phone numbers.
3. **Run** it and check the output against the quality checklist.
4. **Review**: a duty technician approves before anything is sent. Report problems to the template owner.
5. **Verify**: read the reply against the IT Help Desk Facts. Delete any unsupported statement before sending.

---

## Library Rules (Summary)

- One owner per template, and a second person tests it.
- Version every change. Move old versions to `_archive`; do not delete them.
- Save templates as text files (.md or .txt).
- No real data inside the library, including examples.
- A person reviews every output before it is sent.

---

## Change Log

| Date | Change |
|---|---|
| 2026_10_15 | First version of the IT Help Desk library: 5 approved templates, IT Facts block v1, IT Rules v1. |