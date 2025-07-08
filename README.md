<h1 align='center'>Marketing Campaigns A/B Testing – Fashion Retail Case Study</h1>



This project uses A/B testing techniques in Python to determine which marketing campaign is most effective in driving product sales. The analysis evaluates and compares the impact of three different promotional strategies launched across randomly selected outlets of a fashion retail company.

---

## 🧠 Problem Context

A fashion retail company is preparing to launch a new product as part of its apparel catalog expansion. However, the management is uncertain about which of the three proposed marketing campaigns would generate the highest product sales. To make an informed decision, they conduct an **A/B test** by deploying each campaign variant randomly across selected store outlets and tracking the weekly sales for a one-month period (4 weeks). The ultimate goal is to assess which campaign yields the best sales performance and should be adopted for a full-scale rollout.

---

## 🎯 Objectives

The key objectives of this project are:

1. **Compare the effectiveness** of three marketing campaigns (Campaign 1, Campaign 2, Campaign 3) using statistical analysis.
2. **Analyze weekly sales performance** across different market sizes and outlet characteristics.
3. **Identify statistically significant differences** in sales using appropriate A/B testing techniques.
4. **Visualize key trends and insights** to support decision-making for campaign selection.

---

## 📦 Dataset Description

The dataset consists of **548 observations** and the following features:

| Column Name      | Description                                                                           |
| ---------------- | ------------------------------------------------------------------------------------- |
| `OutletID`       | Unique identifier for store location (total of 137 outlets).                          |
| `Market Size`    | Categorical variable describing the outlet’s market as `Small`, `Medium`, or `Large`. |
| `Age of Outlets` | Age of the store in years (ranging from 1 to 28).                                     |
| `Campaigns`      | Categorical variable indicating the type of campaign applied (1, 2, or 3).            |
| `Week`           | Indicates which of the 4 weeks (1–4) the data point represents.                       |
| `Sales ('000)`   | Sales revenue in thousands of dollars for a given campaign, store, and week.          |

---

## 🧪 Methodology

This project uses a mix of **exploratory data analysis (EDA)** and **inferential statistics** to derive insights, including:

* Data cleaning and preprocessing
* Campaign renaming for better interpretation (e.g., Campaign 1 → "Seasonal Promo")
* Group-wise comparison of average weekly sales across campaigns
* Data visualization using bar plots, box plots, and heatmaps
* Statistical testing:

  * One-Way ANOVA to compare mean sales across campaigns
  * Tukey's HSD test for pairwise comparison of campaigns

---

## 📊 Key Visualizations

* Sales trends by campaign and week
* Average sales by market size
* Distribution of sales per campaign
* Pairwise comparison using Compact Letter Display (CLD)

---

## 📚 Python Libraries Used

* `pandas` – Data manipulation and cleaning
* `matplotlib` – Basic plotting
* `seaborn` – Advanced visualization
* `scipy.stats` – Statistical testing (ANOVA, Tukey's HSD)

---

## 📈 Results Summary

* Campaign performance was found to differ significantly, with **Campaign B** showing the highest average sales.
* Market size played a supporting role, with **large markets** performing better overall.
* Weekly sales patterns showed consistent increases or declines depending on the campaign type.
* ANOVA and post-hoc tests confirmed statistically significant differences between some campaigns.

---

## 💡 Conclusion

A/B testing revealed that not all marketing campaigns are equally effective. The analysis helps the company **make data-driven decisions** about future promotional strategies by recommending the most effective campaign based on sales performance.

---

## 🚀 Next Steps

* Apply similar testing in other product lines or seasons.
* Consider customer segmentation for more personalized campaigns.
* Extend testing to include multi-channel promotion (e.g., digital ads, influencer marketing).

---

## 👨‍💻 Author

**Jabulente** – Data Analyst | A/B Testing Enthusiast | Fashion Retail Data Insights
