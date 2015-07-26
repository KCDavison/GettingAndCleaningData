# GettingAndCleaningData
Course Project 


The run_analysis.R script opens the appropriate data files provided and combines them to provide a tidy, meaningful dataset. 

First, the script reads the applicable tables into R. These tables are: the Activity lables, The features table (headers for the data), subject_test amd subject_train (which provide the applicable subjects performing the activities for both the test and the training data set), y_train and y_test (which provide the activity performed for both the training and test datasets). 


First, all of the x data is combined using an rbind function. This gives us the total number of observations in the data. The feautres dataset is assigned as the column names to this new combined data set, which provides the headers to determine which measurement is being provided in each column. 

The y_test and y_train datasets are combind, and then binded to the combined x train & test dataset. The activity labels are merged onto this final dataset. 

The code then determines which headers (calculations) contain the words "mean" or "std". They are subsetting from the combined dataset, as well as the descriptor headers (subject, activiy number, and activity name). 

The final dataset containing only the calculations for mean and std is then summarized to produce a mean calculation for all of these values. This new, tidy dataset is exported to Summarized_Tidy_Table.txt.
