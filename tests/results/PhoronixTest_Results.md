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

***Disclaimer*** - Not all tests ran successfully, however, data was extrapolated as best as possible to obtain valid results to report on. Of the 24 test suites run 14 were successful or seemed to provide adequate reportable data.
 
***

## Method

The tests were initially chosen based on known impact to computing and relevance e.g. memory, cpu etc. As several tests failed due to architecture compatibilities and other issues such as failed dependencies, the test suite selection was subject to further selective refinement and based on information gathered from the RMIT USAP Announocements discussion board [***available here.***](https://rmit.instructure.com/courses/70649/discussion_topics/983460)

Test suites were initially run via SSH CLI, however, due to timeout-related connectivity issues, a shift was made to GUI to minimuise impact based on errors due to lack of user input.

***

## Results

### Test suite 1 - Memory
The below table illustrates the summarised results obtained from running the memory test suite:

Results obtained from ptsmemoryv2 - [***available here.***](completed_tests/ptsmemoryv2/)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011179-KH-PTSMEMORY32)  

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

Results obtained from ptscpuv2 - [***available here.***](completed_tests/ptscpuv2)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011177-KH-PTSCPUV2941)  

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

Results obtained from ptsdiskv2 - [***available here.***](completed_tests/ptsdiskv2)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011162-KH-PTSDISKV231)  

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

Results obtained from ptscompressionresults10Nov - [***available here.***](completed_tests/ptscompressionresults10nov)  
Detailed uploaded results are available on the openbenchmarking.org website [***here.***](https://openbenchmarking.org/result/2011179-KH-PTSCOMPRE60)  

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

According to raw data across three runs of the test and with the standard deviation of 2.28%, there isn't any conclusive evidence (comparative to other tests) to indicate that this is the result of additional unaccounted workload or the demand of the test.  

According to results specified at openbenchmarking.org this Raspberry Pi performs between the 6th and 13th (low tier) percentile across the RAMspeed tests compared to other tested systems.  

More testing would be needed to gather more conclusive evidence.  

***Memory Bandwidth - MBW***  

Surprisingly, the memory bandwidth performance was on the low end of the "Low-Tier" systems tested. It performed below the 8th and 10th percentile for the same array sizes compared to other tested systems. However, the testing pool is smaller in this test category.

#### CPU Analysis:
***Rodinia 2.4***  

The Rodinia 2.4 OpenMP accelerator performed between the 21st and 22nd percentile. While this still classifies it as a "Low-Tier" device, it performed surprisingly well in the LavaMD test, considering its closest competitors were an AMD Ryzen 5 2600 and Intel Xeon Silver 4215R.  

The CFD Solver test placed the unit below the 3rd percentile which initially made it appear as an underperforming device. However, considering its nearest recorded competition is an Intel Core i5-M CPU it is difficult to determine that this is in fact the case. Further testing against similar devices would provide more conclusive evidence and greater context.  

***OpenSSL***  

At 97.27 signs per second the Raspberry Pi performs between the 5th and 7th percentile. This is on par with its competitors in the "Low-Tier" systems.

#### Disk Analysis:
***SQLite***  

This performance metric measures the timed insertions of data into an indexed database. The performance of this test places the Raspberry Pi in the 22nd percentile across its competitors. While it still places in the "Low-Tier" category, it is at the top end and is in competition with reputable brand SSDs and M.2 drives.

***FS-Mark 3.3***  

The file system performance test average result of 19.87 files processed per second places the Raspberry Pi between the 15th and 16th percentile across its competitors when testing 1,000 files at 1MB per file.  

When processing 5000 files of the same size across 4 threads the unit average result is 24.27 files per second. This places it in the 7th percentile across its competitors. However, it is worth noting that the unit performs noticeably better compared to the results for a single thread. In fact, it processes 1,000 more files at a cost of an additional 4.4 seconds. This result had a higher degree of error with a standard deviation of 9.48%.   

When processing 4,000 files across 32 sub-directories the unit performed slightly better  than 1,000 files across one thread. This is impressive considering the additional workload of directory traversal. Unfortunately there was no competition data recorded for comparison.

Finally, when processing 1,000 files at 1MB per file without synchronisation, the performance was significantly degraded. This is understandable as FSync is responsible for optimising file processing. This test was subject to a degree of error as it took 6 runs to achieve, and yielded a standard deviaiton of 8.01%. Again, there is no comparable data across other devices to determine whether there were external factors which contributed to this performance decrease.  

#### Compression Analyis:
***7-Zip Compression***  

The compression speed of 7-Zip places the performance of the Raspberry Pi between the 14th and 15th percentile. While still in the "Low-Tier" category, it is on par with its peers.  

***Parallel BZIP2 Compression***  

Using BZIP2 as a compression mechanism the Raspberry Pi managed to compress a 256MB Linux kernel source in 69.19 seconds. This is still in the "Low-Tier" category, placing between the 7th and 9th percentile among other ARMv7s and lower end AMD and Intel processors.  

***Gzip Compression/Decompression***  

Similar to BZIP2, the Raspberry Pi places in the 9th percentile - and among its peers - at 158.83 seconds to compress a Linux source tree to .tar.gz. Unfortunately, no comparable data is available for decompression results. More testing would need to be done in order to obtain a comparable variety of results.  

***XZ Compression/Decompression***  

Interestingly, according to its peers, the Raspberry Pi placed between the 4th and 6th percentile in performance when compressing an image of ubuntu16.04.3-server-i386. This is towards the bottom of the performance chart. Again, there is no comparable data for file decompression.

***

## Conclusion

Overall, the Raspberry Pi computer performs well compared to its peer architectures and in a number of tests produced more favourable results. Some performance characteristics such as CPU and Disk are comparable to and in some cases better than well known modern hardware such as the AMD Ryzen 5, Intel Xeon Silver and M.2 and other SSD drives.  

The unit test results are relatively consistent given similar test cases such as those within the RAMspeed SMP category. Of those tests, only a few minor noteworthy points and dips in performance were observed. Some tests lack comparative data among competing hardware systems, resulting in a limited test analysis. Quality of the analysis could be improved with a wider testing pool and further iterations of the chosen tests. No major anomalies were observed during the analysis of the test results.  

While the unit consistently performed in the "Low-Tier" computer category, it is important to note is that it is a ~$100 all-in-one computer, after all.

***
