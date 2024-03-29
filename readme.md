
## Getting and Cleaning Data - Course Project -

This file is describing how to run run_analysis.R script and what outcome file generates.

1. download and unzip the data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip and replace spaces (" ") by underscore in the folder so we have a folder with name "UCI_HAR_Dataset".
2. Double check that "UCI_HAR_Dataset" and run_analysis.R script are both in the current working directory.
3. use source("run_analysis.R") command in RStudio. 
4. you will find two output files are generated in the current working directory: 
   * merged_data.txt (7.9 Mb): it contains a data frame called cleanedData with 10299*68 dimension.
   * data_with_means.txt (220 Kb): it contains a data frame called result with 180*68 dimension.

Finally, use data <- read.table("data_with_means.txt") command in RStudio to read the file. 
Since we are required to get the average of each variable for each activity and each subject, 
and there are 6 activities in total and 30 subjects in total, we have 180 rows with all combinations 
for each of the 66 features.