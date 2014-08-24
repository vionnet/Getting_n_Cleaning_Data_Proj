Getting_n_Cleaning_Data_Proj
============================

##This is a repo for the Getting and Cleaning Data course project.
###Below are project instructions and requirements.

The purpose of this project is to demonstrate your ability to collect, work
with, and clean a data set. The goal is to prepare tidy data that can be used
for later analysis. You will be graded by your peers on a series of yes/no
questions related to the project. You will be required to submit: 1) a tidy
data set as described below, 2) a link to a Github repository with your script
for performing the analysis, and 3) a code book that describes the variables,
the data, and any transformations or work that you performed to clean up the
data called CodeBook.md. You should also include a README.md in the repo with
your scripts. This repo explains how all of the scripts work and how they are
connected. 

###Here are the data for the project: 

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

###You should create one R script called run_analysis.R that does the following.  

* Merges the training and the test sets to create one data set.
* Extracts only the measurements on the mean and standard deviation for each
measurement.  
* Uses descriptive activity names to name the activities in the data set
* Appropriately labels the data set with descriptive variable names.  
* Creates a second, independent tidy data set with the average of each variable
for each activity and each subject. 

###Below are steps for data cleaning.
* Setting up the file directories based on the instruction of "the code should
have a file run_analysis.R in the main directory that can be run as long as the
Samsung data is in #your working directory.can be run as long as the Samsung
data is in your working directory". I interpret this instruction as that the
working directory contains the activity_labels.txt, features.txt, etc. It also
contains the test and train folders for test and training datasets.
* Obtaining a list of file names in the test directory, and a list of file
names in the train directory.
* Getting the features file from the working directory.
* Creating a subset of features that only contains "mean()" or "std()" measures.
* Getting activity labels from the activity_labels file.
* Combining text files in the test folder by column based on descriptions of
the files. After this operation, we combine test subjects, test number, and
test feature into one dataset.
* Performing similar operations to obtain the training dataset.
* Combining the test and the training data into one dataset.
This addresses "1. Merges the training and the test sets to create one data
set".
* Transform the combined data set so that test features (with name "VNo.")
are in one column for each subject and test number.
* Put a "V" in front of the feature number for merging.
* Merge the transformed(or melted) dataset with the sub_feature dataset.
for features in the sub_feature data. This addresses "2.Extracts only the
measurements on the mean and standard deviation for each measurement."
* Merge dataset above with activity labels to get activity names.
This addresses "3.Uses descriptive activity names to name the activities in the
data set".
* Change column names so that they are more descriptive.
This addresses "4.Appropriately labels the data set with descriptive variable
names".
* Obtaining the average of each variable (feature) for each activity and each
subject. This addresses "6. Creates a second, independent tidy data set with
the average of each variable for each activity and each subject".
* Created a txt file with write.table() using row.name=FALSE, and write it to
the current directory.





