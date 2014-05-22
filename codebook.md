
## CodeBook for Course Project
## Rick Walsh May 21, 2014

## A. Study Design

Data was collected via the an embedded accelerometer and gyroscope, captured 3-axial linear acceleration 
and 3-axial angular velocity at a constant rate of 50Hz.  Units are noted below.

Attribute Information:

For each record in the dataset it is provided: 
* Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
* Triaxial Angular velocity from the gyroscope. 
* A 561-feature vector with time and frequency domain variables. 
* Its activity label. 
* An identifier of the subject who carried out the experiment.

The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. 

Notes: 
======
* Features are normalized and bounded within [-1,1].
* Each feature vector is a row on the text file.

Reference:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## B. Variables in the Set

The point of the exercise is to process the data above into a 'final' set of Mean and Average values
for the 30 subjects, for 6 measurements.

The data set provided for review is tab delimited and consists of 181 rows (180 data rows and a header) by 68 columns.

The 180 data rows include 6 measurement rows for each of the 30 Subjects as required.

The 68 columns include the Subject number and Activity description as the first two columns, followed 
by 66 columns of sensor signals of averages for mean and standard deviations of various measurements,
as listed below.  The averages in the data set were built from a the larger set of measurements
noted in section A.

There are 66 columns of sensor data in the file created as columns with references to Mean or Std 
were extracted from the 561 columns provided in the larger data set per the system requirements.

The 68 columns are as follows:

* 1. Subject (a number 1-30, for each of the 30 Subjects)
* 2. Activity (one of these 6 descriptions: "Walking", "Walking Upstairs", 
"Walking Downstairs", "Sitting", "Standing", "Laying")
* 3 through 68 are these measurements, in this order: 

* TimeBodyAccelerationMeanX
* TimeBodyAccelerationMeanY
* TimeBodyAccelerationMeanZ
* TimeBodyAccelerationStdX
* TimeBodyAccelerationStdY
* TimeBodyAccelerationStdZ
* TimeGravityAccelerationMeanX
* TimeGravityAccelerationMeanY
* TimeGravityAccelerationMeanZ
* TimeGravityAccelerationStdX
* TimeGravityAccelerationStdY
* TimeGravityAccelerationStdZ
* TimeBodyAccelerationJerkMeanX
* TimeBodyAccelerationJerkMeanY
* TimeBodyAccelerationJerkMeanZ
* TimeBodyAccelerationJerkStdX
* TimeBodyAccelerationJerkStdY
* TimeBodyAccelerationJerkStdZ
* TimeBodyGyroscopeMeanX
* TimeBodyGyroscopeMeanY
* TimeBodyGyroscopeMeanZ
* TimeBodyGyroscopeStdX
* TimeBodyGyroscopeStdY
* TimeBodyGyroscopeStdZ
* TimeBodyGyroscopeJerkMeanX
* TimeBodyGyroscopeJerkMeanY
* TimeBodyGyroscopeJerkMeanZ
* TimeBodyGyroscopeJerkStdX
* TimeBodyGyroscopeJerkStdY
* TimeBodyGyroscopeJerkStdZ
* TimeBodyAccelerationMagnitudeMean
* TimeBodyAccelerationMagnitudeStd
* TimeGravityAccelerationMagnitudeMean
* TimeGravityAccelerationMagnitudeStd
* TimeBodyAccelerationJerkMagnitudeMean
* TimeBodyAccelerationJerkMagnitudeStd
* TimeBodyGyroscopeMagnitudeStd
* TimeBodyGyroscopeMagnitudemad
* TimeBodyGyroscopeJerkMagnitudeMean
* TimeBodyGyroscopeJerkMagnitudeStd
* FrequencyBodyAccelerationMeanX
* FrequencyBodyAccelerationMeanY
* FrequencyBodyAccelerationMeanZ
* FrequencyBodyAccelerationStdX
* FrequencyBodyAccelerationStdY
* FrequencyBodyAccelerationStdZ
* FrequencyBodyAccelerationJerkMeanX
* FrequencyBodyAccelerationJerkMeanY
* FrequencyBodyAccelerationJerkMeanZ
* FrequencyBodyAccelerationJerkStdX
* FrequencyBodyAccelerationJerkStdY
* FrequencyBodyAccelerationJerkStdZ
* FrequencyBodyGyroscopeMeanX
* FrequencyBodyGyroscopeMeanY
* FrequencyBodyGyroscopeMeanZ
* FrequencyBodyGyroscopeStdX
* FrequencyBodyGyroscopeStdY
* FrequencyBodyGyroscopeStdZ
* FrequencyBodyAccelerationMagnitudeMean
* FrequencyBodyAccelerationMagnitudeStd
* FrequencyBodyAccelerationJerkMagnitudeMean
* FrequencyBodyAccelerationJerkMagnitudeStd
* FrequencyBodyGyroscopeMagnitudeMean
* FrequencyBodyGyroscopeMagnitudeStd
* FrequencyBodyGyroscopeJerkMagnitudeMean
* FrequencyBodyGyroscopeJerkMagnitudeStd

Column names for columns 3-68 follow this convention:
* Frequency means Frequency domain signals via Fast Fourier Transformations
* Body means signals from the body, rather than from gravity
* Gravity means signals from gravity, rather than from the body
* Gyroscope means signals from the gyroscope
* Acceleration are signals from the accelerometer
* Magnitude is the magnitude of the signal
* Jerk means jerk signals
* Mean is the average
* Std is standard deviation
* X means in the x-axis
* Y means in the y-axis
* Z means in the z-axis

Note: Capitalization of initial letters in the words, and elimination of most abbreviations 
in the columns noted above was performed to make the column names very clear and descriptive.
(The course materials discuss BOTH capitalizing first letters as well as using all lower
case.  For this circumstance, due to length of column names, initial capitals are used
intentinonally for readability).

## C. Transformations

Column names for the measurements were constructed using the naming conventions listed above.

Activity is a mapping of values 1-6 to the "Walking", "Walking Upstairs", "Walking Downstairs",
"Sitting", "Standing", "Laying" list included above.

The numeric values in the 66 sensor columns are built using the 'mean' function on a 
larger set of data values, by Subject by Activity.

The original data set consists of 561 columns of data.  This analysis is specifically on only data values
of Mean and StandardDeviation (Std).  This means the data was loaded as 561 columns but transformed via
the script to 66 columns of Mean and Std data only, along with Subject and Activity for a total of 
68 columns.

The 68 columns are the following column numbers from the 561 original:
(1:6,41:46,81:86,121:126,161:166,201:202,214:215,
227:228,241:242,253:254,266:271,345:350,
424:429,503:504,516:517,529:530,542:543)

The R script included performs the the transformations described above to create the final data set.
The code was created and executed to produce the file on a Windows 7 computer.


