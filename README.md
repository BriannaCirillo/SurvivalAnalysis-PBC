# SurvivalAnalysis-PBC

# Primary Biliary Cholangitis (PBC) Survival Analysis

This project focuses on the analysis of survival data for patients with Primary Biliary Cholangitis (PBC), an autoimmune disease leading to the destruction of bile ducts in the liver. The dataset comes from a Mayo Clinic trial conducted between 1974 and 1984, investigating the effects of the drug D-penicillamine on PBC patients.

## Project Overview

The dataset includes 424 PBC patients, with 312 participants in the randomized clinical trial and 112 non-randomized participants. The analysis involves survival models, including Kaplan-Meier survival curves, Cox Proportional Hazard models, and Weibull models, to evaluate the effects of treatment, stage of disease, bilirubin, and other factors on patient survival.

### Key Objectives:
- Evaluate the survival rates of PBC patients based on treatment (D-penicillamine vs. placebo).
- Explore the impact of clinical variables such as bilirubin, albumin, and stage on survival outcomes.
- Use model selection techniques like AIC to identify the best-fitting survival models.
- Test for proportional hazards assumptions in the Cox model.

## Dataset

The data contains the following key variables:
- **age**: Age in years.
- **albumin**: Serum albumin levels (g/dl).
- **alk.phos**: Alkaline phosphatase (U/liter).
- **bilirubin**: Serum bilirubin (mg/dl).
- **cholesterol**: Serum cholesterol (mg/dl).
- **copper**: Urine copper (ug/day).
- **status**: Survival status (0 = censored, 1 = dead, 2 = transplant).
- **time**: Time in days from registration to death, transplant, or study analysis.
- **trt**: Treatment group (1 = D-penicillamine, 2 = placebo).

## Methodology

1. **Kaplan-Meier Survival Analysis**: 
   - Estimate survival curves for PBC patients and compare survival rates between treatment groups.
   - Median survival times are computed, and 95% confidence intervals are provided.

2. **Log-Rank Test**:
   - A log-rank test was used to compare the survival distributions of patients in different treatment groups.

3. **Cox Proportional Hazards Model**:
   - Cox models were applied to assess the impact of treatment and other covariates (e.g., bilirubin, albumin, stage) on survival.
   - The proportional hazards assumption was tested for each variable.

4. **Weibull Model**:
   - A Weibull survival model was fit to the data, and model assumptions were assessed.

5. **Model Selection**:
   - Akaike Information Criterion (AIC) was used to compare nested models and identify the best-fitting survival models.

## Results

- **Kaplan-Meier Analysis**: Median survival times for the treatment and control groups were similar, with no significant difference in survival curves based on the log-rank test (p-value = 0.5).
- **Cox Model**: The hazard ratio for D-penicillamine treatment was 0.88, indicating a slight (but non-significant) reduction in the hazard of death compared to the control group.
- **Significant Predictors**: Bilirubin, stage of disease, and age were significant predictors of survival. Higher levels of bilirubin and more advanced stages were associated with worse survival outcomes.
- **Model Fit**: The model including bilirubin, stage, and treatment had the best fit, as determined by AIC.

## Conclusion

The analysis revealed no significant survival benefit for patients receiving D-penicillamine compared to placebo. However, key clinical variables like bilirubin levels and disease stage had a significant impact on patient survival. The final Cox model, which included treatment, stage, bilirubin, and other covariates, was the best-fitting model.

