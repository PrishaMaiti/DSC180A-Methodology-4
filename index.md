# DSC 180A Methodology Assignment 4

**Name:** Prisha Maiti

**Email:** prmaiti@ucsd.edu

**Section:** D07, The value of prediction for resource allocation

**Mentor:** Emily Aiken

## Quarter 2 Project Brainstorm

**1. What is the most interesting topic covered in your domain this quarter?**

The most interesting topic has been the welfare surface framework and the relative value of prediction from Fischer-Abaigar et al. (2026). Instead of only asking how accurate a poverty prediction model is, the framework asks how much social welfare improves when we invest in better prediction versus simply expanding the budget to reach more households. I found it surprising that sometimes, improving a targeting model's accuracy is worth much less than increasing program coverage, which reframes model building as a policy decision rather than a purely technical one.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

The rapid growth of AI data centers is placing new pressure on two shared resources: local water supplies and the electric grid. Agencies responsible for managing these pressures have limited capacity, whether that means budgets for water conservation and oversight in at-risk communities or engineering staff to study the thousands of energy projects waiting to connect to the grid, most of which are never built. I will apply the welfare-surface framework to both settings: first, allocating water mitigation resources across counties that host or are projected to host data centers, using drought and water stress data to measure where need actually materializes; and second, prioritizing grid interconnection requests using LLNL's national queue data. In each case, I will measure the relative value of better prediction versus expanded capacity, and test whether prediction becomes more valuable as data center growth intensifies demand. As someone working in tech and agentic AI, I want to take the physical footprint of my own industry seriously and contribute evidence on how communities and infrastructure can keep pace with it.

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

In Q1, prediction quality only varied through the label fraction, the share of households with PMT data collected. The model itself stayed fixed as a single LASSO regression. That fits a survey setting where collecting data is the main cost, but grid operators and water agencies already have data on every unit, so what they can invest in is a better model. For Q2, I would vary model quality directly by building a ladder of predictors of increasing accuracy and putting that on the welfare surface against capacity. I would also replace random train/test splits with time-based splits, training on earlier years and testing on later ones, so the results reflect how an agency would actually forecast. Q1 also showed that conclusions depend heavily on the welfare definition (the data-to-capacity ratio was 0.57 under step utility but 2.64 under CRRA), so I would test several welfare definitions and cost assumptions instead of fixing one.

**4. What other techniques would you be interested in using in your project?**

I’d like to use gradient boosting models such as XGBoost to build the stronger end of the prediction ladder and capture nonlinear patterns a linear model misses. I’m also interested in geospatial analysis to connect data center locations to counties, watersheds, and transmission infrastructure, and in survival analysis to handle queue projects that are still active and have no final outcome yet. Beyond that, I’d use PNNL's projected data center growth scenarios to simulate whether prediction becomes more valuable as demand grows, as well as subgroup analysis to check whether allocations favor some regions over others.
