# Azure Monitor & Log Analytics – AZ-900 Lab

## 📌 Project Overview
This lab demonstrates how to enable Azure Monitor and Log Analytics for an Azure Virtual Machine.
The goal is to gain visibility into VM health, availability, and basic monitoring, aligned with Azure Fundamentals (AZ-900).

## 🛠 Technologies Used
- Microsoft Azure
- Azure Virtual Machines
- Azure Monitor
- Log Analytics Workspace
- KQL (basic)

## 🎯 Objective
- Enable monitoring for an Azure Virtual Machine
- Centralize logs using Log Analytics
- Validate VM connectivity using heartbeat logs

## 🧭 Implementation Steps

### 1️⃣ Virtual Machine Creation
- Created an Azure Virtual Machine to serve as the monitored resource.

📷 Screenshot: `screenshots/vm-overview.png`

### 2️⃣ Log Analytics Workspace
- Created a Log Analytics Workspace in the same region as the VM to store monitoring data.

📷 Screenshot: `screenshots/log-analytics-workspace.png`

### 3️⃣ Enable Azure Monitor
- Enabled VM Insights to connect the VM to Azure Monitor and Log Analytics.

### 4️⃣ Validation (Heartbeat Query)
- Validated monitoring by running a KQL query in Log Analytics:

```kusto
Heartbeat
| take 10
