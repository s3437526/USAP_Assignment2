# Phoronix test results report
#### By Aleksandar Alduk S3437526 
#### CPT264 – UNIX (Linux) Systems Administration and Programming (USAP), Study Period 3, 2020

***

## Introduction

This report will cover four test suites, including: 

- Test suite 1 - Memory
- Test suite 2 - CPU
- Test suite 3 - Disk
- Test suite 4 - Compression

These test suites will be analysed against known performance metrics and results will be reported in the results section below. 
An analysis will be formed based on those results.

***Disclaimer*** - Not all tests ran successfully, however, data was extrapolated as best as possible to obtain valid results to report on. Of the **xxx** tests run **xx** were successful or seemed to provide adequate reportable data.
 
***

## Method

The tests were initially chosen based on known impact to computing and relevance e.g. memory, cpu etc. As several tests have failed due to architecture compatibilities and other issues, the test suite selection was subject to further selective refinement and based on information gathered from the RMIT USAP Announocements discussion board [***available here.***](https://rmit.instructure.com/courses/70649/discussion_topics/983460)

Test suites were initially run via SSH CLI, however, due to timeout-related connectivity issues, a shift was made to GUI in order to minimuise impact based on errors due to lack of user input.

***

## Results

### Test suite 1 - Memory
The below table illustrates the summarised results obtained from running the memory test suite:

Results obtained from ptsmemoryv2 - [***available here.***](https://github.com/s3437526/USAP_Assignment2/blob/develop/tests/results/completed_tests/ptsmemoryv2/)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011179-KH-PTSMEMORY32)
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

### Test suite 2 - CPU
The below table illustrates the summarised results obtained from running the CPU test suite:

Results obtained from ptscpuv2 - [***available here.***](https://github.com/s3437526/USAP_Assignment2/tree/develop/tests/results/completed_tests/ptscpuv2)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011177-KH-PTSCPUV2941)
# Change all these to master branch URL!

**Summary of results:**
|**Test**|**Runs**|**Average result**|**Standard error**|**Standard deviation (%)**|
|:-----|:-----|:-----|:-----|:-----|
|Rodinia OpenMP LavaMD (Seconds)|3|418.82|2.72|1.13|
|Rodinia OpenMP CFD Solver (Seconds)|3|283.19|4.23|2.59|
|7-Zip Compression - Compress Speed Test (MIPS)|3|3519|43.09|2.12|
|Timed Linux Kernel Compilation (Seconds)|3|1837.42|3.82|0.36|
|OpenSSL - RSA 4096-bit Performance (Signs/s)|3|97.27|0.09|0.16|
|Sysbench - CPU (Events/s)|3|393.57|0.45|0.20|

***Table 2 - CPU test results summary***

***

### Test suite 3 - Disk
The below table illustrates the summarised results obtained from running the Disk test suite:

Results obtained from ptsdiskv2 - [***available here.***](https://github.com/s3437526/USAP_Assignment2/tree/develop/tests/results/completed_tests/ptsdiskv2)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011162-KH-PTSDISKV231)
# Change all these to master branch URL!

**Summary of results:**
|**Test**|**Runs**|**Average result**|**Standard error**|**Standard deviation (%)**|
|:-----|:-----|:-----|:-----|:-----|
|SQLite - Timed Insertions (Seconds)|4|91.18|1.56|3.42|
|FS-Mark - 1,000 Files (@1MB) (Files/s)|3|19.87|0.28|2.48|
|FS-Mark - 5,000 Files (@1MB), 4 Threads (Files/s)|6|24.27|0.94|9.48|
|FS-Mark - 4,000 Files,(@1MB), 32 Sub Dirs  (Files/s)|3|18.77|0.19|1.71|
|FS-Mark - 1,000 Files (@1MB), No Sync/FSync (Files/s)|6|31.08|1.02|8.01|
|Dbench - 12 Clients (MB/s)|3|86.67|0.71|6.72|
|Dbench - 1 Clients (MB/s)|3|44.66|0.43|1.65|
|Compile Bench - Initial Compile (MB/s)|6|11.75|0.44|9.25|
|Compile Bench - Initial Create (MB/s)|3|10.46|0.71|11.74|
|Compile Bench - Read Compiled Tree (MB/s)|3|114.68|0.57|0.86|
|PostMark - Disk Transaction Performance (TPS)|3|67|1.20|3.09|

***Table 3 - Disk test results summary***

***

### Test suite 4 - Compression
The below table illustrates the summarised results obtained from running the Compression test suite:

Results obtained from ptscompressionresults10Nov - [***available here.***](https://github.com/s3437526/USAP_Assignment2/tree/develop/tests/results/completed_tests/ptscompressionresults10nov)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011179-KH-PTSCOMPRE60)
# Change all these to master branch URL!

**Summary of results:**
|**Test**|**Runs**|**Average result**|**Standard error**|**Standard deviation (%)**|
|:-----|:-----|:-----|:-----|:-----|
|Zstd Compression - Level 3 (MB/s)|3|105.80|0.17|0.28|
|Zstd Compression - Level 19 (MB/s)|3|2.58|N/A|0.22|
|Zstd Compression - Compress Speed Test (MIPS)|3|3745|11.05|0.51|
|Parallel BZIP2 Compression - 256 MB File (Seconds)|6|69.19|1.32|4.66|
|Gzip Compression - Linux Source Tree Archiving To .tar.gz (Seconds)|4|158.83|2.67|3.37|
|XZ Compression - ubuntu-16.04.3-server-i386.img, Level 9 (Seconds)|3|375.94|1.69|0.78|
|System GZIP Decompression - Phoronix Test Suite v5.2.1 (Seconds)|4|11.72|0.20|3.36|
|System XZ Decompression - Phoronix Test Suite v5.2.1 (Seconds)|3|14.13|0.04|0.52|
|System ZLIB Decompression - Phoronix Test Suite v5.2.1 (Seconds)|20|5764.39|82.12|6.37|

***Table 4 - Compression test results summary***

***

## Analysis

Due to the large volume of tests performed and the overlap of tests between test suites, the results of some carefully selected key tests will be included in the analysis.
These are:

- RAMspeed SMP (Memory)
- MBW (Memory)
- Rodinia 2.4 (CPU)
- OpenSSL (CPU)
- SQLite (Disk)
- FS-Mark 3.3 (Disk)
- 7-Zip Compression (Compression)
- Parallel BZIP2 Compression (Compression)
- Gzip Compression/Decompression (Compression)
- XZ Compression/Decompression (Compression)

#### Memory Analysis:
***RAMspeed SMP***  
According to the results shown above it can be seen that the RAM performed relatively evenly across the board in the range of 4000 and 5000 MB/s. This includes the whole (integer) and real (floating point) numbers and a variety of computations e.g. Adding, averaging, copying, scaling and triads.  

A noteworthy observation was made about the result of the copying of a floating point number which scored below the range at 3594.52 MB/s. As this computation doesn't seem like such a demanding task compared to other tests it is unclear whether or not there was a dip in the performance due to other influences e.g. additional unplanned computational load such as user-initiated tasks.  

According to raw data across three runs of the test and with the standard deviation of 2.28%, there there isn't any conclusive evidence (comparitive to other tests) which indicates that this is the result of additional unaccounted workload or the demand of the test.  

According to results specified at openbenchmarking.org this Raspberry Pi performs between the 6th and 13th (low tier) percentile across the RAMspeed tests compared to other tested systems.  

More testing would should be done to gather conslusive evidence.  


***Memory Bandwidth - MBW***  

Surprisingly, the memory bandwidth performance was on the low end of the "Low-Tier" systems tested. It performed below the 8th and 10th percentile for the same array sizes compared to other tested systems. However, the testing pool is smaller in this test category.

***Personal notes..***
cover results across the board, and comapre them
compare against other hardware available online
RISC vs CISC?


#### CPU Analysis:
***Rodinia 2.4***  


***OpenSSL***  


#### Disk Analysis:
***SQLite***  


***FS-Mark 3.3***  


#### Compression Analyis:
***7-Zip Compression***  


***Parallel BZIP2 Compression***  


***Gzip Compression/Decompression***  


***XZ Compression/Decompression***  


***

## Conclusion



***



• introduction (2 marks): explain the structure the report will have and what you plan to cover.  
• method (3 Marks): outline what you did to decide which tests to run and the tests that you selected and how you ran them.  
• results (5 marks): summarise the results of the tests you ran, include relevant tables and graphs that show the important parts of the results.  
• analysis (8 Marks): discuss the results that you found and what they mean about the performance of your raspberry pi.  
• conclusions (2 Marks): summarise the key points that you found in the results and analysis. 
