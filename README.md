# Data612
#HW 1
I was using the stock data for homework 1. 
df.head(100) is showing the top 100 rows of the data.
df.tail(100) is showing the last 100 rows of the data.
df.columns is showing all of the column names of the data.
df.dtypes is showing the data type of the data set.
df.shape is showing the number of rows and columns of the data set (67905 rows and 19 columns).
df.groupby(['date','company_name'])['average volume'].mean() is showing the mean of the average volume grouped by the data and company name.

#HW2
I was using the State_Drug_Utilization_Data_2010 provided by Dr.AbdelRahman for HW2.
df.head() is showing tht top rows of the data. 
date= df ['Quarter Begin Date'].max() is find the max date of this column.
df['difference']= (df ['Quarter Begin Date'].max()-df ['Quarter Begin Date']).dt.days is subtracting the max date to every date of the data.
df['daytomonth']=(df['difference']/30) is coverting the days to months.
df.to_csv('df_clean.csv', index=False) is saving the data to csv file.
