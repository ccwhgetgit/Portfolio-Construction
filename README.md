# Portfolio-Construction Analysis (DBA 3713 - Analytics for Risk Management)

## Overview
This project involves the in-depth analysis of 48 industry portfolios to optimize the risk-return tradeoff. Utilizing the Fama-French Three-Factor Model, this report demonstrates the construction of efficient portfolios, both in-sample and out-of-sample, with a focus on covariance shrinkage techniques and robust matrix estimation.

## Introduction
The objective of this analysis is to construct an optimal investment portfolio that maximizes returns over a five-year horizon while minimizing risk. This involves detailed preprocessing, portfolio construction, and performance analysis using various financial models and statistical methods.

## Preprocessing
The initial step in the analysis involved calculating the excess returns of the 48 industry portfolios. This data forms the foundation for constructing and analyzing the portfolios.

## Fama-French Three-Factor Model
The Fama-French Three-Factor Model enhances the traditional Capital Asset Pricing Model (CAPM) by incorporating additional factors, namely:
1. **Market Risk (MKT)**: The excess return on the market.
2. **Size (SMB)**: The return of small-cap stocks minus large-cap stocks.
3. **Value (HML)**: The return of high book-to-market stocks minus low book-to-market stocks.

These factors help explain variations in portfolio returns more comprehensively than CAPM alone.

## Portfolio Construction and In-Sample Analysis
### Basic Portfolio Construction
Four portfolios were constructed using historical data:
1. **Market Portfolio (MKT)**
2. **Equally Weighted Portfolio (EWP)**
3. **Tangency Portfolio (TAN)**
4. **Global Minimum Variance Portfolio (GMV)**

The performance of these portfolios was evaluated using metrics such as expected return, standard deviation, and Sharpe ratio.

### In-Sample Efficient Frontier
The in-sample efficient frontier was plotted, displaying the optimal portfolios that offer the highest expected return for a given level of risk.

## Robust Portfolio Construction and Out-of-Sample Analysis
To ensure robustness and better performance in real-world scenarios, two methods were employed:

### Direct Intervention Method
A small constant (epsilon) was added to the diagonal elements of the covariance matrix to ensure numerical stability. This adjustment improved the stability but required validation through out-of-sample analysis.

### Shrinkage Estimation Method
Shrinkage techniques, proposed by Ledoit and Wolf, were used to combine the sample covariance matrix with a structured estimator, improving the robustness of the covariance matrix. A range of shrinkage intensities (lambda) was tested to find the optimal value.

## Out-of-Sample Performance
The out-of-sample performance was evaluated to validate the robustness of the constructed portfolios. The shrinkage constant method with a lambda of 0.80 provided the most stable and robust performance, minimizing the difference in Sharpe ratios between realized and true portfolios.

## Final Recommendation
Based on the analysis, the portfolio constructed with a shrinkage intensity of 0.80 was recommended. This portfolio demonstrated an annual excess return of 5.89% with a Sharpe ratio of 0.245.
