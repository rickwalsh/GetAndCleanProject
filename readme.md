
## ReadMe for Course Project
## Rick Walsh May 21, 2014

## Description

The following files are used in the analysis.

Subjects are those that performed the activity.  They are in these two files.
* 'subject_train.txt': Each row identifies the subject who performed the activity for 
each window sample. Its range is from 1 to 30. 
* 'subject_test.txt': Each row identifies the subject who performed the activity for 
each window sample. Its range is from 1 to 30. 

Features are the initial descriptions of the measurements taken.  These descriptions are 
reworked in the R code to make them more readable.
* 'features.txt': List of all features.

The measurements from the device are from the tables below.
* 'X_train.txt': Training set.
* 'X_test.txt': Test set.

The Activity for each measurement is stored in these files, with a numeric value.
* 'y_train.txt': Training labels.
* 'y_test.txt': Test labels.

The Activity name for the 6 activities is stored in this file.
* 'activity_labels.txt': Links the class labels with their activity name.

## Pseudocode:

Per the project requirements, the run_analysis.r script does as follows with these files:
*appends the test and train Measurements into one data set
*appends the test and train Activities into one set
*appends the test and train Subject ID's into one set
*eliminates all measurements from the data set except those dealing with 
STD and MEAN as required (transforming from 561 measurements to 66)
*combines subjects, activities, and measurements into a single data set
*modifies the headers from the features file into a more readable format
*maps the activity numbers to the activity_labels for ease of reading
*summarizes the data set by taking the mean of the MEAN and STD measurements by 
subject and activity per the requirements
*in doing so, it creates 180 data records, 6 activities for 30 subjects 
*saves the output in a tab-delimited file called set5.txt, ordered by subject and activity

The run_analysis.r scipt was created and executed to produce the file on a Windows 7 computer.


