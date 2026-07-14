# Python: Assigning to Items in an Array

You can modify values in a NumPy array by assigning to indexed positions or slices.

```py-cell
import numpy as np

a = np.arange(12).reshape([2, 2, 3])
print(a)

a[1, 1, 2] = 50
print(a)
```

The indexing rules used for assignment are the same ones used for selection. You decide which entries to update by choosing indices and slices for each dimension.

# Assignment with a Scalar

When the right-hand side is a single value, that value is assigned to every selected entry.

```py-cell
import numpy as np

a = np.arange(12).reshape([2, 2, 3])
a[1, 1, 2] = 50
a[0, :, 1:] = 40

print(a)
```

# Assignment with an Array

You can also assign values from another array, as long as the selected shape on the left matches the shape of the right-hand side.

```py-cell
import numpy as np

a = np.zeros([4, 2, 3])

a[0, :, :2] = np.arange(1, 5).reshape([2, 2])

print(a)
```

If the shapes do not match, NumPy raises an error:

```py-cell
import numpy as np

a = np.zeros([4, 2, 3])

a[1, :, :2] = np.arange(1, 5)
```