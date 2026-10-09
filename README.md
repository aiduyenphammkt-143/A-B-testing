# A/B Testing Case Study: Evaluating a New Checkout Flow

## 1. Business Context

A Southeast Asian e-commerce company observed that its **visitor-to-purchase conversion rate had plateaued** despite continuous growth in traffic.

To address this challenge, the Product and Engineering teams proposed **a redesigned checkout experience** featuring:

* Fewer checkout steps
* Clearer call-to-action (CTA) elements
* Better mobile optimization

The proposed redesign would require significant engineering resources and could affect downstream business performance. Therefore, management decided to validate its impact through a controlled A/B test before committing to a full rollout.

A cross-functional A/B testing framework was designed involving:

* Product Team: defined business objectives and success criteria.
* Engineering Team: implemented the new checkout experience and experiment infrastructure.
* Business Stakeholders: defined rollout requirements and acceptable risk thresholds.
* Data Analyst: validated the experiment and quantified business impact.

**Experiment Details**

| Component | Experiment Design |
|----------|----------|
| Duration | 4 weeks |
| Population | New users entering the platform |
| Randomization Unit | User level |
| Control Group | Existing checkout flow |
| Treatment Group | New checkout flow |

## 2. Critical analysis question

The company needed to answer a critical business question:

> Should the new checkout flow be rolled out to all users?

A decision based solely on conversion rate could be misleading because:

* More purchases do not always translate into more revenue.
* Faster checkouts may attract lower-quality purchases.
* Changes can negatively affect retention even if short-term conversion improves.

**The key challenge was determining whether the new experience creates sustainable business value while minimizing operational and revenue risks.**

## 3. Role of the Data Analyst

The purpose of the analysis was not only to determine whether the treatment increased conversion, but also to answer:

* Is the observed uplift statistically reliable?
* Is the improvement large enough to justify rollout costs?
* Does conversion growth create revenue growth?
* Does the change introduce retention risks?
* What uncertainties still exist before deployment?

By **quantifying both upside potential and business risks**, the analysis enables decision-makers to make **evidence-based rollout decisions** rather than relying on intuition or isolated metrics.

## 4. Key Findings & Recommendation

### Key Findings

✅ **The new checkout flow increases conversion, showing a statistically significant uplift versus the existing experience.**

* **Absolute conversion lift: +1.65%**
* **Relative improvement: +13.4%**<br>

The redesigned checkout experience helps more users complete purchases, suggesting that simplifying the journey successfully reduces checkout friction.

⚠️ **Conversion growth has not yet translated into proven business value.**

While more users are buying, there is no clear evidence that they are generating more revenue. This suggests the treatment may be converting additional lower-value customers rather than increasing overall customer spend.

✅ **No immediate retention risk detected.**

The experiment found no meaningful deterioration in churn. However, the data are not yet strong enough to completely rule out small downstream retention effects.

⚠️ **Friction may exist beyond the checkout stage.**

Users with unusually long sessions do not spend more, convert more, or retain better. This indicates that customer hesitation may occur earlier in the purchase journey, limiting the overall impact of the checkout redesign.

⚠️ **Rollout decision remains uncertain.**

The treatment delivers a positive conversion signal, but the evidence is not yet sufficient to confirm a meaningful improvement in revenue or long-term customer value.

### Recommendation

* Do not proceed with a full rollout yet; continue testing and data collection to reduce uncertainty around revenue impact.
* Extend the experiment to validate revenue impact with greater confidence.
* Investigate the behavior of high-session users to understand potential friction in the checkout journey.
* Collect additional post-purchase and customer experience data to better understand churn drivers and long-term business impact.

## 5. Methodology

### **Phase 1: EDA & Validity Check**

Before measuring impact, the experiment was audited to ensure trustworthy results and explored customers' behaviors:

* Data quality assessment
* Missing value and duplicate checks
* Randomization validation
* Geography and demographic balance checks
* Behavioral profile analysis

### **Phase 2: Statistical Analysis**

| Analytical aspect | Objective | Metrics Evaluated |
|----------|----------|----------|
| Primary Success Metric | Measure the direct impact of the new checkout flow on purchase completion. | • Conversion Rate<br> • Absolute Conversion Lift<br> • Relative Conversion Lift (Relative Risk) |
| Trade-off Analysis (Within the mechanism) | Verify whether higher conversion translates into meaningful economic value. | • Average Revenue per Buyer (ARPB)<br>• Average Revenue per User (ARPU) |
| Guardrail Metrics (Outside the Conversion Mechanism) | Ensure the treatment does not harm overall business health. | • Overall Churn Rate<br>• Buyer Churn Rate |

## 6. Skills Demonstrated
* Experimental Design
* A/B Testing
* Statistical Inference
* Confidence Interval Interpretation
* Product Analytics
* Conversion Optimization
* Customer Retention Analysis
* Exploratory Data Analysis (EDA)
* Business Storytelling

## 7. Repository Structure

```text
├── Analysis Notebook/
│   ├── Phase 1_EDA_Validity_Check.ipynb
│   │   └── Validates data quality and experiment integrity through EDA, randomization checks, user segmentation analysis, and bias assessment.
│   └── Phase 2_AB_tessting_Statistical_analysis.ipynb
│       └── Quantifies treatment effects on conversion, revenue, and retention using statistical inference and business impact assessment.
├── Data/
│   ├── AB testing_new check out flow.csv
│       └── User-level A/B testing dataset collected during a 4-week checkout flow experiment.
└── README.md
    └── End-to-end case study covering business context, analytical approach, key insights, and rollout recommendations.
```
