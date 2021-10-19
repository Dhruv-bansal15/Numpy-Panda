# Include Numpy library 
1. import numpy as np

# Creating an array 
=> 1D Array
1. arr = np.array([1,2,3])
2. print(arr) => To print it out on console 

=> 2D Array
3. arr = np.array([[1.1,2.3,3.3],[4.2,5.5,6.6]])
4. print(arr) => To print this 2D array 

# Basic functions for arrays 
1. arr.ndim => Returns wheather the array arr is 1 dimensional, or two or anything else 

2. arr.shape => Basically tells how many rows and columns are there in (x,y) format 
 => Eg: arr = np.array([[1.1,2.3,3.3],[4.2,5.5,6.6]]) 
 => arr.shape returns (2.3)

3. arr.dtype => returns the data type of values stored in array 
=> By default for integers, it is 'int32' usually , but we can change it, here is how :- 
=> arr = np.array([1,2,3], dtype= 'int16')
=> Now the integer will be stored in 16 bits or 4 bytes 

4. arr.itemsize => returns how many bytes a particular entity in list take to store in the memory 
=> In above example , arr.itemsize = 4

5. arr.size => returns how many elements are present in the array 

6. arr.nbytes => total bytes array need to get stored in the memory 

7. arr[1,2] => to access a particular element , remember here the indexing is also zero based 

# Slicing in array 
a) arr[0,:] => returns all elements of first row , lly 
b) arr[:,2] 
c) arr[0, 1:6:-2] => for first row, coln index from 1 to 5 alternativey (Ek chod ke)

# Manipulation of data 

=> arr = np.array([[1.1,2.3,3.3],[4.2,5.5,6.6]]) 
1. arr[1,5] = 20 => to change value at a particular place in array 
2. arr[:,2] = [1,2] => to change the entire column with index 2

# Initialize an array of size with a particular value 

1. np.zeros(5) => 1 D array of size 5 having all zeroes 
2. np.zeros(2,3) => 2 D array of size 2,3 with all zeroes 

3. np.ones(5) => 1 D array of size 5 having all one 
4. np.ones((2,3), dtype='int32') => 2 D array of size 2,3 with all one 

5. np.full(5,99) => 1 D array of size 5 having all 99 
6. np.full((2,3),99.2, dtype='float32') => 2 D array of size 2,3 with all 99.2

7. np.full_like(a.shape,4) => have the same shape as of a, with all values equal to 4

8. np.random.rand((4,2)) => to create an array with all random decimal values 

9. np.random.random_sample(a.shape) => to create an array with all random decimal values having same shape as of a 







