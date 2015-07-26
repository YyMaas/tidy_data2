<<<<<<< HEAD
---
title: "README"
author: "YyMaas"
date: "July 25, 2015"
output: html_document
---

#Overview
The accompanying script downloads, unzips, and reads in the data collected
from the accelerometers from the Samsung Galaxy S smartphone. The script 
matches the subjects (1 through 30) with the activities (e.g, walking, 
sitting, etc.), for both the test and train datasets, and combines these 
into a dataset called, fulldata. The script then selects only variables 
that include either the a mean or standard deviation measurement and 
creates a subset called, data_mean_std (dim=1099 x 88). 
The variables in this dataset are then renamed to follow a 
more meaningful pattern. The script then groups by subject and
activity and generates the mean value of each measurement for each
subject-activity pairing in a dataset called, tidy_group_means. 

#Accompanying files
run_analysis.R is the R script that downloads and maniuplates the original 
Samsung Galaxy S smartphone data and generates the dataset tidy_group_means.
Codebook.txt describes in more detail the variable names and data
processing.
tidy_group_means.txt is the final output of the accompanying R script
and can be invoked in R by data <- read.table(file_path, header=TRUE)

#R Libraries used in script in addition to base R
dpylr
Note: if dplyr is not installed, you will need to run
install.packages(dplyr) prior to running the script. This command
is not included in the script.

#Samsung Galaxy S smartphone data and references
##Reference
Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012
##Overview of tests and data
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

Notes: 
======
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.

=======
# get_clean_data
>>>>>>> 7af4a7ba9bb4e4feadbdc7d79da71921ce6fe9cf
