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
    <li>we want tto run the main function without creating a object for class </li>
    <li>the main function will be one which will be running first</li>
    </ul></details>

 ```java
static void main(String[] args)
```

