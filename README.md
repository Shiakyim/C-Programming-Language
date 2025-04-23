# Concise Overview of PF and OOP by 𝔎𝔶𝔦𝔪

This guide covers the basic concepts of C++ and will help you get started with the language. Happy coding! 🚀
---
## Programming Fundamental 

### 1. **Function**

**Theory:**  
A function is a block of code that performs a specific task. It helps in code reusability and modularity.

**Syntax:**
```cpp
returnType functionName(parameters) {
    // code
}
```

**Example:**
```cpp
#include<iostream>
using namespace std;

void greet() {
    cout << "Hello, welcome to C++!" << endl;
}

int main() {
    greet(); // Function call
    return 0;
}
```

**Explanation:**  
The `greet()` function is defined once and called in `main()` to print a greeting.

---

### 2. **Arrays**

**Theory:**  
An array is a collection of elements of the same data type stored in contiguous memory locations.

**Example:**
```cpp
#include<iostream>
using namespace std;

int main() {
    int numbers[5] = {1, 2, 3, 4, 5};

    for(int i = 0; i < 5; i++) {
        cout << numbers[i] << " ";
    }

    return 0;
}
```

**Explanation:**  
We create an integer array of size 5 and use a loop to print its values.

---

### 3. **Structures**

**Theory:**  
A structure is a user-defined data type that allows grouping of variables of different types.

**Example:**
```cpp
#include<iostream>
using namespace std;

struct Student {
    int id;
    string name;
};

int main() {
    Student s1 = {1, "John"};
    cout << "ID: " << s1.id << ", Name: " << s1.name << endl;

    return 0;
}
```

**Explanation:**  
The structure `Student` contains two data members. We create an object `s1` and access its members using the dot `.` operator.

---

### 4. **Pointers**

**Theory:**  
A pointer is a variable that stores the address of another variable.

**Example:**
```cpp
#include<iostream>
using namespace std;

int main() {
    int x = 10;
    int* ptr = &x;

    cout << "Value: " << x << endl;
    cout << "Address: " << ptr << endl;
    cout << "Value using pointer: " << *ptr << endl;

    return 0;
}
```

**Explanation:**  
`ptr` holds the address of `x`. `*ptr` gives the value stored at the address, which is `10`.

---

### 5. **Loops**

We will now cover different types of loops.

---

#### 5.1 **For Loop**

**Theory:**  
Executes a block of code a known number of times.

**Example:**
```cpp
#include<iostream>
using namespace std;

int main() {
    for(int i = 1; i <= 5; i++) {
        cout << "Count: " << i << endl;
    }

    return 0;
}
```

**Explanation:**  
The `for` loop runs from 1 to 5 and prints each value.

---

#### 5.2 **While Loop**

**Theory:**  
Executes code while a condition is true.

**Example:**
```cpp
#include<iostream>
using namespace std;

int main() {
    int i = 1;
    while(i <= 5) {
        cout << "Count: " << i << endl;
        i++;
    }

    return 0;
}
```

**Explanation:**  
As long as `i` is less than or equal to 5, the loop continues.

---

#### 5.3 **Do While Loop**

**Theory:**  
Executes code at least once, then repeats while condition is true.

**Example:**
```cpp
#include<iostream>
using namespace std;

int main() {
    int i = 1;
    do {
        cout << "Count: " << i << endl;
        i++;
    } while(i <= 5);

    return 0;
}
```

**Explanation:**  
Even if the condition is false initially, the block executes at least once.

---


---

## **2. OOP Introduction**

**Theory:**  
OOP stands for **Object-Oriented Programming**, a programming paradigm that uses "objects" to design applications. It is based on four main principles:

- **Encapsulation**: Wrapping data and functions together.
- **Abstraction**: Showing only essential features.
- **Inheritance**: Acquiring properties from another class.
- **Polymorphism**: Using the same function name in different forms.

---

### **1. Class**

**Theory:**  
A **class** is a user-defined blueprint or prototype for creating objects. It groups data members and member functions.

**Syntax:**
```cpp
class ClassName {
    // data members
    // member functions
};
```

**Example:**
```cpp
#include<iostream>
using namespace std;

class Car {
    // Data members and member functions will go here
};
```

**Explanation:**  
This is just a basic class declaration for `Car`.

---

### **2. Object**

**Theory:**  
An **object** is an instance of a class. It is used to access the data and functions defined in the class.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Car {
public:
    void startEngine() {
        cout << "Engine started!" << endl;
    }
};

int main() {
    Car myCar;         // Creating an object
    myCar.startEngine();  // Accessing function using object
    return 0;
}
```

**Explanation:**  
`myCar` is an object of the class `Car`. We use the dot `.` operator to access `startEngine()`.

---

### **3. Data Members**

**Theory:**  
**Data Members** are variables defined inside a class that hold the properties/attributes of an object.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Car {
public:
    string brand;
    int speed;
};

int main() {
    Car myCar;
    myCar.brand = "Toyota";
    myCar.speed = 120;

    cout << "Brand: " << myCar.brand << ", Speed: " << myCar.speed << " km/h" << endl;
    return 0;
}
```

**Explanation:**  
Here, `brand` and `speed` are data members of the class `Car`, and we assign values using the object.

---

### **4. Member Functions**

**Theory:**  
**Member Functions** are functions defined inside a class to operate on its data members.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Car {
public:
    string brand;
    int speed;

    void showDetails() {
        cout << "Brand: " << brand << ", Speed: " << speed << " km/h" << endl;
    }
};

int main() {
    Car myCar;
    myCar.brand = "Honda";
    myCar.speed = 100;

    myCar.showDetails();  // Calling member function
    return 0;
}
```

**Explanation:**  
The `showDetails()` function is a member of `Car` and is used to print the brand and speed of the object.

---

## **5. Constructor**

**Theory:**  
A **constructor** is a special member function that is automatically called when an object is created. It is used to initialize objects.

- Constructor has the same name as the class.
- It has no return type (not even `void`).
- Can be **default**, **parameterized**, or **copy** constructor.

---

### **6. Default Constructor**

**Theory:**  
A **default constructor** is a constructor that takes **no parameters**. If you don’t write any constructor, C++ provides a default one automatically.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Student {
public:
    string name;
    int age;

    // Default constructor
    Student() {
        name = "Unknown";
        age = 0;
    }

    void showInfo() {
        cout << "Name: " << name << ", Age: " << age << endl;
    }
};

int main() {
    Student s1;  // Default constructor is called automatically
    s1.showInfo();
    return 0;
}
```

**Explanation:**  
When the object `s1` is created, the default constructor runs and assigns default values to `name` and `age`.

---

### **6. Parameterized Constructor**

**Theory:**  
A **parameterized constructor** takes arguments to initialize the object with custom values during creation.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Student {
public:
    string name;
    int age;

    // Parameterized constructor
    Student(string n, int a) {
        name = n;
        age = a;
    }

    void showInfo() {
        cout << "Name: " << name << ", Age: " << age << endl;
    }
};

int main() {
    Student s1("Alice", 20);  // Parameters passed to constructor
    s1.showInfo();
    return 0;
}
```

**Explanation:**  
When `s1` is created, the values `"Alice"` and `20` are passed to the constructor, initializing the object directly.

---

### **7. Non-Parameterized Constructor (a.k.a Default Constructor)**

**Theory:**  
A **non-parameterized constructor** is a constructor **that takes no arguments**. It is typically used to initialize data members with fixed default values.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Book {
public:
    string title;
    int pages;

    // Non-parameterized (default) constructor
    Book() {
        title = "No Title";
        pages = 0;
    }

    void display() {
        cout << "Title: " << title << ", Pages: " << pages << endl;
    }
};

int main() {
    Book b1;   // Calls the non-parameterized constructor
    b1.display();
    return 0;
}
```

**Explanation:**  
When we create the object `b1`, the constructor runs **automatically** and assigns `"No Title"` to `title` and `0` to `pages`.  
No arguments are passed — that's why it's **non-parameterized**.

---

### **8. Parameterized Constructor** (Recap)

**Theory:**  
Used to initialize objects with custom values when they’re created.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Employee {
public:
    string name;
    int salary;

    // Parameterized constructor
    Employee(string n, int s) {
        name = n;
        salary = s;
    }

    void showDetails() {
        cout << "Name: " << name << ", Salary: " << salary << endl;
    }
};

int main() {
    Employee e1("John", 50000);
    e1.showDetails();
    return 0;
}
```

**Explanation:**  
Constructor takes `name` and `salary` to initialize the object directly.

---

### **9. Destructor**

**Theory:**  
A **destructor** is a special function that is called **automatically** when an object goes out of scope. It is used to release resources.

- Name is the same as the class but with a `~` (tilde) symbol.
- It has no return type and no parameters.
- Each class can have only **one destructor**.

**Example:**
```cpp
#include<iostream>
using namespace std;

class File {
public:
    File() {
        cout << "File opened." << endl;
    }

    ~File() {
        cout << "File closed (Destructor called)." << endl;
    }
};

int main() {
    File f1;
    return 0;
}
```

**Explanation:**  
When the object `f1` is created, the constructor is called. When `main()` ends, the destructor is automatically triggered.

---

### **10. Practice Task**

**Task:**  
Create a class `Product` with `id`, `name`, and `price`. Use a parameterized constructor to initialize, a method to display, and a destructor to clean up.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Product {
public:
    int id;
    string name;
    float price;

    Product(int i, string n, float p) {
        id = i;
        name = n;
        price = p;
    }

    void display() {
        cout << "ID: " << id << ", Name: " << name << ", Price: $" << price << endl;
    }

    ~Product() {
        cout << "Product " << name << " removed from memory." << endl;
    }
};

int main() {
    Product p1(101, "Laptop", 75000.5);
    p1.display();
    return 0;
}
```

---

### **11. Passing Object into Function**

You can pass an object to a function **by value** or **by reference**.

---

### **11.1 Passing Object by Value**

**Theory:**  
A **copy** of the object is passed. Changes inside the function **don’t affect** the original object.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Box {
public:
    int length;

    Box(int l) {
        length = l;
    }

    void display() {
        cout << "Length: " << length << endl;
    }
};

void modify(Box b) {
    b.length = 50;  // Only modifies the copy
}

int main() {
    Box b1(20);
    modify(b1);
    b1.display();  // Still shows 20
    return 0;
}
```

**Explanation:**  
The object `b1` is passed **by value**, so changes in `modify()` don’t affect `b1`.

---

### **11.2 Passing Object by Reference**

**Theory:**  
A **reference** (alias) of the object is passed. Changes inside the function **affect the original object**.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Box {
public:
    int length;

    Box(int l) {
        length = l;
    }

    void display() {
        cout << "Length: " << length << endl;
    }
};

void modify(Box &b) {
    b.length = 50;  // Modifies original
}

int main() {
    Box b1(20);
    modify(b1);
    b1.display();  // Now shows 50
    return 0;
}
```

---

### **12. Friend Function**

**Theory:**  
A **friend function** is not a member of the class but has access to its private/protected members.

- Declared using `friend` keyword inside the class.
- Defined like a regular function.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Account {
private:
    int balance;

public:
    Account(int b) {
        balance = b;
    }

    // Friend function
    friend void showBalance(Account a);
};

void showBalance(Account a) {
    cout << "Balance: $" << a.balance << endl;  // Accessing private member
}

int main() {
    Account acc(1000);
    showBalance(acc);
    return 0;
}
```

**Explanation:**  
`showBalance()` can access `balance` even though it is private because it's declared as a friend.

---

### **13. Association**

**Theory:**  
Association represents a **"uses-a"** relationship between two classes. It is a loose connection where one class uses another. Both can exist independently.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Teacher {
public:
    string name;
    Teacher(string n) { name = n; }
};

class Subject {
public:
    string subjectName;
    void assignTeacher(Teacher t) {
        cout << t.name << " teaches " << subjectName << endl;
    }
};

int main() {
    Teacher t1("Mr. Ali");
    Subject s1;
    s1.subjectName = "Mathematics";
    s1.assignTeacher(t1);
    return 0;
}
```

**Explanation:**  
`Subject` uses `Teacher`, but they are not dependent on each other for existence.

---

### **14. Aggregation**

**Theory:**  
Aggregation is a **"has-a"** relationship, where one class contains another class **as a part**, but the part can still exist **independently**. It’s a weak form of containment.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Engine {
public:
    string type;
    Engine(string t) { type = t; }
};

class Car {
public:
    string model;
    Engine *engine;

    Car(string m, Engine *e) {
        model = m;
        engine = e;
    }

    void showDetails() {
        cout << model << " has " << engine->type << " engine." << endl;
    }
};

int main() {
    Engine e1("Petrol");
    Car c1("Toyota", &e1);
    c1.showDetails();
    return 0;
}
```

**Explanation:**  
`Car` has an `Engine`, but `Engine` can live on its own too.

---

### **15. Composition**

**Theory:**  
Composition is a strong **"has-a"** relationship. The contained object **cannot exist independently** of the container. If the container is destroyed, so is the part.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Heart {
public:
    Heart() {
        cout << "Heart created." << endl;
    }
    ~Heart() {
        cout << "Heart destroyed." << endl;
    }
};

class Human {
private:
    Heart heart;  // Strong relationship

public:
    Human() {
        cout << "Human created." << endl;
    }
    ~Human() {
        cout << "Human destroyed." << endl;
    }
};

int main() {
    Human h1;
    return 0;
}
```

**Explanation:**  
When `Human` is destroyed, `Heart` is also destroyed. This is **composition**.

---

### **16. Inheritance**

**Theory:**  
Inheritance is an **"is-a"** relationship where one class (child/derived) **inherits** properties and behaviors from another class (base/parent).

**Example:**
```cpp
#include<iostream>
using namespace std;

class Animal {
public:
    void speak() {
        cout << "Animal speaks" << endl;
    }
};

class Dog : public Animal {
public:
    void bark() {
        cout << "Dog barks" << endl;
    }
};

int main() {
    Dog d1;
    d1.speak();  // From base class
    d1.bark();   // From derived class
    return 0;
}
```

**Explanation:**  
`Dog` **inherits** from `Animal`. So it can access both its own and the parent class’s functions.

---

### **17. Object’s Array**

**Theory:**  
An array of objects is simply a collection of multiple instances of a class stored in array format.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Student {
public:
    string name;
    int age;

    void setData(string n, int a) {
        name = n;
        age = a;
    }

    void display() {
        cout << "Name: " << name << ", Age: " << age << endl;
    }
};

int main() {
    Student students[3];

    students[0].setData("Ali", 18);
    students[1].setData("Sara", 19);
    students[2].setData("John", 17);

    for (int i = 0; i < 3; i++) {
        students[i].display();
    }

    return 0;
}
```

**Explanation:**  
We created an array of 3 `Student` objects and accessed each one using a loop.

---

### **18. Single Inheritance**

**Theory:**  
A single derived class inherits from one base class.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Animal {
public:
    void eat() {
        cout << "Animal eats food." << endl;
    }
};

class Dog : public Animal {
public:
    void bark() {
        cout << "Dog barks." << endl;
    }
};

int main() {
    Dog d;
    d.eat();   // Inherited from Animal
    d.bark();  // Own method
    return 0;
}
```

**Explanation:**  
`Dog` inherits from `Animal`. This is **single inheritance**.

---

### **19. Multiple Inheritance**

**Theory:**  
A class inherits from **more than one base class**.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Person {
public:
    void showName() {
        cout << "I am a person." << endl;
    }
};

class Worker {
public:
    void showJob() {
        cout << "I work in an office." << endl;
    }
};

class Engineer : public Person, public Worker {
};

int main() {
    Engineer e;
    e.showName();
    e.showJob();
    return 0;
}
```

**Explanation:**  
`Engineer` inherits from both `Person` and `Worker`. This is **multiple inheritance**.

---

### **20. Multilevel Inheritance**

**Theory:**  
A class is derived from a class which is already derived from another class.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Grandparent {
public:
    void speak() {
        cout << "I am a grandparent." << endl;
    }
};

class Parent : public Grandparent {
public:
    void work() {
        cout << "I am a parent." << endl;
    }
};

class Child : public Parent {
public:
    void play() {
        cout << "I am a child." << endl;
    }
};

int main() {
    Child c;
    c.speak();
    c.work();
    c.play();
    return 0;
}
```

**Explanation:**  
Inheritance moves in levels: `Grandparent -> Parent -> Child`.

---

### **21. Hierarchical Inheritance**

**Theory:**  
**Multiple classes** are derived from a **single base class**.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Vehicle {
public:
    void start() {
        cout << "Vehicle started." << endl;
    }
};

class Car : public Vehicle {
public:
    void drive() {
        cout << "Car is driving." << endl;
    }
};

class Bike : public Vehicle {
public:
    void ride() {
        cout << "Bike is riding." << endl;
    }
};

int main() {
    Car c;
    Bike b;

    c.start(); c.drive();
    b.start(); b.ride();

    return 0;
}
```

**Explanation:**  
Both `Car` and `Bike` are derived from `Vehicle`.

---

### **22. Hybrid Inheritance**

**Theory:**  
A **combination of two or more types** of inheritance, e.g., multilevel + multiple, etc.

**Example:**
```cpp
#include<iostream>
using namespace std;

class A {
public:
    void showA() {
        cout << "Class A" << endl;
    }
};

class B : public A {
public:
    void showB() {
        cout << "Class B (from A)" << endl;
    }
};

class C {
public:
    void showC() {
        cout << "Class C" << endl;
    }
};

class D : public B, public C {
public:
    void showD() {
        cout << "Class D (from B and C)" << endl;
    }
};

int main() {
    D obj;
    obj.showA();
    obj.showB();
    obj.showC();
    obj.showD();
    return 0;
}
```

**Explanation:**  
`D` inherits from both `B` and `C`. `B` itself inherits from `A`. So it's **hybrid**: multilevel + multiple.

---

### **23. Encapsulation**

**Theory:**  
Encapsulation is the process of **wrapping data (variables) and code (methods)** together as a single unit. Data is kept private and accessed only through public methods.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Student {
private:
    string name;
    int age;

public:
    void setDetails(string n, int a) {
        name = n;
        age = a;
    }

    void getDetails() {
        cout << "Name: " << name << ", Age: " << age << endl;
    }
};

int main() {
    Student s;
    s.setDetails("Ali", 18);
    s.getDetails();
    return 0;
}
```

**Explanation:**  
Data members are private. You can only access them using public methods. That’s **encapsulation**.

---

### **24. Abstraction**

**Theory:**  
Abstraction hides internal details and only shows **essential features**. It’s implemented using **classes, access specifiers, and abstract classes/interfaces**.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Vehicle {
public:
    void start() {
        cout << "Vehicle starting..." << endl;
    }
};

int main() {
    Vehicle v;
    v.start();  // We don’t know *how* it starts, just that it does
    return 0;
}
```

**Explanation:**  
You use `start()` but don’t know the internal code — that’s **abstraction**.

---

### **25. Polymorphism**

**Theory:**  
Polymorphism means **“many forms”** — the same function behaves differently in different situations.

### **Types of Polymorphism:**
- **Compile-time (Static) Polymorphism**
- **Runtime (Dynamic) Polymorphism**

---

### **26. Compile-Time Polymorphism (Function Overloading)**

**Theory:**  
Functions with **same name but different parameters**.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Print {
public:
    void show(int x) {
        cout << "Integer: " << x << endl;
    }

    void show(string s) {
        cout << "String: " << s << endl;
    }
};

int main() {
    Print p;
    p.show(5);
    p.show("Hello");
    return 0;
}
```

**Explanation:**  
Same function name, different types/number of arguments.

---

### **27. Runtime Polymorphism (Function Overriding + Virtual Functions)**

**Theory:**  
Function defined in base class is **overridden** in derived class. The base class function is made **virtual** to allow dynamic dispatch.

**Example:**
```cpp
#include<iostream>
using namespace std;

class Animal {
public:
    virtual void sound() {
        cout << "Animal makes sound" << endl;
    }
};

class Dog : public Animal {
public:
    void sound() override {
        cout << "Dog barks" << endl;
    }
};

int main() {
    Animal* a;
    Dog d;
    a = &d;
    a->sound();  // Dog's sound() is called due to virtual function
    return 0;
}
```

**Explanation:**  
Although `a` is of type `Animal*`, the **Dog’s version** of `sound()` is executed at runtime. That’s **runtime polymorphism**.

---

# **Programming Fundamentals (PF) + Object-Oriented Programming (OOP) Summary Sheet**

---

### **1. Functions**
- Reusable block of code.
- Syntax:
```cpp
return_type function_name(parameters) {
    // code
}
```

---

### **2. Arrays**
- Fixed-size collection of similar data types.
```cpp
int arr[5] = {1, 2, 3, 4, 5};
```

---

### **3. Structures**
- Group different data types together.
```cpp
struct Student {
    string name;
    int age;
};
```

---

### **4. Pointers**
- Store memory address of another variable.
```cpp
int x = 10;
int* p = &x;
```

---

### **5. Loops**
- Repeat a block of code.

**For Loop:**
```cpp
for (int i = 0; i < 5; i++) {}
```

**While Loop:**
```cpp
int i = 0;
while (i < 5) { i++; }
```

**Do While Loop:**
```cpp
int i = 0;
do { i++; } while (i < 5);
```

---

## **OOP Concepts**

### **1. Class and Object**
- Class: Blueprint
- Object: Instance
```cpp
class Car {
public:
    void drive() {
        cout << "Driving";
    }
};
Car c;
c.drive();
```

---

### **2. Data Members & Member Functions**
- Data members: variables
- Member functions: functions inside class

---

### **3. Constructor**
- Automatically called when object is created
- Default:
```cpp
class A {
public:
    A() { cout << "Default Constructor"; }
};
```
- Parameterized:
```cpp
A(int x) { cout << x; }
```

---

### **4. Destructor**
- Called when object is destroyed.
```cpp
~A() { cout << "Destroyed"; }
```

---

### **5. Passing Object to Function**
- By value: creates copy
- By reference: uses original

---

### **6. Friend Function**
- Not part of class but can access private members
```cpp
friend void show(A);
```

---

## **Class Relationships**

### **Association:** loosely connected
### **Aggregation:** has-a (can exist independently)
### **Composition:** has-a (cannot exist independently)

---

### **Inheritance**
- Reuse parent class features

**Single, Multiple, Multilevel, Hierarchical, Hybrid**

---

### **Object Arrays**
```cpp
Student arr[3];
```

---

### **Encapsulation**
- Hide data using private members and access via public functions

---

### **Abstraction**
- Show only essential details, hide internal complexity

---

### **Polymorphism**
- Many forms

**Compile-Time:**
- Function Overloading

**Runtime:**
- Function Overriding
- Virtual Functions

```cpp
virtual void display();
```


---

## License & Copyright

**© 2025 𝔎𝔶𝔦𝔪. All rights reserved.**  
This project is owned by Kyim Shia. Unauthorized use, distribution, or modification of any part of this code or documentation is prohibited.

For licensing inquiries, feel free to reach out to:  
📧 [Contact Us!](mailto:Kyimshia@outlook.com)

---

**Note:**  
This guide is designed to make learning C++ both informative and enjoyable. Keep coding and exploring new possibilities in the world of programming! 🌟

---
