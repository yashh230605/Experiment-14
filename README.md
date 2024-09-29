# README.md

## Overview

This repository contains four different C++ programs demonstrating basic object-oriented programming concepts, including inheritance, encapsulation, and polymorphism. Each code snippet represents a distinct scenario where classes are used to model real-world entities.

## Table of Contents

1. [Program 1: University and Department](#program-1-university-and-department)
2. [Program 2: Vehicle and Specifications](#program-2-vehicle-and-specifications)
3. [Program 3: Food and Restaurant](#program-3-food-and-restaurant)
4. [Program 4: Jeans and Variants](#program-4-jeans-and-variants)

---

## Program 1: University and Department

### Aim
To demonstrate single inheritance by creating a base class `Uni` and a derived class `Dep`.

### Theory
- **Class `Uni`**: Represents a university with a discipline method.
- **Class `Dep`**: Inherits from `Uni` and represents a specific department.

### Code
```cpp
#include <iostream>
#include <string>
using namespace std;

class Uni {
    public:
    string uni = "Symbiosis: ";
    void discipline(){
        cout<<"Engineering"<<endl;
    }
};
class Dep: public Uni {
    public:
    string dept="Electronics & Communication";
};

int main(){
    Dep u1;
    u1.discipline();
    cout<<u1.uni+" "+u1.dept;
}
```

### Output
```
Engineering
Symbiosis: Electronics & Communication
```

---

## Program 2: Vehicle and Specifications

### Aim
To demonstrate multiple inheritance using two parent classes, `Vehicle` and `Specs`, with a derived class `Car`.

### Theory
- **Class `Vehicle`**: Represents a vehicle with a company name and type method.
- **Class `Specs`**: Provides specifications such as mileage and color.
- **Class `Car`**: Inherits from both `Vehicle` and `Specs`.

### Code
```cpp
#include <iostream>
#include <string>
using namespace std;

class Vehicle {
    public:string company = "Ford";
    void type() {
        cout << "Mustang" << endl;
    }
};

class Specs {
public:
    string mileage = "8 km/l";
    
    void colour() {
        cout << "Grey" << endl;
    }
};

class Car : public Vehicle, public Specs {
public:
    string seater = "4 seater";
};

int main() {
    Car f2;
    
    f2.colour(); 
    cout << f2.company << endl; 
    f2.type(); 
    cout << "(" << f2.seater << ")" << endl; 
    cout << "MILEAGE: " << f2.mileage << endl; 

    return 0;
}
```

### Output
```
Grey
Ford
Mustang
(4 seater)
MILEAGE: 8 km/l
```

---

## Program 3: Food and Restaurant

### Aim
To illustrate hierarchical inheritance with a base class `Food` and derived classes `Dish` and `Restaurant`.

### Theory
- **Class `Food`**: Represents a cuisine with a type method.
- **Class `Dish`**: Inherits from `Food` and adds a specific dish.
- **Class `Restaurant`**: Inherits from `Dish` and represents a restaurant name.

### Code
```cpp
#include <iostream>
#include <string>
using namespace std;

class Food {
public:
    string cuisine = "Indian";
    
    void type() {
        cout << "Asian" << endl;
    }
};

class Dish : public Food {
public:
    string dish = "Biryani";
};

class Restaurant : public Dish {
public:
    string name = "Spice Kitchen";
};

int main() {
    Restaurant f3;
    
    f3.type();  
    cout << f3.cuisine << ": " << f3.dish << endl;   
    cout << "Restaurant: " << f3.name << endl;  

    return 0;
}
```

### Output
```
Asian
Indian: Biryani
Restaurant: Spice Kitchen
```

---

## Program 4: Jeans and Variants

### Aim
To demonstrate multiple inheritance with a base class `Jeans` and various derived classes for different types of jeans.

### Theory
- **Class `Jeans`**: Contains different types of jeans and a method for brand.
- **Class `Bootcut`, `WL`, `Skinny`**: Each represents a specific type of jeans, inheriting from `Jeans`.

### Code
```cpp
#include <iostream>
#include <string>
using namespace std;

class Jeans {
    public:
    string type[3]= {"Bootcut", "Wide Leg", "Skinny"};
    void brand(){
        cout<<"H&M - &Denim"<<endl;
    }
};

class Bootcut: public Jeans {
    public:
    string color="Dark Blue";
};

class WL: public Jeans {
    public:
    string color="Black";
};

class Skinny: public Jeans {
    public:
    string color="Grey";
};

int main(){
    Bootcut j1;
    cout<<endl;
    j1.brand();
    cout<<j1.type[0]<<": "<<j1.color<<endl;

    WL j2;
    cout<<endl;
    j2.brand();
    cout<<j2.type[1]<<": "<<j2.color<<endl;

    Skinny j3;
    cout<<endl;
    j3.brand();
    cout<<j3.type[2]<<": "<<j3.color<<endl;
}
```

### Output
```
H&M - &Denim
Bootcut: Dark Blue

H&M - &Denim
Wide Leg: Black

H&M - &Denim
Skinny: Grey
```

---

## Conclusion

These four C++ programs illustrate fundamental principles of object-oriented programming. They serve as a practical introduction to classes, inheritance, and the relationships between different types of objects. Feel free to modify and expand on these examples as you explore C++ programming!# Experiment-14
