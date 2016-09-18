# GettingAndCleaningData

This readme contains a description of the functions within run_analysis.R

The script uses the plyr library.

the grab.data function:
a) checks to see if there is a data directory in the working directory, and creates one if there is not;
b) if there is no file named 'Dataset', if downloads one from the url supplied in the script, saving it as Dataset.zip
c) the zip file is unzipped

The merge.dataset function:
a) reads the x and y test and train datasets into separate variables
b) reads in the test and train subject tables
c) merges the x files together, the y files together, and the subject files together, creating three merged datasets
d) returns a list of three datasets: x, y and subject
The user is kept informed of the current stage of the process throughout performance

The extract.meanstd function:
a) accepts a dataframe as a parameter
b) extracts the mean of each measurement and enters them into a column of data
c) extracts the standard deviation of each measurement and enters them into a column of data
d) creates a new dataframe with those columns

The name.activities function:
a) accepts a dataframe as a parameter
b) sets readable and descriptive activity names to the dataframe

The bind.data function:
a) accepts a list of three datasets as parameters
b) combines the x, y and subjects datasets into one dataframe

The create.tidy function:
a) accepts a single dataframe as a parameter 
b) creates a new dataframe with the average of each variable for each avtivity and subject

The clean.data function:
a) is the function that should be called to run the script
b) doanloads the data
c) merges the existing texts files
d) extracts the means and standard deviations
e) renames the activities appropriately
f) produces one data frame
g) outputs a tidy dataset as a .csv file

Usage:
source("run_analysis.R")
clean.data()
