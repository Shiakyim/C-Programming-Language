# C++ Basics: Functions, Loops, Arrays, Pointers, Classes, and Structures

This guide is designed for beginners to help them understand the fundamental concepts of C++ programming. Each section explains a core feature of C++ with an easy-to-understand example.

## 1. Functions in C++
Functions allow breaking the program into smaller, reusable pieces, making the code more manageable and readable.

### Explanation:
A function is a block of code that performs a specific task. Functions help in reducing redundancy and improving code structure.

### Syntax:
```cpp
#include <iostream>
using namespace std;

// Function declaration
int add(int a, int b);

int main() {
    int result = add(5, 10);
    cout << "Sum: " << result << endl;
    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}
```

---

## 2. Loops in C++
Loops allow executing a block of code multiple times, which is useful for automating repetitive tasks.

### Explanation:
Loops help in iterating through arrays, processing lists, or executing operations repeatedly under certain conditions.

### Types of Loops:
1. **For Loop** - Used when the number of iterations is known.
```cpp
for(int i = 1; i <= 5; i++) {
    cout << i << " ";
}
```

2. **While Loop** - Used when the number of iterations is unknown but depends on a condition.
```cpp
int i = 1;
while(i <= 5) {
    cout << i << " ";
    i++;
}
```

3. **Do-While Loop** - Similar to `while`, but guarantees at least one execution.
```cpp
int i = 1;
do {
    cout << i << " ";
    i++;
} while(i <= 5);
```

---

## 3. Arrays in C++
Arrays allow storing multiple values in a single variable, making data management easier.

### Explanation:
An array is a collection of elements of the same type, stored in contiguous memory locations.

### Syntax:
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {10, 20, 30, 40, 50};

    // Accessing elements
    for(int i = 0; i < 5; i++) {
        cout << arr[i] << " ";
    }

    return 0;
}
```

---

## 4. Pointers in C++
Pointers allow direct memory access and manipulation, which helps in dynamic memory allocation and data structures like linked lists.

### Explanation:
A pointer is a variable that stores the memory address of another variable.

### Syntax:
```cpp
#include <iostream>
using namespace std;

int main() {
    int num = 10;
    int* ptr = &num; // Pointer stores address of num

    cout << "Value of num: " << num << endl;
    cout << "Address of num: " << &num << endl;
    cout << "Pointer points to: " << ptr << endl;
    cout << "Value at pointer: " << *ptr << endl; // Dereferencing

    return 0;
}
```

---

## 5. Classes in C++
Classes are the foundation of Object-Oriented Programming (OOP) in C++. They allow organizing data and methods together.

### Explanation:
A class is a user-defined data type that contains attributes (variables) and methods (functions).

### Syntax:
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
    Car car1;
    car1.brand = "Toyota";
    car1.speed = 120;
    car1.display();

    return 0;
}
```

---

## 6. Structures in C++
Structures (`struct`) allow grouping different types of data under one name.

### Explanation:
A structure is similar to a class but does not support access modifiers like `private` by default.

### Syntax:
```cpp
#include <iostream>
using namespace std;

struct Student {
    string name;
    int age;
    float marks;
};

int main() {
    Student s1 = {"Alice", 20, 85.5};

    cout << "Name: " << s1.name << endl;
    cout << "Age: " << s1.age << endl;
    cout << "Marks: " << s1.marks << endl;

    return 0;
}
```

---

## Summary Table
| Feature     | Description |
|-------------|------------|
| **Functions** | Blocks of code that perform specific tasks. |
| **Loops** | Repeat a block of code multiple times (`for`, `while`, `do-while`). |
| **Arrays** | Store multiple values of the same type. |
| **Pointers** | Store memory addresses of variables. |
| **Classes** | Blueprints for objects in Object-Oriented Programming. |
| **Structures** | Similar to classes but used for grouping related data. |

---

## License and Copyright
© 2025 Kyim Shia. All rights reserved.

This project and its contents are the intellectual property of Kyim Shia. Unauthorized copying, distribution, modification, or use of this code and documentation, in whole or in part, without explicit permission is prohibited.

For licensing inquiries, please contact Kyimshia@outlook.com.



