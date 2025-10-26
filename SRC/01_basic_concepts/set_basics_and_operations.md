<h1><sub><img src="https://github.com/RadhikaDeshpande1010/icon-library/blob/main/python-icon/python-icon.png" alt="Icon" height="27" width="27"></sub> Mastering Python Collections — Lists, Sets, and Strings </h1>

<h2>Set Operations and Theory</h2>

This notebook provides a hands-on introduction to **Python sets** and their commonly used methods. It is designed for beginners to build a strong foundation in handling lists through step-by-step examples and exercises.

> **Python version:** 3.8+

---

### How to Run

1. **Clone** this repository and open the folder in your editor/terminal.
2. Start Jupyter Notebook:

   ```bash
    jupyter notebook
   ```

> Tip: You can also copy any solution function into your notebook/REPL to experiment quickly.

---
### Q1. Create a list and print it.

**Input:**
```python
ls = [10,20,30,10,10,40,30,20,40,50]
```

**Output:**
`[10, 20, 30, 10, 10, 40, 30, 20, 40, 50]`

```python
# print_list.py

ls = [10,20,30,10,10,40,30,20,40,50]
print(ls)

Output:
[10, 20, 30, 10, 10, 40, 30, 20, 40, 50]
```

---

### Q2. Create a set and print unique elements.

**Input:**
```python
set1 = {10,20,30,10,10,40,30,20,40,50}
```

**Output:**
`{50, 20, 40, 10, 30}`

```python
# unique_set.py

set1 = {10,20,30,10,10,40,30,20,40,50}
print(set1)

Output:
{50, 20, 40, 10, 30}
```

---

### Q3. Add elements to a set.

**Input:**
```python
set2 = set()
add(10, 20, 30, 40, 50, 10)
```

**Output:**
`{40, 10, 50, 20, 30}`

```python
# add_elements_to_set.py

set2 = set()
set2.add(10)
set2.add(20)
set2.add(30)
set2.add(40)
set2.add(50)
set2.add(10)
print(set2)

Output:
{40, 10, 50, 20, 30}
```

---

### Q4. Remove an element from a set.

**Input:**
```python
set2 = {40, 10, 50, 20, 30}
remove(10)
```

**Output:**
`{40, 50, 20, 30}`

```python
# remove_element_from_set.py

set2 = {40, 10, 50, 20, 30}
set2.remove(10)
print(set2)

Output:
{40, 50, 20, 30}
```

---

### Q5. Find the union of two sets.

**Input:**
```python
set1 = {10,20,30,40}
set2 = {10,20,30,50}
```

**Output:**
`{40, 10, 50, 20, 30}`

```python
# union_of_sets.py

set1 = {10,20,30,40}
set2 = {10,20,30,50}
set3 = set1.union(set2)
print(set3)

Output:
{40, 10, 50, 20, 30}
```

---

### Q6. Find the intersection of two sets.

**Input:**
```python
set1 = {10,20,30,40}
set2 = {10,20,30,50}
```

**Output:**
`{10, 20, 30}`

```python
# intersection_of_sets.py

set1 = {10,20,30,40}
set2 = {10,20,30,50}
set4 = set1.intersection(set2)
print(set4)

Output:
{10, 20, 30}
```

---

### Q7. Find the difference between two sets.

**Input:**
```python
set1 = {10,20,30,40,50,60}
set2 = {10,20,30,50}
```

**Output:**
`{40, 60}`

```python
# difference_of_sets.py

set1 = {10,20,30,40,50,60}
set2 = {10,20,30,50}
set5 = set1.difference(set2)
print(set5)

Output:
{40, 60}
```

---

### Q8. Convert list to set.

**Input:**
```python
ls = [10,20,30,10,10,40,30,20,40,50]
```

**Output:**
`{40, 10, 50, 20, 30}`

```python
# list_to_set.py

ls = [10,20,30,10,10,40,30,20,40,50]
res = set(ls)
print(res)

Output:
{40, 10, 50, 20, 30}
```

---

### Q9. Check if a number exists in a set.

**Input:**
```python
set1 = {80,90,91,100,101,200,201}
num = 91
```

**Output:** `True`

```python
# check_number_in_set.py

set1 = {80,90,91,100,101,200,201}
num = 91
res1 = num in set1
print(res1)

Output:
True
```

---

### Q10. Find common elements between two lists.

**Input:**
```python
list1 = [20,40,10,70]
list2 = [20,400,100,70]
```

**Output:**
`{20, 70}`

```python
# common_elements_between_lists.py

list1 = [20,40,10,70]
list2 = [20,400,100,70]
set1 = set(list1)
set2 = set(list2)
res = set1.intersection(set2)
print(res)

Output:
{20, 70}
```

### Conclusion

By the end of this notebook, you’ll have a solid grasp of sets fundamentals and essential methods that are building blocks for more advanced Python concepts.
