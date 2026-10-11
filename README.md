#Exploratory Data Analysis: Online Retail Dataset

## 1. Project Overview & Data Preprocessing
* **Raw Dataset Scale:** 541,909 total order records with 8 primary attributes.
* **Data Cleaning Steps:**
  * Dropped missing `CustomerID` records (135,080 rows removed).
  * Filtered out order cancellations (`InvoiceNo` starting with 'C') and invalid non-positive unit prices or quantities.
  * Removed duplicate transaction entries.
* **Cleaned Dataset Scale:** 392,692 valid, high-fidelity records retained for downstream analysis.
* **Engineered Features:** Created `TotalSales` (`Quantity` × `UnitPrice`), `YearMonth`, `DayOfWeek`, and `Hour` to enable granular temporal and revenue modeling.

---

## 2. Key Data Insights & Visual Trends

### Sales Growth & Seasonality
* **Peak Revenue Period:** Revenue surges significantly during Q4 (September to November), reaching a peak in November at over 1.15 million GBP.
* **Seasonal Pullback:** December shows a steep decline due to partial monthly data recording and post-holiday tapering.

### Revenue Concentration & Geographic Distribution
* **Dominant Market:** The United Kingdom accounts for **82.0%** of total global sales.
* **Top International Markets:** Netherlands leads non-UK revenue, followed by EIRE, Germany, France, and Australia.

### Customer Purchasing & Operational Patterns
* **Peak Hourly Activity:** Order volume and revenue concentrate heavily between **10:00 AM and 3:00 PM**, peaking around 12:00 PM.
* **Busiest Days:** Thursday delivers the highest total sales volume, followed by Tuesday and Wednesday. Sunday shows the lowest revenue.

### Statistical Correlations & Outliers
* **Strong Linear Determinant:** Total Sales correlates almost perfectly with Quantity ($r = 0.91$), whereas Unit Price shows negligible correlation with Total Sales ($r = 0.08$).
* **Outlier Characteristics:** While Unit Prices remain concentrated below 5 GBP, extreme quantity order spikes (e.g., bulk international wholesale orders in the Netherlands) drive significant variance.

---

## 3. Metric & Visualization Summary Matrix

| Metric Category | Key Finding / Observation | Primary Visual Indicator |
| :--- | :--- | :--- |
| **Monthly Trend** | Q4 volume peak in November ($\approx 1.15\text{M GBP}$) | Line Plot (Monthly Revenue Trend) |
| **Geographic Split** | UK ($82\%$) vs. Rest of World ($18\%$) | Pie Chart (UK vs. World Share) |
| **Top International Markets** | Netherlands, EIRE, and Germany lead international revenue | Bar Chart (Top 10 International Markets) |
| **Top Product** | Paper Craft, Little Birdie & Regency Cakestand 3 Tier | Horizontal Bar Chart (Top Products) |
| **Peak Sales Hours** | Operational peak between 10:00 AM and 2:00 PM | Heatmap & Count Plot (Day vs. Hour) |
| **Key Correlation** | High correlation between Quantity and Total Sales ($r = 0.91$) | Correlation Matrix Heatmap |

---

## 4. Operational & Strategic Recommendations

1. **Inventory & Stocking Prep:** Scale warehouse inventory and supply chain throughput starting in August to meet peak Q4 demand surges (September–November).
2. **Targeted Promotions:** Schedule email marketing campaigns and daily flash sales around midday peak hours (11:00 AM–1:00 PM) on high-converting days (Tuesday–Thursday).
3. **International Expansion:** Standardize bulk order logistics and targeted customer retention for high-value wholesale accounts in the Netherlands, Germany, and EIRE.
