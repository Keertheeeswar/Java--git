# Java--git
<details><summary>-This repository is the documentation of learning java
  </summary></details>



## Functions and methods:
<details><summary>  1) What is a function? </summary> <ul>
    <li>method and functions are used for re-useability</li>
    <li>main will run first and then it will run the method</li>
    </ul></details>

```java
public class StaticFunctionExample {
    public static void main(String[] args) {
        int num1 = 5;
        int num2 = 10;
        
        int sum = addNumbers(num1, num2);
        System.out.println("Sum: " + sum);
    }
    
    public static int addNumbers(int a, int b) {
        return a + b;
    }
}

```
<details><summary>  2) What is return type:</summary> <ul>
    <li> when u call the function ,what is the value of the function call going to be.</li>
    <li>when function call is finished  ,value will be return something.</li>
    <li>statements or code after return statements is not reachable.</li>
    <li>We have to store the return vlaue in the type and then print it.</li>
    <li>int nextAge = calculateNextAge(age);</li>
    </ul></details>

 ```java
public class ReturnTypeExample {
    public static void main(String[] args) {
        String name = "John";
        int age = 25;
        
        greetPerson(name);
        int nextAge = calculateNextAge(age);
        
        System.out.println("Next age: " + nextAge);
    }
    
    public static void greetPerson(String name) {
        System.out.println("Hello, " + name + "!");
    }
    
    public static int calculateNextAge(int currentAge) {
        return currentAge + 1;
    }
}


```

<details><summary>  3) Understanding the function: </summary> <ul>
    <li> The name in function need not be the same ,but executes the same function.</li>
    <li> In java there is only pass by value</li>
    </ul></details>

 ```java
public class HelloWorld{


    
    public static void printName(String name) {
        System.out.println("Name: " + name);//name is copy of reference variable cha.
    }
    public static void main(String[] args) {
        String cha = "keerthe";
        printName(cha);//value of name is passed to method.
    }
       
     }

```
<details><summary>  4) What is Scoping? </summary> <ul>
    <li> the variable will only be changed in the function only.</li>
    <li> Strings are immutable.</li>
    <li> if the actual value is being changed ,like changing the index element in array.</li>
    
</ul></details>

 ```java
public class VariableScopeDemo {

    // This is a global variable with class scope
    static int globalVariable = 10;

    public static void main(String[] args) {
        // This is a local variable with method scope
        int localVariable = 5;

        System.out.println("Global variable value: " + globalVariable);
        System.out.println("Local variable value: " + localVariable);

        // Calling a method to demonstrate block scope
        demonstrateBlockScope();
    }

    public static void demonstrateBlockScope() {
        // This is a local variable with block scope
        int blockVariable = 15;

        System.out.println("Global variable inside method: " + globalVariable);
        // System.out.println("Local variable inside method: " + localVariable); // This will result in an error
        System.out.println("Block variable inside method: " + blockVariable);
    }
}
// Changing the elements of a array.
public class ChangeArrayElement {

    public static void main(String[] args) {
        int[] array = {2, 4, 6, 8, 10};

        // Calling the function to change the zeroth index element
        changeZeroIndexElement(array, 42);

        // Printing the updated array
        for (int num : array) {
            System.out.print(num + " ");
        }
    }

    public static void changeZeroIndexElement(int[] new, int newValue) {
        if (new.length > 0) {
            new[0] = newValue;
        } else {
            System.out.println("Array is empty. Cannot change zeroth index element.");
        }
    }
}


```
<details><summary>  5)What is a Block Scope?  </summary> <ul>
    <li>values initialized inside the block cannot be used outside the block </li>
    
    
</ul></details>

 ```java
public class BlockScopeDemo {

    public static void main(String[] args) {
        // This is a variable with method scope
        int methodScopeVar = 5;
        System.out.println("Method scope variable before block: " + methodScopeVar);

        {
            // This is a variable with block scope
            int blockScopeVar = 10;
            System.out.println("Block scope variable: " + blockScopeVar);

            // Changing the value of block scope variable
            blockScopeVar = 15;
            System.out.println("Block scope variable after change: " + blockScopeVar);

            // Accessing method scope variable inside the block
            System.out.println("Method scope variable inside block: " + methodScopeVar);
        }

        // The following line will result in an error since blockScopeVar is out of scope
        // System.out.println("Block scope variable outside block: " + blockScopeVar);

        // Accessing method scope variable outside the block
        System.out.println("Method scope variable outside block: " + methodScopeVar);
    }
}

```



## Shadowing
<details><summary>  1)What is Shadowing?  </summary> <ul>
    <li>Shadowing in Java occurs when a variable declared within a certain scope has the same name as a variable declared in an outer scope.</li>
    <li>This can lead to confusion as the inner variable "shadows" the outer variable, making it inaccessible within that scope.</li>
    </ul></details>

```java
public class ShadowingExample {
    int x = 10; // Outer variable
    
    void foo() {
        int x = 5; // Inner variable, shadows the outer 'x'
        System.out.println("Inner x: " + x); // Prints the value of inner 'x'
    }
    
    void bar() {
        System.out.println("Outer x: " + x); // Prints the value of outer 'x'
    }
    
    public static void main(String[] args) {
        ShadowingExample example = new ShadowingExample();
        example.foo();
        example.bar();
    }
}

```
## Variable Length arguments:
<details><summary>  1)What is Variable length Arguments?  </summary> <ul>
    <li>Varargs is used when we donot know how many inputs we are giving.</li>
    <li>Varargs are represented by an ellipsis (...) after the data type in the method parameter.</li>
    <li>Varargs should come last at the list.</li>
    </ul></details>

```java
public class VarargsExample {
    // Method that takes variable-length arguments of type int
    static int sum(int... numbers) {
        int total = 0;
        for (int num : numbers) {
            total += num;
        }
        return total;
    }
    
    public static void main(String[] args) {
        int sum1 = sum(1, 2, 3);        // Calling with three arguments
        int sum2 = sum(5, 10, 15, 20); // Calling with four arguments
        
        System.out.println("Sum 1: " + sum1); // Output: Sum 1: 6
        System.out.println("Sum 2: " + sum2); // Output: Sum 2: 50
    }
}

//Another one:
static void fun(int ...v){
    System.out.println(Arrays.toString(v));
}
public static void main(String[] args){
    fun(12,1,31,31,34,13,42,14);
}
```
## :
<details><summary>  1)Function OverLoading:  </summary> <ul>
    <li>It basically says that the function with same name but with different parameter.</li>
    <li>Example: add(int a);add(String b);</li>
    <li>Here the function name is same but the input parameter is Different.</li>
    </ul></details>

```java
public class OverloadingExample {
    public int add(int a, int b) {
        return a + b;
    }

    public double add(double a, double b) {
        return a + b;
    }

    public String concatenate(String str1, String str2) {
        return str1 + str2;
    }
    
    public static void main(String[] args) {
        OverloadingExample example = new OverloadingExample();
        
        int sumInt = example.add(2, 3);
        System.out.println("Sum of integers: " + sumInt);
        
        double sumDouble = example.add(2.5, 3.7);
        System.out.println("Sum of doubles: " + sumDouble);
        
        String result = example.concatenate("Hello, ", "world!");
        System.out.println("Concatenated string: " + result);
    }
}

```



