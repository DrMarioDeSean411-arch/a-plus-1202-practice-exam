# CompTIA A+ 1202 — Full Practice Exam & Study Platform
## Operating Systems · Security · Software Troubleshooting · Operational Procedures · Networking

> **250 practice questions, a five-domain study guide, 9 original diagrams, and 10 interactive tools — all in one self-contained HTML file.**
> **No login. No tracking. No installation. Runs entirely in your browser.**

---

### Live Tool

**[https://DrMarioDeSean411-arch.github.io/a-plus-1202-practice-exam/a_plus_1202_full_exam.html](https://DrMarioDeSean411-arch.github.io/a-plus-1202-practice-exam/a_plus_1202_full_exam.html)**

The tool has four modes, switchable at the top of the page: Practice Questions, Domain Study Guide, Visual Reference, and Interactive Foundations.

---

## What Is This?

This is a practice platform for the CompTIA A+ Core 2 (220-1202) certification exam. A+ 1202 covers operating system installation and configuration, security implementation, software troubleshooting, operational procedures, and networking fundamentals — the "software side" of the A+ certification, paired with the hardware-focused 1201 exam.

Nothing here is copied from CompTIA's proprietary exam bank. Every question was written from scratch against CompTIA's published exam objectives, general IT reference material, and common real-world support scenarios.

---

## Mode 1: Practice Questions

250 multiple-choice questions, 50 per domain, auto-graded with instant feedback.

| Domain | Weight on real exam | Questions here | Foundational | Intermediate | Advanced |
|---|---|---|---|---|---|
| 1.0 Operating Systems | 27% | 50 | 17 | 19 | 14 |
| 2.0 Security | 27% | 50 | 17 | 19 | 14 |
| 3.0 Software Troubleshooting | 19% | 50 | 17 | 19 | 14 |
| 4.0 Operational Procedures | 15% | 50 | 17 | 19 | 14 |
| 5.0 Networking | 12% | 50 | 17 | 19 | 14 |
| **Total** | **100%** | **250** | **85** | **95** | **70** |

Each question includes:
- A clear explanation of the correct answer
- A specific misconception note naming the actual reasoning error behind common wrong answers (not a generic "students get confused here")

Click any domain button to jump between question sets. Answered questions turn green (correct) or red (incorrect) in the tab row, and the breakdown panel at the bottom shows your score by domain and by difficulty level.

**Scoring guide:**

| Score | What it means |
|-------|---------------|
| 90–100% | Exam ready |
| 75–89% | Close — review weak domains |
| Below 75% | More preparation needed before scheduling the assessment |

CompTIA does not publish an exact numeric passing score conversion for 1202 (it uses a scaled score out of 900, with 700 as passing), so 75% raw accuracy here is a reasonable, conservative internal benchmark — not an official CompTIA figure.

---

## Mode 2: Domain Study Guide

Expandable reference cards for every sub-objective tested, organized by domain. Each entry is written in plain language but doesn't oversimplify — encryption, access control models, and networking concepts are explained with the actual terminology you'll need, not hand-wavy analogies. Use this mode to review a domain before or after working through its practice questions.

---

## Mode 3: Visual Reference

Nine original diagrams, built as inline SVG (no external image files, so they render identically everywhere and add no load time):

- Windows boot sequence, with Secure Boot and recovery entry points marked
- Windows / macOS / Linux directory structure, side by side
- User account architecture and NTFS-style permission inheritance
- Encryption at rest vs. in transit vs. in use
- PKI certificate chain of trust, with revocation checking
- Software troubleshooting decision tree
- Network connectivity troubleshooting flowchart
- OSI network stack, annotated for A+ 1202's Layer 2/3/4/7 focus
- Backup and restore hierarchy, with an RPO/RTO timeline

---

## Mode 4: Interactive Foundations

Ten small, dependency-free JavaScript tools for building intuition rather than memorizing facts:

1. Boot Mode Selector (BIOS vs. UEFI comparison)
2. Command-Line Reference (searchable, Windows/macOS/Linux)
3. Disk Partitioning Visualizer (adjustable disk size and scheme)
4. Encryption Method Comparison (symmetric / asymmetric / hashing)
5. Certificate Chain Validator (step through PKI validation)
6. Event Log Parser (sample entries, click to decode)
7. Process Manager (mock Task Manager, flags an unrecognized process)
8. Ping/Tracert Simulator
9. DHCP Lease Timeline (Discover, Offer, Request, Acknowledge)
10. Backup RPO/RTO Calculator

---

## After You Complete the Exam

If this is being used for a WGU or other course requiring results submission, email your instructor:

📧 **mario.booker@wgu.edu**

**Subject line:** `A+ 1202 Practice Exam Results — [Your Name] — [Date]`

**In the body, include:**
1. Your overall score and per-domain breakdown
2. The domain or topic you found most challenging
3. Any questions about topics you missed

---

## Technical Notes (For Instructors / Maintainers)

The entire tool is one self-contained HTML file (`a_plus_1202_full_exam.html`) with zero external dependencies — no CDN calls, no image hosting, no backend. All 250 questions, the study guide, SVG diagrams, and interactive tools are bundled inline. GitHub Pages serves it as a static file; any static file host would work identically.

State is session-only: answers, scores, and interactive tool state reset when the browser tab closes. Nothing is written to localStorage or any server.

To update or add questions, edit the relevant domain array (`OS`, `SEC`, `SW`, `OPS`, `NET`) directly in the `<script>` block and push to `main`. GitHub Pages rebuilds within 1–2 minutes.

**Validation performed before deployment:**
- `node --check` on the full extracted JavaScript — passes with no syntax errors
- Every one of the 250 question objects checked for required fields (`comp`, `objective`, `topic`, `diff`, `stem`, `opts`, `ans`, `rationale`, `misconception`) — zero missing
- Every `ans` index checked against its 4-option array bounds — all valid
- Difficulty distribution checked per domain — all five hit the target 17 foundational / 19 intermediate / 14 advanced split exactly
- All 9 SVG diagrams parsed as well-formed XML — zero errors

---

## Data Sources

- CompTIA A+ Core 2 (220-1202) official exam objectives
- General, publicly available IT reference material (Microsoft Learn documentation, Apple developer documentation, Linux distribution documentation, RFC standards for networking protocols)
- Common real-world IT support scenarios, written from professional experience rather than any single proprietary source

No content was copied from CompTIA's proprietary question bank, any commercial test-prep vendor, or any copyrighted exam-prep publication. All question stems, answer choices, rationale text, and misconception notes are original writing.

---

## Suggested Citation (APA 7th edition)

Booker, M. (2026). *CompTIA A+ 1202 full practice exam* [Interactive web application]. GitHub Pages. https://DrMarioDeSean411-arch.github.io/a-plus-1202-practice-exam/a_plus_1202_full_exam.html

---

## Reference List

CompTIA. (2024). *CompTIA A+ Core 2 (220-1202) exam objectives.* CompTIA, LLC.

Microsoft. (n.d.). *Windows documentation.* Microsoft Learn. https://learn.microsoft.com/windows/

Apple Inc. (n.d.). *Apple platform security guide.* Apple Developer Documentation. https://support.apple.com/guide/security/

The Linux Foundation. (n.d.). *Linux kernel and distribution documentation.*

Internet Engineering Task Force. (n.d.). *Request for Comments (RFC) series* — networking and security protocol standards.

---

*CompTIA A+ Core 2 (220-1202) · Practice exam maintained by Dr. Mario Booker · mario.booker@wgu.edu*
*CompTIA A+ is a registered trademark of CompTIA, Inc. This is an independent, unofficial study resource and is not affiliated with, endorsed by, or sponsored by CompTIA.*
