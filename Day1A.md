# Lab 1A — 4-Tool Comparison Matrix: Task 1 (Summarise)

**Mentor Name:** ___________________________
**Date:** ___________________________

---

## Task 1 Prompt

> "Summarise this article in 5 bullet points. Each bullet: maximum 15 words. Do not lose the key claims. Do not add information not in the article."

---

## Scoring Rubric (Task 1)

| Score | Faithfulness | Structure | Brevity |
|-------|-------------|-----------|---------|
| **5** | All key claims preserved, no fabrication | Numbered, parallel form, easy to read | Every bullet ≤ 15 words |
| **3** | Most key claims preserved, 1–2 minor omissions | Mostly clean, 1 awkward bullet | One or two bullets slightly long |
| **1** | Major omission, fabrication, or misattribution | Inconsistent format, prose blocks | Long-winded, ignored word limit |

---

## Tool Outputs & Scoring

### ChatGPT

**Output:**
- Over 60% of Tier-1 B.Tech students used AI for placements in 2025.
- AI use evolved from resumes to extensive mock interview practice by 2025.
- Recruiters added longer interviews and offline coding rounds against AI-rehearsed responses.
- AI-fluent students were 2.4 times likelier to secure Tier-1 company offers.
- Verification training is crucial as agentic AI expands placement preparation by 2028.

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| Faithfulness | 4 | Covers 4 of 5 key claims well; drops the AICTE 18% statistic and the 60% error-reduction from verification chain — two notable omissions. |
| Structure | 5 | Clean parallel bullets, consistent form throughout. |
| Brevity | 5 | Every bullet is within 15 words. Prompt constraint fully respected. |
| **Overall** | **4** | Clean and readable. Best default for speed, but sacrifices some depth. |

---

### Claude

**Output:**
- AI adoption surge: Over 60% of Tier-1 B.Tech students use AI for placement prep in 2025, rising to a projected 95% by 2028.
- Recruiter response: Interview rounds are 35% longer in 2025; companies like TCS and Infosys now use offline live coding rounds.
- Equity gap: AI-fluent students are 2.4× more likely to land Tier-1 offers; only 18% of placement officers have formal AI training.
- Verification challenge: Frontier AI models are wrong 8–12% of the time; students risk confidently stating fabricated facts in interviews.
- Emerging solution: A three-step verification chain (AI → secondary source → primary source) reduces student factual errors by 60%.

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| Faithfulness | 5 | All key claims preserved — 60% stat, 95% projection, 35% longer interviews, 2.4× offer rate, 18% AICTE figure, hallucination rate, and verification chain outcome. Nothing fabricated. |
| Structure | 4 | Added bold labels (e.g. "AI adoption surge:") which aid scannability but were not requested. Minor stylistic deviation. |
| Brevity | 2 | Multiple bullets exceed 15 words significantly (e.g. bullet 1 = 22 words, bullet 3 = 20 words). Direct violation of the prompt's word limit constraint. |
| **Overall** | **3** | Most thorough on content. Fails the brevity constraint clearly. Valuable teaching moment: more is not always better. |

---

### Gemini

**Output:**
- AI use in Indian engineering campus placement preparation is projected to reach 95% by 2028.
- Recruiters added live coding and unscripted questions to counter heavily rehearsed, AI-polished student answers.
- AI-fluent students are 2.4 times more likely to secure Tier-1 company job offers.
- Most placement officers lack formal AI training, risking widening equity and verification gaps.
- Colleges are teaching a three-step verification chain to eliminate factual errors caused by AI hallucinations.

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| Faithfulness | 4 | Covers verification chain, equity gap, recruiter response, and 2.4× stat. Drops the current 60% adoption figure and the 60% error-reduction outcome. No fabrication. |
| Structure | 5 | Clean, parallel, easy to read. No clutter. |
| Brevity | 4 | All bullets near or within 15 words. Bullet 5 is borderline at ~14 words. |
| **Overall** | **4** | Solid and clean. Slightly less informative than Claude but respects the format better. Strong on structure. |

---

### Perplexity

**Output:**
- By 2025, 60%+ Tier‑1 B.Tech students use ChatGPT‑style AI for placement prep; 95% projected by 2028.
- Students progressed from cover letters (2023) to 50+ AI mock interviews and polished answers (2025).
- Recruiters lengthen interviews and add unscripted follow-ups and offline coding rounds to detect rehearsed answers.
- AI‑fluent students far more likely to get Tier‑1 offers; equity gap and placement‑staff training shortfalls noted.
- 2026 solution: a three‑step verification chain (AI → second source → primary source) reduces factual errors.

| Dimension | Score | Reasoning |
|-----------|-------|-----------|
| Faithfulness | 5 | Covers the widest range: adoption timeline (2023→2025), both stats (60% and 95%), recruiter response, equity gap, staff training gap, and verification chain. Nothing added or fabricated. |
| Structure | 3 | Slightly inconsistent — bullet 4 is vague ("far more likely"), bullet 5 uses a colon-lead style different from the others. Less parallel than ChatGPT or Gemini. |
| Brevity | 3 | Bullets 1 and 3 exceed 15 words. Bullet 4 trades precision for brevity. Mixed adherence. |
| **Overall** | **4** | Best on faithfulness. Structural inconsistency and uneven brevity hold it back. Best choice when source coverage matters most. |

---

## Summary Matrix

| Tool | Faithfulness | Structure | Brevity | **Overall Score** |
|------|-------------|-----------|---------|-------------------|
| ChatGPT | 4 | 5 | 5 | **4** |
| Claude | 5 | 4 | 2 | **3** |
| Gemini | 4 | 5 | 4 | **4** |
| Perplexity | 5 | 3 | 3 | **4** |

---

## My Verdict (3-Sentence Conclusion)

> "I would use **ChatGPT** for general summarisation tasks where clean structure and prompt compliance matter most."

> "I would use **Claude** for high-stakes writing where preserving every key claim is critical — but I must add a strict word-limit reminder to the prompt."

> "I would use **Perplexity** when I need the most complete factual coverage and am less concerned about structural polish."

---

## Key Teaching Observation

Claude demonstrated a clear **faithfulness vs. brevity trade-off**: it preserved the most content but violated the 15-word constraint on multiple bullets. This is a direct example of why prompt constraints must be explicit and repeated — AI tools optimise for what they are rewarded on, and Claude's default leans toward completeness over conciseness.

---

*Lab 1A — Task 1 | Day 1 Placement Mentor Training*
