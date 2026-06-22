### Bellabeat Case Study: How Can a Wellness Technology Company Play It Smart?

## 1. Project Overview
This project analyses smart fitness device data to uncover behavioural trends among users, with the goal of informing Bellabeat's marketing strategy. Using publicly available FitBit tracker data, the analysis follows the full data analysis process: Ask, Prepare, Process, Analyse, Share, and Act. Using Python for data cleaning, SQL for analysis, and Power BI for visualisation. Insights are applied specifically to Bellabeat's Leaf wellness tracker, with high-level marketing recommendations delivered for the executive team.

## 2. Business Task
Bellabeat is a high-tech manufacturer of health-focused smart products for women. Cofounder Urška Sršen asked the marketing analytics team to:

Identify trends in how consumers use non-Bellabeat smart devices
Apply these trends to Bellabeat's customer base
Use these trends to inform Bellabeat's marketing strategy

Stakeholders: Urška Sršen (Cofounder, Chief Creative Officer), Sando Mur (Cofounder), and the Bellabeat Marketing Analytics Team.

## 3. Data Sources
This analysis uses the FitBit Fitness Tracker Data (CC0: Public Domain, via Mobius), containing personal fitness tracker data from 33 FitBit users, including activity, sleep, and weight logs collected over a one-month period (March–May 2016).

# Files used:
| File | Description |
|---|---|
| `dailyActivity_merged.csv` | Daily steps, distance, activity minutes, and calories burned |
| `sleepDay_merged.csv` | Daily total minutes asleep and total time in bed |
| `weightLogInfo_merged.csv` | Weight, BMI, and manual report logs |

Data credibility (ROCCC):

Reliable — Partially. Small, self-selected sample with no demographic data
Original — Third-party data, not collected by Bellabeat directly
Comprehensive — Limited. No age, gender, or location data
Current — No. Data is from 2016
Cited — Yes. Publicly available on Kaggle under a CC0 licence

These limitations are acknowledged throughout the analysis and noted again in the Limitations section below.

## 4. Tools Used

| Tool | Purpose |
|---|---|
| Python (Google Colab) | Data cleaning, type conversion, null/duplicate handling, merging datasets |
| SQL (SQLite) | Aggregation, segmentation, and trend analysis |
| Power BI | Dashboard build and data visualisation |

# Process Summary

Standardised column names and date formats across all datasets
Removed duplicate records and rows with zero recorded steps
Merged dailyActivity_merged with sleepDay_merged on user ID and date
Converted sleep data from minutes to hours for clearer interpretation
Added a day_of_week field (and numeric sort key) to support weekly trend analysis
Exported cleaned datasets and ran segmentation queries in SQL before visualising in Power BI


Full cleaning code is available in BellaBeat.ipynb.

<img width="1078" height="601" alt="Bellabeat Analytical Dashboard" src="https://github.com/user-attachments/assets/f8529f2b-d85d-42bb-b661-3dda34e70e05" />


## 5. Key Insights 
# 1. Activity follows a clear weekly rhythm — with a Sunday slump

Users average their highest step counts on Tuesday (8,949) and Saturday (8,947), dropping to a low of 7,627 steps on Sunday.

Recommendation: Schedule Leaf tracker push notifications and step challenges for Sunday and Friday evenings, when motivation is lowest.

# 2. The user base splits across activity tiers — a segmentation opportunity

Users are spread fairly evenly: Fairly Active (10), Sedentary (9), Low Active (7), Very Active (7).

Recommendation: Target Sedentary/Low Active users with onboarding-style, low-intimidation messaging. Use Very Active users for referral and advocacy campaigns.

# 3. Steps and calories burned are strongly correlated

The scatter plot shows a clear positive trend between steps and calories burned.

Recommendation: Use this relationship directly in marketing copy (e.g. "see your effort turn into real results") to reinforce that consistent tracking leads to visible outcomes.

# 4. Sleep falls below the 7-hour target on five of seven days

Sleep ranges from 7.5 hours (Sunday) down to 6.7 hours (Thursday).

Recommendation: Position the Time watch's sleep-coaching features around Tuesday–Thursday, when sleep quality dips most.

# 5. The majority of users are highly consistent trackers

64% of users (21 of 33) are classified as High Use (25+ days tracked), versus 11 Moderate and just 1 Low Use.

Recommendation: Build a loyalty/milestone system for High Use members, and a re-engagement nudge campaign for the 11 Moderate Use users to convert them to High Use.

## Final Recommendations
Time campaigns around the weekly activity cycle — push engagement content on Sundays and Fridays to counter the predictable motivation dip

Segment marketing by activity tier — onboarding-focused messaging for Sedentary/Low Active users, advocacy-focused for Very Active users

Use the steps-to-calories relationship as proof of product value in marketing materials and app onboarding

Promote Time's sleep-coaching features midweek, when sleep quality is lowest

Introduce a loyalty programme for the 64% of highly engaged users, and a targeted re-engagement campaign for the Moderate Use segment

## 6. Limitations
Sample size of only 33 users limits statistical generalisability

No demographic data (age, gender, location) despite Bellabeat being a women-focused brand

Data collected in 2016 — smart device usage habits may have shifted significantly since

Self-selected FitBit users may not represent Bellabeat's actual customer base


## 7. How to Reproduce This Analysis
├── BellaBeat.ipynb              # Python data cleaning (Google Colab)
├── bellabeat_analysis.sql       # SQL analysis queries
├── Bellabeat_Dashboard.pbix     # Power BI dashboard file
├── dashboard_screenshot.png     # Dashboard preview image
└── README.md                    # Project overview (this file)

## Author

Joseph Bautista
MSc Data Science and Analytics, University of Westminster
LinkedIn · www.linkedin.com/in/joseph-bautista-3a6aab222
