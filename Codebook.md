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

## Variables:

For Downloading the data:
1)ZipUrl- stores the url id
2)ZipFile-  file name

For rading, extracting and summarizing data:

## Reading training data
1)trainingSubjects 
2)trainingValues
3)trainingActivity

## Reading Test Data
4)testSubjects
5)testValues 
6)testActivity

7)features-      stores features from the features.txt
8)activities-    reading activity_labels.txt
9)humanActivity- helps bind together trainingSubjects, trainingValues, trainingActivity,
                 testSubjects, testValues, testActivity
10)columnsToKeep-  determine columns of data set to keep based on column name
11)humanActivityMeans- group by subject and activity and summarise using mean

##library loaded - deplyr

