# **PROGRAMMING ASSIGNMENT #2**
___
## NORMALIZATION PROBLEM
> 1. Called the Numpy Library using `import numpy as np`
> 2. Then, created a 5x5 ndarray by using the `np.random.random((x, y))`
> 3. printed the original X for reference `print(X)`
> 4. I used the `.mean()` and `.std()` calls to compute for the mean and standard deviation
> 5. normalized x by using the formula $\frac{X - mean} {std}$
> 6. Saved the normalized X by using `np.save()` and as *X_normalize.npy*
> 7. Print the results
```phyton
import numpy as np              
X = np.random.random((5, 5))    
print (X)                       
```

