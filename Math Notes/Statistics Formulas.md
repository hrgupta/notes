# List of important Statistics formulas

## 1. **Confidence Interval**

$C.I = \bar{X}\pm Z_{\alpha/2} \sigma/\sqrt{n}$

## 2. **Margin of Error**

$S.E = Z_\alpha \sigma/\sqrt{n}$

## 3. **Sample Standard Deviation**

$S =\frac{\sqrt{\sum(x-\bar{x})^2}}{(n-1)}$

## 4. **Standard Error of the mean (SEM)**

$\sigma_{\bar{x}} =\frac{s}{\sqrt{N}}$

## 5. **1-Sample t-test**

$t = \frac{\bar{X}-\mu}{\frac{s}{\sqrt{N}}}$

## 6. **Paired t-test**

$t = \frac{\bar{d}}{S_d/\sqrt{n}}$

## 7. **2-Sample t-test**

$t = \frac{\bar{X_1}-\bar{X_2}}{\sqrt{\frac{s^2_1}{N_1}+\frac{s^2_2}{N_2}}}$

## 8. **Chi-Square Test**

$\chi^2 = \sum\frac{(O_i-E_i)^2}{E_i}$

## 9. **Regression (Explained) Sum of Squares**

$SSE = \sum\limits_{i=1}^{n}(\hat{y_i}-\bar{y})^2$

## 10. **Residual Sum of Squares**

$SSR = \sum\limits_{i=1}^{n}(y_i-f(x_i))^2$

## 11. **Total Sum of Squares**

$SST = SSE + SSR$

## 12. **Coefficient of Determination (R-Square)**

$R^2 = SSE/SST = 1-SSR/SST$

## 13. **ANOVA**

| Source  | $SS$          | $df$  | $MS$   | $F$         |
| ------- | ------------- | ----- | ------ | ----------- |
| Between | $SS_b$        | $k-1$ | $MS_b$ | $MS_b/MS_w$ |
| Within  | $SS_w$        | $N-k$ | $MS_w$ |
| Total   | $SS_b + SS_w$ | $N-1$ |

$SS_b =\sum\limits_{j=1}^{p} n_j(\bar{X_j}-\bar{X})^2$

$SS_w =\sum\limits_{j=1}^{p}\sum\limits_{i=1}^{n_j}(X_{ij}-\bar{X_j})^2$

$SS_t =\sum\limits_{j=1}^{p}\sum\limits_{i=1}^{n_j}(X_{ij}-\bar{X})^2$

$MS_b = \frac{SS_b}{k-1}$

$MS_w = \frac{SS_w}{N-k}$