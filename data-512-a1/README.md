# Overview

The goal of this assignment is to collect data on Wikipedia page traffic over a multi-year period from Wikimedia REST APIs, perform some simple processing on that data, and then provide a visual analysis thereof. The code, external resources, intermediate files, and final results are all available in this repository. For reproducibility, the notebook `Submission.ipynb` is sufficient and complete (and also documents the necessary code thoroughly). 

# References

The source data is available under Wikipedia's standard Creative Commons license, as well as their standard Terms of Use and Privacy Policy (all linked below). The APIs used (Legacy and Pageviews, which combine to provide all data from 2008 to present) have their own terms of use, also linked below. Finally, the documentation for these APIs is also provided. 

- [Creative Commons Attribution-ShareAlike License](https://en.wikipedia.org/wiki/Wikipedia:Text_of_Creative_Commons_Attribution-ShareAlike_3.0_Unported_License)

    - [Additional Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en)
    
    - [Privacy Policy](https://foundation.wikimedia.org/wiki/Privacy_policy)

- [Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)

- [Legacy API Documentation API](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)

- [Pageviews API Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)


# Additional Documentation

The following are the columns in the final table result of our analysis, as seen at the end of `Submission.ipynb`, or in the CSV file in this repository. 

- `year`: identifies the year pertaining to a given row of data
- `month`: identifies the month 
- `pagecount_desktop_views`: number of views on Wikipedia, via the old "Legacy" API, desktop-version 
- `pagecount_mobile_views`: number of views on Wikipedia, via the old "Legacy" API, mobile-version
- `pagecount_all_views`: number of views on Wikipedia, via the old "Legacy" API, total (sum of desktop and mobile versions)
- `pageview_desktop_views`: number of views on Wikipedia, via the new API, desktop-version 
- `pageview_mobile_views`: number of views on Wikipedia, via the new API, mobile-version
- `pageview_all_views`: number of views on Wikipedia, via the new API, total (sum of desktop and mobile versions)


# Notes

- We refer to the "Legacy" API which provides data from 2008 to 2016, until the "pagecount" terminology was replaced by the "pageview" counterpart via the "Pageview" API (which covers 2015-present). So, despite some overlap, the Legacy and Pageview APIs are "old" and "new", respectively. 

- When using the Pageview API, crawlers/spiders are flagged, but this is not the case for the Legacy API. This is why in our code we are able to filter out only "user" agents in our queries for the Pageview API, but not the Legacy/Pagecount API.

