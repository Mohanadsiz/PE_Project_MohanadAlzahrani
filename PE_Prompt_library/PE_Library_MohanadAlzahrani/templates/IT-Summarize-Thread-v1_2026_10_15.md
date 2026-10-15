# IT-Summarize-Thread-v1_2026_10_15

**Purpose:** Summarize a long ticket thread in three lines for the next technician, using only the Help Desk Facts.
**Use when:** A ticket thread has grown long or mixed, and the next technician needs a short, clear brief before replying.
**Owner:** Mohanad Alzahrani
**Version:** v1
**Date:** 2026_10_15
**Last tested:** 2026-10-15 (input: invented long ticket thread about a laptop request)
**Approved by:** workshop trainer (for training only)

---

## Variables

| Variable | Type | Allowed values | Default | If missing |
|---|---|---|---|---|
| `[INPUT_TEXT]` | Free text | The **masked** ticket thread | none | Ask for it |
| `[LANGUAGE]` | Choice | Arabic · English · Automated · Bilingual · Mixed | Automated | Use the default |
| `[MAX_WORDS]` | Number | 30 to 150 | 80 | Use the default |
| `[FOCUS]` | Choice (optional) | Access · Hardware · Software · Network · None | None | Use the default |
| `[FACTS]` | Block | Text from `blocks/IT-Facts-v1_2026_10_15.md` | none | Ask for it |

---

## Template

```
ROLE: You are an IT help desk assistant who summarizes ticket threads for the
next technician.

ACTION: Summarize the thread in INPUT. First find the main request, then any
deadline or reference code, then write the summary.

CONTEXT:
[FACTS]

INPUT:
---
[INPUT_TEXT]
---

RULES:
* Use only the thread and CONTEXT.
* Do not add facts.
* Keep codes such as User-1, Ticket-X or Device-1 exactly as written.
* If something is unclear, say what is unclear instead of guessing.
* If the thread has several requests, list them in order.
* If [FOCUS] is not None, put that point first.
* If a variable value is missing, use its default. If it has no default, ask
  for it. Do not guess.

EXPECTATION:
* Language: [LANGUAGE]
    - Arabic: answer in Arabic only.
    - English: answer in English only.
    - Automated: reply in the main language of the thread.
    - Bilingual: two separate versions, Arabic under "العربية" and English
      under "English", with the same facts.
    - Mixed: one summary that merges Arabic and English together.
* Maximum [MAX_WORDS] words (for each version if Bilingual).
* Format:
      Main request: one sentence
      Key details: up to three bullet points
      Suggested next step for the technician: one sentence
```

---

## Example Fill (masked, invented)

| Variable | Value |
|---|---|
| `[INPUT_TEXT]` | Ticket-X thread: User-1 opened the ticket on Sunday saying their laptop is too slow to work. User-2 replied on Monday asking for the laptop model and serial number; User-1 sent them (Device-1). On Tuesday User-1 added that they also need a new laptop approved by their manager, and asked how long a replacement would take. User-2 asked the manager to confirm approval; the manager replied yes on Wednesday. The thread is now 7 messages long and the next technician starts today. |
| `[LANGUAGE]` | English |
| `[MAX_WORDS]` | 60 |
| `[FOCUS]` | Hardware |
| `[FACTS]` | The text of `blocks/IT-Facts-v1_2026_10_15.md` |

**Illustrative summary (written by hand to show the expected shape):**

> **Main request:** User-1 needs a new laptop (Device-1) after reporting the current one is too slow; manager approval has been given.
> **Key details:**
> - User-1 first reported slowness on Sunday; ticket is Ticket-X.
> - Laptop model and serial number were provided.
> - Manager approval for a replacement was confirmed on Wednesday.
> **Suggested next step for the technician:** Route the approved request to the procurement team, because the help desk cannot see the status of hardware orders.

---

## Limits

- Summarizes only what the thread says; does not check facts.
- A technician reads the original thread when the case is sensitive.
- The help desk cannot see the status of hardware orders; the summary must say so and refer to the procurement team.

---

## Change Log

| Version | Date | Change |
|---|---|---|
| v1 | 2026_10_15 | First version for the Day 5 Final Project. Adapted from the Lab 4 summarize template to the IT Help Desk scenario. |