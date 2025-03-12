### Q 1
``` python
import numpy as np
array1= np.random.randint(10,51,20)
print(array1)
meanarray1= np.mean(array1)
stdarray1 =np.std(array1)
print("mean= ",meanarray1)
print("standard deviation = ", stdarray1)
```
### Q2
```python
array2 = np.random.rand(6,5)
print(array2)
c=array2.reshape(5,6)
print(c)
```
### Q3
``` python
array3= np.arange(1,26)
array3= array3.reshape(5,5)
print(array3)
print(array3[1:4,0:3])
```
### Q4
``` python
A= np.random.randint(1,101,10)
B= np.random.randint(1,101,10)
C= A+B
print(A)
print(B)
print(C)
print(2*C)
```

### Q5
``` python
arr4=np.random.randint(1,11,12).reshape(3,4)
print(arr4)
arr5=np.array([1,2,3,4])
print(arr5)
arr6=arr4+arr5
print(arr6)
```

### Q6
``` python
arr7=np.random.randint(1,101,9).reshape(3,3)

print(arr7)
print(np.argmax(np.sum(arr7, axis=1)))
print(np.max(arr7[np.argmax(np.sum(arr7, axis=1))]))
```

### Q7
``` python
arr8 =np.random.randint(1,101,4).reshape(2,2)
arr9 =np.random.randint(1,101,4).reshape(2,2)
print(arr8)
print(arr9)
print(np.dot(arr8,arr9))
```

### Q8
``` python
arr9 =np.random.randint(1,51,36).reshape(6,6)9[arr9>25])
```

### Q9
``` python
array10 = np.random.rand(5,5)
print(array10)
print("median along column ",np.median(array10, axis=0))
print("median along row ",np.median(array10, axis=1))
print("variance along row ",np.var(array10, axis=1))
print("variance along column",np.var(array10, axis=0))
```
### Q10
``` python
arr11= np.random.randint(1,11,9).reshape(3,3)
print(arr11)

print(np.reciprocal((arr11-2.1)**2))
```



