# **AXCESSR**

<img width="150" height="150" alt="AXCESSR_logo" src="https://github.com/user-attachments/assets/e00f04a0-dce2-4dc4-942c-2d60c8ea33af" />

**Introduction:**

Three parties make every student-funding decision: the student, the institution, and the lender, yet none of them have the data they need to make it well.

In South Africa, roughly 68 000 "missing middle" students sit in the gap between government bursaries (capped at R350,000 household income) and self-funding affordability - and even after recent policy reforms introducing loan funding for the R350K–R600K income band, only about 47% currently receive any support.[^1] South Africa's first-year university dropout rate sits at 35 – 40%, with financial exclusion and poor programmatic fit consistently identified as primary drivers.[^2] In the United States, the picture is no better: as of December 2025, approximately $180 billion in federal student loans were in default across 7.7 million borrowers, and 29.5% of the active portfolio was delinquent by dollar balance - more than double the pre-pandemic rate.[^3] These outcomes share a common cause: students, higher education institutions, and lenders are all making high-stakes decisions on incomplete and asymmetric information about who will succeed academically and financially.

AXCESSR addresses this by manufacturing data symmetry across all three parties. It is a psychometric assessment and decision platform that produces a shared, validated signal - derived from four measured psychological domains (personality, values, emotion traits, and emotion states) - that students, Higher Education Institutions (HEIs), and lenders can each act on. Students get evidence of programmatic and career fit before committing time and capital. Institutions get completion-likelihood signals beyond academic records. Lenders get repayment-behaviour predictors that work for thin-file applicants without an established credit history. The same psychometric data point underwrites all three decisions, replacing the fragmented and asymmetric inputs each party currently relies on.

*Figure 1. AXCESSR Overview*

<img width="600" height="350" alt="AXCESSR Overview" src="https://github.com/user-attachments/assets/034d5d19-c509-4c79-9119-463f6acf51b3" />

**Purpose of the Assessment:**

The primary objectives of AXCESSR are to:

* Improve access to student funding for academically eligible candidates without an established credit or academic record
* Match students to programmes where they are likely to succeed
* Provide higher education institutions with completion-likelihood signals beyond academic records
* Provide lenders with repayment-behaviour predictors validated for thin-file populations
* Support risk assessment, underwriting, and portfolio management for funders

**How AXCESSR was built:**

AXCESSR was not built with data science as an afterthought. From initial construct mapping and **conceptualisation** through to **data validity** and candidate screening, and into **UX research**, every stage of development was data-informed. The pipeline below illustrates how each phase fed into the next.

*Figure 2. AXCESSR Development Pipeline*

<img width="600" height="500" alt="AXCESSR Development Pipeline V2" src="https://github.com/user-attachments/assets/f8f88d90-b866-4c3d-950c-4d32aa001feb" />

The pipeline above illustrates the three core development phases of AXCESSR - conceptualisation, validation, and UX research - each producing data that feeds the next, and each iteration of the cycle informing a sharper version of the instrument. This is not a linear build. AXCESSR is designed to evolve: findings from validation reshape the item pool, UX research exposes where the assessment places unnecessary burden, and both inform the decisions that define the next iteration - including the move toward a Computerised Adaptive Testing (CAT) engine that shortens assessment time and reduces respondent load without sacrificing measurement precision.

The first cycle began with construct mapping and item generation, grounded in established psychometric reference scales. Validation followed - reliability analyses, IRT diagnostics, and the removal of 41 problematic items refined the instrument from 247 to 206 items. UX research then surfaced the real-world experience of respondents, closing the loop and opening the next one. Each phase fed the next, with all phases being led by data.

# **1) Conceptualisation**

Figma Conceptualisation Presentation Link -> https://www.figma.com/deck/BWVGJvpN2KeOfJEtiEwUf5

**The problem:**

AXCESSR is a psychometric-based credit risk assessment platform designed to extend financial access to individuals overlooked by traditional credit origination methods - either due to limited credit history or an overestimation of risk based on conventional metrics. Rather than relying on historical financial data, the platform evaluates creditworthiness through the measurement of stable personal dispositions shown to predict financial decision-making and repayment behaviour.

*Figure 3. The Funding Access Gap*

<img width="368" height="343" alt="image" src="https://github.com/user-attachments/assets/2ea18234-df5a-4bdd-be35-c5864e69655a" />

The platform targets two primary markets: the student loan market, where millions of academically eligible students lack access to funding, and the broader personal credit market, where thin-file and credit-invisible individuals remain underserved. Psychometric scores can be generated for any candidate irrespective of formal credit history and, because scores are user-generated, they are broadly compliant with consumer privacy regulations.

**Assessment Architecture:**

Four core psychological domains were identified through a review of the behavioural science literature as the constructs most predictive of real-world financial and educational outcomes:

- **Personality** — stable trait dispositions that shape how individuals behave across contexts
- **Values** — motivational orientations that drive long-term decision-making and goal alignment
- **Emotional Traits** — enduring patterns of emotional responding, including impulsivity and self-regulation
- **Emotional States** — situational affective tendencies such as stress reactivity and boredom proneness

*Figure 4. AXCESSR Structure*

<img width="400" height="300" alt="AXCESSR Structure V3" src="https://github.com/user-attachments/assets/e6b1358e-0f07-48d6-a170-bb3670a01daa" />

With the domain structure established theoretically, the next challenge was operationalisation - translating abstract constructs into measurable, defensible items

**Item Development:**

Item development drew on a structured review of established psychometric frameworks, adapting content from validated instruments across each risk domain. Source instruments included the International Personality Item Pool (IPIP), the HEXACO Personality Inventory, the Schwartz Value Survey (SVS), the Trait Emotional Intelligence Questionnaire (TEIQue), the Short Dark Triad (SD3), the Edwards Compulsive Buying Scale (ECBS), the Barratt Impulsivity Scale, the Sensation Seeking Scale, and the UPPS Impulsive Behaviour Scale.

The below figure illustrates the diverse psychological frameworks and reputable assessment scales that were integrated to develop the AXCESSR item pool, highlighting the foundational instruments that informed its construction

*Figure 5. Frameworks Underpinning the AXCESSR Item Pool Development*

<img width="700" height="500" alt="Instrument Design" src="https://github.com/user-attachments/assets/dbdc4bed-83db-49b3-99f0-bf6d39f32f78" />

Every item in the AXCESSR pool traces back to a documented psychological construct. Items were not written opportunistically - each one was derived from a defined theoretical basis and subjected to a structured development pipeline before inclusion in the instrument.

*Figure 6. Item Development Structure*

<img width="614" height="414" alt="image" src="https://github.com/user-attachments/assets/cf785e31-070e-4ad7-b0a8-3a25dbd294e2" />

Each item was engineered to measure a specific construct dimension with precision. The example below illustrates the structural components of a single AXCESSR.

*Table 1. Item Anatomy*

| Component | Example |
|---|---|
| **Construct** | Impulse regulation under financial stress |
| **Item stem** | "When I am under pressure, I tend to make decisions quickly without thinking them through." |
| **Response format** | Continuous slider — strongly disagree to strongly agree |
| **Scoring** | Continuous 0–1, reverse-scored, feeds Emotion Traits domain |
| **Risk direction** | Higher score = elevated impulsivity risk |

**From Score to Decision:**

Item responses aggregate upward through the hierarchy, producing an actionable output at each level.

Item responses → Subfactor score → Factor score → Domain score → Risk profile

# **2) Data Validity**

*Figure 7. Validation Pipeline*

<img width="725" height="247" alt="Validation Pipeline" src="https://github.com/user-attachments/assets/96d90b15-1623-44bb-ac9b-a42a73fd8748" />

**Validation results:**

Validation was conducted on the full cleaned dataset (after removing speeders, boundary cases, etc.). An initial EFA showed excellent overall fit but revealed many weak or cross‑loading factors. Domain‑level EFAs indicated that some subfactors were not meaningfully separated statistically. This provided evidence for collapsing certain subfactors into single dimensions and regrouping others into broader factors where the empirical structure diverged from the current specification. CFA models could not be estimated due to non‑positive definite covariance matrices, though the theorised structure was evident in composite-based correlation plots. Reliability analyses indicated that most subfactors fell below the 0.70 threshold, underscoring limited internal consistency.

**Item removal diagnostics:**

To address these issues, a flat higher‑order CFA was retained as an item‑level diagnostic. Standardised loadings onto higher‑order factors were used as one of three convergent item quality indicators, alongside IRT loadings estimated in isolated subfactor models and corrected item‑total correlations (r.drop). Items with CFA loadings below 0.30, low IRT loadings, and weak r.drop values were flagged as problematic. These diagnostics jointly informed item removal, after which validation analyses were rerun on the reduced set. Convergent evidence across multiple methods led to the removal of 41 items, resulting in a streamlined 206‑item instrument (V2).

**Summary of Problematic items:**

*Table 2. Summary of Problematic Items*

| Diagnostic | Total | Personality | Values | Emotion Traits | Emotion States |
|---|:---:|:---:|:---:|:---:|:---:|
| IRT subfactor loading (< 0.30) | 45 | 23 | 9 | 3 | 10 |
| CFA subfactor loading (λ < 0.30) | 75 | 41 | 15 | 5 | 14 |
| Item-total correlation (r < 0.30) | 98 | 51 | 19 | 8 | 20 |
| **Flagged by all three criteria** | **41** | **22** | **9** | **2** | **8** |

The above table summarises the three metrics used to assess the quality of items. Items that were flagged across all three metrics were defined as problematic and removed in V2.

**Next steps:**

These findings represent a preliminary validation stage. High‑stakes data are still being collected and will be cross‑referenced with the current results. Final decisions regarding item removal and potential subfactor collapsing will be informed by analyses conducted on the high‑stakes dataset.

**Score Stability: Population Stability Index (PSI):**

A key question following item removal is whether the revised instrument produces materially different risk classifications. The Population Stability Index (PSI) is a metric widely used in credit risk modelling to quantify distributional shift between two scoring populations. A PSI below 0.10 indicates a stable distribution; values between 0.10 and 0.25 indicate moderate shift warranting investigation; values above 0.25 indicate significant drift requiring model review.

PSI was computed between V1 (247-item) and V2 (206-item) total and domain-level scores to assess whether item removal destabilised candidate risk profiles.

*Table 3. Summary of Population Stability Index (PSI) Scores After Item Removal*

| Variable | PSI Score | Interpretation |
|---|:---:|---|
| Total Risk (Weighted) | 0.0997 | Stable — minor shift, no action required |
| Personality Risk | 0.0283 | Stable — distribution largely unchanged |
| Values Risk | 0.1884 | Moderate shift — high considering only 9 items were removed |
| Emotion Traits Risk | 0.0036 | Highly stable — negligible distributional change |
| Emotion States Risk | 0.0420 | Stable — minimal shift across versions |

The PSI results indicate that item removal had minimal impact on candidate risk classifications across most domains. Four of five scores fall within the stable range (PSI < 0.10), with Emotion Traits Risk showing negligible shift (PSI = 0.004) and Personality Risk and Emotion States Risk both well within acceptable bounds. The moderate shift observed in Values Risk (PSI = 0.19) is notable given that only 9 items were removed from this domain - suggesting those items were disproportionately influential in shaping the score distribution. Critically, no domain exceeds the intervention threshold of 0.25.

The domain-level breakdown reveals where revision had the most structural impact.

*Figure 8. Population Stability Index (PSI) by Domain*

<img width="1000" height="600" alt="psi_bar" src="https://github.com/user-attachments/assets/4bdf8c89-24bb-4ce2-993e-9958f345b302" />

The bar chart confirms that distributional shift is concentrated in the Values domain. All other domains sit comfortably below the stable threshold, and the total weighted risk score sits precisely at the boundary (PSI = 0.10) - indicating that at the overall scoring level, V1 and V2 produce near-equivalent candidate classifications.

*Figure 9. Score Distributions: V1 (247 items) vs V2 (206 items)*

<img width="1000" height="600" alt="psi_density" src="https://github.com/user-attachments/assets/9e23745d-a946-49b0-80fe-bd023ae1fe69" />

The density curves corroborate the PSI findings. For Emotion Traits and Personality, the V1 and V2 distributions are almost indistinguishable. Emotion States and Total Risk show a slight tightening of the distribution in V2 - consistent with the removal of noisy items reducing score variance. The Values domain shows the most visible shift, with the V2 distribution marginally narrower and shifted slightly rightward, reflecting the influence of the removed items on the lower end of the score range. Across all domains, the core shape of the distribution is preserved, confirming that the revised instrument measures the same underlying constructs in a substantively equivalent way.

Statistical validity confirms the instrument measures what it claims to. UX research addresses a separate question: will candidates actually engage with it honestly and completely?

# **3) UX Research**

Psychometric rigour is a necessary but insufficient condition for a viable assessment product. A well-constructed instrument that candidates disengage from, rush through, or abandon produces compromised data - and compromised data produces unreliable scores. UX research was therefore not a supplementary workstream: it was a data quality intervention. Conducted alongside validation, the research was designed to identify response variability attributable to presentation rather than construct variance - and to use those findings to drive design decisions that optimise the candidate experience and, by extension, the integrity of the data it generates. Every UX metric collected was treated as a signal: evidence of where the instrument was working, where it was creating friction, and where design changes could recover response quality without touching the psychometric structure.

 **A|B Testing:**

In order to improve response quality, A/B testing was conducted to evaluate the impact of UX-driven changes to the assessment instrument. Version B of the survey was developed by iteratively refining the assessment design based on key UX metrics, with the goal of reducing low-quality responses and improving overall participant engagement. The following quality flags were used to compare performance across both versions:

*Table 4. UX Metrics Summary*

| Metric | Explanation |
|-------------------|-----------------------------------------------------|
| Time Taken | Total time a respondent spends completing the assessment. Unusually short times may indicate rushing; unusually long times may reflect connectivity issues or disengagement. |
| Response variance | The degree of variation in answers across items. Low variance may signal disengagement (e.g., straight-lining responses). |
| Long String Responding | The occurrence of consecutive identical responses across items. A strong behavioural indicator of disengagement or deliberate faking. |
| Boundary Overuse | Systematic overuse of extreme response options (e.g., always selecting 0 or 1). Suggests acquiescence bias, satisficing, or deliberate manipulation of scores. |
| Completion rate | The percentage of respondents who finish the assessment once they start. A high rate suggests the test feels manageable and engaging. |
| Click-through rate | The proportion of users who proceed from one section or item to the next. Indicates how intuitive and motivating the flow of the assessment is. |
| Drop-off point | The item or section where respondents most often quit. Helps identify where fatigue or frustration sets in. |
| Inter-item RT consistency | Consistency in response times across items. Large fluctuations can indicate faking, guessing, or loss of attention. |
| Onset of disengagement | The point in the assessment where behavioral signals (e.g., long strings, extreme responding, rapid completion) begin to appear. Shows when users start losing focus. |
| Platform Load Time | The average time it takes for each page or item to load. Longer load times can frustrate users and reduce engagement. |
| Connectivity Drop Events | The number of times users lose connection or experience interruptions during the assessment. Frequent drops can harm the user experience and affect data quality. |

**Completion Times:**

Completion time is a key metric for AXCESSR as it provides a useful lens through which to examine candidate engagement, particularly as the original AXCESSR assessment (Version A) consisted of 247 items. While most respondents worked steadily through the assessment, a subset completed unusually quickly, raising concerns about inattentive responding, whilst other took over 2 hours to complete the assessment. The histogram below illustrates the spread of completion times across the full sample.

*Figure 10. Total Time Taken Distribution*

<img width="550" height="300" alt="image" src="https://github.com/user-attachments/assets/5b74b661-ccc0-4356-b3c8-239162a630b8" />

Completion times ranged from 39 seconds to nearly two hours (7155 seconds), with a median of 1834 seconds (~30 minutes) and a mean of 2043 seconds (~34 minutes). The central bulk of candidates fell between the first and third quartiles (1372–2525 seconds), indicating a typical completion window of 23–42 minutes. The right‑skewed distribution reflects a small group of candidates who took substantially longer, while the left tail captures the ~10% of speeders flagged for accelerated completion. This pattern underscores that the majority of candidates engaged at a reasonable pace, but a notable minority exhibited atypical response behaviour consistent with low engagement.

**Version A:**

*Table 5. UX Quality Flag Summary - Version A (N = 2016)*

| Quality Flag | Criterion | Count | Percentage |
|---|---|:---:|:---:|
| Speeder | Total time taken < 884 seconds | 201 | 9.97% |
| Low Variance | Person SD < 0.11 | 50 | 2.48% |
| Long String | Longest string > 15 | 86 | 4.27% |
| Boundary Overuse | Proportion of 0s > 0.28 or 1s > 0.50 | 192 | 9.52% |
| Completion (single sitting) | Did not complete in a single sitting | 251 | 12.45% |
| High Click-Through | Click-through rate > 0.70 | 218 | 10.81% |
| Early Drop-Off | Abandoned before item 10 | 91 | 4.51% |
| Uniform RT (Inter-item) | RT consistency SD < 1.5 | 67 | 3.32% |
| Early Onset of Disengagement | Onset of disengagement before item 60 | 222 | 11.01% |
| Loading Time | Average page load time exceeds 5 seconds | 215 | 10.66% |
| Connectivity Drop | One or more connectivity drop events | 364 | 18.06% |

**Recommendations:**

**1. Adaptive Item Delivery via CAT**

With 11.86% of candidates failing to complete in a single sitting and click-through rates flagging 10.81% as likely rushing, instrument length is the primary UX risk. A CAT engine addressing this single lever produces downstream improvements across most metrics in Version B - completion rate, click-through, drop-off, onset of disengagement, connectivity drops, and load time exposure all improve as direct consequences of shorter sessions.

**2. Platform Load Optimisation**

With 11.01% of Version A candidates experiencing load times exceeding 5 seconds and 16.12% recording at least one connectivity drop event, platform performance represents a meaningful risk independent of candidate behaviour. Asset delivery optimisation and offline-capable session caching are particularly relevant given variable connectivity in the deployment context.

**3. In-Session Engagement Support**

Speeders (9.97%), long string responding (4.27%) and boundary overuse (9.52%) in Version A indicate that a meaningful minority of candidates are disengaged form the assessment and trying to get through it quickly or with as little effort as possible. Progress indicators, estimated time remaining, and structured domain-break screens are low-cost interventions that delay or prevent onset of disengagement.

These three interventions are not independent. CAT reduces session length, which reduces fatigue, connectivity exposure, and the motivation to rush simultaneously. Platform optimisation reduces the friction that can trigger early drop-off. Engagement support addresses the candidates who would disengage regardless of length. Together they address the full spectrum of UX risk identified in Version A - behavioural, dispositional, and infrastructural.

**Version B:**

Version B reflects the changes in UX quality metrics following the implementation of recommendations made after Version A.

*Table 6. UX Quality Flag Summary - Version B (N = 2016)*

| Quality Flag | Criterion | Count | Percentage |
|---|---|:---:|:---:|
| Speeder | Total time taken < 442 seconds | 46 | 2.28% |
| Low Variance | Person SD < 0.11 | 50 | 2.48% |
| Long String | Longest string > 15 | 0 | 0% |
| Boundary Overuse | Proportion of 0s > 0.28 or 1s > 0.50 | 0 | 0% |
| Completion (single sitting) | Did not complete in a single sitting | 86 | 4.27% |
| High Click-Through | Click-through rate > 0.70 | 6 | 0.3% |
| Early Drop-Off | Abandoned before item 50 | 3 | 0.15% |
| Uniform RT (Inter-item) | RT consistency SD < 1.5 | 6 | 0.3% |
| Early Onset of Disengagement | Onset of disengagement before item 30 | 0 | 0% |
| Loading Time | Average page load time exceeds 5 seconds | 0 | 0% |
| Connectivity Drop | One or more connectivity drop events | 130 | 6.45% |

**A|B Comparison:**

The most immediate consequence of CAT-based adaptive delivery is a compression of completion times. Version A shows the characteristic right-skewed distribution of a fixed-form instrument — a healthy central mass with a long tail driven by connectivity issues, session abandonment, and disengagement. Version B simulates the expected shift under adaptive delivery: a tighter, more normally distributed profile centred around a shorter mean, with both extremes reduced. The disappearance of the extreme right tail reflects fewer candidates experiencing prolonged sessions, while the left tail contraction reflects the adjusted speeder threshold calibrated to the shorter instrument.

*Figure 11. Completion Time Distribution Comparison*

<img width="1245" height="619" alt="image" src="https://github.com/user-attachments/assets/ee7e6539-4b5a-4992-8b85-7226b736a8ea" />

Four continuous UX metrics are compared below as density overlays, allowing direct visual comparison of distributional shift between versions. Click-through rate should shift leftward in Version B - fewer candidates rushing. RT consistency SD should shift rightward - more natural variation in pacing. Load time should compress toward zero following platform optimisation. Onset of disengagement should shift rightward and thin out, reflecting fewer candidates hitting a disengagement point and those who do reaching it later in the session.

*Figure 12. UX Metric Distribution Comparison*

<img width="2112" height="1536" alt="image" src="https://github.com/user-attachments/assets/b88fc0e9-8139-404b-ab25-7dd619614f87" />

The dumbbell chart below provides a single consolidated view of improvement across all eleven UX metrics, comparing flag prevalence between Version A and Version B. Each flag is shown as a connected pair — the dark point representing Version A prevalence and the light point representing Version B. Metrics where the gap between points is largest represent the greatest UX gains from the three interventions. Metrics with little movement reflect either dispositional factors that UX changes cannot address, or infrastructure constraints that require solutions beyond instrument redesign.

*Figure 13. UX Flag Prevalence Comparison*

<img width="1920" height="1344" alt="image" src="https://github.com/user-attachments/assets/04596745-9d24-43b0-a352-caed30c9d089" />

Beyond aggregate UX metrics, individual response patterns were examined to identify candidates whose data quality may compromise scoring integrity.

**Response Quality Screening:**

An initial sample of N = 2016 candidates completed the assessment. Prior to scoring, all responses were screened for indicators of low engagement using four data-driven criteria: accelerated completion (speeders), invariant responding (low variance), consecutive identical responses (long-string), and extreme endpoint selection (boundary overuse). The following table summarises the findings.

*Table 7. Summary of Response Quality Flags*

| Quality Flag | Criterion | Count | Percentage |
|---|---|:---:|:---:|
| Speeder | Completion time < 884 sec | 201 | 9.97% |
| Boundary Overuse | Proportion of 0s > 0.28 or 1s > 0.50 | 192 | 9.52% |
| Long-String | Longest string > 15 | 86 | 4.27% |
| Low Variance | SD < 0.111 | 50 | 2.48% |

*Note.* *Speeders* — completion time below the 10th percentile (< 884 seconds). *Low variance* — person-level response SD below one-third of the sample mean SD (< 0.111). *Long-string* — longest consecutive identical response sequence exceeding the 95th percentile (> 15). *Boundary overuse* — proportion of zero responses exceeding 0.28 or proportion of one responses exceeding 0.50, both derived from the 95th percentile.

The figure below illustrates the intersection structure of response quality flags across the 388 flagged candidates. Each bar represents a unique combination of criteria, with bar height indicating the number of candidates flagged by that particular combination.

*Figure 14. Intersection of Response Quality Flags Across Flagged Candidates*

<img width="787" height="486" alt="image" src="https://github.com/user-attachments/assets/a6fd24f8-7957-48cd-82c6-04a89e086db6" />

The majority of flagged candidates (144) were caught by the speeder criterion alone, with boundary overuse the second most common single flag (114). Co-occurring flags - where the same candidate triggered multiple criteria independently - account for 114 of the 388 flagged candidates, providing convergent evidence of low engagement in those cases.

**Comparison:**

To assess differences in response consistency between groups, the figure below compares person-level variance for respondents flagged on quality checks versus those retained in the clean sample. Examining variability at the individual level provides insight into how consistently participants engaged with the assessment items.

*Figure 15. Comparison of Person-Level Variance in the Flagged and Clean Sample*

| Person-Level Variance in the Flagged Sample (N = 388) | Person-Level Variance in the Clean Sample (N = 1628) |
|--------|--------|
| <img width="400" height="280" alt="image" src="https://github.com/user-attachments/assets/27fd52c5-c121-4bd6-bc11-8f8951d6b42b" />|<img width="400" height="280" alt="image" src="https://github.com/user-attachments/assets/29f473f9-8214-4c90-9ec1-04cc975e63a5" />|

The flagged sample (N = 388) shows a broader and more irregular spread of person-level variance, including a noticeable concentration of lower-variance cases. In contrast, the clean sample (N = 1628) exhibits a more stable and tightly clustered distribution, suggesting more consistent and differentiated responding.

To better understand how flagged respondents differ from the rest of the sample, the figure below compares score distributions across key domains. Density curves are shown for both clean and flagged groups, allowing for a direct visual comparison of their response patterns.

*Figure 16. Comparison of Score Distributions Between the Flagged and Clean Sample*

<img width="787" height="486" alt="image" src="https://github.com/user-attachments/assets/07d91c35-5a24-4667-9f1b-fc0b9e4d2e8b" />

This comparison shows that respondents with quality flags exhibit noticeably different score patterns, with several domains displaying irregular or bimodal distributions. In contrast, the clean sample appears more stable and closer to expected distributional shapes. This divergence suggests that flagged responses may introduce noise or distortion, reinforcing the importance of removing or carefully reviewing suspicious respondents to maintain analytical rigor.

# Conclusion

AXCESSR was built with data science at the core. Data was embedded from the first stage of construct mapping and held through to the final UX iteration.

In Phase 1, the theoretical architecture was not assumed - it was derived. Domain selection, factor structure, and item derivation each traced back to documented empirical literature, ensuring that what AXCESSR measures has a defensible basis before a single response was collected.

In Phase 2, that structure was stress-tested. Validation did not confirm the original specification - it interrogated it. Where the data diverged from theory, the instrument changed. Forty-one items were removed not because they felt wrong, but because three independent statistical diagnostics agreed they were underperforming. The PSI analysis then confirmed that this structural revision did not destabilise candidate classifications - the instrument was improved without being disrupted.

In Phase 3, the same rigour was applied to the candidate experience. UX was not treated as a design layer applied after the psychometrics were finalised - it was recognised as a data quality problem. Response flags, completion distributions, and A/B metrics revealed that a poorly designed experience produces noise, and noise degrades the very scores the instrument was built to generate. Version B was not a redesign - it was a data-driven correction.

The result is an end-to-end development pipeline in which measurement science, statistical validation, and user experience research operated as a single integrated system rather than sequential handoffs. Each phase produced findings that constrained and informed the next. No decision was made in isolation.

---

# References

[^1]: NSFAS (National Student Financial Aid Scheme) and the Department of Higher Education and Training, Comprehensive Student Funding Model and Missing Middle Loan Funding Programme (announced 2023, ongoing implementation). See SAnews coverage at https://www.sanews.gov.za/south-africa/nzimande-announces-r38bn-funding-missing-middle-students and policy analysis at https://www.universityworldnews.com/post.php?story=20250318114841409. Note: the formally identified missing-middle population (~68,000) reflects the policy-target estimate; broader analyses suggest the true funding-gap population is substantially larger.

[^2]: South African Department of Higher Education and Training; Branson, N. (2024). South African student retention during 2020: Evidence from system-wide higher education institutional data. *South African Journal of Economics*, https://onlinelibrary.wiley.com/doi/10.1111/saje.12361. See also HSRC Policy Brief on dropout rates and BusinessTech reporting at https://businesstech.co.za/news/lifestyle/771036/university-dropout-crisis-for-south-africa/.

[^3]: U.S. Department of Education, Federal Student Aid Data Center, December 2025 portfolio reports. See https://fsapartners.ed.gov/knowledge-center/library/electronic-announcements/2025-08-21/federal-student-aid-posts-updated-reports-fsa-data-center and Congressional Research Service analysis of the 2025 default cliff at https://www.congress.gov/crs-product/IF13113.
