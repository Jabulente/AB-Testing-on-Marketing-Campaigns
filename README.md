<h1 align='center'>Marketing Campaigns A/B Testing | Fashion Retail Case Study</h1>

This project uses A/B testing techniques in Python to determine which marketing campaign is most effective in driving product sales. The analysis evaluates and compares the impact of three different promotional strategies launched across randomly selected outlets of a fashion retail company.

---

## 🧠 Problem Context

A fashion retail company is preparing to launch a new product as part of its apparel catalog expansion. However, the management is uncertain about which of the three proposed marketing campaigns would generate the highest product sales. To make an informed decision, they conduct an **A/B test** by deploying each campaign variant randomly across selected store outlets and tracking the weekly sales for a one-month period (4 weeks). The ultimate goal is to assess which campaign yields the best sales performance and should be adopted for a full-scale rollout.

---

## 🎯 Objectives

The key objectives of this project are:

1. **Compare the effectiveness** of three marketing campaigns (Campaign 1, Campaign 2, Campaign 3) using statistical analysis.
2. **Identify statistically significant differences** in sales using appropriate A/B testing techniques.
3. **Recommend** the most impactful campaign based on data-driven insights.

---

## 📦 Dataset Description

The dataset consists of **548 observations** and the following features:

| Column Name    | Description                                                                           |
| -------------- | ------------------------------------------------------------------------------------- |
| OutletID       | Unique identifier for store location (total of 137 outlets).                          |
| Market Size    | Categorical variable describing the outlet’s market as `Small`, `Medium`, or `Large`. |
| Age of Outlets | Age of the store in years (ranging from 1 to 28).                                    |
| Campaigns      | Categorical variable indicating the type of campaign applied (1, 2, or 3).            |
| Week           | Indicates which of the 4 weeks (1–4) the data point represents.                       |
| Sales ('000')  | Sales revenue in thousands of dollars for a given campaign, store, and week.          |


### 🔬 Methodology 

#### **1. Data Preparation and Exploration**
The dataset was first imported and inspected using `pandas`. Summary statistics (mean, standard deviation, etc.) were computed for each group (Control, Loyalty Bonus, and Product Discount). Initial visualizations such as **boxplots** and **histograms** were created using `seaborn` and `matplotlib` to understand the distribution and spread of the sales data across groups.

####  **2. Testing Assumptions for Parametric Tests**
Before conducting any inferential statistics, two assumptions were checked:

* **a. Normality**:
  For each group, the **Shapiro-Wilk test** was applied to assess normality. Additionally, **Q-Q plots** were used for visual confirmation.

* **b. Homogeneity of Variance**:
  **Levene’s test** was performed to verify if the variances across the groups were equal, which is a requirement for ANOVA and t-tests.

#### **3. One-Way ANOVA (Analysis of Variance)**
A **one-way ANOVA** was conducted using `statsmodels` to test whether there were significant differences in mean sales across the three marketing campaigns. The ANOVA determines if at least one group mean is different without specifying which.

####  **4. Independent Samples t-Test (Pairwise Comparison)**
To supplement the ANOVA, **independent t-tests** were conducted between each pair of groups (Control vs Loyalty Bonus, Control vs Product Discount, Loyalty Bonus vs Product Discount). This helped in understanding the **direction and significance** of differences between specific pairs.

####  **5. Post-Hoc Analysis: Tukey’s HSD**
Since ANOVA indicated a statistically significant difference among groups, a **Tukey’s Honest Significant Difference (HSD)** test was used as a post-hoc analysis. This test allowed multiple pairwise comparisons while controlling for Type I error.

#### **6. Compact Letter Display (CLD) for Group Comparison**
The results of Tukey's HSD were summarized using **Compact Letter Display**. Each group was assigned a letter: groups sharing the same letter are **not significantly different**, while groups with different letters **are statistically distinct**. This visual classification made it easier to interpret results and rank campaign effectiveness.

####  **7. Interpretation and Business Implication**
Finally, a summary table with **mean sales ± standard error**, group letters, and **p-values** was constructed. These results were translated into **business insights**, clearly identifying which campaign performed best and offering recommendations for decision-making.


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
