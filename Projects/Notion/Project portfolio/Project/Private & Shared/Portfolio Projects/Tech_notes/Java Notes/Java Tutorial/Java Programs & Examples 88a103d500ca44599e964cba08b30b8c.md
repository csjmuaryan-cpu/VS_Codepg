# Java Programs & Examples

A curated collection of essential Java programs with explanations and best practices.

---

## 🎯 Beginner Programs

### 1. Hello World

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Concepts:** Basic syntax, main method, print statement

### 2. Calculator (Basic Operations)

```java
public class Calculator {
    public static void main(String[] args) {
        int a = 10, b = 5;
        
        System.out.println("Addition: " + (a + b));
        System.out.println("Subtraction: " + (a - b));
        System.out.println("Multiplication: " + (a * b));
        System.out.println("Division: " + (a / b));
        System.out.println("Modulus: " + (a % b));
    }
}
```

**Concepts:** Variables, operators, arithmetic operations

### 3. Even or Odd Number Checker

```java
import java.util.Scanner;

public class EvenOdd {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter a number: ");
        int num = scanner.nextInt();
        
        if (num % 2 == 0) {
            System.out.println(num + " is even.");
        } else {
            System.out.println(num + " is odd.");
        }
        
        scanner.close();
    }
}
```

**Concepts:** User input, conditional statements, Scanner class

### 4. Sum of N Natural Numbers

```java
import java.util.Scanner;

public class SumNaturalNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter N: ");
        int n = scanner.nextInt();
        
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        
        System.out.println("Sum of first " + n + " natural numbers: " + sum);
        scanner.close();
    }
}
```

**Concepts:** Loops (for loop), accumulator pattern

### 5. Factorial Calculator

```java
import java.util.Scanner;

public class Factorial {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter a number: ");
        int num = scanner.nextInt();
        
        long factorial = 1;
        for (int i = 1; i <= num; i++) {
            factorial *= i;
        }
        
        System.out.println("Factorial of " + num + " is: " + factorial);
        scanner.close();
    }
}
```

**Concepts:** Loops, multiplication accumulator, long data type

---

## 🚀 Intermediate Programs

### 6. Fibonacci Series

```java
import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter the number of terms: ");
        int n = scanner.nextInt();
        
        int first = 0, second = 1;
        System.out.print("Fibonacci Series: " + first + " " + second);
        
        for (int i = 2; i < n; i++) {
            int next = first + second;
            System.out.print(" " + next);
            first = second;
            second = next;
        }
        
        scanner.close();
    }
}
```

**Concepts:** Series generation, variable swapping, loop logic

### 7. Prime Number Checker

```java
import java.util.Scanner;

public class PrimeNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter a number: ");
        int num = scanner.nextInt();
        
        boolean isPrime = true;
        
        if (num <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= Math.sqrt(num); i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }
        
        if (isPrime) {
            System.out.println(num + " is a prime number.");
        } else {
            System.out.println(num + " is not a prime number.");
        }
        
        scanner.close();
    }
}
```

**Concepts:** Boolean flags, optimization (sqrt), break statement

### 8. Reverse a String

```java
import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter a string: ");
        String str = scanner.nextLine();
        
        String reversed = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }
        
        System.out.println("Reversed string: " + reversed);
        scanner.close();
    }
}
```

**Concepts:** String manipulation, charAt(), reverse iteration

### 9. Array Sum and Average

```java
import java.util.Scanner;

public class ArrayOperations {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter the number of elements: ");
        int n = scanner.nextInt();
        
        int[] arr = new int[n];
        int sum = 0;
        
        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
            sum += arr[i];
        }
        
        double average = (double) sum / n;
        
        System.out.println("Sum: " + sum);
        System.out.println("Average: " + average);
        
        scanner.close();
    }
}
```

**Concepts:** Arrays, type casting, average calculation

### 10. Palindrome Checker

```java
import java.util.Scanner;

public class PalindromeChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter a string: ");
        String str = scanner.nextLine();
        
        String reversed = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }
        
        if (str.equalsIgnoreCase(reversed)) {
            System.out.println("\"" + str + "\" is a palindrome.");
        } else {
            System.out.println("\"" + str + "\" is not a palindrome.");
        }
        
        scanner.close();
    }
}
```

**Concepts:** String comparison, equalsIgnoreCase(), palindrome logic

---

## 🎓 Advanced Programs

### 11. Student Management System (OOP)

```java
import java.util.ArrayList;
import java.util.Scanner;

class Student {
    private String name;
    private int rollNo;
    private double marks;
    
    public Student(String name, int rollNo, double marks) {
        [this.name](http://this.name) = name;
        this.rollNo = rollNo;
        this.marks = marks;
    }
    
    public void display() {
        System.out.println("Name: " + name + ", Roll No: " + rollNo + ", Marks: " + marks);
    }
    
    public String getName() { return name; }
    public int getRollNo() { return rollNo; }
    public double getMarks() { return marks; }
}

public class StudentManagement {
    public static void main(String[] args) {
        ArrayList<Student> students = new ArrayList<>();
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        System.out.print("Enter number of students: ");
        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline
        
        for (int i = 0; i < n; i++) {
            System.out.println("\nEnter details for student " + (i + 1) + ":");
            System.out.print("Name: ");
            String name = scanner.nextLine();
            System.out.print("Roll No: ");
            int rollNo = scanner.nextInt();
            System.out.print("Marks: ");
            double marks = scanner.nextDouble();
            scanner.nextLine(); // consume newline
            
            students.add(new Student(name, rollNo, marks));
        }
        
        System.out.println("\n--- Student List ---");
        for (Student student : students) {
            student.display();
        }
        
        scanner.close();
    }
}
```

**Concepts:** OOP, classes, constructors, encapsulation, ArrayList, enhanced for loop

### 12. Binary Search Implementation

```java
import java.util.Arrays;
import java.util.Scanner;

public class BinarySearch {
    public static int binarySearch(int[] arr, int target) {
        int left = 0;
        int right = arr.length - 1;
        
        while (left <= right) {
            int mid = left + (right - left) / 2;
            
            if (arr[mid] == target) {
                return mid;
            } else if (arr[mid] < target) {
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }
        
        return -1; // not found
    }
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner([System.in](http://System.in));
        
        int[] arr = {2, 5, 8, 12, 16, 23, 38, 45, 56, 67, 78};
        System.out.println("Array: " + Arrays.toString(arr));
        
        System.out.print("Enter the element to search: ");
        int target = scanner.nextInt();
        
        int result = binarySearch(arr, target);
        
        if (result != -1) {
            System.out.println("Element found at index: " + result);
        } else {
            System.out.println("Element not found.");
        }
        
        scanner.close();
    }
}
```

**Concepts:** Binary search algorithm, static methods, O(log n) complexity

---

## 💡 Practice Tips

<aside>
💡

**Best Practices:**

- Always close Scanner objects to prevent resource leaks
- Use meaningful variable names
- Add comments to explain complex logic
- Handle edge cases (negative numbers, empty inputs, etc.)
- Practice error handling with try-catch blocks
</aside>

## 🔗 Related Resources

- **Parent Tutorial:** [Java Tutorial](../Java%20Tutorial%20017b8ce63c53486a935245c3d125638c.md)
- **Practice Platform:** [LeetCode Java Problems](https://leetcode.com/problemset/all/?difficulty=Easy&page=1&topicSlugs=array)
- **More Programs:** [W3Schools Java Exercises](https://www.w3schools.com/java/java_exercises.asp)