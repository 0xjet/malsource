# The Malsource Dataset



### Description
This repository contains the dataset described in the paper:

* A. Calleja, J. Tapiador, and J. Caballero. "The MalSource Dataset: Quantifying Complexity and Code Reuse in Malware Development." _IEEE Transactions on Information Forensics and Security_, Vol 14, No. 12, pp. 3175-3190, 2018. [[pdf](https://arxiv.org/pdf/1811.06888.pdf)]
\
\
**Abstract**
  > In this paper, we analyze the evolution of malware from 1975 to date from a software engineering perspective. We analyze the source code of 456 samples from 428 unique families and obtain measures of their size, code quality, and estimates of the development costs (effort, time, and number of people). Our results suggest an exponential increment of nearly one order of magnitude per decade in aspects such as size and estimated effort, with code quality metrics similar to those of benign software. We also study the extent to which code reuse is present in our dataset. We detect a significant number of code clones across malware families and report which features and functionalities are more commonly shared. Overall, our results support claims about the increasing complexity of malware and its production progressively becoming an industry.

### The dataset

The [samples](https://github.com/0xjet/malsource/tree/main/samples) folder contains the 456 samples of malware source code. The zip file is split due to GiHub's file size limit.

The [csv](https://github.com/0xjet/malsource/tree/main/csv) folder contains four CSV files with the data used in the measurements. Each CSV is intended for a different set of measurements and there are some redundancies across them.

**types.year.csv:** It contains the creation/detection year and the type of sample for the 456 projects in the dataset:
* **name**: Name of the sample.
* **year**: The year when the sample was written or first spotted in the wild.
* **type**: Type of malware sample (trojan, worm, virus, etc).

**stats.per.project.language:** It contains size stats broken down by language for all projects in the dataset.
* **name:** Name of the sample.
* **language:** Language to which the current rows refers to.
* **files:** Number of *language* files.
* **blanks:** Total number of blank likes in *language* files.
* **comments:** Total number of commented lines in *language* files.
* **SLOC:** Total count of source lines of code for *language*.
* **year:** Year when the sample was written or first spotted in the wild.

**stats.all.projects.csv**: It contains size and cost metrics for all projects in the dataset.
* **name:** Name of the sample.
* **year:** Year when the sample was written or first spotted in the wild.
* **langs:** Number of different programming languages present in the sample.
* **total_files:** Mumber of files in the sample, including all extensions.
* **total_blanks:** Total number of blank likes in all source files.
* **total_comments:** Total number of commented lines in all source files.
* **comment_ratio:** Ratio between comments and SLOCS.
* **total_SLOC:** Total number of source lines of code in all source files.
* **total_FP:** Total number of unadjusted function points (obtained by backfiring from SLOCS).
* **CC_organic_effort:** COCOMO effort estimation using organic coefficients (man/month).
* **CC_organic_time:** COCOMO development time estimation using organic coefficients (months).
* **CC_organic_persons:** COCOMO team size estimation using organic coefficients (people).
* **CC_semide_effort:** COCOMO effort estimation using semi-detached coefficients (man/month).
* **CC_semide_time:** COCOMO development time estimation using semi-detached coefficients (months).
* **CC_semide_persons:** COCOMO team size estimation using semi-detached coefficients (people).
* **CC_embedded_effort:** COCOMO effort estimation using embedded coefficients (man/month).
* **CC_embedded_time:** COCOMO development time estimation using embedded coefficients (months).
* **CC_embedded_persons:** COCOMO team size estimation using embedded coefficients (people). 

**stats.projects.complete.csv:** This CSV contains metrics for a subset of the main dataset: 143 projects for which we were able to compute the cyclomatic complexity and the maintainability index.
* **name:** Name of the sample.
* **year:** Year when the sample was written or first spotted in the wild
* **langs:** Number of different programming languages present in the sample.
* **total_files:** Number of files in the sample, including all extensions.
* **total_blanks:** Total number of blank likes in all source files.
* **total_comments:** Total number of commented lines in all source files.
* **comment_ratio:** Ratio between comments and SLOCS.
* **total_SLOC:** Total number of Source lines of code in all source files.
* **total_FP:** Total number of unadjusted function points (obtained by backfiring from SLOCS).
* **CC_organic_effort:** COCOMO effort estimation using organic coefficients (man/month).
* **CC_organic_time:** COCOMO development time estimation using organic coefficients (months).
* **CC_organic_persons:** COCOMO team size estimation using organic coefficients (people).
* **CC_semide_effort:** COCOMO effort estimation using semi-detached coefficients (man/month).
* **CC_semide_time:** COCOMO development time estimation using semi-detached coefficients (months).
* **CC_semide_persons:** COCOMO team size estimation using semi-detached coefficients (people).
* **CC_embedded_effort:** COCOMO effort estimation using embedded coefficients (man/month).
* **CC_embedded_time:** COCOMO development time estimation using embedded coefficients (months).
* **CC_embedded_persons:** COCOMO team size estimation using embedded coefficients (people).
* **avg_cyclomatic_complexity_per_function:** Average cyclomatic complexity per function in this sample.
* **maitainability_index:** Maintainability index for this project.




