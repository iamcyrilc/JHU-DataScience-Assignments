# Getting and Cleaning Data Code Book- Data Science Assignment 


This is code book contains information about `tidy_data.txt` 
dataset.

## Source Data
The source data is downloaded from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

See `ReadMe,md` for deatils about data processing.

## Project output data

The project output data is `tidy_data.txt`. This is a space separated table. The first row in the dataset list the column mames (variables).

## Variables

### Identifiers
..* `subjectId` - Id of the subject
..* `activity` - Activity performed by the subject while taking measurements.

###Measurements
Adding all columns increase the size of tidy_data.txt file and submission of the assignment fails. Therefore remove all column that are not used in  this analysis.

Retain columns `subjectId`, `analysis`, `*.mean* and `*.std*`

 [1] "subjectId"                                           
 [2] "activity"                                            
 [3] "timeBodyAccelorometer-Mean-Z"                        
 [4] "timeBodyAccelorometerStd-X"                          
 [5] "timeBodyAccelorometerStd-Y"                          
 [6] "timeBodyAccelorometerStd-Z"                          
 [7] "timeBodyAccelorometer-mad-X"                         
 [8] "timeBodyAccelorometer-mad-Y"                         
 [9] "timeGravityAccelorometer-Mean-Z"                     
[10] "timeGravityAccelorometerStd-X"                       
[11] "timeGravityAccelorometerStd-Y"                       
[12] "timeGravityAccelorometerStd-Z"                       
[13] "timeGravityAccelorometer-mad-X"                      
[14] "timeGravityAccelorometer-mad-Y"                      
[15] "timeBodyAccelorometerJerk-Mean-Z"                    
[16] "timeBodyAccelorometerJerkStd-X"                      
[17] "timeBodyAccelorometerJerkStd-Y"                      
[18] "timeBodyAccelorometerJerkStd-Z"                      
[19] "timeBodyAccelorometerJerk-mad-X"                     
[20] "timeBodyAccelorometerJerk-mad-Y"                     
[21] "timeBodyGyroscope-Mean-Z"                            
[22] "timeBodyGyroscopeStd-X"                              
[23] "timeBodyGyroscopeStd-Y"                              
[24] "timeBodyGyroscopeStd-Z"                              
[25] "timeBodyGyroscope-mad-X"                             
[26] "timeBodyGyroscope-mad-Y"                             
[27] "timeBodyGyroscopeJerk-Mean-Z"                        
[28] "timeBodyGyroscopeJerkStd-X"                          
[29] "timeBodyGyroscopeJerkStd-Y"                          
[30] "timeBodyGyroscopeJerkStd-Z"                          
[31] "timeBodyGyroscopeJerk-mad-X"                         
[32] "timeBodyGyroscopeJerk-mad-Y"                         
[33] "timeBodyAccelorometerMagnitude-mad"                  
[34] "timeBodyAccelorometerMagnitude-max"                  
[35] "timeGravityAccelorometerMagnitude-mad"               
[36] "timeGravityAccelorometerMagnitude-max"               
[37] "timeBodyAccelorometerJerkMagnitude-mad"              
[38] "timeBodyAccelorometerJerkMagnitude-max"              
[39] "timeBodyGyroscopeMagnitude-mad"                      
[40] "timeBodyGyroscopeMagnitude-max"                      
[41] "timeBodyGyroscopeJerkMagnitude-mad"                  
[42] "timeBodyGyroscopeJerkMagnitude-max"                  
[43] "frequencyBodyAccelorometer-Mean-Z"                   
[44] "frequencyBodyAccelorometerStd-X"                     
[45] "frequencyBodyAccelorometerStd-Y"                     
[46] "frequencyBodyAccelorometerStd-Z"                     
[47] "frequencyBodyAccelorometer-mad-X"                    
[48] "frequencyBodyAccelorometer-mad-Y"                    
[49] "frequencyBodyAccelorometer-MeanFrequency-Z"          
[50] "frequencyBodyAccelorometer-skewness-X"               
[51] "frequencyBodyAccelorometer-kurtosis-X"               
[52] "frequencyBodyAccelorometerJerk-Mean-Z"               
[53] "frequencyBodyAccelorometerJerkStd-X"                 
[54] "frequencyBodyAccelorometerJerkStd-Y"                 
[55] "frequencyBodyAccelorometerJerkStd-Z"                 
[56] "frequencyBodyAccelorometerJerk-mad-X"                
[57] "frequencyBodyAccelorometerJerk-mad-Y"                
[58] "frequencyBodyAccelorometerJerk-MeanFrequency-Z"      
[59] "frequencyBodyAccelorometerJerk-skewness-X"           
[60] "frequencyBodyAccelorometerJerk-kurtosis-X"           
[61] "frequencyBodyGyroscope-Mean-Z"                       
[62] "frequencyBodyGyroscopeStd-X"                         
[63] "frequencyBodyGyroscopeStd-Y"                         
[64] "frequencyBodyGyroscopeStd-Z"                         
[65] "frequencyBodyGyroscope-mad-X"                        
[66] "frequencyBodyGyroscope-mad-Y"                        
[67] "frequencyBodyGyroscope-MeanFrequency-Z"              
[68] "frequencyBodyGyroscope-skewness-X"                   
[69] "frequencyBodyGyroscope-kurtosis-X"                   
[70] "frequencyBodyAccelorometerMagnitude-mad"             
[71] "frequencyBodyAccelorometerMagnitude-max"             
[72] "frequencyBodyAccelorometerMagnitude-kurtosis"        
[73] "frequencyBodyBodyAccelorometerJerkMagnitude-mad"     
[74] "frequencyBodyBodyAccelorometerJerkMagnitude-max"     
[75] "frequencyBodyBodyAccelorometerJerkMagnitude-kurtosis"
[76] "frequencyBodyBodyGyroscopeMagnitude-mad"             
[77] "frequencyBodyBodyGyroscopeMagnitude-max"             
[78] "frequencyBodyBodyGyroscopeMagnitude-kurtosis"        
[79] "frequencyBodyBodyGyroscopeJerkMagnitude-mad"         
[80] "frequencyBodyBodyGyroscopeJerkMagnitude-max"         
[81] "frequencyBodyBodyGyroscopeJerkMagnitude-kurtosis"    
[82] "angletBodyGyroscopeMean,gravityMean"                 
[83] "angletBodyGyroscopeJerkMean,gravityMean"             
[84] "angleX,gravityMean"                                  
[85] "angleY,gravityMean"                                  
[86] "angleZ,gravityMean"  

##Activity Labels
These are the activities that the subject performed while taking the measurements.

Note: `activity` column is converted to `factor` so that it list descriptive activity names.


..*1 - WALKING
..*2 - WALKING_UPSTAIRS
..*3 - WALKING_DOWNSTAIRS
..*4 - SITTING
..*5 - STANDING
..*6 - LAYING