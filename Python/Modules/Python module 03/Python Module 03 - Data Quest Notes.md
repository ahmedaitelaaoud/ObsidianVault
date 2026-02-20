# Overview

Master Python's core data structures: lists, tuples, sets, and dictionaries while building game analytics systems.

---------------------------------------------------------------
## Exercise 0: Command Quest

### 🎯 **Goal**

Master the entry point of data into a program via the command line.
### 💡 **Core Concept: sys.argv**:

- `sys.argv` -> [arguments]
- `sys.argv[0]` = program name
- `sys.argv[1:]` = actual arguments passed by user
- `len(sys.argv)` = total count of arguments
### 🔑 Key Points

- `sys.argv` is ALWAYS a list (even with 0 args)
- First element `[0]` is program name
- Quoted strings count as 1 argument
- All arguments are strings
----------------------------------------------------------------
## Exercise 1: Score Cruncher

### 🎯 Goal

Process player scores using **lists** and perform analytics.
### 💡 Core Concept: Lists

- **Ordered** collection of items
- **Mutable** (can be modified)
- Perfect for sequential data processing
- Supports: indexing, slicing, iteration
### 🔑 Key Points

- Use `try/except` for input validation
- Convert strings to integers with `int()`
- Lists store values in order
- Built-in functions: `sum()`, `max()`, `min()`, `len()`
- Check for empty lists before calculations
----------------------------------------------------------------
## Exercise 2: Position Tracker
### 🎯 Goal

Use **tuples** to represent 3D coordinates and calculate distances.
### 💡 Core Concept: Tuples

- **Ordered** collection of items
- **Immutable** (cannot be changed after creation)
- Perfect for fixed data: coordinates, RGB colors, dates
- Supports: indexing, slicing, unpacking
### 🔑 Key Points

- **Tuples are immutable**: `position[0] = 5` → ERROR
- **Tuple unpacking**: `x, y, z = (10, 20, 5)`
- Use `split(',')` to parse coordinate strings
- Exception handling with `try/except`
- `math.sqrt()` for distance calculations
- Tuples guarantee data won't accidentally change
----------------------------------------------------------------
## Exercise 3: Achievement Hunter
### 🎯 Goal

Track unique achievements using **sets** and perform set operations.

### 💡 Core Concept: Sets

- **Unordered** collection of **unique** items
- **No duplicates** allowed
- Perfect for: deduplication, membership testing, finding commonalities
- Fast operations: add, remove, check membership
### 🔑 Key Points

- **Automatic deduplication**: `{'a', 'a', 'b'}` → `{'a', 'b'}`
- **Fast membership testing**: `'level_10' in achievements` is O(1)
- **Set operations are powerful**: union, intersection, difference
- Sets are unordered (no indexing)
- Use sets for: unique items, comparisons, analytics
## 📚 Quick Reference: Data Structures

| Structure | Ordered | Mutable | Duplicates         | Use Case                   |
| --------- | ------- | ------- | ------------------ | -------------------------- |
| **List**  | ✅       | ✅       | ✅                  | Sequential data, scores    |
| **Tuple** | ✅       | ❌       | ✅                  | Fixed data, coordinates    |
| **Set**   | ❌       | ✅       | ❌                  | Unique items, analytics    |
| **Dict**  | ✅*      | ✅       | Keys: ❌, Values: ✅ | Key-value pairs, inventory |
## 🎓 Study Tips

1. **Understand WHY each data structure exists**
    - Lists: Order matters, need to modify
    - Tuples: Order matters, should NOT change
    - Sets: Only uniqueness matters
    - Dicts: Need fast lookup by key
2. **Practice conversions**

python

```python
   list_data = [1, 2, 2, 3]
   set_data = set(list_data)  # {1, 2, 3}
   tuple_data = tuple(list_data)  # (1, 2, 2, 3)
   print(list_data)
```



3. **Master error handling**
    - Always use `try/except` for user input
    - Check for empty collections before operations
    - Validate data types
4. **Remember the patterns**
    - Command line: `sys.argv[1:]` for arguments
    - Lists: `for item in list` for iteration
    - Tuples: `x, y, z = position` for unpacking
    - Sets: `set1 & set2` for common elements