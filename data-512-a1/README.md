# data-512-a1
This is Megan Nalani Chun's first assignment for DATA 512 Human Centered Data Science. Last modified 10/6/2020.

## goal
The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020.

## steps to reproduce 
1. Open the jupyter notebook [StepByStepNotebook.ipynb](https://github.com/NalaniKai/data-512/blob/main/data-512-a1/StepByStepNotebook.ipynb)
2. Follow the steps inside the notebook and run each cell in order, installing the specified libraries as needed. There are three main secions for gathering the data, processing the data, and analyzing the data through a time series chart. 

## source data
License:  
Wikimedia Foundation REST API terms of use: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions 

## relevant API documentation
https://www.mediawiki.org/wiki/Wikimedia_REST_API  
PageCounts documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts  
PageCounts endpoint: https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end  
PageViews documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews  
PageViews endpoint: https://wikimedia.org/api/rest_v1/#/Pageviews%20data

## final data file, en-wikipedia_traffic_200801-202008.csv
Column : Value  
  
year : YYYY  
month : MM  
pagecount_all_views : num_views  
pagecount_desktop_views : num_views  
pagecount_mobile_views : num_views  
pageview_all_views : num_views  
pageview_desktop_views : num_views  
pageview_mobile_views : num_views  

## special considerations
- data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not
- mobile data is available starting October 2014