# 5.Panda Missing Data
- import numpy as np
- import pandas as pd
- df=pd.DatatFrame({'A':[1,2,np.nan,4], 'B':[5,np.nan,np.nan,8], 'C':[10,20,30,40]})
- the main method uses is - df.dropna() # you can press tab twice to see the documentation
- df.dropna() # will return a row that have valid datas
- df.dropna(axis=1) # will return a colum that thave valid datas
- df.dropna(axis=1, thresh=2) # with at least two non-null values
- Fill the missing data
- df.fillna() # tab twice to see available parameters
- df.fillna(value='FILL VALUE') #Nan is replaced with 'FILL VALUE'
- if the fill value is string the whole column is converted to string
- if float, the same too
- just to choose column
- df['A'].fillna(value=0) #then we can do some sort of reassignment
- df['A'] = df['A'].fill(value=0) # now permanently change the data frame
- to fill the missing value in B with the average value in B
- df['B'].fillna(value= df['B'].mean())
- to do it to the entire df
- df.fillna(df.mean())
# 6.Groupby Operaton

- similar to split, apply, combine
- the operation chosen with groupby() call must be an aggregation method
- aggregation method -> take in many -> return one result
- import panda as pd
- locate the CSV file
- inside 1-Panda-Crash-Course, create a new notebook
- notebook and Universities.csv must be in the same folder
- then should be able to run the following command
- df = pd.read_csv('Universities.csv') # should be able to call the file with tab or not ok
- df = pd.read_csv('Universities.csv')
- df.head()
- df.groupby('Year') # this will return a groupby object
- df.groupby('Year').mean() # and this returns a dataframe
- can see the available functions in the panda notebook
- can change asending or desending order by
- df.groupby('Year').sum().sort_index(asending=False)
- can groupby multiple columns also
- to group by the year and then goupby the sectors
- df.groupby(['Year','Sector']).sum()
- df.groupby('Year').describe() # displays all count mean std min etc
- df.groupby('Year').describe().transpose()
- describ() function is useful to get statistics
# 7.Panda useful operations

- import panda as pd
- df_one= pd.DataFrame({'k1':['A','A','B','B','C','C'],
                        'col1':[100,200,300,300, 400,500],
                        'col2':['NY','CA','WA','WA','AK','NV']})
- how to get value on uniq values
- def_one['col2'].unique()
- def_one['k1'].nunique() # returns the no of uniques no
- def_one['col2'].value_counts() # returns the no of uniques values
- to drop a duplicate
- df_one.drop_duplicates() # this dropped the duplicate row
- to create new columns with operations and functions
- df_one['NEW'] = df_one['col1']*10 # will add new column
- for more functionality, we can use
- def grab_first_letter(state):
    return state[0]
- df_one['first letter']=df_one['col2'].apply(grab_first_letter)
- let me show slightly more complex function
- 5:21



