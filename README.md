<div align="center">

# 🐍 Python OOPs

### Object-Oriented Programming with Python

A beginner-friendly Jupyter Notebook covering the fundamentals of **Object-Oriented Programming (OOP)** in Python with simple explanations and practical examples.

<br>

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge\&logo=python\&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge\&logo=jupyter\&logoColor=white)
![OOP](https://img.shields.io/badge/Concept-Object%20Oriented%20Programming-purple?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Learning-green?style=for-the-badge)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=180&section=header&text=Python%20OOPs&fontSize=55&fontAlignY=35&desc=Object-Oriented%20Programming%20with%20Python&descAlignY=60&descSize=18" width="100%"/>

</div>

---

## 📖 About This Repository

This repository contains my **Python Object-Oriented Programming (OOP)** notes, concepts, and practical examples created while learning Python.

The notebook explains OOP step-by-step, starting from **classes and objects** and progressing to concepts such as **inheritance, polymorphism, abstraction, encapsulation, class methods, and static methods**.

The examples use simple real-world scenarios to make the concepts easier to understand.

---

## 🧠 Topics Covered

| #  | Topic                          |
| -- | ------------------------------ |
| 01 | 🏗️ Classes                    |
| 02 | 🧩 Objects                     |
| 03 | 🔄 Multiple Objects            |
| 04 | ⚙️ Constructors – `__init__()` |
| 05 | 👤 `self`                      |
| 06 | 📦 Attributes & Methods        |
| 07 | 🔢 Instance & Class Variables  |
| 08 | 🌳 Inheritance                 |
| 09 | 🔀 Polymorphism                |
| 10 | 🎭 Abstraction                 |
| 11 | 🔐 Encapsulation               |
| 12 | 🛠️ Class & Static Methods     |

---

## 🏗️ 1. Classes

A **class** is a blueprint for creating objects.

The notebook demonstrates:

* Creating classes
* Defining attributes
* Defining methods
* Using classes to represent real-world entities

Example concepts are demonstrated using a `Student` class.

---

## 🧩 2. Objects

An **object** is an instance of a class.

The notebook demonstrates how to:

* Create objects
* Access object attributes
* Use methods through objects
* Create multiple objects from the same class

---

## 🔄 3. Multiple Objects

A single class can be used to create multiple objects.

For example:

```python
student1 = Student()
student2 = Student()
student3 = Student()
```

Each object can represent a different instance of the same class.

---

## ⚙️ 4. Constructor – `__init__()`

The `__init__()` method is automatically called when an object is created.

It is used to initialize an object's attributes.

Example:

```python
class Student:

    def __init__(self, name, age):
        self.name = name
        self.age = age
```

The notebook uses student examples to demonstrate constructors and object initialization.

---

## 👤 5. `self`

`self` refers to the **current object**.

It is used to access the object's:

* Attributes
* Methods

Example:

```python
class Student:

    def __init__(self, name):
        self.name = name

    def display(self):
        print(self.name)
```

---

## 📦 6. Attributes & Methods

### Attributes

Attributes represent the **data or properties** of an object.

Example:

```python
self.name
self.age
```

### Methods

A function defined inside a class is called a **method**.

Methods represent the behaviour or actions of an object.

The notebook demonstrates these concepts using student examples.

---

## 🔢 7. Instance & Class Variables

### Instance Variable

An instance variable belongs to a particular object.

```python
self.name
```

Different objects can have different values.

### Class Variable

A class variable is defined directly inside the class and is shared by objects.

```python
class Student:

    clg = "ALTS"
```

The notebook demonstrates the difference between instance variables and class variables.

---

# 🌳 8. Inheritance

**Inheritance** allows one class to use the properties and methods of another class.

It helps with:

* Code reusability
* Reducing duplicate code
* Creating relationships between classes

### Types of Inheritance Covered

1. **Single Inheritance**
2. **Multiple Inheritance**
3. **Multilevel Inheritance**
4. **Hierarchical Inheritance**
5. **Hybrid Inheritance**

The notebook includes practical examples of inheritance and demonstrates how child classes can access functionality from parent classes.

---

## 🔗 `super()`

`super()` is used to access methods or the constructor of a parent class from a child class.

Example:

```python
class Student(Person):

    def __init__(self, name, roll_no, age):
        super().__init__(name, roll_no)
        self.age = age
```

The notebook demonstrates both:

* `super()` with methods
* `super()` with `__init__()`

---

# 🔀 9. Polymorphism

**Polymorphism** means:

> One name, many forms.

The notebook covers three important forms:

### 1. Method Overriding

A child class provides its own implementation of a method inherited from the parent class.

Example:

```python
class Animal:

    def sound(self):
        print("Animal makes a sound")


class Dog(Animal):

    def sound(self):
        print("Dog barks")
```

### 2. Duck Typing

Python focuses on **what an object can do** rather than its specific type.

```python
def make_sound(animal):
    animal.sound()
```

### 3. Operator Overloading

Operators can be given custom behaviour for objects.

The notebook demonstrates operator overloading using:

```python
__add__()
```

---

# 🎭 10. Abstraction

**Abstraction** means hiding unnecessary implementation details and showing only the essential features.

The notebook demonstrates abstraction using Python's `abc` module.

```python
from abc import ABC, abstractmethod
```

It covers:

* Abstract classes
* Abstract methods
* `ABC`
* `@abstractmethod`

Example:

```python
class Car(ABC):

    @abstractmethod
    def start(self):
        pass
```

The notebook demonstrates abstraction using `BMW`, `Tesla`, and `Animal` examples.

---

# 🔐 11. Encapsulation

**Encapsulation** is the process of wrapping data and methods together inside a class and controlling access to the data.

The notebook covers:

| Access Type | Example   | Meaning                            |
| ----------- | --------- | ---------------------------------- |
| Public      | `name`    | Directly accessible                |
| Protected   | `_age`    | Intended for internal/subclass use |
| Private     | `__marks` | Not directly accessible normally   |

A `Bank` example is used to demonstrate private data and controlled access through methods.

Example:

```python
class Bank:

    def __init__(self):
        self.__balance = 50000

    def deposit(self, amount):
        self.__balance += amount

    def show_balance(self):
        print(self.__balance)
```

---

# 🛠️ 12. Class Methods & Static Methods

## Class Method

A class method works with class-level data and takes `cls` as its first parameter.

It is created using:

```python
@classmethod
```

Example:

```python
class Student:

    clg = "ALTS"

    @classmethod
    def change_clg(cls, new_clg):
        cls.clg = new_clg
```

---

## Static Method

A static method does not depend on class or object data.

It is created using:

```python
@staticmethod
```

Example:

```python
class Calculator:

    @staticmethod
    def add(a, b):
        return a + b
```

The notebook demonstrates both class methods and static methods with simple examples.

---

## 📂 Repository Structure

```text
python-oops/
│
├── 📓 oops.ipynb
└── 📄 README.md
```

---

## ▶️ How to Run

### Option 1 — Jupyter Notebook

Clone the repository:

```bash
git clone https://github.com/your-username/python-oops.git
```

Move into the project folder:

```bash
cd python-oops
```

Install Jupyter Notebook:

```bash
pip install notebook
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
oops.ipynb
```

---

### Option 2 — Google Colab

You can also upload `oops.ipynb` to **Google Colab** and run the notebook directly in your browser.

---

## 🎯 Learning Objectives

Through this notebook, I practiced:

* Creating classes
* Creating objects
* Creating multiple objects
* Using constructors
* Understanding `self`
* Working with attributes and methods
* Understanding instance variables
* Understanding class variables
* Implementing inheritance
* Understanding different types of inheritance
* Using `super()`
* Understanding polymorphism
* Method overriding
* Duck typing
* Operator overloading
* Implementing abstraction
* Implementing encapsulation
* Using class methods
* Using static methods

---

## 📈 My Python Learning Journey

This repository is part of my Python learning journey.

```text
Python Basics
      ↓
Functions
      ↓
OOPs ← 📍 Current
      ↓
NumPy
      ↓
Pandas
      ↓
SQL
      ↓
Data Visualization
      ↓
Data Analytics
      ↓
Real-World Projects
```

---

## 🚀 Future Improvements

* [ ] Add more OOP practice problems
* [ ] Add more real-world examples
* [ ] Add a mini OOP project
* [ ] Add advanced OOP concepts
* [ ] Improve documentation
* [ ] Add more exercises and challenges

---

## 📌 Key Takeaway

OOP helps organize Python programs using **classes and objects**, making code easier to reuse, maintain, and structure.

This notebook helped me build a foundation in the core OOP concepts that are important for writing better Python programs.

---

## ⭐ Support

If you find this repository useful or are also learning Python, feel free to ⭐ **Star this repository**.

---

<div align="center">

### 🐍 Keep Learning • Keep Coding • Keep Building 🚀

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=120&section=footer" width="100%"/>

</div>
