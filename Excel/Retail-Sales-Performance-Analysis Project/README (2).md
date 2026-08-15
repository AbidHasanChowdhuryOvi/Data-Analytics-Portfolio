# Retail Sales Performance Analysis Project

> **A comprehensive retail sales performance dashboard and analysis using Microsoft Excel, featuring region-wise sales tracking, target achievement monitoring, delivery efficiency analysis, and customer satisfaction metrics.**

**Author:** Abid Hasan Chowdhury Ovi  
**Role:** Aspiring Data & Business Intelligence Analyst  
**Tools:** Microsoft Excel | Pivot Tables | Dashboard Design | Data Analysis | Business Reporting

---

## Project Focus

- **Sales Performance Tracking** — Region-wise sales vs. target analysis
- **Target Achievement Monitoring** — Gap analysis and attainment ratios
- **Delivery Efficiency** — Average delivery days by region
- **Customer Satisfaction** — Rating distribution and regional comparison
- **Salesforce Performance** — Top and bottom performer identification
- **Store Performance** — Best and worst performing store locations

---

## Business Requirements

The following key business questions were addressed in this analysis:

1. **How is the overall sales performance?**
2. **Which regions are missing their sales targets?**
3. **Which product categories have low profit margins?**
4. **Are delivery delays affecting customer ratings?**
5. **Is there an over-dependency on top-selling products?**
6. **Are there significant performance gaps among salespeople?**

---

## Demo Data

Below is a sample of the raw transaction data used in this analysis:

| Order_ID | Order_Date | Customer_ID | Region_ID | Store_ID | Salesperson_ID | Product_ID | Quantity_Sold | Discount | Target_Sales | Delivery_Days | Customer_Rating | Product_Name | Category | Unit_Price | Sales_Amount | Unit_Cost | Total_Cost | Profit | Customer_Name | Sales_Man | Region | Store_Name |
|----------|------------|-------------|-----------|----------|----------------|------------|---------------|----------|--------------|---------------|-----------------|--------------|----------|------------|--------------|-----------|------------|--------|---------------|-----------|--------|---------------------------|
| ORD-00001 | 2025-06-28 | CUS-RAN-017 | R07 | ST-RAN-01 | SM-RAN-006 | P006 | 1 | 15% | 8,280 | 9 | 2.0 | Electric Kettle | Home Appliance | 7,200 | 7,200 | 5,040 | 5,040 | 2,160 | Tamanna Mia | Tania Hossain | Rangpur | Rangpur Jahaj Company Store |
| ORD-00002 | 2025-05-24 | CUS-RAJ-004 | R04 | ST-RAJ-04 | SM-RAJ-001 | P036 | 1 | 0% | 432 | 2 | 4.6 | Notebook Pack | Stationery | 400 | 400 | 200 | 200 | 200 | Jannat Islam | Imran Khan | Rajshahi | Rajshahi Railgate Store |
| ORD-00003 | 2025-03-28 | CUS-RAJ-005 | R04 | ST-RAJ-02 | SM-RAJ-004 | P009 | 4 | 8% | 19,699 | 7 | 2.8 | Steam Iron | Home Appliance | 4,560 | 18,240 | 3,190 | 12,760 | 5,480 | Tanjim Akter | Farhana Rahman | Rajshahi | Rajshahi Kazla Store |
| ORD-00004 | 2026-04-18 | CUS-MYM-005 | R08 | ST-MYM-01 | SM-MYM-003 | P003 | 3 | 15% | 9,202 | 4 | 3.6 | Power Bank | Electronics | 2,840 | 8,520 | 1,930 | 5,790 | 2,730 | Shamim Hossain | Morshed Islam | Mymensingh | Mymensingh Ganginarpar Store |
| ORD-00005 | 2025-06-26 | CUS-RAN-016 | R07 | ST-RAN-01 | SM-RAN-004 | P028 | 2 | 5% | 7,406 | 6 | 3.2 | Ladies Sandal | Footwear | 3,220 | 6,440 | 1,930 | 3,860 | 2,580 | Tamanna Mia | Farhana Uddin | Rangpur | Rangpur Jahaj Company Store |
| ORD-00006 | 2025-10-30 | CUS-SYL-002 | R03 | ST-SYL-05 | SM-SYL-005 | P023 | 2 | 12% | 2,482 | 5 | 3.3 | Body Lotion | Beauty & Personal Care | 1,160 | 2,320 | 670 | 1,340 | 980 | Rafi Hossain | Fahim Mia | Sylhet | Sylhet Upashahar Store |
| ORD-00007 | 2026-03-06 | CUS-MYM-002 | R08 | ST-MYM-01 | SM-MYM-003 | P009 | 3 | 10% | 14,774 | 4 | 3.7 | Steam Iron | Home Appliance | 4,560 | 13,680 | 3,190 | 9,570 | 4,110 | Karim Chowdhury | Morshed Islam | Mymensingh | Mymensingh Ganginarpar Store |
| ORD-00008 | 2026-05-12 | CUS-DHA-013 | R01 | ST-DHA-03 | SM-DHA-004 | P018 | 2 | 3% | 3,625 | 1 | 4.8 | Lentil 1kg | Grocery | 1,710 | 3,420 | 1,330 | 2,660 | 760 | Arif Hossain | Tania Sultana | Dhaka | Dhaka Mirpur Store |
| ORD-00009 | 2025-08-13 | CUS-RAN-009 | R07 | ST-RAN-02 | SM-RAN-001 | P007 | 1 | 12% | 8,544 | 13 | 1.0 | Rice Cooker | Home Appliance | 7,430 | 7,430 | 5,200 | 5,200 | 2,230 | Samiha Uddin | Morshed Ahmed | Rangpur | Rangpur Shapla Chattar Store |
| ORD-00010 | 2025-04-13 | CUS-BAR-025 | R06 | ST-BAR-05 | SM-BAR-002 | P049 | 1 | 7% | 4,738 | 9 | 2.2 | Bookshelf | Furniture | 4,230 | 4,230 | 3,050 | 3,050 | 1,180 | Fahim Khan | Shaila Akter | Barishal | Barishal Kawnia Store |

**Dataset Overview:**
- **Total Orders:** 1,000
- **Date Range:** March 2025 – May 2026
- **Regions:** Dhaka, Chattogram, Rajshahi, Khulna, Sylhet, Barishal, Rangpur, Mymensingh
- **Fields:** 22 columns including Order ID, Customer, Product, Pricing, Profit, Ratings, Delivery Days

---

## Executive Summary

| Metric | Value |
|--------|-------|
| **Total Orders** | 1,000 |
| **Total Sales** | ৳ 10.37 M |
| **Total Target** | ৳ 11.40 M |
| **Target Achievement** | 90.99% |
| **Target Gap** | ৳ 1.03 M |
| **Average Delivery Days** | 4.59 days |

### Key Findings

- **Overall Performance:** Sales reached 90.99% of target, leaving a BDT 1.03M shortfall against the BDT 11.40M target.
- **Sales Leadership:** Barishal generated the highest regional sales (BDT 1.50M), while Dhaka achieved the strongest target attainment (94.34%).
- **Service Priority:** Rangpur had the slowest average delivery time (6.43 days) and the weakest target attainment (86.96%); it should be the first operational review area.
- **Customer Experience:** Dhaka had the largest 4–5 rating share (63.3%), whereas Rangpur had the smallest (9.7%) and the highest 1–2 rating share (7.3%).
- **Commercial Focus:** Prioritize the strongest stores and salespeople for repeatable practices, then investigate the lowest-performing locations and territories for targeted recovery plans.

---

## Region Performance — Ranked by Sales

| Sales Rank | Region | Sales (BDT) | Target (BDT) | Target Gap (BDT) | Achievement % |
|:----------:|--------|------------:|-------------:|----------------:|--------------:|
| 1 | Barishal | 1,498,090 | 1,677,860 | 179,770 | 89.29% |
| 2 | Dhaka | 1,490,960 | 1,580,413 | 89,453 | 94.34% |
| 3 | Khulna | 1,383,370 | 1,507,877 | 124,507 | 91.74% |
| 4 | Rajshahi | 1,330,400 | 1,436,830 | 106,430 | 92.59% |
| 5 | Chattogram | 1,311,820 | 1,495,472 | 183,652 | 87.72% |
| 6 | Rangpur | 1,221,030 | 1,404,174 | 183,144 | 86.96% |
| 7 | Sylhet | 1,072,720 | 1,147,816 | 75,096 | 93.46% |
| 8 | Mymensingh | 1,064,080 | 1,149,207 | 85,127 | 92.59% |

---

## Delivery Efficiency — Fastest to Slowest

| Speed Rank | Region | Average Delivery Days |
|:----------:|--------|:---------------------:|
| 1 | Dhaka | 2.97 |
| 2 | Khulna | 3.75 |
| 3 | Sylhet | 3.79 |
| 4 | Rajshahi | 4.30 |
| 5 | Mymensingh | 4.56 |
| 6 | Barishal | 5.38 |
| 7 | Chattogram | 5.46 |
| 8 | Rangpur | 6.43 |

---

## Customer Rating Profile by Region

| Region | 1-2 Stars | 2-3 Stars | 3-4 Stars | 4-5 Stars | Total Customers | 4-5 Star Share |
|--------|:---------:|:---------:|:---------:|:---------:|:---------------:|:--------------:|
| Dhaka | 1 | 2 | 44 | 81 | 128 | 63.3% |
| Khulna | 0 | 10 | 65 | 55 | 130 | 42.3% |
| Rajshahi | 0 | 17 | 74 | 47 | 138 | 34.1% |
| Sylhet | 0 | 5 | 58 | 41 | 104 | 39.4% |
| Mymensingh | 2 | 20 | 58 | 37 | 117 | 31.6% |
| Barishal | 2 | 41 | 66 | 23 | 132 | 17.4% |
| Chattogram | 6 | 39 | 64 | 18 | 127 | 14.2% |
| Rangpur | 9 | 56 | 47 | 12 | 124 | 9.7% |

---

## Top 10 Salespeople

| Rank | Salesperson ID | Salesperson | Sales (BDT) | % of Total Sales |
|:----:|:--------------:|-------------|------------:|:----------------:|
| 1 | SM-BAR-003 | Rasel Uddin | 358,680 | 3.46% |
| 2 | SM-RAJ-002 | Karim Khan | 332,980 | 3.21% |
| 3 | SM-CTG-004 | Shakib Ahmed | 323,880 | 3.12% |
| 4 | SM-DHA-001 | Mahmud Hossain | 316,400 | 3.05% |
| 5 | SM-DHA-004 | Tania Sultana | 309,150 | 2.98% |
| 6 | SM-BAR-002 | Shaila Akter | 300,240 | 2.89% |
| 7 | SM-KHL-006 | Fahim Uddin | 299,560 | 2.89% |
| 8 | SM-MYM-004 | Fahim Hossain | 298,350 | 2.88% |
| 9 | SM-KHL-003 | Sadia Sultana | 294,550 | 2.84% |
| 10 | SM-CTG-005 | Nabila Mia | 290,270 | 2.80% |

**Top 10 Total:** 3,124,060 (30.12%)

---

## Bottom 10 Salespeople

| Rank | Salesperson ID | Salesperson | Sales (BDT) | % of Total Sales |
|:----:|:--------------:|-------------|------------:|:----------------:|
| 1 | SM-SYL-006 | Rumana Rahman | 114,660 | 1.11% |
| 2 | SM-MYM-002 | Rahim Rahman | 117,300 | 1.13% |
| 3 | SM-DHA-005 | Imran Mia | 131,450 | 1.27% |
| 4 | SM-CTG-003 | Rafi Akter | 132,740 | 1.28% |
| 5 | SM-MYM-006 | Tanvir Chowdhury | 139,570 | 1.35% |
| 6 | SM-MYM-001 | Sajib Rahman | 139,790 | 1.35% |
| 7 | SM-RAJ-006 | Mim Rahman | 144,880 | 1.40% |
| 8 | SM-SYL-004 | Rasel Akter | 144,970 | 1.40% |
| 9 | SM-BAR-005 | Mehedi Khan | 146,490 | 1.41% |
| 10 | SM-KHL-002 | Nusrat Akter | 146,950 | 1.42% |

**Bottom 10 Total:** 1,358,800 (13.10%)

---

## Top 10 Stores by Sales

| Rank | Store | Sales (BDT) | % of Total Sales |
|:----:|-------|------------:|:----------------:|
| 1 | Rajshahi Kazla Store | 442,120 | 4.26% |
| 2 | Barishal Kawnia Store | 388,430 | 3.74% |
| 3 | Dhaka Dhanmondi Store | 374,700 | 3.61% |
| 4 | Chattogram Nasirabad Store | 364,560 | 3.51% |
| 5 | Khulna Shibbari Store | 350,070 | 3.37% |
| 6 | Barishal Rupatali Store | 318,770 | 3.07% |
| 7 | Chattogram Panchlaish Store | 310,060 | 2.99% |
| 8 | Khulna Boyra Store | 306,700 | 2.96% |
| 9 | Dhaka Uttara Store | 301,110 | 2.90% |
| 10 | Dhaka Mirpur Store | 300,800 | 2.90% |

**Top 10 Total:** 3,457,320 (33.33%)

---

## Bottom 10 Stores by Sales

| Rank | Store | Sales (BDT) | % of Total Sales |
|:----:|-------|------------:|:----------------:|
| 1 | Rajshahi Uposhohor Store | 126,640 | 1.22% |
| 2 | Sylhet Upashahar Store | 158,070 | 1.52% |
| 3 | Mymensingh Kewatkhali Store | 170,090 | 1.64% |
| 4 | Chattogram Agrabad Store | 175,790 | 1.69% |
| 5 | Sylhet Zindabazar Store | 183,710 | 1.77% |
| 6 | Mymensingh Maskanda Store | 186,370 | 1.80% |
| 7 | Mymensingh Charpara Store | 201,090 | 1.94% |
| 8 | Chattogram GEC Store | 211,990 | 2.04% |
| 9 | Khulna Daulatpur Store | 213,060 | 2.05% |
| 10 | Mymensingh Town Hall Store | 213,800 | 2.06% |

**Bottom 10 Total:** 1,840,610 (17.75%)

---

## Analysis Dashboard

![Organized Analysis](Analysis.jpg)

*Region-wise Retail Sales Performance — Organized Analysis with executive summary, region rankings, delivery efficiency, customer ratings, and top/bottom performer tables.*

---

## Dashboard 1 — Sales vs Target Overview

![Dashboard 1](Dashboard%201.jpg)

*Retail Industry Region Wise Sales Performance Dashboard — KPI cards, Top 10 and Bottom 10 salesperson performance chart, Region Sales vs Target bar chart, and Region Sales and Target Achieved Ratio table.*

---

## Dashboard 2 — Delivery & Customer Experience

![Dashboard 2](Dashboard%202.jpg)

*Retail Industry Region Wise Sales Performance Dashboard — Average Delivery Days by region, Customer Ratings distribution by region, and Top 10 Store by Sales Performance Analysis.*

---

## Excel Workbook

The complete analysis, including raw data, pivot tables, calculations, and dashboards, is available in the Excel file:

📊 **[Retail Sales Performance Analysis Project.xlsx](Retail%20Sales%20Performance%20Analysis%20Project.xlsx)**

**Workbook Structure:**
- **Raw Data** — 1,000 transaction records with 22 fields
- **Analysis** — Organized summary tables and executive report
- **Store Average Delivery Days** — Delivery time calculations by store
- **Dashboard 1** — Sales performance and target achievement visualizations
- **Dashboard 2** — Delivery efficiency and customer experience visualizations

---

## Recruiter Value & Key Takeaways

| Skill Area | Evidence |
|------------|----------|
| **Data Analysis** | 1,000-row dataset analyzed with pivot tables and summary statistics |
| **Dashboard Design** | Two interactive dashboards with KPI cards, charts, and slicers |
| **Business Intelligence** | Executive summary with actionable priorities and recommendations |
| **Performance Analytics** | Top/bottom performer identification for salespeople and stores |
| **Operational Insights** | Delivery efficiency linked to customer satisfaction metrics |
| **Financial Analysis** | Target gap analysis, achievement ratios, and revenue breakdown |

> **Project Conclusion:** This project demonstrates end-to-end retail analytics capability — from raw transaction data to executive-ready dashboards — with clear business insights on sales performance, operational efficiency, and customer experience across 8 regions, 1,000 orders, and multiple store locations.

---

*This project is part of the [Data Analytics Portfolio](https://github.com/AbidHasanChowdhuryOvi/Data-Analytics-Portfolio).*
