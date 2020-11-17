# Phoronix test results report
#### By Aleksandar Alduk S3437526 
#### CPT264 – UNIX (Linux) Systems Administration and Programming (USAP), Study Period 3, 2020

***

## Introduction

This report will cover four test suites, including: 

### Test suite 1 - Memory
### Test suite 2 - 
### Test suite 3 - 
### Test suite 4 - 

These test suites will be analysed against known performance metrics and results will be reported in the results section below. 
An analysis will be formed based on those results.

***Disclaimer*** - Not all tests ran successfully, however, data was extrapolated as best as possible to obtain valid results to report on. Of the **xxx** tests run **xx** were successful.
 
***

## Method

The tests were initially chosen based on known impact to computing and relevance e.g. memory, cpu etc. As several tests have failed due to architecture compatibilities and other issues, the test suite selection was subject to further selective refinement and based on information gathered from the RMIT USAP Announocements discussion board [***available here.***](https://rmit.instructure.com/courses/70649/discussion_topics/983460)

Test suites were initially run via SSH CLI, however, due to timeout-related connectivity issues, a shift was made to GUI in order to minimuise impact based on errors due to lack of user input.

***

## Results

**Test suite 1 - Memory**
The below table illustrates the summarised results obtained from running the memory test suite:

which table results were uses - include url

**Results obtained from ptsmemoryv2 - ** [***available here.***](https://github.com/s3437526/USAP_Assignment2/blob/develop/tests/results/completed_tests/ptsmemoryv2/)
# Change all these to master branch URL!

**Summary of results:**
|**Test**|**Runs**|**Average result**|**Standard error**|**Standard deviation (%)**|
|:-----|:-----|:-----|:-----|:-----|
|Add Integer (MB/s)|4|4193.67|60.94|2.91|
|Copy Integer (MB/s)|3|4988.89|77.67|2.70|
|Scale Integer (MB/s)|6|4802.52|113.58|5.79|
|Triad Integer (MB/s)|3|4484.48|5.62|0.22|
|Average Integer (MB/s)|3|4319.34|17.79|0.71|
|Add Floating Point (MB/s)|3|4105.06|33.81|1.43|
|Copy Floating Point (MB/s)|3|3594.52|47.25|2.28|
|Scale Floating Point (MB/s)|6|4827.55|97.46|4.94|
|Triad Floating Point (MB/s)|3|4063.77|1.70|0.07|
|Average Floating Point (MB/s)|3|4040.06|11.36|0.49|
|Stream Copy (MB/s)|5|4013.02|7.73|0.43|
|Stream Scale (MB/s)|5|4042.86|10.96|0.61|
|Stream Triad (MB/s)|5|3718.44|7.17|0.43|
|Stream Add (MB/s)|4|3714.80|9.01|0.49|
|Tinymembench (MB/s)|3|2603.27|3.51|0.23|
|MBW Memory Copy - Array Size: 1024 MiB (MiB/s)|3|2474.92|0.69|0.05|
|MBW Memory Copt, Fixed Block Size - Array Size: 1024 MiB (MiB/s)|3|2481.30|0.90|0.06|
|T-test1 - Threads: 1 (Seconds)|3|203.15|0.32|0.27|
|T-test2 - Threads: 2 (Seconds)|3|72.37|0.16|0.39|
|CacheBench - Read Cache (MB/s)|3|3806.88|2.57|0.12|
|CacheBench - Read Cache (MB/s)|3|5213.89|5.72|0.19|

***Table 1 - Memory test results summary***

***

## Analysis



***

## Conclusion



***



• introduction (2 marks): explain the structure the report will have and what you plan to cover.
• method (3 Marks): outline what you did to decide which tests to run and the tests that you selected and how you ran them.
• results (5 marks): summarise the results of the tests you ran, include relevant tables and graphs that show the important parts of the results.
• analysis (8 Marks): discuss the results that you found and what they mean about the performance of your raspberry pi.
• conclusions (2 Marks): summarise the key points that you found in the results and analysis. 