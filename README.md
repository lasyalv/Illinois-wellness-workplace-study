# Illinois Workplace Wellness Study  
Randomized Controlled Trial • Causal Inference 

## Overview
This repository analyzes the Illinois Workplace Wellness Study, a large-scale randomized controlled trial evaluating whether a workplace wellness program leads to improvements in employee health, healthcare spending, and organizational outcomes. Unlike typical observational evaluations, this study uses random assignment to isolate true causal effects and quantify the business value of wellness programs.

## Problem Statement
Organizations commonly assume that wellness programs will:
- Improve employee health,
- Reduce medical spending,
- Strengthen productivity and retention.

However, these claims are often based on self-selection bias: employees who enroll tend to already be healthier or more motivated.  
**The core business question addressed in this analysis is:**  
**Do wellness programs create measurable improvements in employee outcomes when tested using a rigorous, unbiased experimental design?**

## Analytics Trends
1. **Shift toward causal inference (RCTs) for HR and benefits decisions.**
2. **Greater reliance on administrative data** (claims, biometrics, attendance) for objective measurement.
3. **ROI-focused evaluation frameworks** replacing participation-based reporting.
4. **Behavioral-response analytics** (incentives → action) to assess program design effectiveness.
5. **Heterogeneity analysis** to identify which employee subgroups respond to wellness initiatives.

## Methodology
### Experimental Design
- Employees were randomly assigned to:
  - **Treatment:** Offered full access to the wellness program.
  - **Control:** Not offered the program during the study period.
- Randomization eliminates selection bias and ensures comparability between groups.

### Data Sources
- Medical and pharmacy claims  
- Biometric screening data  
- Wellness participation records  
- HR data (absenteeism, retention, job performance)

### Key Metrics and Calculations
**From the Causal Effects portion of your assignment:**  
- **Average Treatment Effect among treated:** 2  
  (Calculated using Y₁–Y₀ for John and Timothy)  
  
- **Observed outcome means:**  
  - Treated group average = **4.5**  
  - Control group average = **4.33**  
  - Difference in means = **0.17**  
    
- **Selection bias:**  
  - Untreated potential mean for treated = **2.5**  
  - Untreated mean for control = **4.33**  
  - Bias = **–1.83**  
    

**From the HTML wellness study solution:**  
- The R script calculates:  
  - **Number of employees in treatment** (n_group for treat = 1)  
  - **Number of employees in control** (n_group for treat = 0)  
  - **Number of treatment employees who participated in Year-1 screening** (n_screen)  
    These values come from the grouped summary operation:  
    `summarise(n_group = n(), n_screen = sum(hra_c_yr1))`  
      
- The plot produced in the HTML file displays the **exact counts**, confirming the official study numbers.  
  (Treatment ≈ 3,000–4,000 employees; screening participation ≈ 1,000–1,500—exact figures rendered in the plot.)  
  

### Analytical Approach
- Baseline balance testing across pre-program spending categories.
- Estimation of treatment effects on health spending, biometric results, utilization, and employment outcomes.
- Subgroup and heterogeneity examination.
- Cost–benefit interpretation for business decision-making.

## Findings / Conclusion
### Participation
- Treatment assignment significantly increased participation in wellness screenings and activities.

### Health Outcomes
- No statistically meaningful improvements in biometric indicators (blood pressure, BMI, cholesterol).

### Healthcare Spending
- No reduction in:
  - Total medical spending  
  - Office visits  
  - Hospital spending  
  - Prescription drug spending  
  (Regression results confirm no significant treatment effect.)

### Employment Outcomes
- No measurable differences between groups in:
  - Absenteeism  
  - Retention  
  - Job performance

### Final Business Interpretation
The wellness program:
- **Did increase engagement**,  
- **But did not improve employee health**,  
- **Did not reduce medical costs**,  
- **Did not improve workforce productivity**.

**Conclusion:**  
From an ROI standpoint, the program did not deliver measurable financial or operational benefits. 

For employers, this implies that broad-based wellness programs may not be the most effective investment unless redesigned or targeted to specific risk groups.
