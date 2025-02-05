# Method Overriding in Java

## Overview
This Java program demonstrates **method overriding**, where a subclass (`B`) redefines a method (`show()`) that is already present in the parent class (`A`).  

## How It Works

1. **Class `A` (Parent Class):**  
   - Contains two integer variables: `i` and `j`.  
   - Constructor initializes `i` and `j`.  
   - Method `show()` prints `i` and `j`.  

2. **Class `B` (Child Class, Extends `A`):**  
   - Inherits variables `i` and `j` from `A`.  
   - Adds a new variable `k`.  
   - Overrides the `show()` method to print only `k`, instead of `i` and `j`.  

3. **Main Class (`methodoverloading`):**  
   - Creates an object of class `B`.  
   - Calls `show()`, but since `B` has overridden `show()`, only `k` is printed.  

## Code

```java
// Parent class
class A {
    int i, j;

    // Constructor to initialize i and j
    A(int a, int b) {
        i = a;
        j = b;
    }

    // Method to display i and j
    void show() {
        System.out.println("i and j : " + i + " " + j);
    }
}

// Child class extending A
class B extends A {
    int k;

    // Constructor to initialize i, j (via super) and k
    B(int a, int b, int c) {
        super(a, b); // Calls constructor of A
        k = c;
    }

    // Overriding show() method
    void show() {
        System.out.println("k : " + k);
    }
}

// Main class
public class methodoverloading {
    public static void main(String[] args) {
        B subOb = new B(1, 2, 3); // Creating object of B
        subOb.show(); // Calls overridden show() method in B
    }
}





This **README.md** explains everything in simple terms. Let me know if you want any changes! 🚀
