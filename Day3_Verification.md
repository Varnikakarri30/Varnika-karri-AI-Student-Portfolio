# Day 3 — Lab 3A: Verification Chain
**Name:** VarnikaKarri  
**Roll Number:** 23A91A0566  
**Date:** 11 June 2026

---

## Verification Matrix

|  | Claim | AI Source (Gemini) | Perplexity Check URLs | Primary Source URL | Verdict |
|---|-------|-------------------|----------------------|--------------------|---------|
| 1 | 24% year-on-year increase in PPO conversions across all degrees, 2025–2026 | Deloitte India (Campus Workforce Trends Report) | [Deloitte Press Room](https://www.deloitte.com/in/en/about/press-room/campus-hiring-rebounds-in-fy25.html) / [IBEF](https://ibef.org/news/job-market-to-bounce-back-as-campus-hirings-improve-in-2025-deloitte-report) | [Deloitte Campus Workforce Trends 2025](https://www.deloitte.com/in/en/services/consulting/services/human-capital/campus-workforce-trends.html) | **VERIFIED** |
| 2 | Average CTC of ₹29.57 LPA secured during final postgraduate placement, 2025 | IIM Indore | [Shiksha](https://www.shiksha.com/college/iim-indore-indian-institute-of-management-29623/placement) / [CollegeDunia](https://collegedunia.com/university/25665-iimi-indian-institute-of-management-indore/placement) | [IIM Indore Final Placement Report 2025 (Official PDF)](https://iimidr.ac.in/wp-content/uploads/2025/07/Final-Placement-Report-2025.pdf) | **VERIFIED** |
| 3 | 62% placement rate — 312 out of 501 eligible B.Tech students placed, 2025 | NIRF / JNTU Hyderabad | [CollegeDunia JNTUH](https://collegedunia.com/university/25359-jawaharlal-nehru-technological-university-jntuh-hyderabad/placement) / [Beincareer NIRF Data](https://beincareer.com/engineering-placement-stats-2026/) | [CollegeDunia JNTUH Placement 2025](https://collegedunia.com/university/25359-jawaharlal-nehru-technological-university-jntuh-hyderabad/placement) | **PARTIAL** |
| 4 | Highest domestic CTC of ₹1.10 Crore per annum offered during final management placements, 2025 | IIM Ahmedabad | [CollegeDunia IIMA](https://collegedunia.com/university/25494-iima-indian-institute-of-management-ahmedabad/placement) / [EducationPost](https://educationpost.in/news/jobs-in-higher-ed/iim-ahmedabad-concludes-mba-2025-placements-with-highest-package-of-110-crore) | [CollegeDunia IIM Ahmedabad Placement](https://collegedunia.com/university/25494-iima-indian-institute-of-management-ahmedabad/placement) | **VERIFIED** |
| 5 | 9.1% average salary increment projection for corporate workforces, 2026 | Aon (Annual Salary Increase Survey) | [Business Standard](https://www.business-standard.com/industry/news/average-pay-hike-across-sectors-projected-at-9-1-pc-in-2026-survey-126022400786_1.html) / [Daily Pioneer](https://dailypioneer.com/news/average-pay-hike-across-sectors-projected-at-9-1-in-2026-survey) | [Aon Asia Newsroom](https://www.aon.com/apac/in-the-press/asia-newsroom/2025/salaries-in-india-projected-to-increase-by-nine-percent-in-2026-aon-study) | **PARTIAL** |

---

## Verdict Summary

| Verdict | Count |
|---------|-------|
| VERIFIED | 3 |
| PARTIAL | 2 |
| FALSE | 0 |
| NO PRIMARY SOURCE FOUND | 0 |

---

## Why Claim 3 is PARTIAL

Gemini attributed the 62% placement rate (312/501 students) to NIRF/JNTU Hyderabad. The number itself is accurate and traceable to NIRF data. However, the primary source is **NIRF's reporting on JNTUH's own submitted data** — not an independent NIRF publication about this specific metric. CollegeDunia and other aggregators carry the number, but the raw NIRF institutional data portal does not surface this figure as a clean standalone statistic. The claim overstates the attribution authority by implying NIRF independently validated and published this figure, when in reality it is JNTUH's self-reported data submitted to NIRF. The number is likely correct; the sourcing framing is misleading.

---

## Why Claim 5 is PARTIAL

The 9.1% figure is confirmed by Aon's Annual Salary Increase and Turnover Survey 2025–26 India. However, Gemini framed it as directly influencing "entry-level fresher salary bands for campus intakes" — this interpretive link is not stated in the primary Aon report. The original survey measures corporate workforce increments broadly, not campus fresher benchmarks specifically. Gemini added an inferential layer as if it were a cited fact. The number is real; the application to campus placement benchmarking is Gemini's own extrapolation, not Aon's claim.

---

## Reflection Paragraph

The claim that looked most authoritative but was actually weakest was Claim 3: *"62% placement rate — 312 out of 501 eligible B.Tech students placed in 2025, sourced to NIRF/JNTU Hyderabad."* Gemini cited NIRF confidently, which lends institutional credibility — NIRF is a government ranking framework, so any number attributed to it feels official and trustworthy. Perplexity initially confirmed the figures citing CollegeDunia and aggregator sites. But when I checked the primary source trail, the data originates from JNTUH's own self-reported submission to NIRF — not independently audited or published by NIRF as a standalone finding. The number is likely correct, but the attribution implies a level of independent verification that does not exist. The lesson: confidence does not equal correctness. A government-sounding source name attached to a real-looking number is the most dangerous kind of hallucination-adjacent claim — because it is partially true, and partial truth is harder to catch than an outright fabrication. The verification step belongs to the human — every time.
