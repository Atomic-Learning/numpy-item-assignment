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

# Data Types

When assigning to items in a NumPy array, the new value is converted to the data type of the array if possible:

```py-cell
import numpy as np

a = np.array(["a", "b", "c"])
# The int 5 wil be converted to a string "5" when assigned to the array
a[1] = 5
print(a)
```

If the new value cannot be converted to the data type of the array, an error will occur:

```py-cell
import numpy as np
a = np.array([1, 2, 3])

# The string "a" cannot be converted to an int, so this will raise an error
a[1] = "a"
print(a)
```