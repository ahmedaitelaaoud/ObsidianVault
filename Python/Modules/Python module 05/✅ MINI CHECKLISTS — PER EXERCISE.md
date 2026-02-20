

Use these **before you code** and **before you submit**.

---

## 🟢 Exercise 0 — Data Processor Foundation

### Architecture Checklist

- [ ] I have **one abstract base class**
    
- [ ]  Base class defines the **contract**, not behavior
    
- [ ]  `process()` and `validate()` are **abstract**
    
- [ ]  `format_output()` has a **default implementation**
    
- [ ]  All subclasses override **exactly the same method signatures**
    

### Polymorphism Checklist

- [ ]  I can call `process()` on **any processor** without caring which one it is
    
- [ ]  Each subclass changes behavior **without changing the interface**
    
- [ ]  No `if type ==` logic in the caller
    

### Evaluation Self-Test

Ask yourself:

- “What promise does `DataProcessor` make?”
    
- “What happens if I add a new processor tomorrow?”
    
- “Can I explain method overriding without mentioning syntax?”
    

If you can answer those → you’re good.

---

## 🟢 Exercise 1 — Polymorphic Streams

### Architecture Checklist

-  One abstract `DataStream` base class
    
-  `process_batch()` is abstract
    
-  `filter_data()` and `get_stats()` have defaults
    
-  Subclasses override behavior meaningfully (not copy-paste)
    

### Manager Checklist

-  StreamProcessor accepts **any DataStream**
    
-  Manager never checks concrete types
    
-  Streams can be stored in a **single list**
    
-  Same method call → different behavior at runtime
    

### Polymorphism Stress Test

Ask yourself:

- “If I add a `VideoStream`, does the manager change?”
    
- “Who owns stats — the manager or the stream?”
    
- “Why is inheritance better than a big if/else here?”
    

---

## 🟢 Exercise 2 — Nexus Integration (Hard One)

### Architecture Checklist

-  Clear separation:
    
    - Stages → behavior only
        
    - Pipeline → orchestration
        
-  Stages use **Protocol / duck typing**
    
-  Pipelines use **ABC inheritance**
    
-  Adapters override `process()` meaningfully
    
-  NexusManager never depends on concrete pipelines
    

### Design Integrity Check

-  Composition is used more than inheritance
    
-  Pipelines contain stages (HAS-A)
    
-  Adapters extend pipelines (IS-A)
    
-  Data flows stage → stage → stage
    

### Enterprise-Level Question

Ask yourself:

- “What breaks if one stage fails?”
    
- “Where does recovery logic belong?”
    
- “Can I reuse this pipeline with a new adapter?”