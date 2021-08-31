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
