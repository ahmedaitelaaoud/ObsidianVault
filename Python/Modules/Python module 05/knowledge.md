## What is Abstract Base Class

- **Enforce Method Implementation**: An abstract class is a class that you make to make sure every class that <span style="color:rgb(255, 255, 0)">inherits</span> from it has <span style="color:rgb(255, 255, 0)">all methods/attributes</span> it will need
- **Shared Functionality**: Abstract class <span style="color:rgb(192, 0, 0)">can't be instantiated</span>, only exist to be extended
- **Documentation and Clarity**:They serve as a clear <span style="color:rgb(0, 176, 80)">contract</span> for what methods subclasses must implement.
- **Abstract Classes in Python**: Unlike some other languages, Python's abstract classes can have both abstract and concrete methods, providing more flexibility.

***Example***:

```python
from abc import ABC, abstractmethod
class Animal(ABC):

	@abstractmethod
	def make_sound(self):
		pass
	def sleep(self):
		print("Zzz...")
	
  
class Dog(Animal):

	def make_sound(self):
		print("Haw")

  
class Cat(Animal):

	def make_sound(self):
		print("Meow")

  
cat = Cat()

cat.make_sound()

dog = Dog()

dog.make_sound()

dog.sleep()
```

## What is Typing module

In Python **typing** refers to a system of adding optional **type hint** (type annotations) to code, they are checked at <span style="color:rgb(0, 176, 80)">runtime</span>. It's for developers to understand the <span style="color:rgb(255, 255, 0)">e</span><span style="color:rgb(255, 255, 0)">xpected</span> <span style="color:rgb(255, 255, 0)">types</span> of <span style="color:rgb(0, 176, 240)">v<span style="color:rgb(0, 176, 240)">ariable</span>s</span>, <span style="color:rgb(0, 176, 240)">functions parameters</span>, and <span style="color:rgb(0, 176, 240)">return values</span>.

### Key Concepts

- **Dynamic Typing**: Python's default behavior, where a variable's type is determined during execution and can change.
- **Static Typing**: check for type errors _before_ the code runs. This helps catch bugs early and improves code quality.

```python
from typing import Any, List, Dict, Union, Optional
def devision(a: int, b: int) -> float:

	if b != 0:
		print (a / b)
	else:
		print("cannot devise by 0")

devision(10,5)
devision(10,0)
```

## Polymorphism

