---
layout: default
title: Cloud Cost Optimization Alerts Project
permalink: /projects/cloud-cost-tools	.html
---

# Cloud Cost Optimization and Alerting Tools

## 🔍 Project Overview
This project explores practical methods to **monitor and reduce cloud costs** by creating usage alerts, visualizing billing trends, and automating budget checks using AWS and Azure tools.

## 🧰 Tools & Technologies
- **AWS Budgets + CloudWatch + SNS**
- **Azure Cost Management + Alerts**
- **Python scripts** with Boto3 / Azure SDK
- **Lambda Functions / Azure Functions** for automation
- Optional: **Grafana + JSON APIs** for dashboarding

## 📷 Alerting Diagram
![Cost Monitoring Diagram](../assets/cloud-cost-placeholder.png)

## 📁 Repository
- GitHub: [cloud-cost-tools](https://github.com/fernandezdelpeloso/cloud-cost-tools)

## ⚙️ AWS Cost Alert Example
1. Define a budget in AWS:
```bash
aws budgets create-budget \
  --account-id <id> \
  --budget file://budget.json
```
2. Create an SNS topic and subscribe (email/SMS)
3. Link the budget alert to the SNS topic

## ⚙️ Azure Budget Alert Example
1. Navigate to Cost Management → Budgets
2. Create a new budget and define an alert threshold
3. Set an Action Group to email or trigger a Function

## 🧪 Python Example: Forecast Cost
```python
import boto3
client = boto3.client('ce')
response = client.get_cost_forecast(
  TimePeriod={"Start": "2025-05-01", "End": "2025-05-31"},
  Granularity='MONTHLY',
  Metric='UNBLENDED_COST'
)
print(response['ForecastResultsByTime'])
```

## 🧠 Lessons Learned
- Budget alerts aren't real-time — schedule proactively
- Combining data from multiple services improves precision
- Cross-cloud analysis can highlight duplicated workloads

## 📌 Next Steps
- Automate reports to Slack/email daily
- Add cost breakdown per service/account
- Visualize forecasts in Grafana or Power BI
- Trigger shutdown of idle resources using alerts

---

**Back to [Home](../index.html)**
