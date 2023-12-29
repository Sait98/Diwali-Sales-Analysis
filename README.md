# Diwali-Sales-Analysis
# import python libraries

import numpy as np 
import pandas as pd 
import matplotlib.pyplot as plt # visualizing data
%matplotlib inline
import seaborn as sns
# import csv file
df = pd.read_csv('Diwali Sales Data.csv', encoding= 'unicode_escape')
df.shape
(11251, 15)
df.head()
df.info()
#drop unrelated/blank columns
df.drop(['Status', 'unnamed1'], axis=1, inplace=True)
#check for null values
pd.isnull(df).sum()
# drop null values
df.dropna(inplace=True)
# change data type
df['Amount'] = df['Amount'].astype('int')
df['Amount'].dtypes
df.columns
#rename column
df.rename(columns= {'Marital_Status':'Shaadi'})
# describe() method returns description of the data in the DataFrame (i.e. count, mean, std, etc)
df.describe()
# use describe() for specific columns
df[['Age', 'Orders', 'Amount']].describe()

# describe() method returns description of the data in the DataFrame (i.e. count, mean, std, etc)
df.describe()

