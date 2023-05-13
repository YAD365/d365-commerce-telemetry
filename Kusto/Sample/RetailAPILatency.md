# Kusto for all Retail API latency

Below query summarizes API latency summarize into 50, 75, 90 and 99 percentile buckets and can be rendered as a chart as shown in below image

```kusto

let _startTime = datetime('2022-12-01T15:27:36Z');
let _endTime = datetime('2022-12-01T16:27:36Z');
let _environmentId = ''; //Environment Id from LCS
let _retailAPI = ''; 
let ['_scaleunitId']='';
traces
| where timestamp between (['_startTime'] .. ['_endTime'])
| where customDimensions.TenantId == _environmentId
| where isempty(['_scaleunitId']) or customDimensions.ScaleUnitId == ['_scaleunitId']
| where customDimensions.EventId == 5009
| extend latency = toint(customDimensions.executionTimeMilliseconds)
| extend apiAction = tostring(customDimensions.apiAction)
| extend apiController = tostring(customDimensions.apiController)
| extend api = strcat(apiController,"\\",apiAction)
| extend retailAPIModifiedParamter = iif(_retailAPI contains "'", split(_retailAPI, "'")[1], _retailAPI)
| where isempty(retailAPIModifiedParamter) or api == retailAPIModifiedParamter
| summarize percentiles(latency, 50, 75, 90, 99)  by bin(timestamp, 5m)
