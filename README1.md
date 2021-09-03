<H5>Setting up the workspace </H5>

- To check tensorflow version -> 
```
import tensorflow as tf
to install new tools use -> !pip install
tf.__version__
```
- Go to "Edit"->"Notebood Setting"-> "Hardware Accelerator - GPU"
- 
<H5>Nympy</H5>

- import nympy as np
- arr = np.arrange (0,11)
- Try below commands
- arr
- arr[8]
- array[1:5]
- array[:5]
- array[5:]
- <H6>Broadcasting</H6>
- arr[0:5]=100 #cannot do this in python list
- arr=np.arrange(0,11)
- slice_of_arr=arr[0:5]
- slice_of_arr[:]
<H6>Array Copy</H6>
arr_copy = arr.copy()
<H6> </H6>

- arr_2d=np.array([5,10,15],[20,25,30],[35,40,45]])
- arr_2d.shape -> returns no of rows and colums
- arr_2d[0] -> returns 1st row
- arr_2d[1,1] ->row1 colum1
- arr_2d[:2,1:] -> grap a subsection
<H6>Conditional Selection</H6>

- arr =np.arange(1,11)
- arr>4 -> returns bolean array
- bool_arr = arr>4
- arr[bool_arr] -> returns the index of true values
We will quite often see
- arr[arr>4]
<H6>4. Nympy Operations</H6>

- Go to google colab -> https://colab.research.google.com/
- open your file already created
- import numpy as np
- arr = np.arrange(0,10)
- arr+5 will # give element by element basic
- arr + arr # will add element by element; array size must be the same
- arr/arr # will return nan (not a number) in the first element
- 1/arr #will return inf in the first element
- can run the following commands
- np.sqrt(arr) # square root
- np.sin(arr) # sine
- np.log (arr)# the first element will return -inf
- arr.sum() #sum all the elements
- arr.mean(0 # for average
- arr.max(0
- arr.var()
- arr.std() #standard deviation
- arr2d= np.arrange(0,25).reshape(5,5)
- arr2d.shape # returns the shape of the array
- arr2d.sum() #sum up all the elements
- arr2d.sum(axis=0) #perform across the rows (called operation across)
- arr2d.sum(axis=1) #perform across the colums
- 
