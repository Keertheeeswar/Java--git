# Java--git
<details><summary>-This repository is the documentation of learning java
  </summary></details>
<style>
  /* Style the dropdown summary button */
  details summary {
    cursor: pointer;
    list-style: none;
    padding: 0;
    font-weight: bold;
  }

  /* Style the content of the dropdown */
  details ul {
    margin: 0;
    padding-left: 20px;
  }
</style>


## Structure of Java File
<details><summary>  1) Class </summary> <ul>
    <li>File name is the class name </li>
    <li>Class contains the main function</li>
    </ul></details>

```java
public class HelloWorld {
public static void main(String[] args) {

}
}
```
<details><summary>  2) Input </summary> <ul>
    <li>First import Scanner </li>
    <li>Declare Scanner </li>
    </ul></details>

 ```java
import java.util.Scanner;

public class ScannerExample {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the keyboard
        Scanner sc = new Scanner(System.in);

        // Prompt the user to enter their name
        System.out.print("Enter your name: ");
        
        // Read the input (string) provided by the user
        String name = sc.nextLine();

        // Prompt the user to enter their age
        System.out.print("Enter your age: ");
        
        // Read the input (integer) provided by the user
        int age = sc.nextInt();

        // Display the user's name and age
        System.out.println("Hello, " + name + "! You are " + age + " years old.");

        // Don't forget to close the scanner to release resources
        sc.close();
    }
}

```

<details><summary>  3) Output </summary> <ul>
    <li>print command for printing in same line. </li>
    <li>println command for printing in next line. </li>
    </ul></details>

 ```java
public class HelloWorld {
public static void main(String[] args) {
System.out.print("Hello, world!");//Same line
System.out.println("Hello, world!");//Different line
}
}
```
<details><summary>  4) Debugging java in Terminal </summary> <ul>
    <li>Checking whether the code contains any error </li>
    
</ul></details>

 ```java
javac Main.java
```
<details><summary>  5) Running java in Terminal </summary> <ul>
    <li>Expecting the output </li>
    
</ul></details>

 ```java
javac Main
```
<details><summary>  6) Static </summary> <ul>
    <li>we want to run the main function without creating a object for class </li>
    <li>the main function will be one which will be running first</li>
    </ul></details>

 ```java
static void main(String[] args)
```

  
<details><summary>7)what is a package ? </summary>
            <ul>
    <li> It is a folder in which your java file lies</li>
    <li>Used to provides some sort of rules</li>
    <li>10 is object</li>
           </ul></details>
           
```java
package com.keerthe 
```

     
<details><summary>8)what does System.out.println ? </summary>
  <ul>
    <li> System is Class .</li>
    <li>Println is a function.</li>
    <li>System is a class which contains a variable called out of type print Stream</li>
    <li> out is like a reference variable for println</li>
    

  </ul></details>

```java
System.out.println();
```

<details><summary>9)what does Scanner do ? </summary>
  <ul>
    <li> Scanner sc =new Scanner(System.in)</li>
    <li>()<-- in this we write where we are taking the input</li>
    <li> System.in means that we are taking it from the keyboard </li>

    
  </ul></details>
  
  ```java
Scanner sc = new Scanner(System.in);
```




## Primitive datatypes
<details><summary>1)what are the primitive datatype ?</summary>
  <ul>
    <li>int </li>
    <li>char</li>
    <li>float </li>
    <li>double  </li>
    <li>long </li>
    <li>boolean </li>

</ul></details>

<details><summary>2)what does int do?</summary>
  <ul>
    <li>int will store the integer values</li>

</ul></details>

  ```java
int rollno =10;
int n =sc.nextInt();
```
<details><summary>3)what does char do?</summary>
  <ul>
    <li>stores the character values </li>
   

</ul></details>

  ```java
char letter ='r';
char n =sc.nextChar();
```
<details><summary>4)what does float do?</summary>
  <ul>
    <li>stores the decimal point variables </li>
   

</ul></details>

  ```java
float degree =98.88f;
Float n =sc.nextFloat();
```
<details><summary>5)what does double do?</summary>
  <ul>
    <li>used to store large decimal point numbers </li>
   

</ul></details>

  ```java
double accuracy =98.888927;
double n =sc.nextDouble();
```
<details><summary>6)what does long  do?</summary>
  <ul>
    <li>used to store large integer </li>
    <li>name of the variable is identifier </li>

</ul></details>

  ```java
long accuracy =98888927L;
long n =sc.nextLong();
```
<details><summary>7)what does boolean  do?</summary>
  <ul>
    <li>Assign the default value for the variable whether true or false!  </li>
   

</ul></details>

  ```java
boolean score = true;
```
## Type convertion and Type casting
<details><summary>1)what is type casting?</summary>
  <ul>
    <li>when one type of data is assigned to another type of variable then automatic type convertion takes place if the following conditions are met</li>
    <li> two types should br comaptible</li>
    <li>example: float and integer </li>
    </ul></details>

  ```java
    float num =input.nextInt()//this can happen ,since float can accept integer value
    int num = input.nextFloat()//this will not happen, since integer does not allow the float value


  ```

<details><summary>2)what is type convertion?</summary>
  <ul>
    <li>to convert one one datatype to other </li>
    <li> narrowing convertion</li>
    <li>compressing the bigger number into a smaller type explicitly</li>
    </ul></details>

  ```java
int num = (int)(67.56f)//casting the floating to integer
int a =257;
byte b =(byte)(a)// Result:257%256=1
------
byte a = 40;
byte b = 50;
byte c =100;
int d =a * b/c;//expression elevates the byte to integer
----
int a ='A';
System.out.print(a);//gives the ascii value
  ```
  ## String Functions:
  <details><summary>1)How to get input in string?</summary>
  <ul>
    <li>Using next and nextLine.</li>
    <li>next() is used for getting a single word </li>
    <li>nextLine() is used for inputting a full sentence. </li>
    </ul></details>

   ```java
   String s =sc.next();
   String s1 = sc.nextLine();

  ```
  <details><summary>2)Basic operation in strings?</summary>
  <ul>
    <li>Commands to find Length</li>
    <li>Commands to check Whether two Strings are equals</li>
    
  </ul></details>

   ```java
   
  String str = "Hello, World!";
  int length = str.length();// To find the String Length;

  String str1 = "Hello";
  String str2 = "World";
  boolean isEqual = str1.equals(str2);//To Check Whether the two strings are equal.
  String str1 = "hello";
String str2 = "HELLO";
boolean isEqualIgnoreCase = str1.equalsIgnoreCase(str2);//To ignore uppercase and lower case equal cases.

  ```