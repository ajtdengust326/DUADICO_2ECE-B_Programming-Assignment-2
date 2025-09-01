# **PROGRAMMING ASSIGNMENT #2**
___
## NORMALIZATION PROBLEM
> 1. Called the Numpy Library using `import numpy as np`
> 2. Then, created a 5x5 ndarray by using the `np.random.random((x, y))`
> 3. printed the original X for reference `print(X)`
> 4. I used the `.mean()` and `.std()` calls to compute for the mean and standard deviation
> 5. normalized X by using the formula $\frac{X - mean} {std}$, and also denoted normalized X as "*X_normalized*"
> 6. Saved the normalized X by using `np.save()` and as *X_normalize.npy*
> 7. Print the results
```phyton
import numpy as np           #1   
X = np.random.random((5, 5)) #2   
print (X)                    #3  
```
[[0.67817891 0.31366154 0.57525651 0.32282168 0.61647751]  
 [0.11830064 0.79067885 0.12921478 0.8038815  0.12959708]  
 [0.82880854 0.72024453 0.69075244 0.54014456 0.05485816]  
 [0.67512722 0.83486212 0.51502975 0.56962667 0.81783996]  
 [0.20374884 0.10838722 0.60813684 0.28702085 0.87157116]]
```phyton
mean = X.mean()                              #4
std = X.std()
X_normalized = (X - mean) / std              #5

np.save("X_normalized.npy", X_normalized)    #6

print("Original X:\n", X)                    #7
print("\nNormalized X:\n", X_normalized)#3  
``` 
Original X:  
[[0.67817891 0.31366154 0.57525651 0.32282168 0.61647751]  
 [0.11830064 0.79067885 0.12921478 0.8038815  0.12959708]  
 [0.82880854 0.72024453 0.69075244 0.54014456 0.05485816]  
 [0.67512722 0.83486212 0.51502975 0.56962667 0.81783996]  
 [0.20374884 0.10838722 0.60813684 0.28702085 0.87157116]]
  
Normalized X:  
[[ 0.62066485 -0.74216509  0.23586639 -0.70791786  0.38998034]  
 [-1.47256563  1.04127111 -1.4317607   1.09063219 -1.43033138]  
 [ 1.18382751  0.77793662  0.66767383  0.10459247 -1.7097596 ]  
 [ 0.60925544  1.2064602   0.01069512  0.21481795  1.14281901]  
 [-1.15309837 -1.50962917  0.35879689 -0.84176728  1.34370516]]  

___
## **DIVISIBLE BY 3 PROBLEM**
> 1. Called the Numpy Library using `import numpy as np`
> 2. Created an array of squares of the first 100 positive integers represented by (A) `A = np.arange(1, 101)**2`
> 3. Reshaped the array into a 10 by 10 ndarray `A = A.reshape(10, 10)`
> 4. printed ndarray (A) to see if it's working `print(A)`
> 5. To determine if all the numbers are divisible by 3, the formula is made by using this code `div_by_3 = A[A % 3 == 0]`
> 6. Saved the div_by_3 by using `np.save()` and as *div_by_3.npy*
> 7. Print to check the output
```phyton
import numpy as np           #1
A = np.arange(1, 101)**2     #2

A = A.reshape(10, 10)        #3
print(A)                     #4
```
[[    1     4     9    16    25    36    49    64    81   100]  
 [  121   144   169   196   225   256   289   324   361   400]  
 [  441   484   529   576   625   676   729   784   841   900]  
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]  
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]  
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]  
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]  
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]  
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]  
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]
 
```phyton
div_by_3 = A[A % 3 == 0]                          #5

np.save("div_by_3.npy", div_by_3)                 #6

print("Elements divisible by 3:\n", div_by_3)     #7
```
Elements divisible by 3:  
 [   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
 2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
 7569 8100 8649 9216 9801]
