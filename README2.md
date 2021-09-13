Panda Crush course
# 2.Panda Series

- import numpy as np
- import panda as pd
- lablels = ['a','b','c']
- mylist = [10,20,30]
- arr = np.array ([10,20,30])
- d = {'a':10,'b':20,'c':30}
- pd.Series (two tab will shows the suffixes, we will use data)
- pd.Series(data=mylist)
- But here we can have labeled index
- pd.Series(data=mylist, index=label)
- to call it again we can just use
- pd.Series(mylist,labels)
- the same can be done to arry
- pd.Series(arr.labels)
- dictionary can be transformed to series by
- pd.Series(d)
- Key factors about panda series is label index
- We can mae a quick series for data
- salesQ1 = pd.Series(data=[250,450,200,150],index=['USA','China','India','Brazil'])
- salesQ2 = pd.Series(data=[260,500,220,100],index=['USA','China','India','Japan'])
- Calling the data as follow
- salesQ2['China']
- indexed fetching still work
- salesQ2[0] the same as salesQ2['USA']
- out of index or typo will return KeyError
- can perform operation between series
- salesQ1 + salesQ2 -> Brazil and Japan will return NaN
- match မဖြစ်တဲ့ series ကိုလဲ ပေါင်းနိုင်တယ်
# 3.DataFrame

-import numpy as np
- import panda as pd
- columns = ['W','X','Y','Z']
- index = ['A','B','C','D','E']
- from numpy.random import randint
- data = randint (-100,100,(5,4))
- np.randam.seed(42) - to get the same nos
- df = pd.DataFrame (two tabs)
- df = pd.DataFram(data,index,columns)
- to grab a single column
- df['W']
- returns panda series - can check with ->type (df['W'])
- 
- 
