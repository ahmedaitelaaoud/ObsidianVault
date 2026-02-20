## 🧠 Conceptual Overview

The **Recursive Backtracker** is a Depth-First Search (DFS) based algorithm. It is "perfect" because it creates a maze with exactly one path between any two cells, meaning there are no loops and no unreachable areas.

+2

## 🛠️ The Process (Stack-Based)

Since Python has a recursion limit, we use an **explicit stack** to avoid crashes on large mazes.

+1

1. **Start** at a random cell (or $0,0$).
    
2. **Mark** current cell as visited.
    
3. **While** the stack is not empty:
    
    - Look at the top cell on the stack.
        
    - Find all **unvisited neighbors**.
        
    - **If** neighbors exist:
        
        - Pick one randomly.
            
        - **Carve** the wall between the current cell and the neighbor (Bitwise modification).
            
            +1
            
        - Push the neighbor to the stack and mark it as visited.
            
    - **Else**:
        
        - **Pop** from the stack (Backtrack) until you find a cell with unvisited neighbors.
            

## 🔢 Bitwise Representation

To satisfy the project requirements, we use a 4-bit integer for each cell.

|**Bit**|**Direction**|**Value**|
|---|---|---|
|0 (LSB)|North|1|
|1|East|2|
|2|South|4|
|3|West|8|

> [!IMPORTANT] 42 Rule: Neighbor Coherence If cell $(0,0)$ has an open **East** wall, cell $(1,0)$ **MUST** have an open **West** wall.

## 🛡️ Structural Constraints (Student 1 Checklist)

- **No Corridors > 2 cells wide**: DFS naturally creates 1-cell wide paths.
    
- **External Walls**: The maze must have walls at the borders.
    
- **42 Pattern**: Inserted by pre-marking cells as "visited" before generation starts.
    

## 💻 Implementation Snippet


```python
# To remove a wall between Current (C) and Neighbor (N):
# Direction from C to N = dir_bit
# Opposite direction from N to C = opp_bit

grid[cy][cx] &= ~dir_bit  # Remove wall from current
grid[ny][nx] &= ~opp_bit  # Remove wall from neighbor
```

## 🔗 Links

- [[Project Task Board]]
    
- [[A-maze-ing Github]]
    
- [[42_pattern.excalidraw]]