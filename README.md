# 🏡 Airbnb Open Data Analysis

## 📘 Overview

This project explores **Airbnb’s open dataset** to uncover insights into **listing trends, pricing patterns, host behaviors**, and **property characteristics** across different neighborhoods.
Through data cleaning, preprocessing, and visualization, we aim to reveal meaningful relationships and patterns that influence Airbnb’s market dynamics.

---

## 📂 Dataset

* **File Used:** `1730285881-Airbnb_Open_Data.xlsx`
* **Total Records:** Cleaned and analyzed after removing duplicates and invalid entries.
* **Data Source:** Publicly available Airbnb open data.

---

## 🧰 Tools & Libraries

This project leverages Python’s powerful data analytics and visualization ecosystem:

* **Data Processing:** `pandas`, `numpy`
* **Visualization:** `matplotlib.pyplot`, `seaborn`, `plotly.express`

---

## 🧹 Data Cleaning & Preprocessing

To ensure reliability and accuracy, multiple data refinement steps were carried out:

* **Duplicate Handling:** Removed all duplicate entries.
* **Irrelevant Columns:** Dropped `house_rules` and `license`.
* **Data Type Conversion:**

  * Converted `price` and `service_fee` to floats after removing `$` and `,`.
  * Renamed to `price_$` and `service_fee_$` for clarity.
  * Converted `id`, `host_id` → string; `last_review` → datetime; `construction_year` → int.
* **Missing Values:** Dropped rows containing any `NaN` values.
* **Outlier Removal:** Filtered out listings where `availability_365 > 500`.
* **Data Correction:** Corrected `brookln` → `Brooklyn` in `neighbourhood_group`.

---

## 📊 Key Findings & Visualizations

### 🏘️ Property Types Distribution

* **Entire home/apt** and **Private room** dominate the listings with **44,161** and **37,474** entries respectively.
* **Shared rooms** (1,646) and **Hotel rooms** (108) are much less common.

---

### 🌆 Neighbourhood Group Insights

| Neighbourhood Group | Listing Count |
| ------------------- | ------------- |
| Brooklyn            | 34,621        |
| Manhattan           | 34,560        |
| Queens              | 11,124        |
| Bronx               | 2,267         |
| Staten Island       | 816           |

**🏆 Brooklyn** slightly surpasses **Manhattan** in total listings.

---

### 💵 Average Price by Neighbourhood

* **Manhattan** leads with the **highest average price per listing**, reflecting its premium market segment.

---

### 🏗️ Construction Year vs Price

* The trend indicates an **inverse relationship** — **older buildings** often have **higher average prices**, possibly due to location and architectural value.

---

### ✅ Host Identity Verification & Reviews

| Host Identity | Avg. Review Rate |
| ------------- | ---------------- |
| Verified      | 3.28             |
| Unconfirmed   | 3.27             |

✅ Verified hosts enjoy a **slightly higher review rate**, though the difference is minimal.

---

### 📈 Correlation: Price vs Service Fee

* **Correlation Coefficient:** `≈ 0.99999`
  This extremely strong correlation suggests the **service fee is directly proportional** to the listing price — likely a fixed percentage.

---

### 🌍 Review Rate by Location & Room Type

* **Brooklyn (Hotel rooms):** Highest review rate — **3.83**
* **Staten Island (Private rooms):** High average rate — **3.49**
* Most review scores cluster between **3.2 – 3.4**, showing consistent guest satisfaction levels.

---

### 👑 Top 10 Hosts by Listing Count

| Host Name | Listings |
| --------- | -------- |
| John      | 117,175  |
| David     | 104,136  |
| Alex      | 95,958   |
| Michael   | 72,130   |
| Sarah     | 60,394   |
| Jessica   | 55,274   |
| Maria     | 54,618   |
| Kazuya    | 52,260   |
| Daniel    | 51,902   |
| Lisa      | 48,154   |

🏅 **John** is the most active host, holding a commanding lead in total listings.

---

## 📤 Exports

All processed insights were exported to **Google Sheets** for easy sharing, reporting, and collaborative review.

---

## 📈 Conclusion

This analysis of Airbnb’s open data reveals:

* A **dominance of private and entire home listings**.
* **Brooklyn and Manhattan** as the most active regions.
* **Strong linkage** between listing price and service fee.
* **Stable review patterns** across room types and neighborhoods.

The findings provide a solid foundation for further exploration, such as **predictive pricing models**, **host performance analytics**, or **geospatial trend mapping**.

---

## 🚀 Future Work

* Build an **interactive dashboard** using `Plotly Dash` or `Streamlit`.
* Apply **machine learning** for price prediction and host performance scoring.
* Incorporate **geospatial visualization** using `folium` or `geopandas`.

---

## 👩‍💻 Author

**Sydel Wivel Afonso**
