# C++ Programming Language Basics

Welcome to the **C++ Programming Language Basics** guide! This guide is designed to help beginners understand the fundamental concepts of C++ programming. It covers essential topics such as functions, loops, arrays, pointers, classes, and structures with easy-to-understand code examples and explanations.

## Table of Contents

1. [Functions in C++](#functions-in-c++)
2. [Loops in C++](#loops-in-c++)
3. [Arrays in C++](#arrays-in-c++)
4. [Pointers in C++](#pointers-in-c++)
5. [Classes in C++](#classes-in-c++)
6. [Structures in C++](#structures-in-c++)
7. [Summary Table](#summary-table)

---

## Functions in C++

### Explanation:
A function is a block of reusable code that performs a specific task. Functions help break down programs into smaller, more manageable pieces. This makes the program easier to debug, maintain, and understand. Functions can return values and accept inputs in the form of parameters.

### Code Example:
```cpp
#include <iostream>
using namespace std;

// Function declaration
int add(int a, int b);

int main() {
    int result = add(5, 10);  // Calling the function and passing two integers
    cout << "Sum: " << result << endl;  // Printing the result
    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;  // Returns the sum of a and b
}
```

### Explanation of Code:
- **Function Declaration:** `int add(int a, int b);` - This tells the compiler about the function’s return type (`int`) and the types of parameters it accepts (two `int` values).
- **Main Function:** In `main()`, the function `add(5, 10)` is called with arguments `5` and `10`. It returns the sum, which is then printed.
- **Function Definition:** `int add(int a, int b)` defines the function, which calculates the sum of `a` and `b` and returns the result.

---

## Loops in C++

### Explanation:
Loops are used to repeatedly execute a block of code as long as a condition is met. Loops are important for automating repetitive tasks.

### Code Example:

#### For Loop:
```cpp
for(int i = 1; i <= 5; i++) {
    cout << i << " ";
}
```
- **Initialization:** `int i = 1;` - Starts with `i` equal to `1`.
- **Condition:** `i <= 5;` - The loop continues as long as `i` is less than or equal to `5`.
- **Increment:** `i++` - Increments `i` by `1` in each iteration.
- The loop will print `1 2 3 4 5`.

#### While Loop:
```cpp
int i = 1;
while(i <= 5) {
    cout << i << " ";
    i++;  // Increment
}
```
- The loop runs as long as `i <= 5`.
- It prints the numbers `1 2 3 4 5` and increments `i` each time.

#### Do-While Loop:
```cpp
int i = 1;
do {
    cout << i << " ";
    i++;  // Increment
} while(i <= 5);
```
- The `do-while` loop guarantees that the code block runs at least once, even if the condition (`i <= 5`) is false on the first check.

---

## Arrays in C++

### Explanation:
An array is a collection of elements of the same data type, stored in contiguous memory locations. Arrays make it easy to manage and process a large number of similar items.

### Code Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {10, 20, 30, 40, 50};  // Array initialization

    // Accessing elements using a loop
    for(int i = 0; i < 5; i++) {
        cout << arr[i] << " ";  // Prints each element in the array
    }

    return 0;
}
```

### Explanation of Code:
- **Array Initialization:** `int arr[5] = {10, 20, 30, 40, 50};` defines an array of 5 integers.
- **Accessing Array Elements:** The `for` loop accesses and prints each element of the array by using the index `i`.

---

## Pointers in C++

### Explanation:
A pointer is a variable that stores the memory address of another variable. Pointers are crucial for dynamic memory management and working with complex data structures such as linked lists.

### Code Example:
```cpp
#include <iostream>
using namespace std;

int main() {
    int num = 10;
    int* ptr = &num;  // Pointer stores the address of num

    cout << "Value of num: " << num << endl;  // Prints the value of num
    cout << "Address of num: " << &num << endl;  // Prints the address of num
    cout << "Pointer points to: " << ptr << endl;  // Prints the address stored in ptr
    cout << "Value at pointer: " << *ptr << endl;  // Dereferencing pointer to get value

    return 0;
}
```

### Explanation of Code:
- **Pointer Declaration:** `int* ptr = &num;` - `ptr` is a pointer to an integer, and it stores the memory address of the variable `num`.
- **Dereferencing:** `*ptr` accesses the value stored at the memory address pointed to by `ptr`.

---

## Classes in C++

### Explanation:
A class is a user-defined data type that bundles data and methods (functions) together. It is the foundation of Object-Oriented Programming (OOP) in C++.

### Code Example:
```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    int speed;

    void display() {
        cout << "Brand: " << brand << ", Speed: " << speed << " km/h" << endl;
    }
};

int main() {
    Car car1;  // Creating an object of class Car
    car1.brand = "Toyota";  // Assigning values to the object
    car1.speed = 120;
    car1.display();  // Calling method to display car details

    return 0;
}
```

### Explanation of Code:
- **Class Declaration:** `class Car` defines a class with two attributes: `brand` and `speed`, and a method `display()` that prints the car's details.
- **Object Creation:** `Car car1;` creates an object `car1` of the class `Car`.
- **Accessing Members:** `car1.brand` and `car1.speed` set the attributes of the object, and `car1.display()` calls the method to display the car's details.

---

## Structures in C++

### Explanation:
A structure (or `struct`) is similar to a class but does not support access modifiers (like `private` or `public`) by default. It is used to group different types of data together.

### Code Example:
```cpp
#include <iostream>
using namespace std;

struct Student {
    string name;
    int age;
    float marks;
};

int main() {
    Student s1 = {"Alice", 20, 85.5};  // Creating and initializing a struct object

    cout << "Name: " << s1.name << endl;  // Accessing struct members
    cout << "Age: " << s1.age << endl;
    cout << "Marks: " << s1.marks << endl;

    return 0;
}
```

### Explanation of Code:
- **Struct Declaration:** `struct Student` defines a structure to hold student information, such as `name`, `age`, and `marks`.
- **Object Initialization:** `Student s1 = {"Alice", 20, 85.5};` creates a `Student` object `s1` and initializes its members.
- **Accessing Members:** `s1.name`, `s1.age`, and `s1.marks` access the individual fields of the structure.

---

## Summary Table

| Feature      | Description                                                    |
|--------------|----------------------------------------------------------------|
| **Functions** | Blocks of code that perform specific tasks, improving modularity and readability. |
| **Loops**     | Repeat a block of code multiple times (for, while, do-while). |
| **Arrays**    | Store multiple values of the same type in contiguous memory. |
| **Pointers**  | Store memory addresses of variables, enabling dynamic memory management. |
| **Classes**   | Blueprints for objects in Object-Oriented Programming, encapsulating data and methods. |
| **Structures**| Group related data (of different types) under one name, but without access modifiers like classes. |

---

This guide covers the basic concepts of C++ and will help you get started with the language. Happy coding! 😊
```

## License and Copyright
© 2025 Kyim Shia. All rights reserved.

This project and its contents are the intellectual property of Kyim Shia. Unauthorized copying, distribution, modification, or use of this code and documentation, in whole or in part, without explicit permission is prohibited.

For licensing inquiries, please contact Kyimshia@outlook.com.



