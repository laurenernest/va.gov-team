# VA.gov site search monitoring

## Search rate anomaly
https://vagov.ddog-gov.com/monitors/186811

What is: 
* Monitor that checks for calls to `v0/search` API endpoint every hour for anomalies in average search rate success(200 responses). 
* Alarms if calls fall below threshold of 10% of the average anomaly bounds

## VA.gov success rate below threshold
https://vagov.ddog-gov.com/monitors/169139

What is: 
* Monitor that checks for 200 (success) responses from the `v0/search` API endpoint
* Alarms if success rates fall below 97%

[Video](https://us06web.zoom.us/rec/play/1Ea8wq1sRg2QssQox4fJ5TICQZPxBYQq05VncjI0Hyl8-gnao9RbxHQL1rNo1yI9K2yV63MAN9vXVhPh.LOjbjqtrOAjdoQFh?canPlayFromShare=true&from=my_recording&startTime=1698786445000&componentName=rec-play&originRequestUrl=https%3A%2F%2Fus06web.zoom.us%2Frec%2Fshare%2FE5dbb6Ewhi7ILpS2qMwZ1WmEnRa1caieprd3UEQWmlTVGCSKSKCORZeFrodBHPI.o6MlyTOrLC1En0z1%3FstartTime%3D1698786445000) where Adrian Rollett steps through some triage for this monitor
Passcode: 55$kzl1+

* Scroll down to Status & History. Click-drag and highlight the red or orange warn/error timeframe, to zoom/highlight it
* This will modify the date/timestamp in the "UTC" field right above the toolbar. Click in that field to highlight / copy the timeframe for use on other screens. 
* Go to https://vagov.ddog-gov.com/apm/home?env=eks-prod
  * Go to vets-api, paste the timeframe - look for any big picture errors that might indicate vets-api latency is the problem
  * Go to [search](https://vagov.ddog-gov.com/apm/services/search/operations/rack.request/resources?env=eks-prod&panels=qson%3A%28data%3A%28%29%2Cversion%3A%210%29&resources=qson%3A%28data%3A%28visible%3A%21t%2Chits%3A%28selected%3Atotal%29%2Cerrors%3A%28selected%3Atotal%29%2Clatency%3A%28selected%3Ap95%29%2CtopN%3A%215%29%2Cversion%3A%211%29&summary=qson%3A%28data%3A%28visible%3A%21t%2Cerrors%3A%28selected%3Acount%29%2Chits%3A%28selected%3Acount%29%2Clatency%3A%28selected%3Alatency%2Cslot%3A%28agg%3A95%29%2Cdistribution%3A%28isLogScale%3A%21f%29%2CshowTraceOutliers%3A%21f%29%2Csublayer%3A%28slot%3A%28layers%3Aservice%29%2Cselected%3Apercentage%29%29%2Cversion%3A%211%29&view=spans&start=1704213833501&end=1704217433501&paused=false), paste the timeframe
* Check for error states / API response errors / logs

## Slack Channels for Alerts
- #public-websites-monitoring
- #devops-alerts
