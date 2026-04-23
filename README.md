# CS-23.202
Java Lab Programs 4th Semester 2026

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
```<img width="222" height="95" alt="image" src="https://github.com/user-attachments/assets/0bb9600f-ed8e-4d35-a3c1-45c75eee99b6" />


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
class Test_B extends TestA{
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
<img width="224" height="95" alt="image" src="https://github.com/user-attachments/assets/f4c71b18-3062-457e-bd0c-db84d9026d29" />


/





