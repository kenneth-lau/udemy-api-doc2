# Exercise 4: Documenting query parameters

## Bug Squisher API

### Query parameters

Parameter | Description | Type | Required | Notes
--- | --- | --- | --- | --- |
startDate | Start date for when the bug was created | Date | Optional |  Format: YYYY-MM-DD. Default is the earliest recorded bug.
endDate | The end date for when the bug was created | Date | Optional |  Format: YYYY-MM-DD. Default is today's date.
priority | The priority value. (How important is it.) | Integer | Optional | Integer of 1 to 4, where 1 is the highest priority. Default is all priorities.
severity | The severity value. (How big the impact is.) | Integer | Optional | Integer of 1 to 4, where 1 is the most severe. Default is all severities.
status | The status of the bug. | String | Optional | Valid values: open, closed, duplicate, notabug. Default is all statuses.
start | For pagination, the starting index. Zero is the first bug on the list. | Number | Optional | Default is zero.
total | For pagination, the total number of bugs to return | Number | Optional | Default is the number of bugs minus the start value.

### Sample request

This request returns the first 10 bugs from November 26, 2016 to December 31, 2016.

`GET https://api.bugsquisher.com/bug?startDate=2016-11-26&endDate=2016-12-31&total=10`
