# Getting and Cleaning Data Course Project

This repository contains the R code and documentation files for the "Getting and Cleaning Data" course project.

## Files

- `run_analysis.R`: The main R script that performs the data cleaning and transformation
- `CodeBook.md`: Describes the variables, the data, and transformations performed
- `README.md`: Explains how the scripts work and how they are connected
- `final_tidy_data.txt`: The output tidy dataset created by the script

## How the Script Works

1. First, it downloads and unzips the dataset if not already present in the working directory.
2. It reads all the relevant data files (features, activity labels, test data, train data).
3. It merges the training and test sets to create one dataset.
4. It extracts only the measurements on the mean and standard deviation for each measurement.
5. It uses descriptive activity names to name the activities in the dataset.
6. It appropriately labels the dataset with descriptive variable names.
7. It creates a second, independent tidy dataset with the average of each variable for each activity and each subject.
8. Finally, it writes the tidy dataset to a file called `final_tidy_data.txt`.

To run the script, simply source it in R:
```r
source("run_analysis.R")
```

## Requirements

The script requires the following R packages:
- dplyr
- tidyr

These can be installed with:
```r
install.packages(c("dplyr", "tidyr"))
```
