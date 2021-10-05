# data-512-a1

## Goal
The goal of this project is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2021. All analysis is performed in a single Jupyter notebook. Generated data file and a time series graphic visualization of the dataset can also be found in this repo.

## Data 
In this project, data is collected from two different API endpoints, the Legacy Pagecounts API and the Pageviews API: <br />

* The Legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from December 2007 through July 2016.

* The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month.

[Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)


## Final data file fields
| Column        | Value         |
| ------------- | ------------- |
| year          | YYYY          |
| month         | MM            |
| pagecount_all_views  | num_views            |
| pagecount_desktop_views  | num_views            |
| pagecount_mobile_views  | num_views            |
| pageview_all_views  | num_views            |
| pageview_desktop_views  | num_views            |
| pageview_mobile_views  | num_views            |


## Notes for user
* The data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
* Data collected from the Pageviews API provides values for mobile-app and mobile-web. This project combines them to create a total mobile traffic count for each month.

## License
This project is under [The MIT License](https://opensource.org/licenses/MIT)
