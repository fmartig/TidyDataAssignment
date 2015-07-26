###Tidy data assignment for the "Getting and Cleaning data" course on Coursera
***
The aim of this project was to collect data from [this study](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) and prepare a tidy data set. The R script "run_analyis.R" in this repository allows you to perform all the steps, from downloading the data in your working directory to creating a tidy data set and writing it into a txt file. The Code Book "il faudra qu'il ait un nom" describes the variables and their units. 
The downloaded files contain additional information on the experimental set up, the method used and the original variables.    

***
> Information about the original data set  

Once downloaded and extracted (cf: using the R script, first step), some of the txt files provide information on the experimental set up and the different treatments applied to the data: "README.txt" and "features_info.txt". The information contained in these files are not added to this README.  

> Using the R script

* Preliminaries:
Set the working directory with setwd(), load the R packages "plyr" and "dplyr". 
  
* First step:  
Download the compressed files into the working directory and extract the files.

* Second step:  
Make a complete data set with the training data by joining the data from the file "./train/X\_train.txt" (the actual measurements) with the "subject id" variable contained in the file "./train/subject\_train.txt" (which indicates the id number of the subject for each observation) and the "activity" variable fom the file "./train/y\_train.txt". The variable names in the "X\_train.txt" file (the "features") are simplified: the 561 variables correspond to the 561 names given in the "./features.txt" file (eg *tBodyAcc-mean()-X* is the original variable name for the first column in the "X_train.txt" file).   
NB: the "tbl_df()" function from the dplyr package is used to load the data into data frame tbls to make their printing and viewing easier. 
  
  The test data is provided under the same format, and is treated with the same procedure.  
  
  These two complete data sets are then joined "vertically", to obtain a wide data set with 10,299 observations of 563 variables.  
  
* Third step:   
"Extract only the measurements on the mean and standard deviation for each measurement". 
The original data contain several types of variables which could match. The following choices were made based on the information provided in the "features_info.txt" file. 
  + The suffixe "std()" added to the variable name (ex: *tBodyAcc-std()-X*) indicates that the corresponding variable is the standard deviation of a measurement. Thus, the key word "std" is used with the grepl() function to extract the subset of desired columns. 
  + The suffixe "mean()" (ex: *tGravityAcc-mean()-X*) has a similar meaning and was used to identify and extract the columns corresponding to the means of each measurements. The mean frequencies (*meanFreq*) and the various means used on the angle measurements (ex: *angle(tBodyAccMean,gravity)*) are excluded from the data set: the key word "Freq" is used with grepl() to exclude the mean frequencies from the subset. See below the "Selection of the "mean" variables" paragraph for the explanation of this choice.   
  
  NB: the variable names are detailed in the adjacent code book.  

* Fourth step:  
Change the activity IDs by replacing the numbers by the corresponding labels. The equivalence between an activity number (from 1 to 6) to the actual activities recorded (laying, walking...) are found in the "./activity\_labels.txt" file. As a result, the activities are properly labelled in the data set created in the step 3 by merging that data frame with the data frame obtained from the "./activity\_labels.txt" file.  
  
  NB: additional editing is performed to change the second variable name to "activity" and to remove the column with the activity numbers from the data frame (these function calls are strung together with the "chaining" method.  
  
* Fifth step:  
"Appropriately label the data set with descriptive variable names". The choice was made to simply change all the names to lower case, remove the parentheses and change the "-" signs into ".". It was also observed that some variable names contained the pattern "BodyBody", which appeared to be a typo as it doesn't match the naming pattern explained in the "features\_info.txt" and is thus changed into "body". However, the variable names are not further modified since the Code Book is available for additional clarification.   
  
* Sixth step:    
Use the data frame obtained at the end of Step 5 to create an independent, tidy data frame containing the mean of each variable for each activity and each subject. The chaining method is again used for these two operations; functions from the dplyr package are used. First, the group\_by() function is called to break up the data set into groups of rows based on the values of the "activity" and "subject" variables. This allows the use of the summarise\_each() and mean() functions on the grouped data to obtained the desired output: a tidy data set in a wide form with 180 observations (6 activities* 30 subjects) and 68 variables: it has one variable per column and one observation per row.  

  
* Seventh step:  
Create a txt file containing the data set obtained in step 6. This file is called "finaldataset.txt" and is saved in the directory where the original dataset was downloaded.   
  
  
> Read the txt file created with the script  

If you need to open the final data set in R, the command is the following:
```{r}
final_output <- read.table("finaldataset.txt", header = TRUE)
View(final_output)
```

> Selection of the "mean" variables    

The instructions were to "extract only the measurements on the mean [...] for each measurement". As the word "mean" appears in the variable names with three different patterns (*mean()*, *meanFreq()* and *angle...Mean*) and only one was used to select columns, it was deemed necessary to justify that choice.  
  
In the "features\_info.txt" file, the *meanFreq()* variables are described as the "weighted average of the frequency components[...]", and only apply to the measurements that have undergone a Fast Fourier Transform FFT (variables with the preffix *f*). These variables are related to the FFT and not to the original measurements and it was thus decided to exclude them from the final data set.   
  
The *angle...Mean* naming pattern describes "additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable" (features\_info.txt). As they are features of angle(), it was decided that they do not match the project requirements.  
