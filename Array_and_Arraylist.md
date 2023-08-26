# Java--git
<details><summary>-This repository is the documentation of learning java
  </summary></details>

  ## Arrays

 
<details><summary>  1) What are arrays and declaration of array? </summary> <ul>
    <li>Used to store the collection of datatypes.</li>
    <li>Datatype represents what type of data stored in a array.</li>
    <li>indexes of arrays starts from 0.</li>
    <li>The first element is denoted at index 0.</li>
    <li>The array syntax  consist of (int[])-->datatype ,(arr)-->reference  variable and (new int[5])-->creating the object in a heap memory. </li>
    

    
  </ul></details>

  ```java
    DataType[] arrayName = new DataType[length];//Syntax for creating a one dimensional array .
// Creating a one-dimensional integer array
int[] numbers = new int[5]; // Creates an array of size 5

// Initializing elements of the array
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;

    DataType[][] arrayName = new DataType[rows][columns];//Syntax for creating a two dimensional Array.
    // Creating a two-dimensional integer array
int[][] matrix = new int[3][3]; // Creates a 3x3 array

// Initializing elements of the array
matrix[0][0] = 1;
matrix[0][1] = 2;
matrix[0][2] = 3;

matrix[1][0] = 4;
matrix[1][1] = 5;
matrix[1][2] = 6;

matrix[2][0] = 7;
matrix[2][1] = 8;
matrix[2][2] = 9;


 ```

  <details><summary>  2) Is Array objects in java continous?</summary> <ul>
   <li>it may or maynot ,it depends on JVM.</li>
    <li> The array objects are in heap memory.</li>
    <li>Heap memory is not continous</li>
    <li>Dynamic memory Allocation.</li>
    
    
  </ul></details>
  <details><summary>  3)What is a null?  </summary> <ul>
    <li>In Java, null is a special value that represents the absence of a value or the lack of an object reference. </li>
    <li>It cannot be alloted to primitive types.</li>
    <li>It is often used to indicate that a variable does not currently point to any valid object in memory.</li>
    <li>"null" is the default value for object references that have not been explicitly initialized.</li>
    
  </ul></details>

  ```java
  public class NullAssignmentExample {
    public static void main(String[] args) {
        String str = null;  // Assigning null to a String reference
        System.out.println(str);  // Output: null
        
        // Attempting to perform operations on a null reference can lead to NullPointerException
        // For example: str.length();  // This would result in a NullPointerException
    }
}

  ```
  <details><summary>  4) Enhanced for Loop </summary> <ul>
    <li>Used for mainly printing the every element in array or list.</li>
    
    
  </ul></details>

  ```java
public class EnhancedForLoopExample {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5};
        
        for (int num : numbers) {
            System.out.println(num);
        }
    }
}

  ```
 <details><summary>  5) Input in 2D and one D index </summary> <ul>
    <li>input is done using the index of the array</li>
    
    
  </ul></details>

  ```java
  //Input in 2D array in Java
  import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();
        System.out.print("Enter the number of columns: ");
        int columns = scanner.nextInt();
        
        int[][] twoDArray = new int[rows][columns];
        
        System.out.println("Enter the elements of the 2D array:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                twoDArray[i][j] = scanner.nextInt();
            }
        }
        
        // Now you have the 2D array filled with input values
    }
}

//Input in 1D array in java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter the size of the array: ");
        int size = scanner.nextInt();
        
        int[] oneDArray = new int[size];
        
        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < size; i++) {
            oneDArray[i] = scanner.nextInt();
        }
        
        // Now you have the 1D array filled with input values
    }
}


  ```

   <details><summary>  6) Input for variable column length</summary> <ul>
    <li>properly handles rows of varying lengths and ensures that you're accessing the correct elements during input and output.</li>
    
    
  </ul></details>  

  ```java
  import java.util.*;

public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello, World!");
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int arr[][] = new int[n][n];
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < arr[i].length; j++) {
                arr[i][j] = sc.nextInt();
            }
        }

        for (int j = 0; j < n; j++) {
            for (int i = 0; i < arr.length; i++) {
                if (i < arr[j].length) {
                    System.out.print(arr[i][j] + " ");
                } else {
                    System.out.print("0 "); // Assuming default value for missing elements
                }
            }
            System.out.println();
        }
    }
}

  ```

## Array List:
<details><summary>  1)What are Array list? </summary> <ul>
    <li>If we donot know how many items we are gonna store</li>
    <li>If we want java to handle the size of the array </li>
    
  </ul></details> 

  ```java
  import java.util.ArrayList;

public class ArrayListExample {

    public static void main(String[] args) {
        // Create an ArrayList to store integers
        ArrayList<Integer> numbers = new ArrayList<>();
        
        // Adding elements to the ArrayList
        numbers.add(5);
        numbers.add(10);
        numbers.add(15);
        
        // Adding an element at a specific index
        numbers.add(1, 7); // Adds 7 at index 1
        
        // Accessing elements from the ArrayList
        System.out.println("Element at index 2: " + numbers.get(2)); // Output: 15
        
        // Modifying an element
        numbers.set(0, 3); // Replaces the element at index 0 with 3
        
        // Removing an element
        numbers.remove(2); // Removes the element at index 2
        
        // Size of the ArrayList
        System.out.println("Size of ArrayList: " + numbers.size()); // Output: 3
        
        // Iterating through the ArrayList
        System.out.print("ArrayList elements: ");
        for (int num : numbers) {
            System.out.print(num + " ");
        }
        System.out.println();
    }
}

  ```


  <details><summary>  2)How the array list thing works internally? </summary> <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul></details> 

  <details><summary>  3) </summary> <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul></details> 

  <details><summary>  4) </summary> <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul></details> 

  <details><summary>  5) </summary> <ul>
    <li></li>
    <li></li>
    <li></li>
  </ul></details> 