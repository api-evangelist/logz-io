<!-- fetched 2026-10-13 from https://api-docs.logz.io/docs/logz/search/ by sweep-shape-compat.py; text extracted from the provider's own page -->

Search logs | Logz.io API docs Skip to main content 
 API Ship data API System status Blog 
 Search 
 Get a Demo Free Trial Login 
 Logz-api 
 Introduction 
 Search logs 
 Search logs 
 Scroll logs 
 Unified Alerts 
 Alerts 
 Deployments 
 Insights 
 Logz.io snapshots 
 Security account 
 Security rules 
 Security events 
 Lookup lists 
 Manage users 
 Manage metrics account 
 Manage consumption tracing accounts 
 Authentication groups 
 Associated accounts 
 Who am I 
 Manage time-based log accounts 
 Manage shared tokens 
 Manage API tokens 
 Manage notification endpoints 
 Import or export Kibana objects 
 Manage log shipping tokens 
 Drop filters 
 Archive logs 
 Restore logs 
 Parsing 
 Delete object API 
 Retrieve audit trail 
 Connect to CloudTrail 
 Connect to S3 Buckets 
 Get instant query 
 Get label names 
 Get label values 
 Get metric metadata 
 Get range query 
 Get series by labels 
 Post instant query 
 Post label names 
 Post range query 
 Post series by labels 
 Logz.io Dashboards 
 Dashboard Folders (Projects) 
 Grafana get all folders 
 Grafana contact points 
 Grafana data source 
 Grafana alerting provisioning 
 Grafana silence management 
 Grafana annotations 
 Grafana dashboards 
 Grafana dashboard search 
 Grafana snapshots 
 Logz-api 
 Search logs 
 Search logs 
 Search logs
 POST /v1/search
 Searches your account data using the Elasticsearch Search API DSL query language. total: This call returns up to 1,000 results per query for aggregated results, or 10,000 results for non-aggregated results. Note: To ensure speed and availability of your logs, we restrict some options from the Elasticsearch defaults that could hamper system performance. Restrictions are described with their respective elements below. Please ensure to change the region in the URL to match your account's region.
 Request ​ 
 application/json
 Body
 required 
 query object required The query can take any of the parameters described in the Elasticsearch Search API DSL documentation with the exceptions stated below.
 If you don’t want to apply any filters, pass an empty JSON object in the request body using --data '{}'.
 Limitations
 When using query_string , allow_leading_wildcard must be set to false 
 wildcard can't start with * or ? 
 Can't contain fuzzy_max_expansions , max_expansions , or max_determinized_states 
 Notes on the search time range
 By default, your query runs on data sent today and yesterday, UTC. You can move this 2-calendar-day window by using the dayOffset query parameter.
 Searches without a timestamp filter will return the last 2 calendar days, UTC. You can search other calendar days (up to 2 at a time) using a filter on the timestamp .
 from integer Of the results found, the first result to return.
 size integer Possible values: <= 10000 
 Default value: 10 
 Number of results to return
 sort object[] Limitations
 Can't sort or aggregate on analyzed fields, such as the message field
 _source object The object includes specifies an array of strings specifying an array of fields to return.
 If you omit _source from the request, all fields are returned.
 If you pass '_source': false , it will exclude the _source field from the results.
 includes string[] Array of fields to return
 post_filter object A filter applied after the aggregations have been calculated. Useful for reusing a single query to calculate several outputs with different filtering criteria. See the Elasticsearch guide for details.
 docvalue_fields string[] Powers inverted indexing. Allows queries to look up the search term in unique sorted list by @timestamp. See the Elasticsearch guide for details.
 version boolean Returns a version for each result. See the Elasticsearch guide for details.
 stored_fields string[] Useful for querying for fields that don’t appear in the _source field or querying for larger documents by date or title. See the Elasticsearch guide for details.
 highlight object Highlight strings in one or more fields in your search results. See the Elasticsearch guide for details.
 aggregations object Apply field aggregations. See the Elasticsearch guide for details.
 Limitations
 When using the size element, the value must be ≤ 1000 
 Can't nest 2 or more bucket aggregations of these types: date_histogram , geohash_grid , histogram , ip_ranges , significant_terms , terms 
 Can't sort or aggregate on analyzed fields, such as the message field
 Aggregation type significant_terms and multi_terms can't be used Note: You can use aggs or aggregations as the field name
 Responses ​ 
 200
 successful query. hits are the total number of logs that match the query, which will always be in the 0-2 day range. total are the actual logs that are returned when using the query, which are not limited by the selected time range.
 application/json
 Schema 
 Schema 
 object
 Loading...
 Previous
 Search logs
 Next
 Scroll logs
 Additional Links
 Blog 
 Videos 
 Notices for 3rd Party Software included with the Logz.io Platform 
 Report a security issue 
 Legal
 Privacy Policy 
 Terms of Use 
 Sending Data to Logz.io 
 Trademark Legal Notice 
 Contributers 
 Social
 Facebook 
 Twitter 
 YouTube 
 LinkedIn 
 GitHub 
 Any use of the Logz.io API is subject to our Terms of Use .
Copyright © 2026 Logshero Ltd.
