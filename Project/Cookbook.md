#Code Book

##Initial Data
The dataset for this project, see the README.txt found in

##Data Cleaning
The steps followed for data cleaning
1. Merge training and the test datasets to create one dataset
2. Extracts only the measure ments on the mean and standard deviation for each measurement
    - Read feature labels
    - Set the feature labels on the UCI daataset
    - Select only mean() and std() measurements
3. Uses descriptive activity names to name of the activities in the dataset
    - Load Activity labels
    - join with activity data.table 
  This will be used to add descriptive name to the activities
4. Appropriately labels the data set with descriptive variable names
    - Merge Subject and Activity tables
    - Merge the above with UCI dataset
   - Melt the data table to reshape it from a short and wide format to a tall and narrow format.
    - Seperate featuers from feature Name using helper function grepVar

5. Create a second, independent tidy data set with average of each variable for each activity and each subject
   - Create Tidydataset
    - Save Tidydataset

##Output Data Columns

> The resulting data set has 
[1] "subject": The subject id, an integer in the range 1:30          
[2] "activityNum": The activity id assigned to the activity performed      
[3] "activityName": The activity name assigned to the activity     
[4] "featureDomain": Features were calculated using the time and frequency Domain    
[5] "featureSensor": The two sensors used in the SmartPhone accelerometer and gyroscope   
[6] "featureMotion": the motion compoonents Body and Gravity    
[7] "featureJerk":    Jerk signal calculated   
[8] "featureMagnitude": Magniture of the signals calculated using Euclidean norm 
[9] "featureMeasure": Mean and Std Measures
[10] "featureAxis": 3 axial signals in X, Y and Z directions    
[11] "count":            Count of data points used to calculate average
[12] "average" :    Average of each variable for each activity and each subject

