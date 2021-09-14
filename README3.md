# 5.Panda Missing Data
- import numpy as np
- import pandas as pd
- df=pd.DatatFrame({'A':[1,2,np.nan,4], 'B':[5,np.nan,np.nan,8], 'C':[10,20,30,40]})
- the main method uses is - df.dropna() # you can press tab twice to see the documentation
- df.dropna() # will return a row that have valid datas
- 
