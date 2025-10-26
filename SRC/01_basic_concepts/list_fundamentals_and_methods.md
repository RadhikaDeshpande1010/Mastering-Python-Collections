<h1><sub><img src="https://github.com/RadhikaDeshpande1010/icon-library/blob/main/python-icon/python-icon.png" alt="Icon" height="27" width="27"></sub> Mastering Python Collections — Lists, Sets, and Strings </h1>

<h2>Lists Fundamentals and Methods</h2>

This notebook provides a hands-on introduction to **Python lists** and their commonly used methods. It is designed for beginners to build a strong foundation in handling lists through step-by-step examples and exercises.

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
### Q1. Check if a number exists in a list.

**Input:** 
`list1 = [10, 20, 30, 40, 50]`
`number = 10`

**Output:** `true`

```python
# check_number_in_list.py

list1 = [10, 20, 30, 40, 50]
number = 10
res1 = number in list1
print(res1)

Output:
True
```

---
### Q2. Check if a number does not exist in a list.

**Input:** 
`list1 = [10, 20, 30, 40, 50]`
`number = 100`

**Output:** `false`

```python
# check_number_not_in_list.py

list1 = [10, 20, 30, 40, 50]
number = 100
res1 = number in list1
print(res1)

Output:
False
```

---
### Q3. Verify if a number is not present in a list.

**Input:** 
`list1 = [10, 20, 30, 40, 50]`
`number = 100`

**Output:** `true`

```python
# check_number_not_present.py

list1 = [10, 20, 30, 40, 50]
number = 100
res1 = number not in list1
print(res1)

Output:
True
```

---
### Q4. Verify if a number is not present in a list (number exists).

**Input:** 
`list1 = [10, 20, 30, 40, 50]`
`number = 10`

**Output:** `false`

```python
# check_number_present_with_not_in.py

list1 = [10, 20, 30, 40, 50]
number = 10
res1 = number not in list1
print(res1)

Output:
False
```

---
### Q5. Count how many times a number appears in a list.

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
`number = 30`

**Output:** `2`

```python
# count_number_in_list.py

list1 = [10, 20, 30, 40, 40, 30, 10]
number = 30
res1 = list1.count(number)
print(res1)

Output:
2
```

---
### Q6. Count how many times a number appears in a list (number not present).

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
`number = 300`

**Output:** `0`

```python
# count_number_not_in_list.py

list1 = [10, 20, 30, 40, 40, 30, 10]
number = 300
res1 = list1.count(number)
print(res1)

Output:
0
```

---
### Q7. Find the index of the first occurrence of a number in a list.

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
`number = 20`

**Output:** `1`

```python
# find_index_in_list.py

list1 = [10, 20, 30, 40, 40, 30, 10]
number = 20
res1 = list1.index(number)
print(res1)

Output:
1
```

---
### Q8. Find the index of the first occurrence of a number in a list (number at start).

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
`number = 10`

**Output:** `0`

```python
# find_index_in_list_start.py

list1 = [10, 20, 30, 40, 40, 30, 10]
number = 10
res1 = list1.index(number)
print(res1)

Output:
0
```

---
### Q9. Find the index of a number not present in a list.

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
`number = 100`

**Output:** `ValueError: 100 is not in list`

```python
# find_index_not_in_list.py

list1 = [10, 20, 30, 40, 40, 30, 10]
number = 100
res1 = list1.index(number)
print(res1)

Output:
ValueError: 100 is not in list
```

---
### Q10. Delete an element from a list by index.

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
`Delete element at index = 2`

**Output:** `[10, 20, 40, 40, 30, 10]`

```python
# delete_element_by_index.py

list1 = [10, 20, 30, 40, 40, 30, 10]
del list1[2]
print(list1)

Output:
[10, 20, 40, 40, 30, 10]
```

---
### Q11. Delete an element from a list by index.

**Input:** 
`list1 = []`
`Append = 1`

**Output:** `[1]`

```python
# append_to_empty_list.py

list1 = []
list1.append(1)
print(list1)

Output:
[1]
```

---
### Q12. Update an element in a list by index.

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
Update element at index `2` to `100`

**Output:** `[10, 20, 100, 40, 40, 30, 10]`

```python
# update_element_by_index.py

list1 = [10, 20, 30, 40, 40, 30, 10]
list1[2] = 100
print(list1)

Output:
[10, 20, 100, 40, 40, 30, 10]
```

---
### Q13. Insert an element at a specific index in a list.

**Input:** 
`list1 = [10, 20, 30, 40, 40, 30, 10]`
Insert `100` at index `2`

**Output:** `[10, 20, 100, 30, 40, 40, 30, 10]`

```python
# insert_element_by_index.py

list1 = [10, 20, 30, 40, 40, 30, 10]
list1.insert(2, 100)
print(list1)

Output:
[10, 20, 100, 30, 40, 40, 30, 10]
```

---
### Q14. Remove duplicates from a list while preserving order.

**Input:** 
`list1 = [10, 10, 20, 30, 30, 40]`

**Output:** `[10, 20, 30, 40]`

```python
# remove_duplicates_preserve_order.py

list1 = [10, 10, 20, 30, 30, 40]
list2 = []
for i in list1:
    if i not in list2:
        list2.append(i)
print(list2)

Output:
[10, 20, 30, 40]
```

---
### Q15. Step-by-step: Remove duplicates from a list.

**Input:** 
`list1 = [10, 10, 20, 30, 30, 40]`

Step 1: Remove duplicates → `[10, 20, 30, 40]`

**Output:** `[10, 20, 30, 40]`

```python
# remove_duplicates_stepwise.py

list1 = [10, 10, 20, 30, 30, 40]

# step1 :=> remove the duplicate from the list ([10, 20, 30, 40])
list2 = []
for i in list1:
    if i not in list2:
        list2.append(i)

print(list2)

Output:
[10, 20, 30, 40]
```

---
### Q16. Find elements that occur only once in a list.

**Input:** 
`list1 = [10, 10, 20, 30, 30, 40]`

**Output:** `10` `20`

```python
# find_unique_elements.py

list1 = [10, 10, 20, 30, 30, 40]

# step1: remove duplicates
list2 = []
for i in list1:
    if i not in list2:
        list2.append(i)

# step2: print elements that occur only once
for i in list2:
    if list1.count(i) == 1:
        print(i)

Output:
10
20
```

---

### ✅Conclusion

By the end of this notebook, you’ll have a solid grasp of lists fundamentals and essential methods that are building blocks for more advanced Python concepts.

