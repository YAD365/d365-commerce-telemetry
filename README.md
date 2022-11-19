# d365-commerce-telemetry
Kusto queries and dashboards for Dynamics 365 Commerce/ Finance and Operations operational insights

# Table of Contents
- [Introduction](#what-is-operational-insights)
- [Prerequisites](#prerequisites)
- [Enable Operational Insights](#how-to-enable)
- [Supported Events](Kusto/README.md)
- [Sample Kusto Queries](Kusto/Sample/README.md)
- [Sample Dashboards](Kusto/Downloads/README.md)

# Introduction
## What is Operational Insights
Operational Insights is a Dynamics 365 Finance and Operations/ Commerce HQ out of box feature to enable commerce scale units diagnostic events in customer application insights subscription.

# Prerequisites
- Azure Application Insights resource. Refer [Create an Appliation Insights resource](https://learn.microsoft.com/en-us/azure/azure-monitor/app/create-new-resource#create-an-application-insights-resource-1)
- Or an existing Application Insights Instrumentation Key
- Operations Insights feature enabled. Refer [How to enable](#how-to-enable)
- Experience with Kusto query language. Refer [language overview](https://docs.microsoft.com/en-us/azure/kusto/query/) for language overview and tutorial

# How to Enable
Refer this article for steps needed to enable commerce scale units telemetry
[Enable diagnostic events in application insights](https://learn.microsoft.com/en-us/dynamics365/commerce/dev-itpro/retail-component-events-diagnostics-troubleshooting#enable-diagnostic-events-in-application-insights)