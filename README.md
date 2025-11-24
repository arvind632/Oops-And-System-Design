👋 Hello Developers!

**Welcome to my GitHub repository!** 🙏

### Today we are going to learn the four core concepts of OOP. These principles are essential for every software developer because they provide the foundation for building real-world applications using a structured and maintainable approach.


# Object-Oriented Programming (OOP) – Complete Guide with Real-Life Examples

Object-Oriented Programming (OOP) is a programming paradigm centered around the concept of **objects**—entities that contain both data and behavior.  
OOP makes software **modular, reusable, scalable, and easier to maintain**.

This guide explains the four foundational pillars of OOP with clear, real-life examples and code samples.

---

## 🔵 1. Encapsulation  
Encapsulation is the practice of **bundling data (variables)** and **methods (functions)** inside a single class and controlling access using access modifiers.

### ✔ Benefits
- Protects data from unauthorized access  
- Prevents accidental modification  
- Keeps code clean and predictable  

### ✔ Real-Life Example  
**ATM Machine**  
You can withdraw money or check balance, but you cannot access the internal bank database.  
Only necessary operations are exposed; internal logic is hidden.

### ✔ Code Example

```js
class BankAccount {
  #balance = 0;  // private variable

  deposit(amount) {
    this.#balance += amount;
  }

  getBalance() {
    return this.#balance;
  }
}

const acc = new BankAccount();
acc.deposit(500);
console.log(acc.getBalance()); // 500

```
---

## 🔵 2. Abstraction

## Abstraction means hiding complex implementation details and exposing only the required functionality.

✔ Benefits

Reduces complexity

Simplifies interaction

Focuses on what the system does, not how

✔ Real-Life Example

## Car Steering Wheel
you use a car steering wheel without knowing how the engine works internally

```js

class Car {
  startCar() {
    this.#igniteEngine();
    console.log("Car started");
  }

  #igniteEngine() {  // private method (hidden)
    console.log("Engine ignition...");
  }
}

const myCar = new Car();
myCar.startCar();


```
---

### 🔵 3. Inheritance

Inheritance allows a class (child) to inherit the properties and behavior of another class (parent).

✔ Benefits

Reduces code duplication

Promotes code reusability

Helps model real-world hierarchies

✔ Real-Life Example

Family Traits
A child inherits characteristics from parents (eyes, height, etc).

```js

class Animal {
  speak() {
    console.log("Animal speaks");
  }
}

class Dog extends Animal {
  bark() {
    console.log("Dog barks");
  }
}

const d = new Dog();
d.speak(); // from parent
d.bark();

```


---

### 🔵 4. Polymorphism
Polymorphism allows the same method with different functionality.

```js

class Animal {
  speak() {
    console.log("Animal makes sound");
  }
}

class Cat extends Animal {
  speak() {
    console.log("Cat meows");
  }
}

class Dog extends Animal {
  speak() {
    console.log("Dog barks");
  }
}

const pets = [new Cat(), new Dog()];
pets.forEach(pet => pet.speak());

```






