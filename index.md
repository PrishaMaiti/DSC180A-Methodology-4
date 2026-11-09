# DSC 180A Methodology Assignment 4

**Name:** Prisha Maiti

**Email:** prmaiti@ucsd.edu

**Section:** D07, The value of prediction for resource allocation

**Mentor:** Emily Aiken

## Quarter 2 Project Brainstorm

**1. What is the most interesting topic covered in your domain this quarter?**

The most interesting topic has been the welfare surface framework and the relative value of prediction from Fischer-Abaigar et al. (2026). Instead of only asking how accurate a poverty prediction model is, the framework asks how much social welfare improves when we invest in better prediction versus simply expanding the budget to reach more households. I found it surprising that, in some regimes, improving a targeting model's accuracy is worth much less than modestly increasing program coverage, which reframes model building as a policy decision rather than a purely technical one.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to apply the welfare surface framework to food assistance targeting in the United States using the Current Population Survey Food Security Supplement, which is publicly available household microdata. The investigation would build models that predict household food insecurity from the kinds of proxy variables an agency could realistically observe (income bands, household composition, employment, region), then trace out welfare surfaces to quantify how much a better predictor is worth relative to increasing the number of households a program can serve. This would test whether the conclusions from Ethiopia and Malawi hold in a high-income setting with a very different poverty distribution.

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

In Quarter 1 we evaluate models on randomly held-out households from the same survey wave. A change I would make is to evaluate temporally: train on an earlier LSMS wave and test on a later one. Real targeting programs deploy models on future populations, so this would show how much predictive accuracy, and therefore the relative value of prediction, decays as household conditions shift over time.

**4. What other techniques would you be interested in using in your project?**

I am interested in gradient boosted models with SHAP values to understand which features drive targeting decisions, conformal prediction to attach uncertainty estimates to each household's predicted welfare, and group fairness metrics to check whether errors in targeting fall disproportionately on particular regions or household types. I would also like to explore cost-sensitive evaluation that accounts for the expense of collecting each additional feature.
