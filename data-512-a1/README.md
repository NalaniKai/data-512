# data-512-a1
This is Megan Nalani Chun's first assignment for DATA 512 Human Centered Data Science. Last modified 10/6/2020.

## goal
The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020.

## steps to reproduce 
1. Open the jupyter notebook [StepByStepNotebook.ipynb](https://github.com/NalaniKai/data-512/blob/main/data-512-a1/StepByStepNotebook.ipynb)
2. Follow the steps inside the notebook and run each cell in order, installing the specified libraries as needed. There are three main secions for gathering the data, processing the data, and analyzing the data through a time series chart. 

## data sources
License: https://creativecommons.org/licenses/by-sa/3.0/  
Wikimedia Foundation REST API terms of use: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions 

### relevant API documentation
API: https://www.mediawiki.org/wiki/Wikimedia_REST_API  
PageCounts documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts  
PageCounts endpoint: https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end  
PageViews documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews  
PageViews endpoint: https://wikimedia.org/api/rest_v1/#/Pageviews%20data

## outputs
Outputs include:  
A. the raw data from the APIs in json format  
B. the final data file  
C. the image of the time series chart  

### A. the raw data from the APIs in json format   
These 5 json files have the format apiname_accesstype_firstyearmonth-lastyearmonth.json where yearmonth is YYYYMM.  

### B. the final data file
The final time series data can be found in [en-wikipedia_traffic_200801-202008.csv](https://github.com/NalaniKai/data-512/blob/main/data-512-a1/en-wikipedia_traffic_200801-202008.csv)  

This file has the following columns : values where pageview_mobile_views is the sum of the mobile app and mobile web pageview data from the pageview API.  
  
year : YYYY  
month : MM  
pagecount_all_views : num_views  
pagecount_desktop_views : num_views  
pagecount_mobile_views : num_views  
pageview_all_views : num_views  
pageview_desktop_views : num_views  
pageview_mobile_views : num_views  

### C. the image of the time series chart 
The final chart image can be found in [Time Series.png](https://github.com/NalaniKai/data-512/blob/main/data-512-a1/Time%20Series.png).

## special considerations
- data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not
- mobile data is available starting October 2014
- all views indicate the sum of the mobile and desktop views
- the license for this project is the license in the main folder for this repo