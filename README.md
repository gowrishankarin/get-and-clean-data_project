# Geting & Cleaning Data - PROJECT

This document explains the flow of code to tidy-up [Human Activity Recognition Using Smartphones Data Set][1] from [UCI ML Repository][2] using [R-Programming Language][3]. 
This repo has 3 files
  - **run_analysis.R** - Run analysis file is a copy of my actual development file in Data_Scient Repository. This file is created for project submission purpose only. Complete history of development can be found in its source repository. [Data_Science][4], [run_analysis.R][5]
  - **README.md** - Read Me file consummates the project details.
  - CookBook.md - Cook Book lists the variables and tidied data of HAR repo.

### How to Reproduce the result
>git clone https://github.com/shankarchari/get-and-clean-data_project

>cd get-and-clean-data_project

>wget https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

>unzip getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

>R

>source('run_analysis.R')

>tidy_data <- main()

>tidy_data



### FLOW

STEP 1 - Load train and test data set of X data. - read.table()

STEP 2 - Load features information from features.txt file - read.table()

STEP 3 - Convert meaningful variable names from feature set - gsub()

STEP 4 - Merge train and test dataset - rbind()


STEP 5 - Load subject info and activity list from relevant files - read.table()

STEP 6 - Merge them with features dataset


STEP 7 - Extract MEAN and STANDARD DEVIATION datasets from the merged dataset.

STEP 8 - Convert them to table data frame - tbl_df


STEP 9 - Calculate average value for all columns arranged via Subject and Activity - ddply()

STEP 10 - Write resultant tidy data to tidy_data.txt file


### R Functions for Getting, Cleaning and Tidy-up data
>Run Analysis R file has 7 functions,

**main()** - Main function is the entry point to rest all function. It takes no Input and returns tidies data.

**load()**   - Reads the X train and test data and merges. It takes location at which HAR data is stored. Default: current directory

**read_dataset()**  - Reads the datasets(activity and subject) and merges with x data.

**extract()**   - Extracts the relevant mean and standard deviation data. Frequency mean is also extracted from the data.

**tidy_dataset()**  - Extracted data is passed as input and returns tidied data to Main function.

**read_inertial_data()**  - This function is unused but reads the inertial dataset.

**main2()** - This function is written for quick development and testing.






[1]:http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
[2]:http://archive.ics.uci.edu/ml/index.html
[3]:http://www.r-project.org/
[4]:https://github.com/shankarchari/data_science
[5]:https://github.com/shankarchari/data_science/blob/master/gcd/project/run_analysis.R
