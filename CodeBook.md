##This is a code book that describes the variables, the data, and any
transformations or work that I performed to clean up the data

###Variables
| Name | Class | Size | Description    |
|------|-------|------|----------------|
|curdir|charactor|1   | URL for current directory|
|testFileUrl|charactor| 1 | URL for the test directory|
|trainFileUrl|charactor|1 | URL for the train directory|
|testFN|charactor|3 | A vector that contains file names in the test directory|
|trainFN|charactor|3|A vector that contains file names in the train directory|

###Data
| Name | Class | Size | Description    |
|------|-------|------|----------------|
|features|data.frame| 561 by 2| The features dataset|
|sub_features|data.frame| 66 by 2| Dataset extracted from the features dataset|
|activity_labels|data.frame| 6 by 2|The activity labels dataset|
|test_data|data.frame|2947 by 563| dataset created from files in the test folder|
|train_data|data.frame|7352 by 563| dataset created from files in the train folder|
|data|data.frame|10299 by 563|A combined test and training datasets|
|mdata|data.frame|5777739 by 4| A melted dataset with test subject and number being the ID and feature name being the variable|
|ddata|data.frame|679734 by 5| A subset of the mdata that only contains features in the sub_features data|
|ddata2|data.frame|679734 by 6| Dataset as above with names of activities|
|clean_data| data.frame| 679734 by 4| Same as ddata2 without redundant columns|
|tidy_data|data.frame|11880 by 4| Summary of clean_data with the average value for each feature, test subject, and activity combination|


###Transformations
|Transformation| Purpose|
|--------------|--------|
|Changing first and last column names of test_data| Column names more descriptive|
|Changing first and last column names of train_data| Column names more descriptive|
|Melt data| Subject and Test_No become IDs, and feature name become variables|
|add V to feature number in the sub_feature data| Names become consistent with those in the mdata for merging|
|merge mdata and sub_features| To get a subset of  mean and std features and their names|
|merge ddata and activity_labels| To get activity names|
|change last two column names of ddata2| Column names are more descriptive|
|Delete 2 columns from ddata2 and re-order remaining columns| To get an organized data without any redundant columns|
|Summarize clean_data| To get tidy data required|  

