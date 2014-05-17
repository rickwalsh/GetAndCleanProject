
ReadMe for Course Project
Rick Walsh May 15, 2014

The following files are used in the analysis.

Subjects are those that performed the activity.  They are in these two files.
- 'subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 
- 'subject_test.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

Features are the initial descriptions of the measurements taken.  These descriptions are reworked in the code to make 
them more readable.
- 'features.txt': List of all features.

The measurements from the device are from the tables below.
- 'X_train.txt': Training set.
- 'X_test.txt': Test set.

The Activity for each measurement is stored in these files, with a numeric value.
- 'y_train.txt': Training labels.
- 'y_test.txt': Test labels.

The Activity name for the 6 activities is stored in this file.
- 'activity_labels.txt': Links the class labels with their activity name.

Per the project requirements, the run_analysis.r script does as follows with these files:
--appends the test and train measurements into one data set
--appends the test and train activities into one set
--appends the test and train subject ID's into one set
--eliminates all measurements from the data set except those dealing with STD and MEAN as required
--combines subjects, activities, and measurements into a single data set
--modifies the headers from the features file into a more readable format
--maps the activity numbers to the activity_labels for ease of reading
--summarizes the data set by taking the mean of the MEAN and STD measurements by subject and activity
--saves the output in a tab-delimited file called set5.txt

