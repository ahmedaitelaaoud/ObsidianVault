
Answer these **out loud**. This is VERY close to real evaluation questions.

---

## 🔹 General Polymorphism

**Q:** What is polymorphism in this project?  
**A (model):**  
Polymorphism allows different objects to respond differently to the same method call while sharing a common interface. In this project, I can call the same method on different processors, streams, or pipelines, and each behaves according to its specific implementation.

---

## 🔹 Exercise 0 Defense

**Q:** Why use an abstract base class here?  
**A:**  
To define a contract that all processors must follow. It guarantees that every processor implements required behavior while allowing each to specialize its logic.

**Q:** Why not just write separate functions?  
**A:**  
Because separate functions don’t scale. Polymorphism lets me add new processors without modifying existing logic, following the Open/Closed Principle.

---

## 🔹 Exercise 1 Defense

**Q:** How does the StreamProcessor handle different streams without knowing their type?  
**A:**  
It relies on the shared interface defined by the base class. As long as a stream implements the required methods, the processor can use it polymorphically.

**Q:** Why avoid `isinstance()` checks?  
**A:**  
They break polymorphism by coupling logic to concrete types. Proper overriding removes the need for type checks.

---

## 🔹 Exercise 2 Defense (Important)

**Q:** Why use Protocol for stages instead of inheritance?  
**A:**  
Because stages only need to satisfy a behavior contract (`process()`), not share implementation. Protocol allows flexibility without forcing inheritance.

**Q:** Why do adapters inherit from the pipeline?  
**A:**  
Adapters represent specialized pipelines that alter behavior while keeping the same interface, making inheritance appropriate.

**Q:** Where is polymorphism most powerful here?  
**A:**  
In the NexusManager, which can orchestrate multiple pipelines without knowing their concrete types.