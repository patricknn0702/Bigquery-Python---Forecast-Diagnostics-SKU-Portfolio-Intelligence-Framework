# 📊 BigQuery & Python — Forecast Diagnostics & SKU Portfolio Intelligence Framework

End-to-end e-commerce forecasting diagnostics system integrating:

- ETL in BigQuery  
- Python EDA & lifecycle clustering  
- Forecast bias and error evaluation  
- Automated rolling alerting with backtesting  

---

## I. Project Overview  
**Yes4All – Amazon Marketplace Analytics**

This project builds a unified diagnostic framework to monitor and evaluate forecast performance across a 200+ SKU Amazon portfolio.

The system integrates:

- Portfolio monitoring  
- Lifecycle segmentation  
- Forecast accuracy diagnostics  
- Anomaly detection and alert validation  

<img width="1469" height="872" alt="image" src="https://github.com/user-attachments/assets/9b3e2b15-a77c-405b-a721-048f158cb4a3" />


## II. Business Context

Yes4All manages 200+ SKUs across fitness and wellness categories on Amazon.

Sales, projections, inventory, and event data existed in silos, limiting visibility into:

- Forecast deviations  
- Revenue concentration risk  
- Product lifecycle maturity  
- Inventory misallocation  

This project designs a centralized monitoring system to proactively evaluate forecast reliability and quantify financial exposure.

<img width="1558" height="661" alt="image" src="https://github.com/user-attachments/assets/022f0a9e-bb25-4156-8db0-ec5d56209487" />

<img width="1562" height="754" alt="image" src="https://github.com/user-attachments/assets/d604cc9b-24ca-454c-8c16-2f58ad5f7b9f" />
## III. Framework Architecture

The framework integrates four analytical phases:

### 1️⃣ ETL in BigQuery
- Standardized 5 datasets  
- 23K+ transaction rows  
- 231 SKUs  
- Cleaned identifiers, numeric casting, date normalization  

### 2️⃣ Portfolio Diagnostics
- Active SKU trend analysis  
- Monthly sales & GMV trends  
- Pareto revenue concentration (~20 SKUs generate ~80% of GMV)  

### 3️⃣ Lifecycle Clustering
- K-means segmentation  
- Features: product age, launch-to-first-order timing  
- Three lifecycle trajectories identified:
  - Fast-to-market  
  - Moderate traction  
  - Severely delayed (>800 days to first order)  

Lifecycle maturity directly impacts forecast stability and capital efficiency.

### 4️⃣ Forecast Diagnostics & Alerting
- Accuracy metrics: MAE, RMSE, MAPE  
- Directional bias analysis  
- Rolling anomaly detection (MAD-based threshold)  

<img width="1555" height="640" alt="image" src="https://github.com/user-attachments/assets/36246bd5-b829-4a87-9ef5-bb7b1ddcb292" />

## IV. Key Portfolio Insights

- 2023 sales decline was driven by **reduction in active SKUs**, not product underperformance  
- Revenue concentration amplifies forecast risk  
- Forecast errors are systematic and SKU-specific  
- Lifecycle maturity influences forecast stability  
<img width="1637" height="751" alt="image" src="https://github.com/user-attachments/assets/bee4c17a-7a3f-40e8-aeab-e8c6ae4391b6" />
<img width="1663" height="723" alt="image" src="https://github.com/user-attachments/assets/a5ed7536-eeb8-4df2-891b-ff079b1a3f43" />
<img width="1638" height="703" alt="image" src="https://github.com/user-attachments/assets/6f18cf9e-b943-44b9-b025-39b7b25b0b2f" />
<img width="1629" height="844" alt="image" src="https://github.com/user-attachments/assets/0fa12cfb-3300-4bd4-8f7c-8aa646528a30" />
<img width="1497" height="762" alt="image" src="https://github.com/user-attachments/assets/b3c53f93-8786-463e-a493-9913ba21ebcd" />
<img width="1655" height="664" alt="image" src="https://github.com/user-attachments/assets/365b1707-26c9-42f7-bf77-c0045cfe6ce8" />
<img width="1424" height="838" alt="image" src="https://github.com/user-attachments/assets/fd09b0a4-b57a-410f-ab91-795b5520a9d0" />
<img width="1604" height="864" alt="image" src="https://github.com/user-attachments/assets/1e1eda53-e4e2-4c8b-8377-889e80e2f1ff" />
<img width="1583" height="836" alt="image" src="https://github.com/user-attachments/assets/3d5a945b-c94f-4fa2-a1d1-d4361e6b5560" />
<img width="1541" height="917" alt="image" src="https://github.com/user-attachments/assets/6febcc87-a879-4a89-a245-eea98c0303a6" />
<img width="1361" height="790" alt="image" src="https://github.com/user-attachments/assets/454c06e7-4c1a-4725-8194-8ee650d393db" />
<img width="1593" height="887" alt="image" src="https://github.com/user-attachments/assets/fc2d43b8-bbfb-498c-bc26-2bfe6c6c12b2" />
<img width="1379" height="780" alt="image" src="https://github.com/user-attachments/assets/b4f7e554-0254-46eb-bb3b-f241c856e0c3" />
<img width="1563" height="820" alt="image" src="https://github.com/user-attachments/assets/00a3a972-8798-4395-a69e-82bd3ecd19c9" />
<img width="1570" height="813" alt="image" src="https://github.com/user-attachments/assets/71b32c1c-6f8d-4cae-9568-e82eab6f50ec" />

## V. Forecast Evaluation

Forecast accuracy was evaluated at both category and SKU levels using:

- **MAE** (Mean Absolute Error)  
- **RMSE**  
- **MAPE**  
- **Bias** (directional error)

### Key Findings

- Exercise Equipment Mats showed persistent under-forecasting (+48 unit bias)  
- SKU-level MAE ranged from minimal to 500+ units  
- Average metrics mask concentrated operational risk  

Global model tuning alone cannot resolve structural SKU-level bias.

## VI. Automated Alert Framework

Designed a rolling 3-month monitoring system with:

- Threshold: 1.5σ above rolling Median Absolute Deviation  
- Event-aware exclusion logic  
- Dual-level evaluation (SKU + category)  

### Backtesting Results

- **Precision:** 82.9%  
- **Recall:** 78.0%  
- **Alert Rate:** 15.1%  

The alert system balances responsiveness with operational manageability.


## VII. Business Impact
<img width="1602" height="756" alt="image" src="https://github.com/user-attachments/assets/84af314b-e45d-4347-80ec-3dfa4b5c5af7" />

Estimated annual exposure identified:

- $115K excess inventory carrying cost  
- $165K lost revenue risk from under-forecasting  
- $78K–$195K recoverable via alert intervention  

### Total Estimated Exposure:
> **$280K–$310K annually**


## VIII. Key Takeaways

- Revenue concentration amplifies forecast risk  
- Portfolio contraction can drive sales decline  
- Forecast bias is directional and persistent  
- Rolling anomaly detection enables proactive intervention  
<img width="1565" height="848" alt="image" src="https://github.com/user-attachments/assets/42225a90-b65f-46e0-8164-d1f19ec663ba" />
<img width="1583" height="848" alt="image" src="https://github.com/user-attachments/assets/d797b12b-d509-4049-ae66-da53dd019871" />



**Author:**  
Patrick Nguyen  
M.S. Business Analytics  
Growth & Marketplace Analytics Focus
