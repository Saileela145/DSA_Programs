# 1. Basic For Loop (Classic Linear Search)
```
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1
```
# Example
data = [4, 2, 7, 1, 9]

print(linear_search(data, 7))  # Output: 2

# 2. While Loop Version
```
def linear_search(arr, target):
    i = 0
    while i < len(arr):
        if arr[i] == target:
            return i
        i += 1
    return -1
```
# Example

print(linear_search([4, 2, 7, 1, 9], 1))  # Output: 3
# 3. Using in and index()
```
def linear_search(arr, target):
    if target in arr:
        return arr.index(target)
    return -1
```
# Example

print(linear_search([4, 2, 7, 1, 9], 9))  # Output: 4

# 4. Using Enumerate
```
def linear_search(arr, target):
    for index, value in enumerate(arr):
        if value == target:
            return index
    return -1

# Example
print(linear_search([4, 2, 7, 1, 9], 2))  # Output: 1
```
# 5. Recursive Linear Search
```
def linear_search(arr, target, index=0):
    if index >= len(arr):
        return -1
    if arr[index] == target:
        return index
    return linear_search(arr, target, index + 1)
```
# Example

print(linear_search([4, 2, 7, 1, 9], 4))  # Output: 0

# 6. Using List Comprehension

def linear_search(arr, target):
    indices = [i for i, v in enumerate(arr) if v == target]
    return indices[0] if indices else -1

# Example
print(linear_search([4, 2, 7, 1, 9], 7))  # Output: 2

# 7. Sentinel Method

def linear_search(arr, target):
    arr.append(target)
    i = 0
    while arr[i] != target:
        i += 1
    arr.pop()  # Remove the sentinel
    return i if i < len(arr) else -1

# Example
print(linear_search([4, 2, 7, 1, 9], 1))  # Output: 3





