# PE Prompt Library — Internal IT Help Desk

A clean, approved prompt library built for the Internal IT Help Desk, as part of the Day 5 Final Project of the Prompt Engineering & Responsible AI Use training program.

---

## Project Details

| Field | Value |
|---|---|
| **Path** | B (Guided) |
| **Scenario** | B2 — Internal IT Help Desk for Employees |
| **Prefix** | `IT-` |
| **Author** | Mohanad Alzahrani |
| **Date** | 2026_10_15 |
| **Library folder** | [`PE_Library_MohanadAlzahrani/`](PE_Library_MohanadAlzahrani/) |

---

## The 10 Tasks (B2 — Internal IT Help Desk)

Only 5 tasks were built into approved templates (marked ✅). The other 5 remain available for future work.

| # | Task | Goal | Status |
|---|---|---|---|
| 1 | Resolve a support ticket | Write a clear reply to an employee's support ticket using only the Help Desk Facts. | ✅ **Built** |
| 2 | Shorten a ticket thread | Summarize a long ticket thread in three lines for the next technician. | ✅ **Built** |
| 3 | Route tickets to teams | Label each ticket as Access, Hardware, Software, Network or Other. | ✅ **Built** |
| 4 | Explain it simply | Rewrite a technical answer in plain language for a non-technical employee. | ⬜ |
| 5 | Bilingual status message | Translate an approved service status message between Arabic and English without changing any time or fact. | ⬜ |
| 6 | Planned maintenance notice | Write a short notice about planned maintenance with the date, time and what to do. | ✅ **Built** |
| 7 | Fix-it steps | Turn a known fix into short numbered steps an employee can follow alone. | ✅ **Built** |
| 8 | Clean a ticket before pasting | Replace names, usernames, emails and device codes in a ticket with codes before it goes to an AI tool. | ⬜ |
| 9 | Self-help cheat sheet | Turn five common problems and their fixes into a short self-help list. | ⬜ |
| 10 | Senior technician handoff | Write a short note for the senior technician when a ticket needs a person's decision. | ⬜ |

**Built (5 of 10):** Tasks 1, 2, 3, 6, 7.

---

## The Library

The library folder [`PE_Library_MohanadAlzahrani/`](PE_Library_MohanadAlzahrani/) contains:

| Item | What it is |
|---|---|
| `library_index.md` | The table of the 5 approved templates, the shared facts block, the rules, the 5 `[LANGUAGE]` values and the change log. |
| `library_guide.md` | How to use the library: what is inside, how to fill the variables, how to check an output, and who owns each file. |
| `Test_Results_Report.pdf` | The three-test quality report: summary page + one page per template, with one screenshot per approved template. |
| `blocks/IT-Facts-v1_2026_10_15.md` | The 7 invented facts that a template may use. |
| `templates/` | The 5 approved templates (one text file each). |
| `rules/IT-Rules-v1_2026_10_15.md` | The 5 responsible-use rules (Data, Verification, Fairness, Policy, Human decision). |
| `_archive/` | Older versions kept for history. |

### The 5 approved templates

| # | File | Task |
|---|---|---|
| 1 | `templates/IT-Reply-Ticket-v1_2026_10_15.md` | Reply to a support ticket |
| 2 | `templates/IT-Summarize-Thread-v1_2026_10_15.md` | Summarize a ticket thread |
| 3 | `templates/IT-Route-Ticket-v1_2026_10_15.md` | Route tickets to teams |
| 4 | `templates/IT-Notice-Maintenance-v1_2026_10_15.md` | Planned-maintenance notice |
| 5 | `templates/IT-Steps-Fix-v1_2026_10_15.md` | Fix-it steps |

Each template scored **5/5 (Prompt), 6/6 (Template) and 5/5 (Output)** in the three-test quality report.

---

## How the Library Works

1. **Pick** the right template from `library_index.md`.
2. **Fill** every `[VARIABLE]`. Mask personal data first using codes such as `User-1`, `Ticket-X` or `Device-1`.
3. **Run** the template in any approved AI assistant.
4. **Review**: a duty technician approves the reply before it is sent.
5. **Verify**: read the reply against the IT Help Desk Facts, and delete any unsupported statement.

The method follows Days 1 to 4 of the training: RACE prompts, reusable templates with variables, verification, and responsible-use rules. A person always reviews every output before it is used.

---

## Files and Naming

All template files follow the pattern `PREFIX-Task-Object-vN_yyyy_mm_dd.md`:

| Item | Pattern | Example |
|---|---|---|
| Template | `PREFIX-Task-Object-vN_date.md` | `IT-Reply-Ticket-v1_2026_10_15.md` |
| Facts block | `PREFIX-Facts-vN_date.md` | `IT-Facts-v1_2026_10_15.md` |
| Rules file | `PREFIX-Rules-vN_date.md` | `IT-Rules-v1_2026_10_15.md` |
| Library folder | `PE_Library_YourName` | `PE_Library_MohanadAlzahrani` |
| Test report | `Test_Results_Report.pdf` | `Test_Results_Report.pdf` |

---

## Training Program

This project was completed as part of the Prompt Engineering and Responsible AI Use training program at SDAIA Academy, under the supervision of Abdullah Khalid AlShahrani.

The project demonstrates the practical application of prompt engineering and responsible AI use — building a clean, approved prompt library through structured RACE prompts, reusable templates with variables and fixed output formats, safe handling of sensitive data, verification and responsible-use rules, and a documented three-test quality report.

Official SDAIA Academy GitHub: https://github.com/SDAIAAcademy