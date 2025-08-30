## 👾 ECE2112 - Numerical Python 🐍
Experiment 2: basic string, list, and function problems.


## Getting Started
1. Download `ECE2112.PA.2.NUMPY.ipynb`
2. Open the file on your **Jupyter Notebook**
3. Run cells

## Requirements 
- VSCode or Jupyter Notebook
- Python 3

## Code - Explains 
### 01 📊 Normalization Problem
 Generate a random 5×5 NumPy ndarray and normalize it using the formula:

The normalization formula (displayed):

$$
Z = \frac{X - \bar{x}}{\sigma}
$$

where:
- $X$ = original ndarray  
- $\bar{x}$ = mean of all elements in $X$  
- $\sigma$ = standard deviation of all elements in $X$ 

Finally, save the normalized ndarray as `X_normalized.npy`.
---

### **Steps Performed**
1. Import NumPy.  
2. Generate a random 5×5 ndarray using `np.random.random()`.  
3. Compute the **mean** and **standard deviation** of the ndarray.  
4. Apply the normalization formula: `(X - mean) / std`.  
5. Save the normalized data into **`X_normalized.npy`**.  
6. Display a success message and reload the saved file to confirm.  

---

### 02 ⨸ Division by 3 Problem
### **Problem Statement**
Create a 10×10 NumPy ndarray consisting of the squares of the first 100 positive integers.  
From this array, determine all the elements that are divisible by **3**.  
Finally, save the result as **`div_by_3.npy`**.

---

### **Steps Performed**
1. Import NumPy.  
2. Generate the first 100 positive integers using `np.arange(1, 101)`.  
3. Compute their squares with `**2`.  
4. Reshape the result into a 10×10 ndarray using `.reshape(10, 10)`.  
5. Use boolean indexing to extract all elements divisible by 3.  
6. Save the result into a file named **`div_by_3.npy`**.  
7. Display a success message and reload the saved file to confirm.  

---

### **Reference Code**
```python
# to access NumPy library
import numpy as np 

# generates a 10x10 ndarray with squares of the first 100 positive integers
squares = np.arange(1, 101)**2
squares_reshape = squares.reshape(10, 10) 

# display the 10x10 array
print("10x10 ndarray of squares of first 100 positive integers:")
print(squares_reshape) 

# find the elements in the ndarray that are divisible by 3
div_by_3 = squares_reshape[squares_reshape % 3 == 0] 

# store the elements that are divisible by 3 to a file named 'div_by_3.npy'
np.save('div_by_3.npy', div_by_3) 

# display a successful message
print("The elements that are divisible by 3 has been saved as ‘div_by_3.npy’.") 

# reload and display the elements
data = np.load('div_by_3.npy')
data

-----------------------------------------------------------------------------------------

  
💡 *Keep it simple. Run code. Explore. Learn.*  











