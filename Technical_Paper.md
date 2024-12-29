# Scenario: Introduction to Object-Oriented Programming (OOPs)

## Overview
Object-Oriented Programming (OOPs) is a programming paradigm based on the concept of objects. Objects contain data in the form of fields (attributes) and code in the form of methods (functions). OOP promotes code reusability, modularity, and scalability, making it easier to manage complex codebases.

# Key Concepts of OOPs

### 1. Class and Object
* Class: A blueprint for creating objects.
* Object: An instance of a class.
* class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

     def display_info(self):
        return f"{self.brand} {self.model}"

  car1 = Car("Toyota", "Corolla")
  print(car1.display_info())

### 2. Encapsulation
* Bundles data and methods that operate on the data.
* Ensures data security by restricting direct access.
* class Account:
    def __init__(self, balance):
        self.__balance = balance  # Private variable

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

    account = Account(1000)
    account.deposit(500)
    print(account.get_balance())

### 3. Inheritance
* Enables a class to derive properties and behavior from another class.
* class Animal:
    def speak(self):
        return "Animal sound"

  class Dog(Animal):
    def speak(self):
        return "Bark"

  dog = Dog()
  print(dog.speak())

### 4. Polymorphism
* Allows methods to have the same name but behave differently based on the object.
* class Bird:
    def fly(self):
        return "Bird can fly"

   class Penguin(Bird):
    def fly(self):
        return "Penguin cannot fly"

   birds = [Bird(), Penguin()]
   for bird in birds:
   print(bird.fly())

### 5. Abstraction
* Hides implementation details and exposes only essential features.
* from abc import ABC, abstractmethod

* class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

   class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

   rect = Rectangle(10, 5)
   print(rect.area())

## Advantages of OOPs
* Enhances code reusability through inheritance.
* Improves code maintainability with modular design.
* Provides data security via encapsulation.
* Simplifies code extension and scaling.
* Makes code easier to debug and test.

## Best Practices
* Follow naming conventions for classes and methods.
* Use comments and documentation for clarity.
* Implement design patterns for better structure.
* Avoid deeply nested inheritance.
* Write unit tests for class methods.

## References

* Python OOP Documentation
* GeeksforGeeks - OOP Concepts
* Grammarly
