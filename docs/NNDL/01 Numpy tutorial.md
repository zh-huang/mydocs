# 01 Numpy tutorial

## Array operations

```py
# 1. Import numpy
import numpy as np

# 2. Create a one-dimensional array a initialized to [4,5,6], (1) print the type of a (2) print the shape of a (3) print the first element of a (value is 4)
a = np.array([4, 5, 6])
print(type(a), a.shape, a[0])

# 3. Create a two-dimensional array b, initialized to [[4, 5, 6], [1, 2, 3]] (1) print the shape of b (2) print the elements b(0,0), b(0,1), b(1,1) (values are 4, 5, 2)
b = np.array([[4, 5, 6], [1, 2, 3]])
print(b.shape, b[0][0], b[0][1], b[1][1])

# 4. (1) Create a matrix a filled with zeros, size 3x3, integer type (2) Create a matrix b filled with ones, size 4x5 (3) Create an identity matrix c, size 4x4 (4) Generate a random matrix d, size 3x2
a = np.zeros((3, 3), dtype=int)
b = np.ones((4, 5))
c = np.eye(4)
d = np.random.rand(3, 2)
print(a)
print(b)
print(c)
print(d)

# 5. Create an array a, (value is [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]]), (1) print a (2) print the values of elements at indices (2,3) and (0,0)
a = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
print(a)
print(a[2][3], a[0][0])

# 6. Assign the elements of rows 0 to 1 and columns 2 to 3 of array a to b, (1) print b (2) print the value of the element at (0,0) in b
b = a[0:2, 2:4]
print(b)
print(b[0][0])

# 7. Assign the last two rows of array a to c, (1) print c (2) print the last element of the first row in c
c = a[1:, :]
print(c)
print(c[0][-1])

# 8. Create array a, initialized to [[1, 2], [3, 4], [5, 6]], print the elements at indices (0,0), (1,1), (2,0)
a = np.array([[1, 2], [3, 4], [5, 6]])
print(a[[0, 1, 2], [0, 1, 0]])

# 9. Create matrix a, initialized to [[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]], print elements at indices (0,0), (1,2), (2,0), (3,1)
a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
b = np.array([0, 2, 0, 1])
print(a[np.arange(4), b])

# 10. Add 10 to each of the four elements obtained in the previous step and print matrix a
a[np.arange(4), b] += 10
print(a)
```

## Array mathematical operations

```py
# 11. Execute x = np.array([1, 2]), then print the data type of x
x = np.array([1, 2])
print(x.dtype)

# 12. Execute x = np.array([1.0, 2.0]), then print the data type of x
x = np.array([1.0, 2.0])
print(x.dtype)

# 13. Execute x = np.array([[1, 2], [3, 4]], dtype=np.float64), y = np.array([[5, 6], [7, 8]], dtype=np.float64), then print x+y, np.add(x,y)
x = np.array([[1, 2], [3, 4]], dtype=np.float64)
y = np.array([[5, 6], [7, 8]], dtype=np.float64)
print(x + y)
print(np.add(x, y))

# 14. Subtract y from x and print the result, both using "-" operator and np.subtract() function
print(x - y)
print(np.subtract(x, y))

# 15. Multiply x and y element-wise and print the result, also print the result of np.multiply(), and np.dot() for matrix multiplication
print(x * y)
print(np.multiply(x, y))
print(np.dot(x, y))

# 16. Divide x by y and print the result using np.divide()
print(np.divide(x, y))

# 17. Calculate the square root of x and print the result using np.sqrt()
print(np.sqrt(x))

# 18. Perform matrix multiplication of x and y using both x.dot(y) and np.dot(x,y), then print the results
print(x.dot(y))
print(np.dot(x, y))

# 19. Calculate the sum of elements in x along different axes and print the results
print(np.sum(x))
print(np.sum(x, axis=0))
print(np.sum(x, axis=1))

# 20. Calculate the mean of elements in x along different axes and print the results
print(np.mean(x))
print(np.mean(x, axis=0))
print(np.mean(x, axis=1))

# 21. Transpose matrix x and print the result
print(x.T)

# 22. Calculate the exponential of each element in x and print the result
print(np.exp(x))

# 23. Find the indices of the maximum values in x along different axes and print the results
print(np.argmax(x))
print(np.argmax(x, axis=0))
print(np.argmax(x, axis=1))

# 24. Plot y = x^2 where x = np.arange(0, 100, 0.1)
import matplotlib.pyplot as plt
x = np.arange(0, 100, 0.1)
y = x * x
plt.plot(x, y)
plt.show()

# 25. Plot sin(x) and cos(x) where x = np.arange(0, 3*np.pi, 0.1)
x = np.arange(0, 3 * np.pi, 0.1)
plt.plot(x, np.sin(x))
plt.show()
plt.plot(x, np.cos(x))
plt.show()
```
