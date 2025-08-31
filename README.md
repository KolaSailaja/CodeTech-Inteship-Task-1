
# Cloud Monitoring – Alerts Setup

This project demonstrates the setup of **Google Cloud Monitoring Alerts** to track API request counts and send notifications when defined thresholds are exceeded.

---

## 📌 Step-by-Step Explanation of Cloud Monitoring Alerts Setup

---

### **1. Navigating to Cloud Monitoring**

Open the **Google Cloud Console → Monitoring**.

* From the left-side menu, select **Monitoring → Overview / Dashboards / Application Monitoring / Metrics Explorer / Alerting**.
* This is the entry point for creating dashboards, monitoring metrics, and setting up alerts.

👉 **Purpose**: To monitor API usage, resources, or custom metrics.

---

### **2. Adding a Widget for Monitoring**

Inside a **Cloud Monitoring Dashboard**, select **Add Widget**.

* Options available include:

  * **Data**: Metric, Logs, Observability Analytics
  * **Detection**: Alerting Policy, SLO, Incidents, Errors
  * **Visualization**: Line chart, Stacked area, Bar chart, Heatmap, Table, Gauge, Scorecard, Pie chart
  * **Layout**: Text, Collapsible groups, Dropdown groups

👉 **Purpose**: A **Line Chart Widget** is selected to visualize API request counts.

---

### **3. Configuring the Widget**

Widget configuration:

* **Metric**: Consumed API → Request Count
* **Aggregation**: Sum
* **Result**: A line graph showing request\_count over time
* **Chart Title**: *Consumed API - Request count \[SUM]*

👉 **Purpose**: To monitor API calls over time in the dashboard.

---

### **4. Creating an Alerting Policy**

Create an **Alerting Policy**.

* Choose **+ Add alert condition**
* Policy Configuration Mode: **Builder** (can also use MQL or PromQL)
* Select metric: **API Request Count**

👉 **Purpose**: To trigger alerts when the metric crosses a threshold.

---

### **5. Configuring Alert Condition**

Define the alert condition:

* **Condition Type**: Threshold
* **Metric**: Consumed API - Request count
* **Trigger**: When any time series crosses threshold
* **Threshold Position**: Above threshold
* **Threshold Value**: 8 requests/second
* **Retest Window**: No retest

👉 **Purpose**: If API requests exceed **8 per second**, an alert will fire.

---

### **6. Setting up Notification Channels**

Configure a **Notification Channel**.

* Options include: Mobile App, Google Chat, PagerDuty, Slack, Webhooks, Email, SMS
* Email notification configured: `Sample@gmail.com` (Display Name: VVIT)

👉 **Purpose**: Alerts are delivered to email in real time.

---

### **7. Alert Policy Review & Save**

Finalize and save the alert policy.

* **Policy Name**: VVIT Alerts
* **Condition**: API Request Count > 8/s
* **Status**: Saved and active

👉 **Purpose**: Confirms that the alert is active and functional.

---

### **8. Documentation Reference**

Refer to the **Google Cloud Monitoring Documentation** for additional details.

* Covers metrics, dashboards, events, and alerting policies
* Explains use of **Bindplane** for hybrid and multi-cloud monitoring

👉 **Purpose**: Provides background knowledge and best practices.

---

## ✅ Final Flow (Summary)

1. Open **Google Cloud Monitoring** from console
2. Create a **Dashboard → Add Widget → Line Chart**
3. Select **Metric: API Request Count** and configure aggregation
4. Go to **Alerting → Create Policy → Add Condition**
5. Set **Threshold: Request Count > 8/s**
6. Configure **Notification Channel** (Email, SMS, Slack, etc.)
7. Save policy as **VVIT Alerts**
8. Test by generating API requests and confirm alert delivery

---

## 📖 Reference

* [Google Cloud Monitoring Documentation](https://cloud.google.com/monitoring/docs)



