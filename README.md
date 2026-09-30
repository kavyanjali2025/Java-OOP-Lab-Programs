# Java OOP Lab Programs 

[Program-1 Write a class with four methods add, subtract, multiply and divide and test all the methods in the main](#assi-1)

[Program-2 Write a class for addition of two distances where each distance is given in m, cm and mm](#assi-2)

[Program-3 Write a class for addition of two times where each time is given in hr, min and sec](#assi-3)

[Program-4 Write a class to reverse an 1D array with necessary methods](#assi-4)

[Program‑5 
Write a class to transpose a 2D array (matrix) with necessary methods.
Test the transpose method in the main function by displaying the original matrix and its transposed form.](#assi-5)

[Program‑6  
Write a class in Java to perform matrix multiplication with necessary methods.
The program should:
Accept two matrices from the user.
Check if multiplication is possible (columns of the first matrix equal rows of the second).
Multiply the matrices if valid.
Display the result and the execution time.](#assi-6)

[Program‑7 Write a class to compute the sum of elements in a 1D array with necessary methods.](#pro-7)

[Program‑8  
Write a class to compute the sum of the primary and secondary diagonals of a square matrix with necessary methods.
The program should:
Accept the size and elements of the matrix from the user.
Implement methods to calculate the sum of the primary diagonal and the secondary diagonal.
Display both sums and the total of the diagonals in the main method.](#assi-8)

[Program‑9 Collect any 5 codes in c language like factorial, armstrong, palindrome etc and convert them in object oriented in java and test the result in the main](#assi-9)

[Program‑10  
Write a class in Java to demonstrate the use of the this keyword.
The program should:
Accept values for object fields using a constructor.
Use this to distinguish between instance variables and parameters.
Display the object details in the main method.](#assi-10)

[Program‑11  
Write a Java program to demonstrate the use of the super keyword.
The program should:
Create a base class with fields and methods.
Create a derived class that uses super to access the parent class’s constructor and methods.
Display the results in the main method.](#assi-11)

[Program-12 
Write a Java program to demonstrate multi‑level inheritance with three classes (TestA, TestB, TestC). 
Each class should define its own method, and in main create objects of all three classes to call their methods.](#assi-12)

[Program‑13  
Write a Java program to demonstrate method overriding.
Create a parent class with a method, and two child classes that override the same method. Call the overridden methods using a parent class reference to show polymorphism.](#assi-13)

[Program-14
Create a Student Registration Form using Java and store the entered data in a database using JDBC (Java Database Connectivity).](#assi-14)

[Program-15
Create a GUI using JFrame that contains 10 buttons, each with different functionalities or structure.](#assi-15)

[Program-16
Write a Java program using ArrayList to show that duplicates are allowed and retrieve the first element.](#assi-16)

[Program-17
Write a Java program to demonstrate the commonly used methods of the ArrayList class, including:
Adding elements at the end and at a specific index
Accessing elements by index and finding their position
Updating elements using set()
Removing elements by index, by value, and clearing the list
Checking size, emptiness, and whether an element exists
Traversing the list using forEach and Iterator](#assi-17)

[Program‑18  
Write a Java program using LinkedList to demonstrate different ways of adding elements, including:
add(E e) → add at end
add(int index, E e) → insert at index
addFirst(E e) → add at beginning
addLast(E e) → add at end
offer(E e) → add in queue style
offerFirst(E e) → add at front
offerLast(E e) → add at en](#assi-18)

[Program‑19  
Write a Java program using LinkedList to demonstrate different ways of accessing elements, including:
get(int index) → get element at a specific position
getFirst() → get the first element
getLast() → get the last element
peek() → get the head element without removing it
peekFirst() → get the first element
peekLast() → get the last element](#assi-19)

[Program‑20 
Write a Java program using LinkedList to demonstrate how to replace an element at a specific index using the set(int index, E e) method.](#aassi-20)

[Program‑21
Write a Java program using LinkedList to demonstrate different ways of removing elements, including:
remove() → remove first element
remove(int index) → remove by index
remove(Object o) → remove by value
removeFirst() → remove first element
removeLast() → remove last element
poll() → remove head element
pollFirst() → remove first element
pollLast() → remove last element
clear() → remove all elements](#assi-21)

[Program-22
Write a Java program to demonstrate Stack operations using the Collection Framework, including push, pop, peek, and checking whether the stack is empty.
](#assi-22)

[Program-23
Write a Java program to implement HashMap and perform operations such as inserting key-value pairs, retrieving values using keys, removing entries, and iterating through the map.](##assi-23)

[Program-24
Write a Java program to demonstrate TreeMap by inserting elements, displaying them in sorted order, searching for a key, and removing elements.](#assi-24)

[Program-25
Write a Java program to implement a Stack using arrays and perform operations such as push, pop, displaying elements, and handling stack overflow and underflow conditions](#assi-25)

[Program-26 Implement File transfer/copy in Java using: 1.Byte Stream 2.Character Stream ](#assi-26)

[Program-27 Create a package pkg1 containing a class PkgTest with a method fun() that prints a message and creates an object of the same class. Then, write a separate class PkgMain (outside the package) to import pkg1.PkgTest and call the fun() method.](#assi-27)


## assi-1
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

/**
 *
 * @author kavya
 */
public class Test_01 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Calculator calc = new Calculator();
        System.out.println("Add: " + calc.add(10, 5));
        System.out.println("Subtract: " + calc.subtract(10, 5));
        System.out.println("Multiply: " + calc.multiply(10, 5));
        System.out.println("Divide: " + calc.divide(10, 5));
    }
}
class Calculator {
    public int add(int a, int b) { return a + b; }
    public int subtract(int a, int b) { return a - b; }
    public int multiply(int a, int b) { return a * b; }
    public double divide(int a, int b) {
        if (b == 0) return 0;
        return (double) a / b;
    }
}

```
<img width="221" height="87" alt="image" src="https://github.com/user-attachments/assets/0fcd3c4f-cbbc-4f6d-8239-f4c60e920c0d" />


## assi-2
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

/**
 *
 * @author kavya
 */
import java.util.Scanner;
public class Distance_add {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Distance o1= new Distance();
        Distance o2= new Distance();
        Distance o3= new Distance();
        o1.input();
        o2.input();
        o3.add(o1,o2);
        o3.output();
    }
    
}

// Distance.java - separate class for distance operations
class Distance {
    int m, cm, mm; // Declare variables 
    // Method to take input 
    void input(){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter meters: ");
        m = sc.nextInt(); 
        System.out.print("Enter centimeters: "); 
        cm = sc.nextInt(); 
        System.out.print("Enter millimeters: ");
        mm = sc.nextInt(); }
    
    void add(Distance d1, Distance d2){
        //they are just placeholders for the actual objects you pass in.
        m = d1.m + d2.m;
        //d1.m really means “use the m value from o1.”
        cm = d1.cm + d2.cm; 
        mm = d1.mm + d2.mm; 
        // Normalize mm to cm 
        cm += mm / 10;
        mm = mm % 10; 
        // Normalize cm to m
        m += cm / 100; 
        cm = cm % 100;
    }
    void output(){
        System.out.println("Total Distance: " + m + "m " + cm + "cm " + mm + "mm");
    } 
}
//o1, o2, and o3 are variables that hold references to Distance objects in memory.
//Each one is a separate Distance object with its own m, cm, and mm values.

```
<img width="220" height="133" alt="image" src="https://github.com/user-attachments/assets/5990689e-801b-4d2f-b1cc-328bdd8663c1" />


## assi-3
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

/**
 *
 * @author kavya
 */
import java.util.Scanner;
public class Time_add {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Scanner sc = new Scanner(System.in);

        // Input first time
        System.out.print("Enter first time (hh mm ss): ");
        int h1 = sc.nextInt();
        int m1 = sc.nextInt();
        int s1 = sc.nextInt();

        // Input second time
        System.out.print("Enter second time (hh mm ss): ");
        int h2 = sc.nextInt();
        int m2 = sc.nextInt();
        int s2 = sc.nextInt();

        // Add seconds
        int totalSeconds = s1 + s2;
        int carryMinutes = totalSeconds / 60;
        totalSeconds = totalSeconds % 60;

        // Add minutes
        int totalMinutes = m1 + m2 + carryMinutes;
        int carryHours = totalMinutes / 60;
        totalMinutes = totalMinutes % 60;

        // Add hours
        int totalHours = h1 + h2 + carryHours;
        totalHours = totalHours % 24; // wrap around 24-hour format

        // Display result
        System.out.printf("Resultant Time: %02d:%02d:%02d\n", totalHours, totalMinutes, totalSeconds);
    }
}
```
<img width="220" height="118" alt="image" src="https://github.com/user-attachments/assets/7ad905c5-6866-4191-841a-c281c3fce760" />


## assi-4
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

/**
 *
 * @author kavya
 */
import java.util.Scanner;
public class Array_test1 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Array_test o1 = new Array_test();
        o1.input();
        System.out.println("Original Array:");
        o1.outarrorg();
        System.out.println("Reversed Array:");
        o1.rev();
        o1.outarrrev();
    }
    
}

class Array_test{
    int x[];//original array 
    //not doing memory optimize right now
    int rev[];//reverse array
    void input(){
        //can create array in input
        x = new int[5]; // allocate memory
        rev = new int[5]; // allocate memory for reversed array
        Scanner sc= new Scanner(System.in);
        System.out.println("Enter 5 integers:");
        for(int i=0; i<5; i++){
            x[i]=sc.nextInt();
        }    
    }
    // Print original array
    void outarrorg(){
        for(int i=0; i<5; i++){
          System.out.println(x[i]);  
        }
    }
    // Reverse array and print
    void rev(){
        for(int i=0; i<5; i++){
            rev[i] = x[4 - i];
        }
    } 
    void outarrrev(){
       for(int i=0; i<5; i++){
           System.out.println(rev[i]);
       }  
    }
}
```
<img width="236" height="190" alt="image" src="https://github.com/user-attachments/assets/42b8fe44-9cb1-4745-9ed3-9909b65a84b4" />

## assi-5
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

/**
 *
 * @author kavya
 */
import java.util.Scanner;
public class Array_test2 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Transpose o1= new Transpose();
        o1.input();
        o1.transpose();
        o1.output1();
        o1.output2();
    }
    
}


class Transpose{
    int[][] x = new int[2][2];
    int[][] y = new int[2][2];
    void input(){
        Scanner sc= new Scanner(System.in);
        System.out.println("Enter 4 elements of array:");
        for(int i=0; i<2; i++){
            for(int j=0; j<2; j++){
                x[i][j]=sc.nextInt();
            }
        }    
    }    
    void transpose(){
        for(int i=0; i<2; i++){
            for(int j=0; j<2; j++){
                y[j][i]=x[i][j];
            }    
        }
    }
    void output1(){
        System.out.println("Original array: ");
        for(int i=0; i<2; i++){
            for(int j=0; j<2; j++){
                System.out.print(x[i][j]+" ");
            }
            System.out.println(); // new line after each row
        }
    }
    void output2(){
        System.out.println("Transpose array: ");
        for(int i=0; i<2; i++){
            for(int j=0; j<2; j++){
                System.out.print(y[i][j]+ " ");
            } 
            System.out.println(); // new line after each row
        }
    }  
}
```
<img width="226" height="125" alt="image" src="https://github.com/user-attachments/assets/7b17e7c8-c5b1-4957-b63e-36937afa433b" />

## assi-6
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

/**
 *
 * @author kavya
 */
import java.util.Scanner;
public class Array_test3 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter rows of first matrix: ");
        int r1 = sc.nextInt();
        System.out.print("Enter columns of first matrix: ");
        int c1 = sc.nextInt(); 
        System.out.print("Enter rows of 2nd matrix: ");
        int r2 = sc.nextInt();
        System.out.print("Enter columns of 2nd matrix: ");
        int c2 = sc.nextInt(); 
        if (c1 != r2) { 
            System.out.println("Multiplication not possible");
            return; 
        } 
        Array_mul A = new Array_mul(r1, c1); 
        Array_mul B = new Array_mul(r2, c2);
        Array_mul C = new Array_mul(r1, c2); 
        A.input(sc);
        B.input(sc); 
        
        //Start timer
        long start = System.nanoTime();
        // Direct multiplication logic here
        for (int i = 0; i < r1; i++){
            for (int j = 0; j < c2; j++){
                for (int k = 0; k < c1; k++)
                    //loop over k
                    C.data[i][j] += A.data[i][k] * B.data[k][j]; 
            }
        }
        // End timer
        long end = System.nanoTime();
        C.output();
        // Print execution time in milliseconds
        System.out.println("Execution time: " + (end - start) / 1_000_000.0 + " ms");
        //underscore for readability
    }
    
}

class Array_mul{
    //
    int[][] data; 
    int rows, cols; 
    Array_mul(int r, int c) {
        rows = r; cols = c;
        data = new int[r][c]; 
    } 
    void input(Scanner sc) { 
        System.out.println("give matrix elements:");
        for (int i = 0; i < rows; i++){ 
            for (int j = 0; j < cols; j++){ 
                data[i][j] = sc.nextInt();
            }    
            System.out.println();
        }    
    }
    void output() {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) 
                System.out.print(data[i][j] + " "); 
            System.out.println(); 
        } 
    }
}
```
<img width="245" height="206" alt="image" src="https://github.com/user-attachments/assets/a65984cb-75c3-4652-99b0-50a3d54e24e7" />

## pro-7
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

import java.util.Scanner;

/**
 *
 * @author kavya
 */
public class Array_test4 {

    public static void main(String[] args) {
        array_add o1 = new array_add();
        o1.input();
        int total = o1.computeSum();
        // get final sum
        System.out.println("Final sum of array elements = " + total);
    }
}

class array_add {
    int[] x;       // main array
    int[] prefix;  // prefix array

    void input() {
        x = new int[5];       // allocate memory
        prefix = new int[5];  // allocate memory for prefix
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter 5 integers:");
        for (int i = 0; i < 5; i++) {
            x[i] = sc.nextInt();
        }
    }

    int computeSum() { 
        int sum = 0;
        for (int i = 0; i < x.length; i++) {
            sum += x[i];// add each element
        }
        return sum; // return final sum 
    } 
}     
```
<img width="221" height="67" alt="image" src="https://github.com/user-attachments/assets/6cc7986c-8ef1-4b0c-9b28-305475ec7add" />

## assi-8
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_01;

/**
 *
 * @author kavya
 */
import java.util.Scanner;
public class Array_test5 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Scanner sc = new Scanner(System.in);

        // Input matrix size
        System.out.print("Enter size of square matrix (n): ");
        int n = sc.nextInt();

        int[][] matrix = new int[n][n];

        // Input matrix elements
        System.out.println("Enter matrix elements:");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                matrix[i][j] = sc.nextInt();
            }
        }

        // Compute diagonal sums
        int primarySum = 0;   // left-to-right diagonal
        int secondarySum = 0; // right-to-left diagonal

        for (int i = 0; i < n; i++) {
            primarySum += matrix[i][i];           // (i,i)
            secondarySum += matrix[i][n - 1 - i]; // (i, n-1-i)
        }

        // Display results
        System.out.println("Primary diagonal sum = " + primarySum);
        System.out.println("Secondary diagonal sum = " + secondarySum);
        System.out.println("Total of both diagonals = " + (primarySum + secondarySum));
    }
    
}
```
<img width="230" height="115" alt="image" src="https://github.com/user-attachments/assets/8ef225cf-cf04-4ee1-b2ae-55f451e9657c" />

## assi-9 
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_02;

/**
 *
 * @author kavya
 */
public class Test_02 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        OOP_Programs.Factorial f = new OOP_Programs.Factorial();
        System.out.println("Factorial of 5 = " + f.compute(5));

        OOP_Programs.Armstrong a = new OOP_Programs.Armstrong();
        System.out.println("153 is Armstrong? " + a.isArmstrong(153));

        OOP_Programs.Palindrome p = new OOP_Programs.Palindrome();
        System.out.println("121 is Palindrome? " + p.isPalindrome(121));

        OOP_Programs.Prime pr = new OOP_Programs.Prime();
        System.out.println("17 is Prime? " + pr.isPrime(17));

        OOP_Programs.Fibonacci fib = new OOP_Programs.Fibonacci();
        fib.printSeries(10);
    }
    
}
class OOP_Programs {

    // Factorial
    static class Factorial {
        int compute(int n) {
            int fact = 1;
            for (int i = 1; i <= n; i++) fact *= i;
            return fact;
        }
    }

    // Armstrong number
    static class Armstrong {
        boolean isArmstrong(int n) {
            int temp = n, sum = 0;
            while (temp > 0) {
                int d = temp % 10;
                sum += d * d * d;
                temp /= 10;
            }
            return sum == n;
        }
    }

    // Palindrome number
    static class Palindrome {
        boolean isPalindrome(int n) {
            int temp = n, rev = 0;
            while (temp > 0) {
                rev = rev * 10 + temp % 10;
                temp /= 10;
            }
            return rev == n;
        }
    }

    // Prime check
    static class Prime {
        boolean isPrime(int n) {
            if (n <= 1) return false;
            for (int i = 2; i <= Math.sqrt(n); i++) {
                if (n % i == 0) return false;
            }
            return true;
        }
    }

    // Fibonacci series
    static class Fibonacci {
        void printSeries(int terms) {
            int a = 0, b = 1;
            System.out.print("Fibonacci: ");
            for (int i = 0; i < terms; i++) {
                System.out.print(a + " ");
                int next = a + b;
                a = b;
                b = next;
            }
            System.out.println();
        }
    }
}
```
<img width="221" height="107" alt="image" src="https://github.com/user-attachments/assets/f6810bbb-801e-4ab9-954d-ba9ac0cfc8d4" />

## assi-10
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_02;

/**
 *
 * @author kavya
 */

/* NAME: KAVYANJALI BHATT
   ENROLL NO: 240141
   OBJECTIVE: TO UNDERSTAND USE OF This 
*/
public class This_test {

    /**
     * @param args the command line arguments
     */
    String name;
    int roll;

    // Constructor using 'this' keyword
    This_test(String name, int roll) {
        this.name = name;   // 'this' refers to current object
        this.roll = roll;
    }

    void display() {
        System.out.println("Name: " + this.name);
        System.out.println("Roll No: " + this.roll);
    }
    
    public static void main(String[] args) {
        // TODO code application logic here
        This_test s1 = new This_test("Kavya", 101);
        This_test s2 = new This_test("Anjali", 102);

        s1.display();
        s2.display();
    }
    
}
```
<img width="218" height="95" alt="image" src="https://github.com/user-attachments/assets/feeb87f0-167c-43c4-ac91-e216def67f70" />

## assi-11
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_02;

/**
 *
 * @author kavya
 */

/* NAME: KAVYANJALI BHATT
   ENROLL NO: 240141
   OBJECTIVE: TO UNDERSTAND USE OF Super 
*/
// Base class
class Person {
    String name;

    Person(String name) {
        this.name = name;
    }

    void display() {
        System.out.println("Name: " + name);
    }
}

// Derived class using 'super'
class Student extends Person {
    int roll;

    Student(String name, int roll) {
        super(name); // call parent constructor
        this.roll = roll;
    }

    @Override
    void display() {
        super.display(); // call parent method
        System.out.println("Roll No: " + roll);
    }
}

// Driver class
public class Super_test {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Student s1 = new Student("Kavya", 101);
        Student s2 = new Student("Anjali", 102);

        s1.display();
        s2.display();
    }
    
}
```
<img width="244" height="95" alt="image" src="https://github.com/user-attachments/assets/da064827-d666-4202-9a73-c20cb2ef6453" />

## assi-12
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_02;

/**
 *
 * @author kavya
 */

/* NAME: KAVYANJALI BHATT
   ENROLL NO: 240141
   OBJECTIVE: MULTI LEVEL INHERITANCE
*/
public class Inheri_test1 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        System.out.println("MULTI LEVEL INHERITANCE");
        TestA o1= new TestA();
        TestB o2= new TestB();
        TestC o3= new TestC();
        o1.funA();
        o2.funB();
        o3.funC();
    }
    
}
//MULTI  LEVEL INHERITANCE
//every method must declare a return type
class TestA{
    void funA(){
        System.out.println("IN CLASS A");
    }
    
}
class TestB extends TestA{
    void funB(){
        System.out.println("IN CLASS B");
    }
    
}
class TestC extends TestB{
    //all 3 functions will be considered
    void funC(){
        System.out.println("IN CLASS C");
    }
}
```
<img width="222" height="95" alt="image" src="https://github.com/user-attachments/assets/0bb9600f-ed8e-4d35-a3c1-45c75eee99b6" />


## asii-13
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package test_02;

/**
 *
 * @author kavya
 */

/* NAME: KAVYANJALI BHATT
   ENROLL NO: 240141
   OBJECTIVE: HIERARICHAL INHERITANCE
*/
public class Inheri_test2 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        System.out.println("HIERARICHAL INHERITANCE");
        Test_A o1= new Test_A();
        Test_B o2= new Test_B();
        Test_C o3= new Test_C();
        o1.funA();
        o2.funB();
        o3.funC();
    }
    
}

//HIERARICHAL INHERITANCE
class Test_A{
    void funA(){
        System.out.println("IN CLASS A");
    }
    
}
class Test_B extends Test_A{
    void funB(){
        System.out.println("IN CLASS B");
    }
    
}
class Test_C extends Test_A{
    //all 3 functions will be considered
    void funC(){
        System.out.println("IN CLASS C");
    }
}
```
<img width="231" height="100" alt="image" src="https://github.com/user-attachments/assets/ca276acf-8f25-467c-921d-e6fe04909e00" />

## assi-14
```
/*
 * Student Registration Form with JDBC
 * Demonstrates inserting form data into a database
 */

/**
 *
 * @author kavya
 */
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.sql.*;

public class StudentRegistrationForm extends JFrame implements ActionListener {
    // Form fields
    private JTextField nameField, emailField, courseField;
    private JButton submitButton;

    public StudentRegistrationForm() {
        // Frame setup
        setTitle("Student Registration Form");
        setSize(400, 250);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new GridLayout(4, 2));

        // Labels and fields
        add(new JLabel("Name:"));
        nameField = new JTextField();
        add(nameField);

        add(new JLabel("Email:"));
        emailField = new JTextField();
        add(emailField);

        add(new JLabel("Course:"));
        courseField = new JTextField();
        add(courseField);

        // Submit button
        submitButton = new JButton("Register");
        submitButton.addActionListener(this);
        add(submitButton);

        setVisible(true);
    }

    @Override
    public void actionPerformed(ActionEvent e) {
        String name = nameField.getText();
        String email = emailField.getText();
        String course = courseField.getText();

        // JDBC connection
        try {
            // Load driver
            Class.forName("oracle.jdbc.OracleDriver"); // or "com.mysql.cj.jdbc.Driver" for MySQL

            // Connect to DB (update with your DB details)
            Connection con = DriverManager.getConnection(
                "jdbc:oracle:thin:@localhost:1521:xe", "username", "password");

            // Insert query
            String sql = "INSERT INTO students (name, email, course) VALUES (?, ?, ?)";
            PreparedStatement pst = con.prepareStatement(sql);
            pst.setString(1, name);
            pst.setString(2, email);
            pst.setString(3, course);

            int rows = pst.executeUpdate();
            if (rows > 0) {
                JOptionPane.showMessageDialog(this, "Student registered successfully!");
            }

            con.close();
        } catch (Exception ex) {
            JOptionPane.showMessageDialog(this, "Error: " + ex.getMessage());
        }
    }

    public static void main(String[] args) {
        new StudentRegistrationForm();
    }
}
```
<img width="269" height="167" alt="image" src="https://github.com/user-attachments/assets/ae0f56d1-a226-4a64-8fda-fbb3e949a915" />

## assi-15
```
/*
 * GUI with 10 Buttons
 * Demonstrates different functionalities in a single JFrame
 */

/**
 *
 * @author kavya
 */
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class TenButtonsDemo extends JFrame implements ActionListener {
    JButton b1, b2, b3, b4, b5, b6, b7, b8, b9, b10;

    public TenButtonsDemo() {
        setTitle("10 Buttons Demo");
        setSize(500, 400);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new GridLayout(5, 2)); // 5 rows, 2 columns

        // Create buttons
        b1 = new JButton("Show Message");
        b2 = new JButton("Exit");
        b3 = new JButton("Change Color");
        b4 = new JButton("Disable Me");
        b5 = new JButton("Enable B4");
        b6 = new JButton("Count Clicks");
        b7 = new JButton("Open Dialog");
        b8 = new JButton("Set Text");
        b9 = new JButton("Clear Text");
        b10 = new JButton("Print Console");

        // Add buttons to frame
        add(b1); add(b2); add(b3); add(b4); add(b5);
        add(b6); add(b7); add(b8); add(b9); add(b10);

        // Register listeners
        b1.addActionListener(this);
        b2.addActionListener(this);
        b3.addActionListener(this);
        b4.addActionListener(this);
        b5.addActionListener(this);
        b6.addActionListener(this);
        b7.addActionListener(this);
        b8.addActionListener(this);
        b9.addActionListener(this);
        b10.addActionListener(this);

        setVisible(true);
    }

    int clickCount = 0;
    JTextField textField = new JTextField("Editable Text", 15);

    @Override
    public void actionPerformed(ActionEvent e) {
        if (e.getSource() == b1) {
            JOptionPane.showMessageDialog(this, "Hello, this is a message!");
        } else if (e.getSource() == b2) {
            System.exit(0);
        } else if (e.getSource() == b3) {
            getContentPane().setBackground(Color.CYAN);
        } else if (e.getSource() == b4) {
            b4.setEnabled(false);
        } else if (e.getSource() == b5) {
            b4.setEnabled(true);
        } else if (e.getSource() == b6) {
            clickCount++;
            JOptionPane.showMessageDialog(this, "Button clicked " + clickCount + " times");
        } else if (e.getSource() == b7) {
            JOptionPane.showConfirmDialog(this, "Do you like Java?");
        } else if (e.getSource() == b8) {
            textField.setText("Text set by Button 8");
            add(textField);
            validate();
        } else if (e.getSource() == b9) {
            textField.setText("");
        } else if (e.getSource() == b10) {
            System.out.println("Button 10 pressed!");
        }
    }

    public static void main(String[] args) {
        new TenButtonsDemo();
    }
}
```
<img width="310" height="192" alt="image" src="https://github.com/user-attachments/assets/e882c9e7-f627-4da9-b50d-9def5b67fc66" />
<img width="306" height="189" alt="image" src="https://github.com/user-attachments/assets/641ecf38-3d82-4349-aa62-efe8f9146d0f" />
<img width="326" height="197" alt="image" src="https://github.com/user-attachments/assets/0c4b2116-f2e9-4784-b0de-4778d438c524" />
<img width="300" height="199" alt="image" src="https://github.com/user-attachments/assets/c58f2470-2c05-457c-a261-0f845888c117" />
<img width="313" height="221" alt="image" src="https://github.com/user-attachments/assets/b29e5c36-8dfc-4a48-901a-0f02f5c95756" />
<img width="350" height="224" alt="image" src="https://github.com/user-attachments/assets/8cab651a-53ec-44f0-aa38-9e5eab892c16" />
<img width="310" height="247" alt="image" src="https://github.com/user-attachments/assets/522a8253-2ac8-4cb4-9f26-dd2395c58843" />
<img width="299" height="218" alt="image" src="https://github.com/user-attachments/assets/c67820b8-7154-4d9f-83db-781ffea50d70" />

## assi-16
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class List_example {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // Example using ArrayList
        List<String> list = new ArrayList<>();
        list.add("A");
        list.add("B");
        list.add("A"); // duplicate allowed

        System.out.println("First element: " + list.get(0)); // prints A
    }
}
```
<img width="238" height="61" alt="image" src="https://github.com/user-attachments/assets/911bb9a9-0e8b-4f9d-8e99-d99705532874" />

## assi-17
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class ListMethodsDemo {

    public static void main(String[] args) {
        // Create ArrayList
        List<String> list = new ArrayList<String>();

        // --- Add ---
        list.add("A"); // add at end
        list.add("B");
        list.add(1, "C"); // insert at index

        // --- Access ---
        System.out.println("Element at index 0: " + list.get(0));
        System.out.println("Index of 'B': " + list.indexOf("B"));

        // --- Update ---
        list.set(0, "Z"); // replace element
        System.out.println("After update: " + list);

        // --- Remove ---
        list.remove(1); // remove by index
        list.remove("B"); // remove by value
        System.out.println("After removals: " + list);

        // --- Size/Check ---
        System.out.println("Size: " + list.size());
        System.out.println("Is empty? " + list.isEmpty());
        System.out.println("Contains 'Z'? " + list.contains("Z"));

        // --- Traversal ---
        System.out.println("Traversal using forEach:");
        list.forEach(e -> System.out.println(e));

        System.out.println("Traversal using Iterator:");
        Iterator<String> it = list.iterator();
        while (it.hasNext()) {
            System.out.println(it.next());
        }

        // --- Clear ---
        list.clear();
        System.out.println("After clear, size: " + list.size());
    }
}
```
<img width="221" height="163" alt="image" src="https://github.com/user-attachments/assets/62ff66a8-b1eb-4f24-afb4-bebe7ce7fabe" />

## assi-18
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class AddMethodsDemo {

    public static void main(String[] args) {
        // Using LinkedList to demonstrate all add methods
        LinkedList<String> list = new LinkedList<String>();

        // --- Add ---
        list.add("A"); // add at end
        list.add("B");
        list.add(1, "C"); // insert at index

        // --- AddFirst / AddLast ---
        list.addFirst("Start"); // add at beginning
        list.addLast("End");    // add at end

        // --- Offer methods ---
        list.offer("D");        // add (queue style, at end)
        list.offerFirst("Front"); // add at front
        list.offerLast("Back");   // add at end

        // Display final list
        System.out.println("Final list: " + list);
    }
}
```
<img width="275" height="65" alt="image" src="https://github.com/user-attachments/assets/367dfa3b-8b3a-4632-902f-1585c4696f7d" />

## assi-19
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class AccessMethodsDemo {

    public static void main(String[] args) {
        // Create LinkedList
        LinkedList<String> list = new LinkedList<String>();

        // Add some elements
        list.add("A");
        list.add("B");
        list.add("C");
        list.add("D");

        // --- Access methods ---
        System.out.println("Element at index 2: " + list.get(2));   // get(int index)
        System.out.println("First element: " + list.getFirst());    // getFirst()
        System.out.println("Last element: " + list.getLast());      // getLast()

        System.out.println("Peek (head, no remove): " + list.peek());       // peek()
        System.out.println("Peek First: " + list.peekFirst());              // peekFirst()
        System.out.println("Peek Last: " + list.peekLast());                // peekLast()

        // Show final list to confirm nothing removed
        System.out.println("Final list: " + list);
    }
}
```
<img width="226" height="125" alt="image" src="https://github.com/user-attachments/assets/dd5ca5a0-ef2c-43a5-ac8c-eae26750c356" />

## assi-20
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class SetMethodDemo {

    public static void main(String[] args) {
        // Create LinkedList
        LinkedList<String> list = new LinkedList<String>();

        // Add elements
        list.add("A");
        list.add("B");
        list.add("C");

        System.out.println("Original list: " + list);

        // --- Replace element at index 1 ---
        list.set(1, "Z"); // replaces "B" with "Z"

        System.out.println("After set(1, \"Z\"): " + list);
    }
}
```
<img width="223" height="65" alt="image" src="https://github.com/user-attachments/assets/daee53d9-c083-43ed-b08f-e6a2652c380a" />

## assi-21
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class RemoveMethodsDemo {

    public static void main(String[] args) {
        // Create LinkedList
        LinkedList<String> list = new LinkedList<String>();

        // Add elements
        list.add("A");
        list.add("B");
        list.add("C");
        list.add("D");
        list.add("E");

        System.out.println("Original list: " + list);

        // --- Remove methods ---
        list.remove(); // remove first
        System.out.println("After remove(): " + list);

        list.remove(1); // remove by index
        System.out.println("After remove(1): " + list);

        list.remove("D"); // remove by value
        System.out.println("After remove(\"D\"): " + list);

        list.removeFirst(); // remove first
        System.out.println("After removeFirst(): " + list);

        list.removeLast(); // remove last
        System.out.println("After removeLast(): " + list);

        // --- Poll methods ---
        list.add("X");
        list.add("Y");
        list.add("Z");

        System.out.println("List before poll: " + list);
        System.out.println("poll(): " + list.poll());       // remove head
        System.out.println("pollFirst(): " + list.pollFirst()); // remove first
        System.out.println("pollLast(): " + list.pollLast());   // remove last
        System.out.println("List after polls: " + list);

        // --- Clear ---
        list.clear();
        System.out.println("After clear(): " + list);
    }
}
```
<img width="233" height="170" alt="image" src="https://github.com/user-attachments/assets/fbae63aa-780a-4a76-8c4f-3f59d7b1a4f4" />

## assi-22
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class StackDemo {

    public static void main(String[] args) {
        // Create a Stack of Strings
        Stack<String> stack = new Stack<String>();

        // --- Push elements ---
        stack.push("A");
        stack.push("B");
        stack.push("C");
        System.out.println("Stack after pushes: " + stack);

        // --- Peek (top element without removing) ---
        System.out.println("Peek: " + stack.peek());

        // --- Pop (remove top element) ---
        System.out.println("Pop: " + stack.pop());
        System.out.println("Stack after pop: " + stack);

        // --- Check if empty ---
        System.out.println("Is stack empty? " + stack.isEmpty());

        // Pop remaining elements
        stack.pop();
        stack.pop();
        System.out.println("Stack after removing all: " + stack);
        System.out.println("Is stack empty now? " + stack.isEmpty());
    }
}
```
<img width="232" height="134" alt="image" src="https://github.com/user-attachments/assets/f95adc90-eb5b-4266-949d-bdaca35a8375" />

## assi-23
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class HashMapDemo {

    public static void main(String[] args) {
        // Create a HashMap with Integer keys and String values
        HashMap<Integer, String> map = new HashMap<Integer, String>();

        // --- Insert key-value pairs ---
        map.put(1, "Apple");
        map.put(2, "Banana");
        map.put(3, "Cherry");
        System.out.println("HashMap after insertions: " + map);

        // --- Retrieve values using keys ---
        System.out.println("Value for key 2: " + map.get(2));
        System.out.println("Value for key 3: " + map.get(3));

        // --- Remove an entry ---
        map.remove(2); // remove entry with key 2
        System.out.println("HashMap after removing key 2: " + map);

        // --- Iterate through the map ---
        System.out.println("Iterating using entrySet:");
        for (Map.Entry<Integer, String> entry : map.entrySet()) {
            System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
        }

        System.out.println("Iterating using keySet:");
        for (Integer key : map.keySet()) {
            System.out.println("Key: " + key + ", Value: " + map.get(key));
        }

        System.out.println("Iterating using values:");
        for (String value : map.values()) {
            System.out.println("Value: " + value);
        }
    }
}
```
<img width="299" height="202" alt="image" src="https://github.com/user-attachments/assets/d0320150-106e-40e1-8375-9277d941f50f" />

## assi-24
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the editor.
 */

/**
 *
 * @author kavya
 */
import java.util.*;

public class TreeMapDemo {

    public static void main(String[] args) {
        // Create a TreeMap with Integer keys and String values
        TreeMap<Integer, String> map = new TreeMap<Integer, String>();

        // --- Insert elements ---
        map.put(3, "Banana");
        map.put(1, "Apple");
        map.put(4, "Cherry");
        map.put(2, "Mango");

        // Display elements in sorted order (TreeMap keeps keys sorted)
        System.out.println("TreeMap elements (sorted by key): " + map);

        // --- Search for a key ---
        int searchKey = 2;
        if (map.containsKey(searchKey)) {
            System.out.println("Value for key " + searchKey + ": " + map.get(searchKey));
        } else {
            System.out.println("Key " + searchKey + " not found.");
        }

        // --- Remove an element ---
        map.remove(3); // remove entry with key 3
        System.out.println("TreeMap after removing key 3: " + map);

        // --- Iterate through the map ---
        System.out.println("Iterating through TreeMap:");
        for (Map.Entry<Integer, String> entry : map.entrySet()) {
            System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
        }
    }
}
```
<img width="385" height="134" alt="image" src="https://github.com/user-attachments/assets/5713eda1-b838-4917-897e-e30d230aaffa" />

## assi-25
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the editor.
 */

/**
 *
 * @author kavya
 */
public class ArrayStackDemo {

    static class Stack {
        private int maxSize;
        private int top;
        private int[] stackArray;

        // Constructor
        public Stack(int size) {
            maxSize = size;
            stackArray = new int[maxSize];
            top = -1; // empty stack
        }

        // Push operation
        public void push(int value) {
            if (top == maxSize - 1) {
                System.out.println("Stack Overflow! Cannot push " + value);
            } else {
                stackArray[++top] = value;
                System.out.println("Pushed: " + value);
            }
        }

        // Pop operation
        public void pop() {
            if (top == -1) {
                System.out.println("Stack Underflow! Cannot pop.");
            } else {
                int value = stackArray[top--];
                System.out.println("Popped: " + value);
            }
        }

        // Display elements
        public void display() {
            if (top == -1) {
                System.out.println("Stack is empty.");
            } else {
                System.out.print("Stack elements: ");
                for (int i = 0; i <= top; i++) {
                    System.out.print(stackArray[i] + " ");
                }
                System.out.println();
            }
        }
    }

    public static void main(String[] args) {
        Stack stack = new Stack(3); // stack of size 3

        // Demonstrate operations
        stack.push(10);
        stack.push(20);
        stack.push(30);
        stack.push(40); // overflow

        stack.display();

        stack.pop();
        stack.pop();
        stack.pop();
        stack.pop(); // underflow

        stack.display();
    }
}
```
<img width="247" height="155" alt="image" src="https://github.com/user-attachments/assets/34a7923c-0999-46cf-9a3e-14b586903819" />


## assi-26
```
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author kavya
 */
import java.io.*;

public class File1 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // Example source and destination files
        String source = "source.txt";
        String destByte = "copy_byte.txt";
        String destChar = "copy_char.txt";

        // 1. Copy using Byte Stream
        try (FileInputStream fis = new FileInputStream(source);
             FileOutputStream fos = new FileOutputStream(destByte)) {

            int b;
            while ((b = fis.read()) != -1) {
                fos.write(b);
            }
            System.out.println("File copied successfully using Byte Stream!");
        } catch (IOException e) {
            e.printStackTrace();
        }

        // 2. Copy using Character Stream
        try (FileReader fr = new FileReader(source);
             FileWriter fw = new FileWriter(destChar)) {

            int c;
            while ((c = fr.read()) != -1) {
                fw.write(c);
            }
            System.out.println("File copied successfully using Character Stream!");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```
<img width="445" height="196" alt="image" src="https://github.com/user-attachments/assets/2a260794-06b8-4a9f-9ead-4737368ef293" />

## assi-27
<img width="324" height="188" alt="image" src="https://github.com/user-attachments/assets/6be6ac08-7d6d-4c6b-9666-e5f0e24f2bba" />
<img width="554" height="121" alt="image" src="https://github.com/user-attachments/assets/324d35bb-4724-4b55-bb7f-9a8b2bd7e009" />
<img width="160" height="42" alt="image" src="https://github.com/user-attachments/assets/505cb4b8-7ba1-4786-bc85-4cd4dced87ab" />







