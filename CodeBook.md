# Coursera GACD Project Codebook

## September 20, 2014
## Experimental Design and Background

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years.
Each person performed six activities (WALKING, WALKING UPSTAIRS, WALKING DOWNSTAIRS,
SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its
embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity
at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually.
The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected
for generating the training data and 30

## Raw Data

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then
sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor
acceleration signal, which has gravitational and body motion components, was separated using a Butterworth
low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only
low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window,
a vector of features was obtained by calculating variables from the time and frequency domain. See ’features
info.txt’ for more details. The features selected for this database come from the accelerometer and
gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix ’t’ to denote
time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and
a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the
acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and
tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.
Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals
(tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals
were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBody-
GyroMag, tBodyGyroJerkMag).

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ,
fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note
the ’f’ to indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for each pattern: ’-XYZ’ is used to denote
3-axial signals in the X, Y and Z directions.

## Data Source

Dataset Description:

Data Download: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
The dataset includes the following files: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

 Within the ’UCI HAR Dataset’ folder:
– activity labels.txt
– features.txt
– features info.txt
– README.txt
 Within the ’Train’ sub-folder:
– subject train.txt
– X train.txt
– y train.txt
– Inertial Signals (folder contents not used)
 Within the ’Test’ sub-folder:
– subject test.txt
– X test.txt
– y test.txt
– Inertial Signals (folder contents not used)

## Processed Data

Ensure that dplyr is installed on your machine before running the associated script file. This can be done
by utilizing the following code:

install.packages(“dplyr”)

Additionally, the R script was run on a machine utilizing Windows 7 and R 3.1.1.

The mean and the standard deviation data was calculated for each of the measurements from the raw
data. The raw data was then provided in a “test” and “train” data sets with the averaged values. The average
and standard deviation values are of particular interest, thus they were extracted from the data set.
The data was tidied and the renamed such that abbreviations were eliminated from the descriptions, nonalphanumeric
characters were eliminated, and the titles were written in camel-case to make for easier reading.

### The activities for the 30 subjects are designated as follows:
1. Walking
2. Walking Upstairs
3. Walking Downstairs
4. Sitting
5. Standing
6. Laying

### The labels are as follow:
1. TimeBodyAccelerationMeanX
2. TimeBodyAccelerationMeanY
3. TimeBodyAccelerationMeanZ
4. TimeBodyAccelerationStandardDevX
5. TimeBodyAccelerationStandardDevY
6. TimeBodyAccelerationStandardDevZ
7. TimeGravityAccelerationMeanX
8. TimeGravityAccelerationMeanY
9. TimeGravityAccelerationMeanZ
10. TimeGravityAccelerationStandardDevX
11. TimeGravityAccelerationStandardDevY
12. TimeGravityAccelerationStandardDevZ
13. TimeBodyAccelerationJerkMeanX
14. TimeBodyAccelerationJerkMeanY
15. TimeBodyAccelerationJerkMeanZ
16. TimeBodyAccelerationJerkStandardDevX
17. TimeBodyAccelerationJerkStandardDevY
18. TimeBodyAccelerationJerkStandardDevZ
19. TimeBodyGyroMeanX
20. TimeBodyGyroMeanY
21. TimeBodyGyroMeanZ
22. TimeBodyGyroStandardDevX
23. TimeBodyGyroStandardDevY
24. TimeBodyGyroStandardDevZ
25. TimeBodyGyroJerkMeanX
26. TimeBodyGyroJerkMeanY
27. TimeBodyGyroJerkMeanZ
28. TimeBodyGyroJerkStandardDevX
29. TimeBodyGyroJerkStandardDevY
30. TimeBodyGyroJerkStandardDevZ
31. TimeBodyAccelerationMagMean
32. TimeBodyAccelerationMagStandardDev
33. TimeGravityAccelerationMagMean
34. TimeGravityAccelerationMagStandardDev
35. TimeBodyAccelerationJerkMagMean
36. TimeBodyAccelerationJerkMagStandardDev
37. TimeBodyGyroMagMean
38. TimeBodyGyroMagStandardDev
39. TimeBodyGyroJerkMagMean
40. TimeBodyGyroJerkMagStandardDev
41. FrequencyBodyAccelerationMeanX
42. FrequencyBodyAccelerationMeanY
43. FrequencyBodyAccelerationMeanZ
44. FrequencyBodyAccelerationsTimedX
45. FrequencyBodyAccelerationsTimedY
46. FrequencyBodyAccelerationsTimedZ
47. FrequencyBodyAccelerationMeanX
48. FrequencyBodyAccelerationMeanY
49. FrequencyBodyAccelerationMeanZ
50. FrequencyBodyAccelerationJerkMeanX
51. FrequencyBodyAccelerationJerkMeanY
52. FrequencyBodyAccelerationJerkMeanZ
53. FrequencyBodyAccelerationJerksTimedX
54. FrequencyBodyAccelerationJerksTimedY
55. FrequencyBodyAccelerationJerksTimedZ
56. FrequencyBodyAccelerationJerkMeanX
57. FrequencyBodyAccelerationJerkMeanY
58. FrequencyBodyAccelerationJerkMeanZ
59. FrequencyBodyGyroMeanX
60. FrequencyBodyGyroMeanY
61. FrequencyBodyGyroMeanZ
62. FrequencyBodyGyrosTimedX
63. FrequencyBodyGyrosTimedY
64. FrequencyBodyGyrosTimedZ
65. FrequencyBodyGyroMeanX
66. FrequencyBodyGyroMeanY
67. FrequencyBodyGyroMeanZ
68. FrequencyBodyAccelerationMagMean
69. FrequencyBodyAccelerationMagsTimed
70. FrequencyBodyAccelerationMagMean
71. FrequencyBodyAccelerationJerkMagMean
72. FrequencyBodyAccelerationJerkMagsTimed
73. FrequencyBodyAccelerationJerkMagMean
74. FrequencyBodyGyroMagMean
75. FrequencyBodyGyroMagsTimed
76. FrequencyBodyGyroMagMean
77. FrequencyBodyGyroJerkMagMean
78. FrequencyBodyGyroJerkMagsTimed
79. FrequencyBodyGyroJerkMagMean

Each of these data values were then averaged for each subject according to the activity to produce the final
table of processed data. This data is then written to a text file titled "course_project.txt"
