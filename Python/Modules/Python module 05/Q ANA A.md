- _Q: What is an Abstract Base Class (ABC) and why is it useful?_
    
    - **A:** An ABC defines a common interface. It's useful because it enforces a strict contract using `@abstractmethod`, guaranteeing that all subclasses will have specific methods, which is required for safe polymorphism.
        
- _Q: What is the difference between method overriding and method overloading?_
    
    - **A:** Overriding is when a child class redefines a method from its parent (same name, same parameters) to change its behavior. Overloading (which Python doesn't natively support in the traditional sense) is having multiple methods with the _same name but different parameters_ in the same class.