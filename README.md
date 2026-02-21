# Bigquery-Python---Forecast-Diagnostics-SKU-Portfolio-Intelligence-Framework
End-to-end e-commerce forecasting diagnostics: ETL in BigQuery, Python EDA + clustering, forecast bias/error evaluation, and automated alerting with backtesting.

Forecast Diagnostics & SKU Portfolio Intelligence
Yes4All – Amazon Marketplace Analytics Project

End-to-end e-commerce diagnostic framework integrating ETL, portfolio analytics, lifecycle clustering, forecast bias evaluation, and automated alerting.
Business Context

Yes4All manages 200+ SKUs on Amazon across fitness and wellness categories.
Sales, projections, inventory, and event data existed in silos, limiting visibility into:

Forecast deviations

Revenue concentration risk

Product lifecycle maturity

Inventory misallocation

This project designs a unified diagnostic system to proactively monitor forecast performance and quantify financial exposure.

Framework Overview

The system integrates four analytical phases:

ETL in BigQuery – Standardized 5 datasets (23K+ transactions, 231 SKUs)

Portfolio Diagnostics – Active SKU trends, GMV analysis, Pareto concentration

Lifecycle Clustering – K-means segmentation using product age & launch timing

Forecast Diagnostics & Alerting – MAE, RMSE, MAPE, Bias + rolling anomaly detection

Key Portfolio Insights

~20 SKUs generate ~80% of total GMV (revenue concentration risk)

Sales decline in 2023 was driven by reduction in active SKUs, not product underperformance

Three distinct lifecycle trajectories identified:

Fast-to-market

Moderate traction

Severely delayed (>800 days to first order)

Lifecycle maturity impacts forecast stability and capital efficiency.

Forecast Evaluation

Forecast accuracy evaluated at category and SKU level using:

MAE

RMSE

MAPE

Bias (directional error)

Findings:

Errors are systematic and SKU-specific

Exercise Equipment Mats showed persistent under-forecasting (+48 unit bias)

Average metrics mask concentrated operational risk

Global model tuning alone cannot fix structural SKU-level bias.

Automated Alert Framework

Designed a rolling 3-month baseline alert system:

Threshold: 1.5σ above rolling MAD

Event-aware exclusion logic

Dual-level evaluation (SKU + category)

Backtesting Results:

Precision: 82.9%

Recall: 78.0%

Alert rate: 15.1%

Operationally deployable monitoring system.

Business Impact

Estimated annual exposure:

$115K excess inventory carrying cost

$165K lost revenue risk from under-forecasting

$78K–$195K recoverable via alert intervention

Total: $280K–$310K

Key Takeaways

Revenue concentration amplifies forecast risk

Portfolio contraction can drive sales decline

Forecast bias is directional and persistent

Rolling anomaly detection enables proactive intervention
