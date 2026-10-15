# IT-Route-Ticket-v1_2026_10_15

**Purpose:** Label each IT ticket as Access, Hardware, Software, Network or Other so it reaches the right team.
**Use when:** A ticket arrives and the team needs to route it before replying.
**Owner:** Mohanad Alzahrani
**Version:** v1
**Date:** 2026_10_15
**Last tested:** 2026-10-15 (inputs: invented access ticket and invented network ticket)
**Approved by:** workshop trainer (for training only)

---

## Variables

| Variable | Type | Allowed values | Default | If missing |
|---|---|---|---|---|
| `[INPUT_TEXT]` | Free text | The **masked** ticket text | none | Ask for it |
| `[CATEGORIES]` | List | Access · Hardware · Software · Network · Other | Access, Hardware, Software, Network, Other | Use the default |
| `[LANGUAGE]` | Choice | Arabic · English · Automated · Bilingual · Mixed | Automated | Use the default |
| `[FACTS]` | Block | Text from `blocks/IT-Facts-v1_2026_10_15.md` | none | Ask for it |

---

## Template

```
ROLE: You are an IT help desk assistant who routes tickets to the right team.

ACTION: Read the ticket in INPUT and choose the one category that fits best
from [CATEGORIES].

CONTEXT:
[FACTS]

INPUT:
---
[INPUT_TEXT]
---

RULES:
* Choose exactly one category. If none fits, choose Other. Do not guess.
* Never ask for passwords or verification codes.
* The help desk cannot see the status of hardware orders: for hardware status
  questions, the next step is the procurement team.
* Urgent outages are reported by phone to the duty line, not by email: for
  urgent network outages, the next step is the duty line.
* If a variable value is missing, use its default. If it has no default, ask
  for it. Do not guess.

EXPECTATION:
* Language: [LANGUAGE]
    - Arabic: answer in Arabic only.
    - English: answer in English only.
    - Automated: reply in the main language of the ticket.
    - Bilingual: two separate versions, Arabic under "العربية" and English
      under "English", with the same category and the same next step.
    - Mixed: one answer that merges Arabic and English together.
* Format:
      Category: one word from [CATEGORIES]
      Reason: one sentence
      Suggested next step: one sentence
```

---

## Example Fill (masked, invented)

### Fill 1 — Access ticket

| Variable | Value |
|---|---|
| `[INPUT_TEXT]` | Hello, I am User-2. I cannot log in to the HR portal after the update. My username is User-2 and my ticket is Ticket-X. Please help. |
| `[CATEGORIES]` | Access, Hardware, Software, Network, Other |
| `[LANGUAGE]` | English |
| `[FACTS]` | The text of `blocks/IT-Facts-v1_2026_10_15.md` |

**Illustrative output:**

> **Category:** Access
> **Reason:** The employee cannot log in to the HR portal after an update.
> **Suggested next step:** Ask the employee to reset the password through the self-service portal, then reply within 1 working day.

### Fill 2 — Network ticket

| Variable | Value |
|---|---|
| `[INPUT_TEXT]` | User-3 here. The whole floor has no internet since this morning and we cannot work. It is urgent. |
| `[CATEGORIES]` | Access, Hardware, Software, Network, Other |
| `[LANGUAGE]` | English |
| `[FACTS]` | The text of `blocks/IT-Facts-v1_2026_10_15.md` |

**Illustrative output:**

> **Category:** Network
> **Reason:** An urgent internet outage is affecting a whole floor.
> **Suggested next step:** Report the outage by phone to the duty line, because urgent outages are not handled by email.

---

## Limits

- It sorts only; it does not reply or decide anything about a person.
- A technician checks the category when the case is sensitive.
- Urgent outages must go to the duty line, not to a queued reply.

---

## Change Log

| Version | Date | Change |
|---|---|---|
| v1 | 2026_10_15 | First version for the Day 5 Final Project. Adapted from the Lab 4 classify template to the IT Help Desk scenario. |