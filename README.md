# Getting-and-Cleaning-Data
Coursera Course

## explaining Code
# Clean up workspace
# 1. Merge the training and the test sets to create one data set.

#set working directory to the location where the UCI HAR Dataset was unzipped
Read in the data from files
Read in the test data
Assigin column names to the data imported above
Assign column names to the test data imported above
Create the final training set by merging yTrain, subjectTrain, and xTrain
Create the final test set by merging the xTest, yTest and subjectTest data
Combine training and test data to create a final data set
Create a vector for the column names from the finalData, which will be used to select the desired mean() & stddev() columns

# 2. Extract only the measurements on the mean and standard deviation for each measurement. 
Create a logicalVector that contains TRUE values for the ID, mean() & stddev() columns and FALSE for others
Subset finalData table based on the logicalVector to keep only desired columns
Merge the finalData set with the acitivityType table to include descriptive activity names
Updating the colNames vector to include the new column names after merge

# 4. Appropriately label the data set with descriptive activity names. 

Cleaning up the variable names by removing 
-std to stdDev
-mean to Mean
(t) to Time ...
Reassigning the new descriptive column names to the finalData set

# 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject. 
Create a new table, finalDataNoActivityType without the activityType column
Summarizing the finalDataNoActivityType table to include just the mean of each variable for each activity and each subject
Merging the tidyData with activityType to include descriptive acitvity names
Export the tidyData set using write.table ()
