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
- We will define a funcion
```
def complex_letter(state):
  if state[0] == "W":
    return "Washington"
  else:
    return "Error"
```
- def_one['col2'].apply(complex_letter) # this demands string input; if integer input, error
- another way to create a column is mapping
- def_one['k1']
- my_map = {'A':1,'B':2,'C':3}
- def_one['k1'].map(my_map)
- we can add to the df by
- df_one['num'] = def_one['k1'].map(my_map)
- to get the max no in a column -> df_one['col1'].max()
- df_one['col1'].idxmax() #this returns the location of the max
- to grab all the columns -> df_one.columns
- df_one.column = ['c1','c2','c3','c4','c5','c6'] # this reassign the columns
- for sorting
- df_one.sort_values('c3') # c3 is alphabetical
- typical data structure ->
-  features = pd.DataFrame({'A':[100,200,300,400, 500],
-                           'B'[12,13,14,15,16]}
-   predictions = pd.Dataframe({'pred':[0,1,1,0,1]})
-   to join those two dataframe:
-   pd.concat([features,preductions, axis=1)
-   to create dummy variable
-   df_one['c1']
-   pd.get_dummies(df_one['C1']) # returns as many columns as categoriy and
- it returns 1 if category mataches up




