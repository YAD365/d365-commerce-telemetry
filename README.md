# d365-commerce-telemtry
Kusto queries and dashboards for D365 commerce operational insights

# Introduction

# How to Enable
Refer this article for steps needed to enable commerce scale units telemetry
[Enable diagnostic events in application insights](https://learn.microsoft.com/en-us/dynamics365/commerce/dev-itpro/retail-component-events-diagnostics-troubleshooting#enable-diagnostic-events-in-application-insights)
# Commerce EventIds
Below are the events emitted to customer application insights

| Event Id | Event Name |
| -- | -- |
| 1804 | CrtdataAccessSqlServerStoredProcedureFinished |
| 1809 | CrtDataAccessSqlServerSelectFinished |
| 1810 | CrtDataAccessSqlServerError |
| 1811 | CrtDataAcessSqlServerDataTypenoSupported |
| 5009 | RetailServerRequestFinished |
| 5008 | RetailServerRequestErrorFailure |