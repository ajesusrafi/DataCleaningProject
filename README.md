# DataCleaningProject
Coursera Data Cleaning Project
The following R code performs several tasks to prepare raw accelerometer data for analysis and transform it into a tidy format. It checks the existence of the data directory and downloads the dataset zip file from a specified URL and unzips it if it's not present. The dataset contains accelerometer data collected from Samsung Galaxy S smartphones, and it reads various data files into R data frames. These files include training and test subject data, accelerometer measurement data, activity labels, and feature names.

Next, the code merges the training and test datasets into a single dataset named "humanActivity" by binding rows for subject, accelerometer measurements, and activity labels. It also sets appropriate column names for the merged dataset using the features file for feature names. It then extracts only the columns related to the subject, activity, mean, and standard deviation measurements from the dataset.

The code also transforms the activity identifiers in the dataset to descriptive activity names by matching them with the activity labels read from the activity labels file. It ensures that the column names are descriptive and appropriate for further analysis by sanitizing them with the make.names function.

The final step is to create a tidy dataset named "humanActivityMeans" by calculating the mean of each variable for each combination of subject and activity, using the dplyr package's summarise and across functions. The resulting tidy dataset is then written to a file named "tidy_data.txt" in the working directory using write.table.

Overall, this code demonstrates best practices in data cleaning, transformation, and summarization in R, utilizing popular packages such as dplyr for data manipulation.

This R code conducts the following steps: 
Data Downloading and Preparation:

    It checks whether the data directory exists. If not, it downloads the dataset zip file from a specified URL and unzips it. The dataset contains accelerometer data collected from Samsung Galaxy S smartphones.
    It reads various data files into R data frames. These files include training and test subject data, accelerometer measurement data, activity labels, and feature names.

Data Merging:

    It merges the training and test datasets into a single dataset (humanActivity) by binding rows for subject, accelerometer measurements, and activity labels.

Data Cleaning:

    It sets appropriate column names for the merged dataset, using the features file for feature names.
    It extracts only the columns related to the subject, activity, mean, and standard deviation measurements from the dataset.

Data Transformation:

    It converts the activity identifiers in the dataset to descriptive activity names by matching them with the activity labels read from the activity labels file.

Data Labeling:

    It ensures that the column names are descriptive and suitable for further analysis by sanitizing them with the make.names function.

Tidy Data Creation:

    It calculates the mean of each variable for each combination of subject and activity, resulting in a tidy dataset (humanActivityMeans) using the dplyr package's summarise and across functions.

Data Output:

    It writes the resulting tidy dataset to a file named "tidy_data.txt" in the working directory using write.table
