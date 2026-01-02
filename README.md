# email-campaign-analysis Project Structure (GitHub Repository)

email-campaign-analysis/
│
├── README.md
├── email_campaign_analysis.py
├── sample_email_data.csv
└── report.md


📄 1. README.md (Project Description)

# Email Campaign Analysis

This project analyzes email marketing campaign performance with a focus on:
- Open Rate
- Click-Through Rate (CTR)
- Engagement patterns

The goal is to understand how users interact with email campaigns and identify
factors that improve engagement.

## Metrics Used
- Open Rate
- Click-Through Rate (CTR)

## Tools & Technologies
- Python
- Pandas
- CSV dataset

## Files in This Repository
- email_campaign_analysis.py : Python script for analysis
- sample_email_data.csv : Sample email campaign dataset
- report.md : Project report and findings

## How to Run
1. Install Python
2. Install pandas:
   pip install pandas
3. Run:
   python email_campaign_analysis.py


📄 2. sample_email_data.csv (Dataset)

Campaign_ID,Emails_Sent,Emails_Delivered,Emails_Opened,Link_Clicks
C001,1000,980,420,120
C002,1200,1180,500,150
C003,900,880,300,60
C004,1500,1470,700,240
C005,1100,1080,450,130


📄 3. email_campaign_analysis.py (Python Code)

import pandas as pd

# Load dataset
data = pd.read_csv("sample_email_data.csv")

# Calculate Open Rate and Click-Through Rate
data["Open_Rate (%)"] = (data["Emails_Opened"] / data["Emails_Delivered"]) * 100
data["Click_Through_Rate (%)"] = (data["Link_Clicks"] / data["Emails_Delivered"]) * 100

# Display results
print("Email Campaign Analysis\n")
print(data)

# Average metrics
avg_open_rate = data["Open_Rate (%)"].mean()
avg_ctr = data["Click_Through_Rate (%)"].mean()

print("\nAverage Open Rate: {:.2f}%".format(avg_open_rate))
print("Average Click-Through Rate: {:.2f}%".format(avg_ctr))


📄 4. report.md (Project Report)

# Email Campaign Analysis Report

## Introduction
Email marketing is a powerful digital communication tool. This project analyzes
email campaign performance using open rates and click-through patterns.

## Open Rate Analysis
Open rate indicates how many recipients opened the email.
Higher open rates were observed in campaigns with better engagement.

## Click-Through Pattern Analysis
Click-through rate measures how many users clicked on links inside the email.
Campaigns with higher open rates generally showed higher CTR.

## Key Findings
- Campaign C004 had the highest open and click-through rate
- Higher engagement leads to better campaign performance
- Email content and timing play a major role

## Conclusion
Analyzing open rates and click-through patterns helps improve email campaign
effectiveness and audience engagement.

