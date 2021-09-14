# Data Visualization
 <H3> matplotlib </H3>
 
 - import numpy as np
 - import panda as pd
 - import matplotlib.pyplot as plt
 - plotting x and y axis
 - x=[0,1,2]
 - y=[100,200,300]
 - plt.plot(x,y)
 - plt.show() #no longer shows output of the line
 - copy and paste data frame
 ```
  housing = pd.DataFrame({'rooms':[1,1,2,2,2,3,3,3],
                          'price':[100,120,190,200,230,310,330,305]})
  plt.scatter(housing['room'],housing['price'])
  ```
  - How to add label and title
  - plot.plot(x,y)
  - plt.title('Title')
  - plt.xlabel('X Label')
  - plt.ylabel('Y Label');
  - Axis Limits
  - plot.plot(x,y)
  - plt.xlim(0,2)
  - plt.ylim(0,300)
  - To add color
  - plt.plt(x,y, color='red', marker='o', markersize=15, linestyle='--') # or can add Hex color code

<H3> seaborn library </H3>

- import numpy as np
- import panda as pd
- we wil use medical data set
- 
- df = pd.read_csv('../DATA/heart.csv')
- import seaborn as sns
- how to cal histogram
- sns.distplot(df['age'], kde=False, bins=2, color='red') # kde=False for turning off kde line; bins ကဘယ်နှပိုင်းပိုင်းမလဲ ဆိုတာ
- to resize the image , before sns.distplot...
- plt.figure(figsize=(12,8))
- now we will see the countplot
- df.head() # to see the heads
- sns.countplot(x='sex', data=df)
- sns.countplot(x='cp', data=df, hue='sex',pallete='terrian') # that categorize by male/femal
<H3>box plot</H3>

- sns.boxplot(x='sex',y='age',data=df) # sex should be categorical and age should be countinuous
- sns.boxplot(x='target', y='thalach', data=df,hue='sex')
<H3>Scattered plot</H3>

- sns.scatterplot(x='chol', y= 'trestbps', data=df, hue='sex', pallete='Dark2', size= 'age')
<H3> Paired plot</H3>

- iris = pd.read_csv('../data/iris.csv')
- sns.pairplog(iris, hue='species')
- 
- 
