This analysis file will do the following:

1. Check for a specific directory "UCIdata" to see if the script has already been run. 
    It functions within the current working directory set
2. If no directory is found it creates one and downloads the required zip file.
3. Unzips the file into the UCIdata directory
4. Reads in all the required data as tables and merges them into one dataframe along with subjects and activities
5. Changes column names for readability and also converts them all to lower case
6. Subsets the data to only the columns that include the following text "mean", "std", "subject", "activity"
7. Replaces the activity numbers with the labels
8. Counts the columns without the subject and activity column and stores this number
9. Using number from step 8 it then aggregates the data removing the last two columns which are subject and activity. 
  The aggregation is an average by subject and activity
10. Writes this aggregates out to a table if required and also returns it as an object
