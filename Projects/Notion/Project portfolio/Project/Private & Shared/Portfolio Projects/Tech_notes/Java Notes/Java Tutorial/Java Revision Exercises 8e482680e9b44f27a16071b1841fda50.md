# Java Revision Exercises

Structured exercises to reinforce your Java knowledge, organized by difficulty and topic.

---

## 🎯 Topic 1: Basics & Syntax

### Exercise 1.1: Variables and Data Types

**Task:** Create a program that demonstrates all primitive data types in Java.

- [ ]  Declare variables of each primitive type (byte, short, int, long, float, double, char, boolean)
- [ ]  Assign appropriate values
- [ ]  Print each variable with its type and value
- [ ]  Show type casting examples (implicit and explicit)

**Expected Output:**

```
byte: 127
short: 32000
int: 2147483647
...
```

---

### Exercise 1.2: Operators Practice

**Task:** Build a program that demonstrates all types of operators.

- [ ]  Arithmetic operators (+, -, *, /, %)
- [ ]  Relational operators (==, !=, >, <, >=, <=)
- [ ]  Logical operators (&&, ||, !)
- [ ]  Assignment operators (=, +=, -=, etc.)
- [ ]  Increment/Decrement operators (++, --)

**Challenge:** Create a simple calculator that uses all arithmetic operators

---

### Exercise 1.3: Control Flow Mastery

**Task:** Write programs using different control structures.

- [ ]  **Part A:** Grade calculator using if-else-if ladder (A: 90-100, B: 80-89, etc.)
- [ ]  **Part B:** Day of week using switch statement (1-7 maps to Mon-Sun)
- [ ]  **Part C:** Multiplication table using for loop
- [ ]  **Part D:** Number guessing game using while loop
- [ ]  **Part E:** Menu-driven program using do-while loop

---

## 🚀 Topic 2: Methods & Functions

### Exercise 2.1: Method Creation

**Task:** Create a utility class with various methods.

- [ ]  Method to check if a number is prime
- [ ]  Method to find GCD of two numbers
- [ ]  Method to calculate power (x^n)
- [ ]  Method to check if a year is a leap year
- [ ]  Method to convert Celsius to Fahrenheit

**Requirements:**

- Use appropriate return types
- Add JavaDoc comments
- Handle edge cases

---

### Exercise 2.2: Method Overloading

**Task:** Create an `Area` class with overloaded methods.

- [ ]  `area(double side)` - for square
- [ ]  `area(double length, double width)` - for rectangle
- [ ]  `area(double radius, boolean isCircle)` - for circle
- [ ]  `area(double base, double height, boolean isTriangle)` - for triangle

**Challenge:** Add volume calculation methods for 3D shapes

---

### Exercise 2.3: Recursion Practice

**Task:** Implement recursive solutions.

- [ ]  Factorial of a number
- [ ]  Fibonacci number at position n
- [ ]  Sum of digits of a number
- [ ]  Tower of Hanoi solution
- [ ]  String reversal using recursion

**Bonus:** Compare recursive vs iterative performance

---

## 🎓 Topic 3: Object-Oriented Programming

### Exercise 3.1: Class Design

**Task:** Design a `BankAccount` class.

- [ ]  **Attributes:** accountNumber, accountHolder, balance
- [ ]  **Constructor:** Initialize with account details
- [ ]  **Methods:**
    - `deposit(double amount)` - add money
    - `withdraw(double amount)` - remove money (check sufficient balance)
    - `getBalance()` - return current balance
    - `displayAccountInfo()` - show all details

**Challenge:** Add interest calculation method

---

### Exercise 3.2: Inheritance

**Task:** Create an inheritance hierarchy.

```
       Shape (abstract)
          |
  ________________
  |       |      |
Circle  Square Rectangle
```

- [ ]  Create abstract `Shape` class with abstract method `calculateArea()`
- [ ]  Implement `Circle`, `Square`, and `Rectangle` classes
- [ ]  Override `calculateArea()` in each subclass
- [ ]  Add a `displayInfo()` method in parent class
- [ ]  Create objects and test polymorphism

---

### Exercise 3.3: Encapsulation & Data Hiding

**Task:** Create a `Person` class with proper encapsulation.

- [ ]  Private fields: name, age, email
- [ ]  Public getters and setters
- [ ]  **Validation in setters:**
    - Age should be between 0 and 150
    - Email should contain '@'
    - Name should not be empty
- [ ]  Override `toString()` method

---

### Exercise 3.4: Interface Implementation

**Task:** Design and implement interfaces.

- [ ]  Create `Payable` interface with method `calculatePayment()`
- [ ]  Create classes: `Employee`, `Contractor`, `Invoice`
- [ ]  Implement `Payable` in all classes with different logic
- [ ]  Create array of `Payable` objects and process payments

---

## 📦 Topic 4: Collections Framework

### Exercise 4.1: ArrayList Operations

**Task:** Build a task manager using ArrayList.

- [ ]  Add tasks
- [ ]  Remove tasks by index
- [ ]  Display all tasks
- [ ]  Search for a task
- [ ]  Sort tasks alphabetically
- [ ]  Count total tasks

---

### Exercise 4.2: HashMap Practice

**Task:** Create a phone directory.

- [ ]  Store name-phone number pairs
- [ ]  Add new contacts
- [ ]  Search contact by name
- [ ]  Update contact number
- [ ]  Delete contact
- [ ]  Display all contacts

**Challenge:** Handle duplicate names

---

### Exercise 4.3: Collections Algorithms

**Task:** Practice Collections utility methods.

- [ ]  Sort a list in ascending and descending order
- [ ]  Find max and min elements
- [ ]  Shuffle a list
- [ ]  Reverse a list
- [ ]  Search using binary search
- [ ]  Find frequency of an element

---

## 🔥 Topic 5: Exception Handling

### Exercise 5.1: Try-Catch Blocks

**Task:** Handle different exceptions.

- [ ]  **Division by zero:** ArithmeticException
- [ ]  **Array index:** ArrayIndexOutOfBoundsException
- [ ]  **Number format:** NumberFormatException
- [ ]  **Null pointer:** NullPointerException

**Requirements:**

- Use specific catch blocks
- Add finally block for cleanup
- Display user-friendly error messages

---

### Exercise 5.2: Custom Exceptions

**Task:** Create custom exception classes.

- [ ]  Create `InsufficientBalanceException`
- [ ]  Create `InvalidAgeException`
- [ ]  Use these in appropriate scenarios
- [ ]  Throw exceptions with meaningful messages

---

## 📁 Topic 6: File Handling

### Exercise 6.1: File Read/Write

**Task:** Create a simple note-taking application.

- [ ]  Write notes to a file
- [ ]  Read notes from a file
- [ ]  Append new notes
- [ ]  Handle FileNotFoundException
- [ ]  Handle IOException

---

### Exercise 6.2: Student Record System

**Task:** Build a file-based student database.

- [ ]  Save student records to file (CSV format)
- [ ]  Load records from file
- [ ]  Search student by roll number
- [ ]  Update student marks
- [ ]  Delete student record

---

## 🏆 Challenge Projects

### Challenge 1: Library Management System

**Combine multiple concepts:**

- [ ]  Use OOP (Book, Member, Library classes)
- [ ]  ArrayList for storing books and members
- [ ]  File I/O for persistence
- [ ]  Exception handling for errors
- [ ]  Menu-driven interface

**Features:**

- Add/Remove books
- Register members
- Issue/Return books
- View available books
- Search functionality

---

### Challenge 2: Banking Application

**Full-featured banking system:**

- [ ]  Multiple account types (Savings, Current)
- [ ]  Inheritance hierarchy
- [ ]  Transaction history
- [ ]  File-based storage
- [ ]  Custom exceptions
- [ ]  Interest calculation

---

### Challenge 3: Student Grade Analyzer

**Data analysis program:**

- [ ]  Read student data from file
- [ ]  Calculate average, highest, lowest grades
- [ ]  Generate grade distribution
- [ ]  Identify top performers
- [ ]  Generate report to file

---

## 📊 Progress Tracker

**Basics & Syntax:** ⬜⬜⬜ (0/3)

**Methods & Functions:** ⬜⬜⬜ (0/3)

**OOP:** ⬜⬜⬜⬜ (0/4)

**Collections:** ⬜⬜⬜ (0/3)

**Exception Handling:** ⬜⬜ (0/2)

**File Handling:** ⬜⬜ (0/2)

**Challenge Projects:** ⬜⬜⬜ (0/3)

**Overall Progress:** 0/20 exercises completed

---

## 💡 Study Tips

<aside>
🎯

**Effective Practice Strategy:**

1. **Understand First:** Read the exercise requirements carefully
2. **Plan:** Write pseudocode before coding
3. **Code:** Implement the solution
4. **Test:** Try different inputs, including edge cases
5. **Optimize:** Can you make it better?
6. **Document:** Add comments explaining your logic
</aside>

<aside>
⏰

**Time Management:**

- Basic exercises: 15-30 minutes each
- Intermediate exercises: 30-60 minutes each
- Challenge projects: 2-4 hours each
</aside>

## 🔗 Related Pages

- **Theory:** [Java Tutorial](../Java%20Tutorial%20017b8ce63c53486a935245c3d125638c.md)
- **Programs:** Java Programs & Examples (created above)
- **Practice:** [Java Exercises on W3Schools](https://www.w3schools.com/java/java_exercises.asp)