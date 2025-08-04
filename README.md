# SOLID Principles Demonstrated in C++ Projects

This repository contains multiple C++ projects that demonstrate key SOLID principles of object-oriented design. Below is an explanation of how each project implements the principles of:

- **Liskov Substitution Principle (LSP)**
- **Single Responsibility Principle (SRP)**
- **Open/Closed Principle (OCP)**

---

## 1. Bank Account Management System — Liskov Substitution Principle (LSP)

**What is LSP?**  
Subtypes must be substitutable for their base types without altering program correctness.

**How this project demonstrates LSP:**  
- Abstract base classes (`DepositOnlyAccount`, `WithdrawableAccount`) define clear interfaces for different account capabilities.
- Derived classes (`SavingAccount`, `CurrentAccount`, `FixedTermAccount`) implement these interfaces correctly according to their allowed operations.
- The `BankClient` uses base class pointers, enabling seamless substitution of any derived account type without breaking functionality.
- Interface segregation ensures accounts that do not support withdrawal (e.g., `FixedTermAccount`) do not expose a withdrawal interface, preventing misuse and upholding LSP.

---

## 2. Shopping Cart System — Single Responsibility Principle (SRP)

**What is SRP?**  
A class should have only one reason to change — it should have a single responsibility.

**How this project demonstrates SRP:**  
- The system separates concerns into distinct classes:
  - `Product`: Manages product data.
  - `ShoppingCart`: Manages cart contents and calculates totals.
  - `ShoppingCartPrinter`: Responsible solely for printing invoices.
  - `ShoppingCartStorage`: Handles saving the cart data to a database (simulated).
- Each class handles one specific responsibility, ensuring changes to one aspect (e.g., printing or storage) do not affect others, improving maintainability.

---

## 3. Shopping Cart System — Open/Closed Principle (OCP)

**What is OCP?**  
Software entities should be open for extension but closed for modification.

**How this project demonstrates OCP:**  
- Defines an abstract base class `Persistence` with a `save()` interface.
- Concrete implementations (`SQLPersistence`, `MongoPersistence`, `FilePersistence`) extend the base class to add new storage behaviors without modifying existing code.
- This design allows new storage types (e.g., cloud storage) to be added by creating new classes, keeping existing classes unchanged, and preserving system stability.

---

## Summary Table

| Project                     | SOLID Principle                  | Key Implementation Details                                   |
|-----------------------------|---------------------------------|--------------------------------------------------------------|
| Bank Account Management      | Liskov Substitution Principle   | Interface segregation and substitutable account types        |
| Shopping Cart (SRP)          | Single Responsibility Principle | Separate classes for product, cart management, printing, and storage |
| Shopping Cart (OCP)          | Open/Closed Principle            | Abstract persistence interface with extendable concrete classes |

---

## License

This repository is licensed under the MIT License.
