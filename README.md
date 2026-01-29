# 🍔 Food Ordering Funnel Analysis & Drop-off Optimization

## 📌 Project Overview
This project is a deep dive into the food ordering lifecycle of a delivery platform. As a final-year Computer Science student specializing in AI, I approached this project to bridge the gap between technical data processing and high-level product strategy. 

The goal was to move beyond simple data cleaning and answer the critical business question: **"Where is our revenue leaking, and how much is it costing us?"**.

---

## 🚀 The Business Problem
Even with a high-performing logistics network, a product can fail if the user journey has high friction points. This analysis identifies exactly where users "drop off" the path to purchase and evaluates the financial impact of these lost opportunities.

### **Key Business Questions Addressed:**
1. **The Leak:** At which stage of the funnel do we lose the most potential revenue?.
2. **Logistics vs. Product:** Is the bottleneck caused by slow delivery times or checkout friction?.
3. **Temporal Habits:** How does user behavior differ between the work-week and the weekend?.
4. **ROI:** What is the projected revenue lift if we improve the checkout completion rate by just 10%?.

---

## 🛠️ Technical Stack & Skills
* **Languages/Tools:** Python (Pandas, NumPy), SQL (CTEs, Aggregations).
* **Methodology:** Clickstream Simulation, Funnel Visualization, Root Cause Analysis.
* **Domain:** Product Management (PM) Metrics, Business Analytics.

---

## 📊 Conversion Funnel Performance
Using a simulated activity log of **17,950 events** mapped against real-world order data, the following funnel was established:

| Stage | User Count | Conversion Rate | Drop-off Rate |
| :--- | :--- | :--- | :--- |
| **App Open** | 9,490 | 100.00% | 0.00% |
| **View Restaurant** | 5,722 | 60.30% | 39.70% |
| **Add to Cart** | 2,271 | 23.93% | 60.31% |
| **Order Placed** | 467 | 4.92% | **79.44% (CRITICAL)** |

**Insight:** The most significant "leak" occurs at the final step. Nearly **80% of high-intent users** (those who already added items to their cart) fail to complete the transaction.

---

## 🔍 Root Cause Analysis (The "Why")
* **Delivery Efficiency:** The average delivery time is **24.16 minutes**. Since this is highly competitive, logistics is **not** the primary reason for the 79% checkout drop-off.
* **Demand Peaks:** Weekend orders (**1,351**) outpace Weekday orders (**547**) by a ratio of roughly 3:1.
* **The Hypothesis:** The high checkout drop-off suggests "Window Shopping" behavior or price-sensitivity—particularly on weekdays when users may be deterred by delivery fees or service charges.

---

## 💡 Strategic Recommendations & ROI
1. **Abandoned Cart Recovery:** Deploy automated push notifications for the **1,804 users** who reached the "Add to Cart" stage but didn't convert.
2. **Weekday Incentive Program:** Bridge the 3:1 demand gap by introducing weekday-exclusive "Workday Fuel" bundles or waived delivery fees for orders over $15.
3. **Financial Impact:** Recovering just **10%** of these "lost" checkout users would generate an estimated **extra revenue of $2,900+** based on the average order value of $16.50.

---

## 📂 Project Structure
* `food_order.csv`: Original order metadata (cost, delivery time, day of week).
* `activity_log.csv`: Simulated clickstream data representing the full user journey.
* `Funnel_Analysis.ipynb`: Python notebook containing the data pipeline and visualizations.

---
*Developed as a portfolio piece for Product Management and Data Analytics roles, demonstrating the ability to turn raw data into actionable business growth strategies.*.
