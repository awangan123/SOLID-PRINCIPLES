# 🛒 Simple eCommerce Shopping Cart (C++)

This project demonstrates a basic eCommerce shopping cart system implemented in C++, following the **Single Responsibility Principle (SRP)** — one of the SOLID principles of object-oriented design.

## 📌 Features

- Add products to a shopping cart
- Print a simple invoice
- Simulate saving the cart to a database
- Clean separation of concerns using SRP

## 🧱 Classes and Responsibilities

| Class                  | Responsibility                                  |
|------------------------|-------------------------------------------------|
| `Product`              | Represents a product with name and price        |
| `ShoppingCart`         | Manages products and calculates total           |
| `ShoppingCartPrinter`  | Prints the cart invoice                         |
| `ShoppingCartStorage`  | Simulates saving the cart to a database         |

Each class has **only one reason to change**, adhering to SRP.

## 🛠️ How to Compile and Run

### Prerequisites:
- A C++ compiler (e.g., `g++`)

### Compile:
```bash
g++ -o shopping_cart main.cpp


# 🛒 eCommerce Shopping Cart (C++) — OCP-Compliant Design

This project showcases a simple C++ implementation of an eCommerce **shopping cart system**, with a clean design that follows the **Open/Closed Principle (OCP)** — one of the core **SOLID principles** of object-oriented design.

---

## ✅ What’s Implemented?

- Add products to a shopping cart
- Calculate total cart price
- Print a user-friendly invoice
- Save the cart to different storage types (SQL, MongoDB, File)
- Use of abstract class (`Persistence`) to demonstrate OCP

---

## 📚 SOLID Principle Focus: Open/Closed Principle (OCP)

> **Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.**

### ✅ How This Code Follows OCP:
- The `Persistence` class is an **abstract base class** with a `save()` function.
- Concrete classes like `SQLPersistence`, `MongoPersistence`, and `FilePersistence` **extend** behavior **without modifying existing code**.
- You can add new storage types (e.g., `CloudPersistence`, `APIPersistence`) by simply creating a new class that inherits from `Persistence`.

---

## 🧱 Class Responsibilities

| Class                 | Responsibility                              |
|-----------------------|---------------------------------------------|
| `Product`             | Represents a product with name and price    |
| `ShoppingCart`        | Manages products and calculates total       |
| `ShoppingCartPrinter` | Prints invoice for the cart                 |
| `Persistence`         | Abstract class defining a save interface    |
| `SQLPersistence`      | Saves the cart to an SQL database           |
| `MongoPersistence`    | Saves the cart to MongoDB                   |
| `FilePersistence`     | Saves the cart to a file                    |

---

## 🛠️ How to Compile and Run

### 🔧 Requirements:
- C++ compiler (e.g., `g++`)

### 🧪 Compile:
```bash
g++ -o shopping_cart_ocp main.cpp
