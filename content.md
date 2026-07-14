# 1D Arrays

Assigning a new value to a single entry in a NumPy array is done in the same way as it is for lists:

```py-cell
import numpy as np

a = np.array([0, 0, 0, 0, 0])
a[2] = 5
print(a)
```

# Multi-Dimensional Arrays

We can assign values to entries in multi-dimensional arrays by specifying the index for each dimension, separated by commas:

```py-cell
import numpy as np

a = np.array([[0, 0, 0], [0, 0, 0]])
a[1, 2] = 5
print(a)
```