# 🧪 Feature Adoption & A/B Testing Analysis

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![PowerBI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-00e5a0?style=flat)

> **22% lift in task completion rate** and improved 30-day retention — validated
> through a controlled A/B test on 1,000+ users across 3 segments.

---

## 🧩 Problem Statement

An advanced reporting feature on an AI SaaS platform had only **12% adoption**
across 3 user segments — despite being one of the platform's highest-value
capabilities.

The business question was:
> *"Why are users not discovering or using the advanced reporting feature,
> and can a change to the onboarding flow measurably improve adoption and
> retention?"*

---

## 🎯 Objective

- Quantify the feature adoption gap across user segments
- Identify which segments showed the lowest adoption and why
- Design a controlled A/B test to validate a directed onboarding solution
- Measure impact on task completion rate and 30-day retention
- Build a live dashboard for ongoing monitoring post-launch

---

## 🔬 Hypothesis

> If new users are shown a **directed onboarding flow** that contextually
> surfaces the advanced reporting feature at the right moment, they will
> complete the core task at a higher rate — and return more often within
> 30 days — compared to users on the standard onboarding flow.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| SQL + BigQuery | Test assignment, result queries, retention analysis |
| Power BI | Live monitoring dashboard (adoption, DAUs, funnel, retention) |
| Excel | Pre-analysis, segment breakdown, results visualisation |
| A/B Testing | Controlled experiment design, lift measurement |
| User Segmentation | 3-segment breakdown for balanced test assignment |

---

## 🔍 Methodology

**1. Adoption Baseline Analysis**
Queried event data to establish that only 12% of users across 3 segments
had ever used the advanced reporting feature. Broken down by segment, device,
and region to confirm the gap was consistent — not isolated to one group.

**2. Test Design**

| Parameter | Detail |
|---|---|
| Sample size | 1,000+ users |
| Groups | Control (standard flow) vs Variant (directed flow) |
| Split | 50/50, stratified across all 3 user segments |
| Primary metric | Task completion rate |
| Secondary metric | 30-day retention rate |
| Test duration | Full billing cycle to capture retention signal |

**Control group** — experienced the existing standard onboarding flow with
no changes.

**Variant group** — experienced a directed onboarding flow with contextual
prompts that surfaced the advanced reporting feature at the moment most
relevant to their workflow.

**3. Results Analysis**
Used conditional SQL aggregation to calculate both metrics side by side for
control and variant. Computed absolute lift, percentage lift, and confirmed
results across all 3 segments independently to rule out Simpson's paradox.

**4. Dashboard Build**
Built an automated Power BI dashboard post-launch tracking feature adoption
rate, DAUs, funnel conversion, and 30-day retention — used by stakeholders
for weekly monitoring.

---

## 📈 Results

### A/B Test Outcome

| Metric | Control | Variant | Lift |
|---|---|---|---|
| Task Completion Rate | baseline | +22% | **+22%** ✅ |
| 30-Day Retention | baseline | improved | significant |
| Feature Adoption Rate | 12% | growing | tracked live |
| Users tested | ~500 | ~500 | 1,000+ total |

### Adoption Baseline by Segment

| User Segment | Adoption Rate | Gap vs Target |
|---|---|---|
| Segment A | 18% | −32 pts |
| Segment B | 11% | −39 pts |
| Segment C | 7% | **−43 pts** ⚠️ |

Segment C had the lowest adoption and was the highest-priority target for
the directed onboarding intervention.

---

## 💡 Business Impact

- **+22% task completion rate** in the variant group — adopted as the new
  default onboarding flow for all new users
- **Improved 30-day retention** — confirmed the improvement was behavioural,
  not a one-time spike
- **Live Power BI dashboard** adopted by stakeholders for weekly product reviews
- Findings directly influenced the **product roadmap for the following quarter**
- Connected to Project 1: this test validated the interactive walkthrough
  recommendation made after the funnel analysis

---

## 📊 Dashboards

![A/B Test Results](dashboards/ab_test_results.png)
*Control vs variant — task completion rate comparison*

![Feature Adoption by Segment](dashboards/feature_adoption_baseline.png)
*12% baseline adoption broken down across 3 user segments*

![30-Day Retention Comparison](dashboards/retention_comparison.png)
*Retention curve: control group vs variant group over 30 days*

![Live Monitoring Dashboard](dashboards/powerbi_dashboard.png)
*Automated Power BI dashboard tracking adoption, DAUs, funnel, and retention*

---

## 📁 Repository Structure
```
feature-adoption-ab-testing/
│
├── queries/
│   ├── 01_feature_adoption_baseline.sql   # 12% adoption baseline by segment
│   ├── 02_ab_test_assignment.sql          # User split: control vs variant
│   ├── 03_ab_test_results.sql             # Task completion lift calculation
│   └── 04_retention_by_group.sql          # 30-day retention cohort comparison
│
├── dashboards/
│   ├── ab_test_results.png                # Control vs variant bar chart
│   ├── feature_adoption_baseline.png      # Adoption by segment
│   ├── retention_comparison.png           # 30-day retention curve
│   └── powerbi_dashboard.png             # Full live monitoring dashboard
│
├── data/
│   └── sample_data.csv                    # Anonymised 50-row sample dataset
│
├── notebooks/
│   └── ab_test_analysis.ipynb             # Statistical analysis (Python)
│
└── README.md
```

---

## 🔑 Key Skills Demonstrated

`A/B Testing` `Experiment Design` `Feature Adoption Analysis` `User Segmentation`
`SQL` `BigQuery` `Power BI` `Excel` `Cohort Analysis` `Retention Analysis`
`KPI Definition` `Dashboard Automation` `SaaS Analytics`

---

## 📌 Related Projects

| Project | Description | Link |
|---|---|---|
| SaaS Onboarding Funnel Analysis | Identified the 40% drop-off that led to this experiment | [View →](https://github.com/omkarpattnaik8080/saas-onboarding-funnel-analysis) |

---

*If Project 1 found the problem, Project 2 proved the fix.*
*Together they represent a complete product analytics cycle: diagnose → hypothesise → test → validate.*
