# Java--git
<details><summary>-This is about Learning String and Loops
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

## String:
<details><summary>  1) String input:</summary> <ul>
    <li>For inputting a single word --> next() is used. </li>
    <li>For inputting a whole Line --> nextLine() is used.</li>
    </ul></details>

```java
String str = "Hello, World!";
int length = str.length();//To find the string length.

String str1 = "Hello";
String str2 = "World";
boolean isEqual = str1.equals(str2);//To compare the two Strings.

String str1 = "hello";
String str2 = "HELLO";
boolean isEqualIgnoreCase = str1.equalsIgnoreCase(str2);//To ignore the upper and lower cases while comparing.


```

## Loop:
<details><summary>  1) for Loop:</summary> <ul>
    <li>Use it when we know how many times the code is gonna run. </li>
    </ul></details>

```java
public class ForLoopExample {
    public static void main(String[] args) {
        int n = 5; // Since we know how many times the loop should run.
        
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        
        System.out.println("Sum of first " + n + " natural numbers: " + sum);
    }
}

```
<details><summary>  2) While loop:</summary> <ul>
    <li>When we donot know how many times the loop will run.</li>
    </ul></details>

```java
public class SumOfDigitsWhileLoop {
    public static void main(String[] args) {
        int number = 12345; // we can give any input.
        
        int sum = 0;
        int temp = number;
        
        while (temp > 0) {
            int digit = temp % 10;
            sum += digit;
            temp /= 10;
        }
        
        System.out.println("Sum of digits of " + number + " is: " + sum);
    }
}


```
<details><summary>  3) do while:</summary> <ul>
    <li>If we want to run the loop atleast once independent of condition.</li>
    </ul></details>

```java
import java.util.*;
public class sum_of_all {
    public static void main(String[] args){
        Scanner sc =new Scanner(System.in);
        int sum=0;
        int n;
        do{//For executing it atleast once.
           n=  sc.nextInt();
          sum = sum+n;
        }while(n!=0);
        System.out.println(sum);
    }
}

```

<details><summary>  4) else if:</summary> <ul>
    <li>Used to perform a certain condition.</li>
    </ul></details>

```java
import java.util.Scanner;

public class CGPACalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.println("Enter the number of subjects: ");
        int numSubjects = sc.nextInt();
        
        double totalCredits = 0;
        double totalGradePoints = 0;
        
        for (int i = 1; i <= numSubjects; i++) {
            System.out.println("Enter credits for subject " + i + ": ");
            int credits = sc.nextInt();
            
            System.out.println("Enter grade for subject " + i + " (A/B/C/D/F): ");
            char grade = sc.next().charAt(0);
            
            double gradePoints;
            
            if (grade == 'A') {
                gradePoints = 4.0;
            } else if (grade == 'B') {
                gradePoints = 3.0;
            } else if (grade == 'C') {
                gradePoints = 2.0;
            } else if (grade == 'D') {
                gradePoints = 1.0;
            } else {
                gradePoints = 0.0;
            }
            
            totalGradePoints += (gradePoints * credits);
            totalCredits += credits;
        }
        
        double cgpa = totalGradePoints / totalCredits;
        
        System.out.println("Your CGPA is: " + cgpa);
    }
}


```
<details><summary>  5) switch statement:</summary> <ul>
    <li>If we wanna check the given input is this or not.</li>
    <li>Or to used to group under the certain category .</li>
    </ul></details>

```java
import java.util.Scanner;

public class EnhancedSwitchCGPACalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.println("Enter the number of subjects: ");
        int numSubjects = sc.nextInt();
        
        double totalCredits = 0;
        double totalGradePoints = 0;
        
        for (int i = 1; i <= numSubjects; i++) {
            System.out.println("Enter credits for subject " + i + ": ");
            int credits = sc.nextInt();
            
            System.out.println("Enter grade for subject " + i + " (A/B/C/D/F): ");
            char grade = sc.next().charAt(0);
            
            double gradePoints;
            
            switch (grade) {
                case 'A' -> gradePoints = 4.0;
                case 'B' -> gradePoints = 3.0;
                case 'C' -> gradePoints = 2.0;
                case 'D' -> gradePoints = 1.0;
                default -> gradePoints = 0.0;
            }
            
            totalGradePoints += (gradePoints * credits);
            totalCredits += credits;
        }
        
        double cgpa = totalGradePoints / totalCredits;
        
        System.out.println("Your CGPA is: " + cgpa);
    }
}


```

<details><summary>  5) enhanced switch statement:</summary> <ul>
    <li>If we wanna check the given input is this or not.</li>
    <li>Or to used to group under the certain category .</li>
    <li>Reduced number of lines of code than normal Switch statement.</li>
    </ul></details>

```java
import java.util.Scanner;

public class SwitchCGPACalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.println("Enter the number of subjects: ");
        int numSubjects = sc.nextInt();
        
        double totalCredits = 0;
        double totalGradePoints = 0;
        
        for (int i = 1; i <= numSubjects; i++) {
            System.out.println("Enter credits for subject " + i + ": ");
            int credits = sc.nextInt();
            
            System.out.println("Enter grade for subject " + i + " (A/B/C/D/F): ");
            char grade = sc.next().charAt(0);
            
            double gradePoints;
            
            switch (grade) {
                case 'A':
                    gradePoints = 4.0;
                    break;
                case 'B':
                    gradePoints = 3.0;
                    break;
                case 'C':
                    gradePoints = 2.0;
                    break;
                case 'D':
                    gradePoints = 1.0;
                    break;
                default:
                    gradePoints = 0.0;
            }
            
            totalGradePoints += (gradePoints * credits);
            totalCredits += credits;
        }
        
        double cgpa = totalGradePoints / totalCredits;
        
        System.out.println("Your CGPA is: " + cgpa);
    }
}



```