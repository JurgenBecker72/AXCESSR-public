# **AXCESSR**

<img width="150" height="150" alt="AXCESSR_logo" src="https://github.com/user-attachments/assets/4813ad88-46e5-4406-981d-71dbe98f8c66" />

## **Introduction**

AXCESSR is a data-driven assessment and decision platform designed to support student funding and success. It combines psychometric measurement, behavioural data, and predictive modelling to match students to suitable tertiary study pathways and funding opportunities.

The assessment generates insights into students’ interests, skills, and behavioural tendencies, which are used to predict academic success and inform funding decisions. Beyond assessment, AXCESSR forms part of a broader ecosystem that integrates assessment data, tracking, and financial information to support both students and funders.

## **Purpose of the Assessment**

The primary objectives of AXCESSR are to:

* Improve access to student funding
* Match students to programmes where they are likely to succeed
* Provide data-driven predictions of student outcomes
* Support risk assessment and management for funders

## How AXCESSR was built

AXCESSR was not built with data science as an afterthought. From initial construct mapping through to item validation and candidate screening, every stage of development was data-informed. The pipeline below illustrates how each phase fed into the next.

*Figure 1. AXCESSR Development Pipeline*

<img width="2475" height="1779" alt="Instrument Design" src="https://github.com/user-attachments/assets/5e99d5e7-f83d-4e2e-995c-a41c96b9e05c" />

The pipeline above illustrates the five core development phases of AXCESSR - from theoretical construct mapping through to the adaptive decision engine - each phase producing data that informed the next.

### **1) Product Conceptualisation**

AXCESSR is a psychometric-based credit risk assessment platform designed to extend financial access to individuals overlooked by traditional credit origination methods - either due to limited credit history or an overestimation of risk based on conventional metrics. Rather than relying on historical financial data, the platform evaluates creditworthiness through the measurement of stable personal dispositions shown to predict financial decision-making and repayment behaviour.

The platform targets two primary markets: the student loan market, where millions of academically eligible students lack access to funding, and the broader personal credit market, where thin-file and credit-invisible individuals remain underserved. Psychometric scores can be generated for any candidate irrespective of formal credit history and, because scores are user-generated, they are broadly compliant with consumer privacy regulations.

*Figure 2. Process for Obtaining a Student Loan*

<img width="700" height="400" alt="image" src="https://github.com/user-attachments/assets/96a27274-a8a4-4a9e-8c8a-c23037e195a7" />

### **2) Instrument Design**

Item development drew on a structured review of established psychometric frameworks, adapting content from validated instruments across each risk domain. Source instruments included the International Personality Item Pool (IPIP), the HEXACO Personality Inventory, the Schwartz Value Survey (SVS), the Trait Emotional Intelligence Questionnaire (TEIQue), the Short Dark Triad (SD3), the Edwards Compulsive Buying Scale (ECBS), the Barratt Impulsivity Scale, the Sensation Seeking Scale, and the UPPS Impulsive Behaviour Scale.

The resulting instrument assesses risk across four domains - Personality Risk, Values Risk, Emotion Traits Risk, and Emotion States Risk - each decomposed into higher-order factors and subfactors.

The below figure illustrates the diverse psychological frameworks and reputable assessment scales that were integrated to develop the AXCESSR item pool, highlighting the foundational instruments that informed its construction

*Figure 3. Frameworks Underpinning the AXCESSR Item Pool Development*

<img width="1000" height="700" alt="Instrument Design" src="https://github.com/user-attachments/assets/dbdc4bed-83db-49b3-99f0-bf6d39f32f78" />

### **3) Psychometric Validation**

#### Validation results  

Validation was conducted on the full cleaned dataset (after removing speeders, boundary cases, etc.). An initial EFA showed excellent overall fit but revealed many weak or cross‑loading factors. Domain‑level EFAs indicated that some subfactors were not meaningfully separated statistically. This provided evidence for collapsing certain subfactors into single dimensions and regrouping others into broader factors where the empirical structure diverged from the current specification. CFA models could not be estimated due to non‑positive definite covariance matrices, though the theorised structure was evident in composite-based correlation plots. Reliability analyses indicated that most subfactors fell below the 0.70 threshold, underscoring limited internal consistency.

#### Item removal diagnostics  

To address these issues, a flat higher‑order CFA was retained as an item‑level diagnostic. Standardised loadings onto higher‑order factors were used as one of three convergent item quality indicators, alongside IRT loadings estimated in isolated subfactor models and corrected item‑total correlations (r.drop). Items with CFA loadings below 0.30, low IRT loadings, and weak r.drop values were flagged as problematic. These diagnostics jointly informed item removal, after which validation analyses were rerun on the reduced set.

Convergent evidence across multiple methods led to the removal of 41 items, resulting in a streamlined 206‑item instrument (V2).

**Summary of Problematic items**

*Table 1. Summary of Problmeatic Items*

| Diagnostic | Total | Personality | Values | Emotion Traits | Emotion States |
|---|:---:|:---:|:---:|:---:|:---:|
| IRT subfactor loading (< 0.30) | 45 | 23 | 9 | 3 | 10 |
| CFA subfactor loading (λ < 0.30) | 75 | 41 | 15 | 5 | 14 |
| Item-total correlation (r < 0.30) | 98 | 51 | 19 | 8 | 20 |
| **Flagged by all three criteria** | **41** | **22** | **9** | **2** | **8** |

The above table summarises the three metrics used to assess the quality of items. Items that were flagged across all three metrics were defined as problematic and removed in V2.

#### Next steps

These findings represent a preliminary validation stage. High‑stakes data are still being collected and will be cross‑referenced with the current results. Final decisions regarding item removal and potential subfactor collapsing will be informed by analyses conducted on the high‑stakes dataset.

#### **Score Stability: Population Stability Index (PSI)**

A key question following item removal is whether the revised instrument produces materially different risk classifications. The Population Stability Index (PSI) is a metric widely used in credit risk modelling to quantify distributional shift between two scoring populations. A PSI below 0.10 indicates a stable distribution; values between 0.10 and 0.25 indicate moderate shift warranting investigation; values above 0.25 indicate significant drift requiring model review. PSI was computed between V1 (247-item) and V2 (206-item) total and domain-level scores to assess whether item removal destabilised candidate risk profiles.

*Table 2. Summary of Population Stability Index (PSI) Scores After Item Removal*

| Variable | PSI Score | Interpretation |
|---|:---:|---|
| Total Risk (Weighted) | 0.0997 | Stable — minor shift, no action required |
| Personality Risk | 0.0283 | Stable — distribution largely unchanged |
| Values Risk | 0.1884 | Moderate shift — high considering only 9 items were removed |
| Emotion Traits Risk | 0.0036 | Highly stable — negligible distributional change |
| Emotion States Risk | 0.0420 | Stable — minimal shift across versions |

The PSI results indicate that item removal had minimal impact on candidate risk classifications across most domains. Four of five scores fall within the stable range (PSI < 0.10), with Emotion Traits Risk showing negligible shift (PSI = 0.004) and Personality Risk and Emotion States Risk both well within acceptable bounds. The moderate shift observed in Values Risk (PSI = 0.19) is notable given that only 9 items were removed from this domain - suggesting those items were disproportionately influential in shaping the score distribution. Critically, no domain exceeds the intervention threshold of 0.25.

*Figure 4. Population Stability Index (PSI) by Domain*

<img width="1000" height="500" alt="psi_bar" src="https://github.com/user-attachments/assets/4c2737e4-1db2-4f40-a7c3-d4d8af2eb484" />

The bar chart confirms that distributional shift is concentrated in the Values domain. All other domains sit comfortably below the stable threshold, and the total weighted risk score sits precisely at the boundary (PSI = 0.10) - indicating that at the overall scoring level, V1 and V2 produce near-equivalent candidate classifications.

*Figure 5. Score Distributions: V1 (247 items) vs V2 (206 items)*

<img width="1000" height="600" alt="psi_density" src="https://github.com/user-attachments/assets/9e23745d-a946-49b0-80fe-bd023ae1fe69" />

The density curves corroborate the PSI findings. For Emotion Traits and Personality, the V1 and V2 distributions are almost indistinguishable. Emotion States and Total Risk show a slight tightening of the distribution in V2 - consistent with the removal of noisy items reducing score variance. The Values domain shows the most visible shift, with the V2 distribution marginally narrower and shifted slightly rightward, reflecting the influence of the removed items on the lower end of the score range. Across all domains, the core shape of the distribution is preserved, confirming that the revised instrument measures the same underlying constructs in a substantively equivalent way.

### **4) UX Research**

Psychometric rigour is a necessary but insufficient condition for a viable assessment product. UX research was conducted alongside validation to evaluate the candidate-facing experience and identify response variability attributable to presentation rather than construct variance.

*Table 3. UX MEtrics Summary*

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

##### Completion Times

Completion time provides a useful lens through which to examine candidate engagement. While most respondents worked steadily through the assessment, a subset completed unusually quickly, raising concerns about inattentive responding. The histogram below illustrates the spread of completion times across the full sample.

*Figure 6. Total Time Taken Distribution*

<img width="550" height="300" alt="image" src="https://github.com/user-attachments/assets/5b74b661-ccc0-4356-b3c8-239162a630b8" />

Completion times ranged from 39 seconds to nearly two hours (7155 seconds), with a median of 1834 seconds (~30 minutes) and a mean of 2043 seconds (~34 minutes). The central bulk of candidates fell between the first and third quartiles (1372–2525 seconds), indicating a typical completion window of 23–42 minutes. The right‑skewed distribution reflects a small group of candidates who took substantially longer, while the left tail captures the ~10% of speeders flagged for accelerated completion. This pattern underscores that the majority of candidates engaged at a reasonable pace, but a notable minority exhibited atypical response behaviour consistent with low engagement.

##### Person-Level Variance

Person-level standard deviations offer a useful perspective on response consistency across the assessment. Higher variability can indicate differentiated responding across items, while unusually low variability may suggest patterned or inattentive answering. The histogram below displays the distribution of standard deviations across all respondents.

*Figure 7. Person-Level Variance Distribution*

<img width="550" height="300" alt="image" src="https://github.com/user-attachments/assets/bd4bf96c-e4a8-4f3b-b709-dc5e3f0738b7" />

Person-level standard deviations ranged from 0.00 to 0.499, with a median of 0.345 and a mean of 0.333. The middle 50% of respondents fell between 0.291 and 0.393, indicating a typical band of moderate response variability. The distribution is slightly left-skewed, with most respondents clustering between approximately 0.30 and 0.40, and a thinner tail extending toward very low values. This lower tail suggests a small subset of respondents with minimal variation in their answers, potentially reflecting uniform or inattentive responding. Overall, the pattern indicates that most respondents demonstrated a reasonable degree of variability, consistent with engaged and differentiated answering, while a minority exhibited atypical response patterns.

#### **Response Quality Screening**

An initial sample of N = 2016 candidates completed the assessment. Prior to scoring, all responses were screened for indicators of low engagement using four data-driven criteria: accelerated completion (speeders), invariant responding (low variance), consecutive identical responses (long-string), and extreme endpoint selection (boundary overuse). The following table summarises the findings.

*Table 4. Summary of Response Quality Flags*

| Quality Flag | Criterion | Count | Percentage |
|---|---|:---:|:---:|
| Speeder | Completion time < 884 sec | 201 | 9.97% |
| Boundary Overuse | Proportion of 0s > 0.28 or 1s > 0.50 | 192 | 9.52% |
| Long-String | Longest string > 15 | 86 | 4.27% |
| Low Variance | SD < 0.111 | 50 | 2.48% |

*Note.* *Speeders* — completion time below the 10th percentile (< 884 seconds). 

*Low variance* — person-level response SD below one-third of the sample mean SD (< 0.111). 

*Long-string* — longest consecutive identical response sequence exceeding the 95th percentile (> 15). 

*Boundary overuse* — proportion of zero responses exceeding 0.28 or proportion of one responses exceeding 0.50, both derived from the 95th percentile. 

*Figure 8. Response Quality Flag*

The figure below illustrates the intersection structure of response quality flags across the 388 flagged candidates. Each bar represents a unique combination of criteria, with bar height indicating the number of candidates flagged by that particular combination.

<img width="787" height="486" alt="image" src="https://github.com/user-attachments/assets/a6fd24f8-7957-48cd-82c6-04a89e086db6" />

The majority of flagged candidates (144) were caught by the speeder criterion alone, with boundary overuse the second most common single flag (114). Co-occurring flags - where the same candidate triggered multiple criteria independently - account for 114 of the 388 flagged candidates, providing convergent evidence of low engagement in those cases.

#### Comparison

To assess differences in response consistency between groups, the figure below compares person-level variance for respondents flagged on quality checks versus those retained in the clean sample. Examining variability at the individual level provides insight into how consistently participants engaged with the assessment items.

*Figure 9. Comparison of Person-Level Variance in the Flagged and Clean Sample*

| Person-Level Variance in the Flagged Sample (N = 388) | Person-Level Variance in the Clean Sample (N = 1628) |
|--------|--------|
| <img width="400" height="280" alt="image" src="https://github.com/user-attachments/assets/27fd52c5-c121-4bd6-bc11-8f8951d6b42b" />|<img width="400" height="280" alt="image" src="https://github.com/user-attachments/assets/29f473f9-8214-4c90-9ec1-04cc975e63a5" />|

The flagged sample (N = 388) shows a broader and more irregular spread of person-level variance, including a noticeable concentration of lower-variance cases. In contrast, the clean sample (N = 1628) exhibits a more stable and tightly clustered distribution, suggesting more consistent and differentiated responding.

To better understand how flagged respondents differ from the rest of the sample, the figure below compares score distributions across key domains. Density curves are shown for both clean and flagged groups, allowing for a direct visual comparison of their response patterns.

*Figure 10. Comparison of Score Distributions Between the Flagged and Clean Sample*

<img width="787" height="486" alt="image" src="https://github.com/user-attachments/assets/07d91c35-5a24-4667-9f1b-fc0b9e4d2e8b" />

This comparison shows that respondents with quality flags exhibit noticeably different score patterns, with several domains displaying irregular or bimodal distributions. In contrast, the clean sample appears more stable and closer to expected distributional shapes. This divergence suggests that flagged responses may introduce noise or distortion, reinforcing the importance of removing or carefully reviewing suspicious respondents to maintain analytical rigor.

### **5) Decision Engine**

Candidate responses are scored against the revised 206-item instrument, aggregated across the four risk domains using a weighted composite approach, and converted to a total risk score on a standardised 0–1 scale. Candidates scoring below the 0.30 threshold are classified as lower risk and enter the funding consideration pool.

The engine supports computerised adaptive testing (CAT), whereby item selection is determined dynamically on the basis of prior responses — concentrating measurement precision where it is most needed and reducing burden where sufficient information has already been obtained.

AXCESSR demonstrates that rigorous psychometric methodology and scalable product engineering are not competing priorities. Each stage of development - from construct mapping to adaptive item delivery - was data-informed, and each data decision shaped the product.
