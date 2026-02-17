# -Customer-Satisfaction-Sales-Performance-Analysis
Egyptian Supermarket Chain | Quantitative Research Project

![Data Analytics](https://img.shields.io/badge/Domain-Data%20Analytics-blue)
![PSPP](https://img.shields.io/badge/Tool-PSPP-green)
![Power BI](https://img.shields.io/badge/Tool-Power%20BI-yellow)
![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

##  Project Overview

This project presents a comprehensive end-to-end quantitative analysis of **1,000 customer transactions** from an Egyptian supermarket chain operating across three branches — **Alexandria, Cairo, and Giza**. The study investigates customer satisfaction drivers, demographic purchasing behavior, revenue patterns, and the relationship between financial metrics and satisfaction levels.

The analysis was conducted using **PSPP statistical software** and visualized through an interactive **Power BI dashboard**, producing actionable business recommendations grounded in statistical evidence.

---

##  Research Objectives

- Determine the overall customer satisfaction level across the supermarket chain
- Examine whether demographic factors (gender, customer type) influence purchasing behavior and payment preferences
- Identify which product lines generate the highest revenue and satisfaction
- Assess whether financial transaction metrics predict customer satisfaction
- Compare satisfaction levels across branches, product lines, and payment methods

---

##  Research Questions

| # | Research Question |
|---|---|
| RQ1 | What is the overall customer satisfaction level across the supermarket chain? |
| RQ2 | Is there a significant relationship between customer gender and product line preference? |
| RQ3 | Does customer type (Member vs Normal) influence payment method preference? |
| RQ4 | Does branch location significantly affect product line purchasing patterns? |
| RQ5 | What is the relationship between financial transaction metrics and customer satisfaction? |
| RQ6 | What factors are significant predictors of customer satisfaction rating? |

---

##  Dataset Description

**Source:** Kaggle — Supermarket Sales Dataset  
**Records:** 1,000 customer transactions  
**Time Period:** January 2019 — March 2019  
**Locations:** Alexandria, Cairo, Giza (Egypt)

| Column | Description |
|---|---|
| Invoice_ID | Unique transaction identifier |
| Branch | Store branch location (Alex, Cairo, Giza) |
| City | City of the branch |
| Customer_Type | Member or Normal customer |
| Gender | Customer gender |
| Product_Line | Product category purchased |
| Unit_Price | Price per unit |
| Quantity | Number of items purchased |
| Tax_5% | 5% tax on transaction |
| Total | Total transaction amount including tax |
| Date | Transaction date |
| Payment | Payment method (Cash, Credit Card, Ewallet) |
| COGS | Cost of goods sold |
| Gross_Margin_% | Gross margin percentage |
| Gross_Income | Profit from transaction |
| Rating | Customer satisfaction score (1–10) |

---

##  Tools & Technologies

| Tool | Purpose |
|---|---|
| **PSPP** | Statistical analysis (free SPSS alternative) |
| **Microsoft Excel** | Data cleaning and preparation |
| **Power BI Desktop** | Interactive dashboard and data visualization |
| **Kaggle** | Dataset source |

---

##  Methodology

### Data Preparation
- Imported raw CSV dataset into Microsoft Excel
- Removed time column to resolve delimiter conflicts during PSPP import
- Verified data completeness — **zero missing values** across all 1,000 records
- Configured variable types in PSPP (Nominal, Scale) prior to analysis

### Statistical Analyses Conducted

| Analysis | Test Used | Variables |
|---|---|---|
| Customer Profile | Descriptive Statistics | Rating, Unit Price, Quantity, Gross Income |
| Demographic Breakdown | Frequency Distribution | Gender, Branch, Product Line, Customer Type, Payment |
| Gender vs Product Preference | Chi-Square Test | Gender × Product Line |
| Gender vs Payment Method | Chi-Square Test | Gender × Payment |
| Customer Type vs Payment | Chi-Square Test | Customer Type × Payment |
| Branch vs Product Line | Chi-Square Test | Branch × Product Line |
| Financial Relationships | Pearson Correlation | Rating, Gross Income, Unit Price, Quantity |
| Branch vs Satisfaction | One-Way ANOVA | Branch × Rating |
| Product Line vs Satisfaction | One-Way ANOVA | Product Line × Rating |
| Payment vs Satisfaction | One-Way ANOVA | Payment × Rating |
| Satisfaction Predictors | Multiple Linear Regression | Rating ~ Gross Income + Unit Price + Quantity |

---

##  Key Findings

### 1. Descriptive Statistics
- Mean customer satisfaction score: **6.97 / 10** (SD = 1.72)
- Satisfaction ranged from **4.0 to 10.0**
- Average gross income per transaction: **$15.38**
- Average quantity purchased: **5.51 items**

### 2. Customer Demographics
| Variable | Finding |
|---|---|
| Gender | Female customers dominate at **57.1%** (n=571) |
| Top Branch | Alexandria leads at **34.0%** (n=340) |
| Top Product Line | Fashion Accessories at **17.8%** (n=178) |
| Customer Loyalty | Members constitute **56.5%** (n=565) |
| Payment Preference | Ewallet leads at **34.5%** — cashless payments total **65.6%** |

### 3. Chi-Square Tests (Independence)
| Test | χ² | df | p-value | Result |
|---|---|---|---|---|
| Gender × Product Line | 5.44 | 5 | 0.365 |  Not Significant |
| Gender × Payment Method | 3.58 | 2 | 0.167 |  Not Significant |
| Customer Type × Payment | 2.67 | 2 | 0.263 |  Not Significant |
| Branch × Product Line | 11.56 | 10 | 0.316 |  Not Significant |

> **Insight:** Customer behavior is remarkably uniform regardless of gender, membership status, or branch location — indicating a highly inclusive and diverse customer base.

### 4. Correlation Analysis
| Relationship | r | p-value | Result |
|---|---|---|---|
| Rating vs Gross Income | -0.036 | 0.250 |  Not Significant |
| Rating vs Unit Price | -0.009 | 0.782 |  Not Significant |
| Rating vs Quantity | -0.016 | 0.617 |  Not Significant |
| Gross Income vs Unit Price | **0.634** | 0.000 |  Significant |
| Gross Income vs Quantity | **0.706** | 0.000 |  Significant |

> **Key Insight:** Spending amount, unit price, and quantity have **no significant relationship** with customer satisfaction — satisfaction is driven by experiential factors, not financial ones.

### 5. One-Way ANOVA
| Test | F | p-value | Result | Highest Mean |
|---|---|---|---|---|
| Branch vs Rating | 2.08 | 0.126 |  Not Significant | Giza (M=7.07) |
| Product Line vs Rating | 0.54 | 0.746 |  Not Significant | Food & Beverages (M=7.11) |
| Payment vs Rating | 0.09 | 0.918 |  Not Significant | Credit Card (M=7.00) |

> **Insight:** Satisfaction is consistent across all branches, product lines, and payment methods — reflecting uniform service delivery across the chain.

### 6. Multiple Linear Regression
| Variable | B | Beta | t | p-value |
|---|---|---|---|---|
| Constant | 6.64 | — | 24.58 | 0.000 |
| Gross Income | -0.03 | -0.18 | -1.90 | 0.058 |
| Unit Price | 0.01 | 0.10 | 1.55 | 0.121 |
| Quantity | 0.07 | 0.11 | 1.50 | 0.134 |

**Model:** R² = 0.00 | F(3, 996) = 1.31 | p = 0.270

> **Insight:** The regression model explains virtually 0% of satisfaction variance — conclusively confirming that financial transaction metrics cannot predict customer satisfaction.

---

##  Business Recommendations

| # | Recommendation | Based On |
|---|---|---|
| 1 | **Invest in service quality training** for staff — satisfaction is driven by experience not spending | Correlation + Regression findings |
| 2 | **Expand Ewallet and digital payment infrastructure** — 65.6% of customers prefer cashless transactions | Payment frequency analysis |
| 3 | **Develop targeted membership recruitment campaigns** — 43.5% of customers remain non-members | Customer type frequency |
| 4 | **Boost Health & Beauty product line promotion** — lowest sales volume at 15.2% | Product line frequency |
| 5 | **Replicate Cairo and Alexandria's fashion/sports strategy in Giza** — Giza under-indexes in these categories | Branch × Product line crosstab |
| 6 | **Deploy customer experience surveys** to capture qualitative satisfaction drivers not measurable through transactional data | Overall regression finding |

---

##  Headline Conclusions

> **"Customer satisfaction at this Egyptian supermarket chain averages 6.97/10 and remains statistically consistent across all branches, product lines, and payment methods — reflecting strong operational uniformity."**

> **"Demographic factors including gender and membership status have no significant influence on purchasing or payment behavior — indicating a highly inclusive customer base that engages freely across all product categories."**

> **"Financial transactional metrics including spending amount, unit price, and quantity purchased are not significant predictors of customer satisfaction — conclusively demonstrating that satisfaction is determined by qualitative service experience factors beyond transactional data."**

---

##  Project Structure

```
supermarket-satisfaction-analysis/
│
├── data/
│   ├── supermarket_sales_raw.csv        # Original dataset
│   └── SuperMarket_fixed.csv            # Cleaned dataset used for analysis
│
├── analysis/
│   └── Supermarket_Analysis_Output.pdf  # Full PSPP statistical output
│
├── dashboard/
│   └── Supermarket_Dashboard.pbix       # Power BI dashboard file
│
├── report/
│   └── Research_Report.pdf              # Full written research report
│
└── README.md                            # Project documentation (this file)
```

---

##  Dashboard Preview

> *Interactive Power BI dashboard featuring 5 pages:*
> - **Page 1:** Executive Overview & KPIs
> - **Page 2:** Customer Demographics
> - **Page 3:** Sales & Revenue Analysis
> - **Page 4:** Satisfaction Analysis
> - **Page 5:** Branch & Product Performance

---

##  Author

**Iorbee Collins Terver**  
Data Analyst | Quantitative Researcher |

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/collins-iorbee-22a125214/)
[![Email](https://img.shields.io/badge/Email-Contact-red)](iorbeeterver@gmail.com)

---



* If you found this project useful or insightful, please consider giving it a star on GitHub!*

