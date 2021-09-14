# 8.Data Input and Output
- import numpy as np
- import panda as pd
- df = pd.read_csv('example.csv')
- to see the current path of your notebook -> pwd #print working directory
- ls # to list the files
- to convert dataframe to csv
- df.to_csv('output.csv',index =False) # index=False will not save index nos
- df.to_csv('output.csv',index =True)
- pd.read_csv('output.csv') # will returns index no with new indices
- How to read html table
- tables = pd.read_html('...')
- if not found error, need to install them -> 
```
 conda install lxml
 conda install html5lib
 conda install beautifulsoup4
 ```
 - type(tables) # will return a list
 - 
