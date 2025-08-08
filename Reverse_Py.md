# 1. Using Two Pointers (Manual Swap) — Your Method
```
 arr = [1, 2, 3, 4, 5]
start = 0
end = len(arr) - 1

while start < end:
    arr[start], arr[end] = arr[end], arr[start]
    start += 1
    end -= 1

print("Reversed array:", arr)
```

# 2. Using Slicing (Python Shortcut)
```
 arr = [1, 2, 3, 4, 5]
reversed_arr = arr[::-1]
print("Reversed array:", reversed_arr)
```

# 3. Using reversed() Built-in Function
```
arr = [1, 2, 3, 4, 5]
reversed_arr = list(reversed(arr))
print("Reversed array:", reversed_arr)
```
# 4. Using reverse() Method (In-Place)
```
arr = [1, 2, 3, 4, 5]
arr.reverse()
print("Reversed array:", arr)
```
# 5. Using a For Loop (Appending from End)
```
arr = [1, 2, 3, 4, 5]
reversed_arr = []
for i in range(len(arr) - 1, -1, -1):
    reversed_arr.append(arr[i])

print("Reversed array:", reversed_arr)
```

# 6. Using Recursion
```
def reverse_recursive(arr):
    if len(arr) <= 1:
        return arr
    return [arr[-1]] + reverse_recursive(arr[:-1])

arr = [1, 2, 3, 4, 5]
print("Reversed array:", reverse_recursive(arr))
```

# 7. Using Stack (LIFO Principle)
```
arr = [1, 2, 3, 4, 5]
stack = []
for i in arr:
    stack.append(i)

reversed_arr = []
while stack:
    reversed_arr.append(stack.pop())

print("Reversed array:", reversed_arr)
```

# 8. Using NumPy (for numeric arrays)
```
import numpy as np
arr = np.array([1, 2, 3, 4, 5])
reversed_arr = arr[::-1]
print("Reversed array:", reversed_arr)
```
# 9.XOR Swap Method (Bitwise Trick — in-place)
```
def reverse_array_xor(arr):
    start, end = 0, len(arr) - 1
    while start < end:
        arr[start] ^= arr[end]
        arr[end] ^= arr[start]
        arr[start] ^= arr[end]
        start += 1
        end -= 1
    return arr

print(reverse_array_xor([1, 2, 3, 4, 5]))
```
# 10. Using deque from collections
```
from collections import deque

arr = [1, 2, 3, 4, 5]
dq = deque(arr)
dq.reverse()
reversed_arr = list(dq)
print("Reversed using deque:", reversed_arr)
```
# 11. Using List Comprehension
```
arr = [1, 2, 3, 4, 5]
reversed_arr = [arr[i] for i in range(len(arr)-1, -1, -1)]
print("Reversed using list comprehension:", reversed_arr)
```
# 12. Using functools.reduce()
```
from functools import reduce

arr = [1, 2, 3, 4, 5]
reversed_arr = reduce(lambda acc, x: [x] + acc, arr, [])
print("Reversed using reduce:", reversed_arr)
```
# 13.Using Generators
```
arr = [1, 2, 3, 4, 5]
reversed_gen = (arr[i] for i in range(len(arr)-1, -1, -1))
print("Reversed using generator:", list(reversed_gen))
```
# 14. Using zip() with reversed range
```
arr = [1, 2, 3, 4, 5]
reversed_arr = [x for _, x in zip(range(len(arr)), reversed(arr))]
print("Reversed using zip:", reversed_arr)
```
