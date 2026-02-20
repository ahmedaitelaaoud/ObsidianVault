
## Exercise 0 - Ancient Text Recovery

### Testing Checklist

- [ ] Opens the file using `open()`
- [ ] Reads the entire content using `read()`
- [ ] Displays the content correctly with `print()`
- [ ] Closes the file properly using `close()`
- [ ] Works with different file contents
- [ ] Follows the pattern: open, read, print, close

### Key Question

**Q: What happens if a file isn't closed properly?**

**Expected Answer:**

- File descriptors/handles remain open, consuming system resources
- May lead to resource exhaustion if many files are opened
- Data might not be flushed to disk (potential data loss)
- Other programs might not be able to access the file
- Operating system has a limit on open file descriptors

---

## Exercise 1 - Archive Creation

### Testing Checklist

- [ ] Opens a file for writing using `open()` with `'w'` mode
- [ ] Writes content to the file using `write()`
- [ ] Closes the file properly using `close()`
- [ ] Creates the file if it doesn't exist
- [ ] Created file contains expected content
- [ ] Program overwrites existing files (if applicable)

### Key Questions

**Q: What's the difference between 'r' and 'w' modes?**

**Expected Answer:**

- `'r'` mode (read):
    
    - Opens file for reading only
    - File must exist or FileNotFoundError is raised
    - Cannot write to the file
    - File pointer starts at beginning
- `'w'` mode (write):
    
    - Opens file for writing
    - Creates file if it doesn't exist
    - **Overwrites** existing file content (truncates to zero)
    - Cannot read from the file

**Q: Why is 'w' mode potentially dangerous?**

**Expected Answer:**

- It overwrites/deletes all existing data in the file without warning
- Need to be careful not to accidentally destroy important data
- Use `'a'` (append) mode if you want to preserve existing content

---

## Exercise 2 - Stream Management

### Testing Checklist

- [ ] Reads input from `sys.stdin` (or uses `input()`)
- [ ] Writes normal output to `sys.stdout` (standard `print()`)
- [ ] Writes alerts/errors to `sys.stderr` using `print(message, file=sys.stderr)`
- [ ] Demonstrates understanding of the three streams
- [ ] Different message types go to appropriate streams

### Key Questions

**Q: Why do programs have separate streams for normal output and errors?**

**Expected Answer:**

- **Separation of concerns**: Normal output vs diagnostic/error messages
- **Redirection**: Can redirect stdout and stderr independently
    - Example: `program > output.txt 2> errors.txt`
- **Pipeline compatibility**: Errors don't contaminate data pipelines
- **User experience**: Errors can be displayed even when output is redirected
- **Logging**: Easier to separate logs from actual program output

**Q: What are the three standard streams?**

**Expected Answer:**

- `stdin` (0): Standard input - for reading user input
- `stdout` (1): Standard output - for normal program output
- `stderr` (2): Standard error - for error messages and diagnostics

---

## Exercise 3 - Vault Security

### Testing Checklist

- [ ] Uses `with` statement for all file operations
- [ ] File reading: `with open(filename, 'r') as file:`
- [ ] File writing: `with open(filename, 'w') as file:`
- [ ] Files are automatically closed when using `with`
- [ ] File is closed even if exception occurs
- [ ] Demonstrates understanding of context managers

### Key Questions

**Q: How does the `with` statement make file operations safer?**

**Expected Answer:**

- **Automatic cleanup**: File is automatically closed when block exits
- **Exception safety**: File is closed even if an exception occurs
- **No forgotten close()**: Eliminates human error of forgetting to close
- **Cleaner code**: More readable and concise
- **Resource management**: Ensures proper resource cleanup

**Q: What does RAII (Resource Acquisition Is Initialization) mean?**

**Expected Answer:**

- Programming idiom where resource lifetime is tied to object lifetime
- Resource is acquired when object is created (initialized)
- Resource is released when object is destroyed (goes out of scope)
- The `with` statement implements RAII in Python
- Ensures resources (like file handles) are always released
- Common in languages like C++ with destructors

**Q: What is a context manager?**

**Expected Answer:**

- Object that defines `__enter__()` and `__exit__()` methods
- Used with the `with` statement
- `__enter__()` is called when entering the block
- `__exit__()` is called when exiting the block (even on exception)
- Provides setup and cleanup logic
- File objects are context managers

---

## Exercise 4 - Crisis Response

### Testing Checklist

- [ ] Combines `try/except` blocks with `with` statement
- [ ] Handles `FileNotFoundError` gracefully
- [ ] Shows appropriate error message for missing files
- [ ] Handles `PermissionError` (if testable)
- [ ] Normal file operations work correctly
- [ ] Doesn't crash on errors
- [ ] Success cases are handled properly

### Key Questions

**Q: What are the most common file operation errors?**

**Expected Answer:**

- **FileNotFoundError**: File doesn't exist when trying to read
- **PermissionError**: Insufficient permissions to access file
- **IsADirectoryError**: Trying to open a directory as a file
- **IOError/OSError**: General I/O errors (disk full, disk removed, etc.)
- **UnicodeDecodeError**: File encoding doesn't match expected encoding

**Q: How does proper error handling prevent data loss?**

**Expected Answer:**

- **Graceful degradation**: Program doesn't crash, can save work elsewhere
- **User notification**: User is informed of issues and can take action
- **Rollback capability**: Can abort operations that might corrupt data
- **Logging**: Records errors for debugging and auditing
- **Alternative paths**: Can try backup locations or methods
- **Data integrity**: Ensures partial writes don't corrupt files

**Q: What are defensive programming principles?**

**Expected Answer:**

- Anticipate and handle potential errors before they occur
- Validate inputs and assumptions
- Use exception handling for recoverable errors
- Provide meaningful error messages
- Fail safely without data loss
- Don't trust external resources (files, network, user input)
- Test error paths, not just success paths

---

## Knowledge Review - Comprehensive Questions

### Question 1: File Closure

**Q: What happens to the storage system if connections aren't properly closed?**

**Expected Answer:**

- Resource leaks (file descriptors remain allocated)
- System may run out of available file handles
- Data may not be written to disk (buffers not flushed)
- File locks may remain, preventing other processes from accessing
- Potential memory leaks in some implementations
- Performance degradation over time

### Question 2: Read vs Write Modes

**Q: What's the critical difference between extraction mode ('r') and preservation mode ('w')?**

**Expected Answer:**

- **'r' (read/extraction)**: Non-destructive, requires file to exist
- **'w' (write/preservation)**: Destructive, truncates existing content
- **'r'** is safe - cannot modify existing data
- **'w'** is dangerous - overwrites everything
- Always verify you're using the correct mode before opening files

### Question 3: Stream Separation

**Q: Why do the Archives maintain separate channels for standard data and alerts?**

**Expected Answer:**

- Allows independent handling of data vs diagnostics
- Enables redirection without mixing concerns
- Maintains data pipeline integrity
- Provides flexibility in logging and monitoring
- Separates what the program produces from how it's running
- Industry standard practice (Unix philosophy)

### Question 4: Context Managers and RAII

**Q: How does the `with` protocol prevent data corruption? What is the RAII principle?**

**Expected Answer:**

- **With protocol**:
    - Guarantees cleanup code runs (file closure)
    - Works even if exceptions occur
    - Flushes buffers before closing
    - Prevents incomplete writes from being left open
- **RAII**:
    - Resource Acquisition Is Initialization
    - Resources tied to object lifetime
    - Automatic cleanup when object goes out of scope
    - Prevents resource leaks
    - Ensures proper ordering of resource release

### Question 5: Digital Archive Threats

**Q: What are the most dangerous threats to digital archives?**

**Expected Answer:**

- **Uncaught exceptions** during write operations
- **Permission errors** preventing access
- **Disk space exhaustion** causing incomplete writes
- **Concurrent access** without proper locking
- **Hardware failures** without proper error handling
- **Improper encoding** causing data corruption
- **Missing error handling** leading to data loss
- **Resource leaks** from unclosed files

---

## Basic File Operation Pattern

### The Fundamental Pattern

```python
# Without context manager (manual cleanup)
file = open("filename.txt", "r")
try:
    content = file.read()
    print(content)
finally:
    file.close()

# With context manager (automatic cleanup)
with open("filename.txt", "r") as file:
    content = file.read()
    print(content)
# File automatically closed here
```

### Expected Demonstration

Student should be able to:

1. Show the basic pattern: open → read/write → close
2. Explain why each step is necessary
3. Demonstrate the `with` statement
4. Show exception handling for file operations
5. Explain the benefits of context managers

---

## Grading Notes

### Pass Criteria

- ✅ All exercises function correctly
- ✅ Proper understanding of file operations
- ✅ Can explain concepts clearly
- ✅ Demonstrates defensive programming
- ✅ Understands context managers and error handling

### Fail Criteria

- ❌ Code doesn't run or crashes
- ❌ Doesn't understand basic file operations
- ❌ Can't explain key concepts
- ❌ Missing error handling
- ❌ Doesn't use `with` statement where required
- ❌ Memory leaks or resource leaks

### Red Flags

- ⚠️ Hardcoded file paths
- ⚠️ No error handling
- ⚠️ Doesn't close files
- ⚠️ Doesn't understand stream separation
- ⚠️ Can't explain RAII or context managers
- ⚠️ Mixing concerns (errors to stdout)

---

## Additional Tips for Evaluators

1. **Be patient**: File I/O concepts can be abstract for beginners
2. **Ask for demonstrations**: Theory + practice shows understanding
3. **Check edge cases**: What happens with empty files? Large files?
4. **Verify error handling**: Don't just test happy paths
5. **Confirm understanding**: Ask "why" not just "what"
6. **Encourage best practices**: Context managers, error handling, etc.

---

_This guide is based on the Python Module 04 evaluation scale. Adjust questions based on student's level and responses._