# 📊 Linear Regression -- Concepts & Assumptions

This document explains fundamental Linear Regression concepts including:

-   Ordinary Least Squares (OLS)
-   R² Interpretation
-   Regression Assumptions
-   Independence of Observations
-   Homoscedasticity vs Heteroscedasticity
-   Multicollinearity
-   Consequences of Assumption Violations

------------------------------------------------------------------------

# 1. Ordinary Least Squares (OLS)

Ordinary Least Squares is a method used to estimate regression
coefficients.

It minimizes:

Sum of squared residuals:\
Σ (yᵢ − ŷᵢ)²

Why squared error? - Prevents positive/negative errors from canceling
out - Penalizes large errors more heavily - Allows closed-form
mathematical solution - If residuals are normally distributed, OLS
equals Maximum Likelihood Estimation

------------------------------------------------------------------------

# 2. Intercept Interpretation

Regression equation:

ŷ = β₀ + β₁x₁ + ... + βₖxₖ

β₀ (Intercept) = Predicted value of Y when all X variables equal 0.

------------------------------------------------------------------------

# 3. R² (Coefficient of Determination)

R² = 1 − (SS_res / SS_tot)

R² represents:

The proportion of variance in the dependent variable explained by the
model.

Example: If R² = 0.80 → 80% of variation in Y is explained by
predictors. Remaining 20% is unexplained (noise or missing variables).

Important: R² does NOT imply causation or prediction accuracy
percentage.

------------------------------------------------------------------------

# 4. Regression Assumptions

1.  Linearity -- Relationship between X and Y is linear.
2.  Independence -- Error terms are independent.
3.  Homoscedasticity -- Constant variance of residuals.
4.  Normality -- Residuals are normally distributed (important for
    inference).
5.  No Multicollinearity -- Predictors are not highly correlated.

------------------------------------------------------------------------

# 5. Independence of Observations

Independence means: The error term of one observation does not depend on
another.

How to check:

Cross-sectional data: - Verify study design - Ensure no repeated
measurements - Ensure no clustering

Time-series data: - Durbin--Watson test (≈ 2 indicates no
autocorrelation) - Residual vs time plot - Autocorrelation Function
(ACF)

If independence fails: Standard errors and p-values become unreliable.

------------------------------------------------------------------------

# 6. Homoscedasticity vs Heteroscedasticity

Homoscedasticity: Residual variance remains constant across fitted
values.

Heteroscedasticity: Residual variance changes (often funnel-shaped).

Impact: Coefficients remain unbiased, but inference becomes unreliable.

------------------------------------------------------------------------

# 7. Multicollinearity

Occurs when independent variables are highly correlated.

Problems: - Inflated standard errors - Unstable coefficients - Sign
flipping - Harder interpretation

Detection: - Correlation matrix - Variance Inflation Factor (VIF \> 5 or
10 indicates concern)

------------------------------------------------------------------------

# 8. What Happens When Assumptions Fail?

Linearity fails → Model becomes biased\
Independence fails → Incorrect inference\
Heteroscedasticity → Wrong standard errors\
Non-normal residuals → Weak inference (small samples)\
Multicollinearity → Unstable coefficients

------------------------------------------------------------------------

# 🎯 Summary

-   OLS minimizes squared residuals.
-   R² measures explained variance.
-   Independence applies to error terms.
-   Homoscedasticity ensures reliable inference.
-   Multicollinearity affects coefficient stability.
