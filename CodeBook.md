Code Book


### STEPS and PROCEDURES FOLLOWED TO CRAFT TIDY DATASET

- STEP 1 - Load train and test data set of X data. - read.table()

- STEP 2 - Load features information from features.txt file - read.table()

- STEP 3 - Convert meaningful variable names from feature set - gsub()

- STEP 4 - Merge train and test dataset - rbind()


- STEP 5 - Load subject info and activity list from relevant files - read.table()

- STEP 6 - Merge them with features dataset


- STEP 7 - Extract MEAN and STANDARD DEVIATION datasets from the merged dataset.

- STEP 8 - Convert them to table data frame - tbl_df


- STEP 9 - Calculate average value for all columns arranged via Subject and Activity - ddply()

- STEP 10 - Write resultant tidy data to tidy_data.txt file


### INPUT DATASET

No of Feature vector: 561

No of Observations: 10299

No of Subjects: 30

No of Activities: 6 (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) 

### OUTPUT DATASET

No of Feature Vector: 81 (33 + 33 + 13 + 1 + 1)
	- Means: 33
	- Standard Deviation: 33
	- Frequency Means: 13
	- Subject: 1
	- Activity: 1

**Feature Vectors**

                       subject                        activity                 tBodyAcc_mean_X                 tBodyAcc_mean_Y 
                      "subject"                      "activity"               "tBodyAcc_mean_X"               "tBodyAcc_mean_Y" 
                tBodyAcc_mean_Z                  tBodyAcc_std_X                  tBodyAcc_std_Y                  tBodyAcc_std_Z 
              "tBodyAcc_mean_Z"                "tBodyAcc_std_X"                "tBodyAcc_std_Y"                "tBodyAcc_std_Z" 
             tGravityAcc_mean_X              tGravityAcc_mean_Y              tGravityAcc_mean_Z               tGravityAcc_std_X 
           "tGravityAcc_mean_X"            "tGravityAcc_mean_Y"            "tGravityAcc_mean_Z"             "tGravityAcc_std_X" 
              tGravityAcc_std_Y               tGravityAcc_std_Z             tBodyAccJerk_mean_X             tBodyAccJerk_mean_Y 
            "tGravityAcc_std_Y"             "tGravityAcc_std_Z"           "tBodyAccJerk_mean_X"           "tBodyAccJerk_mean_Y" 
            tBodyAccJerk_mean_Z              tBodyAccJerk_std_X              tBodyAccJerk_std_Y              tBodyAccJerk_std_Z 
          "tBodyAccJerk_mean_Z"            "tBodyAccJerk_std_X"            "tBodyAccJerk_std_Y"            "tBodyAccJerk_std_Z" 
               tBodyGyro_mean_X                tBodyGyro_mean_Y                tBodyGyro_mean_Z                 tBodyGyro_std_X 
             "tBodyGyro_mean_X"              "tBodyGyro_mean_Y"              "tBodyGyro_mean_Z"               "tBodyGyro_std_X" 
                tBodyGyro_std_Y                 tBodyGyro_std_Z            tBodyGyroJerk_mean_X            tBodyGyroJerk_mean_Y 
              "tBodyGyro_std_Y"               "tBodyGyro_std_Z"          "tBodyGyroJerk_mean_X"          "tBodyGyroJerk_mean_Y" 
           tBodyGyroJerk_mean_Z             tBodyGyroJerk_std_X             tBodyGyroJerk_std_Y             tBodyGyroJerk_std_Z 
         "tBodyGyroJerk_mean_Z"           "tBodyGyroJerk_std_X"           "tBodyGyroJerk_std_Y"           "tBodyGyroJerk_std_Z" 
               tBodyAccMag_mean                 tBodyAccMag_std             tGravityAccMag_mean              tGravityAccMag_std 
             "tBodyAccMag_mean"               "tBodyAccMag_std"           "tGravityAccMag_mean"            "tGravityAccMag_std" 
           tBodyAccJerkMag_mean             tBodyAccJerkMag_std               tBodyGyroMag_mean                tBodyGyroMag_std 
         "tBodyAccJerkMag_mean"           "tBodyAccJerkMag_std"             "tBodyGyroMag_mean"              "tBodyGyroMag_std" 
          tBodyGyroJerkMag_mean            tBodyGyroJerkMag_std                 fBodyAcc_mean_X                 fBodyAcc_mean_Y 
        "tBodyGyroJerkMag_mean"          "tBodyGyroJerkMag_std"               "fBodyAcc_mean_X"               "fBodyAcc_mean_Y" 
                fBodyAcc_mean_Z                  fBodyAcc_std_X                  fBodyAcc_std_Y                  fBodyAcc_std_Z 
              "fBodyAcc_mean_Z"                "fBodyAcc_std_X"                "fBodyAcc_std_Y"                "fBodyAcc_std_Z" 
            fBodyAcc_meanFreq_X             fBodyAcc_meanFreq_Y             fBodyAcc_meanFreq_Z             fBodyAccJerk_mean_X 
          "fBodyAcc_meanFreq_X"           "fBodyAcc_meanFreq_Y"           "fBodyAcc_meanFreq_Z"           "fBodyAccJerk_mean_X" 
            fBodyAccJerk_mean_Y             fBodyAccJerk_mean_Z              fBodyAccJerk_std_X              fBodyAccJerk_std_Y 
          "fBodyAccJerk_mean_Y"           "fBodyAccJerk_mean_Z"            "fBodyAccJerk_std_X"            "fBodyAccJerk_std_Y" 
             fBodyAccJerk_std_Z         fBodyAccJerk_meanFreq_X         fBodyAccJerk_meanFreq_Y         fBodyAccJerk_meanFreq_Z 
           "fBodyAccJerk_std_Z"       "fBodyAccJerk_meanFreq_X"       "fBodyAccJerk_meanFreq_Y"       "fBodyAccJerk_meanFreq_Z" 
               fBodyGyro_mean_X                fBodyGyro_mean_Y                fBodyGyro_mean_Z                 fBodyGyro_std_X 
             "fBodyGyro_mean_X"              "fBodyGyro_mean_Y"              "fBodyGyro_mean_Z"               "fBodyGyro_std_X" 
                fBodyGyro_std_Y                 fBodyGyro_std_Z            fBodyGyro_meanFreq_X            fBodyGyro_meanFreq_Y 
              "fBodyGyro_std_Y"               "fBodyGyro_std_Z"          "fBodyGyro_meanFreq_X"          "fBodyGyro_meanFreq_Y" 
           fBodyGyro_meanFreq_Z                fBodyAccMag_mean                 fBodyAccMag_std            fBodyAccMag_meanFreq 
         "fBodyGyro_meanFreq_Z"              "fBodyAccMag_mean"               "fBodyAccMag_std"          "fBodyAccMag_meanFreq" 
       fBodyBodyAccJerkMag_mean         fBodyBodyAccJerkMag_std    fBodyBodyAccJerkMag_meanFreq           fBodyBodyGyroMag_mean 
     "fBodyBodyAccJerkMag_mean"       "fBodyBodyAccJerkMag_std"  "fBodyBodyAccJerkMag_meanFreq"         "fBodyBodyGyroMag_mean" 
           fBodyBodyGyroMag_std       fBodyBodyGyroMag_meanFreq       fBodyBodyGyroJerkMag_mean        fBodyBodyGyroJerkMag_std 
         "fBodyBodyGyroMag_std"     "fBodyBodyGyroMag_meanFreq"     "fBodyBodyGyroJerkMag_mean"      "fBodyBodyGyroJerkMag_std" 