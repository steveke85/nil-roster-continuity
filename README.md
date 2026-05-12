# NIL & Roster Continuity in College Basketball

**Does keeping your players together still matter?**

In July 2021, the NCAA introduced Name, Image, and Likeness (NIL) compensation and a one-time transfer waiver that eliminated the requirement for transferring players to sit out a season. This project examines how those policy changes reshaped the relationship between roster continuity and on-court performance across Division I men's basketball.

---

## Key Findings

1. **Continuity has collapsed.** Average roster continuity fell from ~51% pre-NIL to ~24% by 2026 — the sharpest single-era decline in the dataset.

2. **The predictive signal nearly vanished.** Continuity explained ~9% of AdjEM variance before NIL (slope: +0.24). Post-NIL, that dropped to ~2.3% (slope: +0.10). A 20 pct-pt continuity edge once predicted a ~4.7 AdjEM point performance gap; today it predicts roughly 2.0 points.

3. **Elite programs were hit hardest.** Top 100 programs saw their continuity-to-performance R² drop 78% (0.116 → 0.026). Bottom-tier programs dropped 51% (0.118 → 0.058). The transfer portal appears to allow elite programs to reload with high-impact transfers regardless of how many players return — decoupling continuity from success at the top.

---

## Data & Methodology

- **Dataset:** 5,949 Division I men's basketball team-seasons, 2008–2026
- **Source:** [KenPom.com](https://kenpom.com)
- **Dependent variable:** Adjusted Efficiency Margin (AdjEM) — net points per 100 possessions adjusted for opponent strength
- **Independent variable:** Roster continuity (% of minutes returning from prior season)
- **Method:** OLS linear regression with pre/post era comparison and tier interaction analysis
- **Exclusions:** 2020 (COVID-shortened season) and 2021 (NIL/portal transition year) excluded from both groups to avoid contaminating the pre/post comparison

**Era definitions:**
- Pre-NIL: 2008–2019
- Post-NIL/Portal: 2022–2026

**Tier definitions:**
- Top 100: teams ranked in the top 100 by average AdjEM within each era
- Bottom: all remaining Division I programs

---

## Visualizations

| Chart | What it shows |
|---|---|
| Continuity trend line | Average continuity across all D1 programs, 2008–2026 |
| Side-by-side scatter + regression | Continuity vs. AdjEM, pre- vs. post-NIL |
| 2×2 tier subplot | Regression by era × tier (top/bottom 100) |
| Grouped bar chart | R² comparison across all four era/tier combinations |

---

## Limitations

- Single-predictor model. Continuity was never a dominant driver of performance, and the post-NIL decline could reflect other structural changes — conference realignment, shifts in recruiting strategy, or the portal itself — rather than NIL alone.
- The post-NIL sample (5 years) is shorter than the pre-NIL sample (12 years), which affects statistical power.
- Correlation does not imply causation. A multivariate model controlling for recruiting class strength and roster composition would sharpen the causal story.

---

## Tools

- Python (pandas, scikit-learn, matplotlib, seaborn)
- Jupyter Notebook

---

## Background

This project was originally conducted as part of the **Michigan Sports Analytics Society** research program (2025–26) and was presented at the MSAS annual symposium. This repository is a full Python rebuild of the original Google Sheets analysis, with expanded visualizations and updated data through the 2026 season.

---

## Author

**Steven Kenny** — University of Michigan, B.S. Mathematics / Finance & Risk Management + B.S. Honors Data Science (Class of 2028)
