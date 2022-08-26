---
title: "CodeBook"
author: "Kareena Mulchandani"
date: "27/08/2022"
output: html_document
---

```{r script}

## Description

Additional information about the variables, data and transformations used in the course project for the Johns Hopkins Getting and Cleaning Data course.

## Source Data

Data + Description can be found here [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

The run_analysis.R script will make the necessary transformations to answer the questions asked in the subject

The data.table and reshape2 library is required for the following:

##1 We first need to download the files and dataset and unzip them in the data/UCI HAR Dataset folder.

Download and unzip the "getdata_projectfiles_UCI HAR Dataset.zip" in your data folder. It must contain the following files:

activity_labels.txt: The list of the text labels and their ids
measurements: values
features.txt: The list of the features

README.txt 5: A short description of the Human Activity Recognition Using Smartphones Dataset and its methodology And the following folders containing respectively:


train (folder): 1.1. subject_train.txt 20 ko: Identifies the subject who performed the activity for each sample 1.2. X_train.txt 64 460 ko: The train sets 1.3. y_train.txt 15 ko: The list of activities ids associated with each train set row

test (folder): Identifies the subject who performed the activity for each sample 


##2 We performed the read.table function to create : - the dataframe features_df (561 rows, 2 cols) with the content of "./data/UCI HAR Dataset/features.txt" and named the columns "id" and "pattern". It is the list of the features collected by the various sensors described in the "features_info.txt" document. - the dataframe activities_df (6 rows, 2 cols) with the content of "./data/UCI HAR Dataset/activity_labels.txt" and named the columns "id" and "label", it gives us a readable label for the activities listed in the y_test and y_train datasets.

##3 Merging the training and the test sets to create one data set. We did this with test and train as we merged all by column bind.


##5 Uses descriptive activity names to name the activities in the data set Now we replace the activities ids in the dataset with their text value stored in the label column of the activities_df dataset

##6 Appropriately labels the data set with descriptive variable names. - The column Y represents the activities, so it will be renamed "activity" - The other names are composed with the following abbreviations or string repetition are replaced with the "gsub" function.

##7 create a new data set with the average of each variable for each activity and each subject - Creation of the dataframe by Subject_activity with tidyData rows grouped by "subject" and "activity" columns and summarised with the mean function on each variable using reshape2.
```


