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
df.head() is showing the top rows of the data. 
date= df ['Quarter Begin Date'].max() is find the max date of this column.
df['difference']= (df ['Quarter Begin Date'].max()-df ['Quarter Begin Date']).dt.days is subtracting the max date to every date of the data.
df['daytomonth']=(df['difference']/30) is coverting the days to months.
df.to_csv('df_clean.csv', index=False) is saving the data to csv file.

#HW3
I was using the baseballdatabank-master/Salaries provided by Dr.AbdelRahman for HW3
df.head() is showing the top rows of the data. 
df['salary2']= (df ['salary']/100000) is creating a new column to make the number size smaller
hist, ax = plt.subplots() is using the distplot function from seaborn to create our plot. 
den, ax = plt.subplots() is creating a density plot for the data. 
hist_den_rug, ax = plt.subplots() is creating a rug plot for the data.
count, ax = plt.subplots() is creating a count plot for the data.

#HW4
I was using the baseballdatabank-master/AwardsManagers and AwardsShareManagers provided by Dr.AbdelRahman for HW4
print(data1) and print(data2) are showing the values in two seperate data source.
data12= data1.merge(data2, left_on='awardID', right_on='awardID') is merging the two data pieces.
print(np.count_nonzero(data12.isnull()))is counting the missing values in the merged data sets.
print(data12.fillna(0).iloc[0:29325, 0:12]) is replacing all missing values to 0.
new = data12.drop(labels=["tie","notes"],axis=1) is dropping columns ("tie" and "notes") since these two columns are full with "NaN".

#HW5
I was using the baseballdatabank-master provided by Dr.AbdelRahman for HW5.
df['lgID'] = df['lgID'].astype('category') is coverting a column of non-categorical type into a categorical type.
df['gameID_str'] = df['gameID'].astype('str') is converting gameID column into a string type.

#HW6
I was using the baseballdatabank-master provided by Dr.AbdelRahman for HW6.
import re

year='0000'

m = re.match(pattern='\d\d\d\d', string=year)

if m:

    print('match')

else:

    print('no match')
is cleaning a column on my data set using regular expression methods.
def sum(vec), def mean(vec), def get_first_mode(a),def median(lst, def range(lst) are creating a function that returns the mean, sum, mode, median, and range (separately).
sum1 = df.apply(sum) etc are running the function into your chosen data set using the .apply() method.

