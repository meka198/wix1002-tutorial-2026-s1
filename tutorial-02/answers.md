# Tutorial 2 = Answer

## 1. Display “Faculty of Computer Science and Information Technology”
### a. One line, multiple statements
```java
System.out.print("Faculty of ");
System.out.print("Computer Science ");
System.out.print("and Information Technology");
```
### b. Multiple lines, one statement
```java
System.out.println("Faculty of\nComputer Science\nand Information Technology");
```
## 2. Print “SDN” - Software-defined networking
```java
System.out.println("\"SDN\" - Software-defined networking");
```
## 3. Correct the errors

### a. System.Println("Java Programming");
Answer : System.out.println("Java Programming"); (Println should be println, and it is out, not a capital P)

### b. System.in.println("Introduction to Java!")
Answer : System.out.println("Introduction to Java!"); (System.in is for input, and the semicolon was missing)

### c. System.out.println("\t is the horizontal tab character");
Answer : System.out.println("\t is the horizontal tab character"); is already correct. Note that \t will print as an actual tab. To show it literally, write "\\t is the horizontal tab character".

### d. system.out.println("Java is case sensitive!" ); 
Answer : System.out.println("Java is case sensitive!"); (system should be System)

## 4. Write statements for each of the following

### a. Declare a variable that used to store the value of a matric number.

int matricNo; (or String matricNo; if it contains letters, such as S2012345)

### b. Declare a variable that used to store the value of π. 

double pi;

### c. Initialize a variable named M with the value set to false.

boolean M = false;

### d. Initialize a variable named P with the value set to 8800000000.

long P = 8800000000L; (this exceeds the int range, so it needs long and the L suffix)

### e. Initialize a variable named letter with the value set to U.

char letter = 'U';

### f. Declare a constant variable named PRO. The value of the constant variable is Java

final String PRO = "Java";

## 5. Correct the error for the following statements.

### a. 
Question :
final double AMOUNT = "32.5";
AMOUNT += 10;
System.out.println("The amount is " + AMOUNT);

Answer :
```java
double amount = 32.5;      // a number, not a String; and it can't be final if modified
amount += 10;
System.out.println("The amount is " + amount);
```

### b. 
Question :
string chapter = 'Summary';
System.out.println(chapter);

Answer :
```java
String chapter = "Summary";
System.out.println(chapter);
```

### c. 
Question :
int num;
++num++;
num1 = num;

Answer :
```java
int num = 0;        // must be initialized before use
++num;              // ++num++ is invalid
int num1 = num;     // num1 was never declared
```

### d. 
Question :
int num = 3000;
System.out.printf("%4.2f\n", num);

Answer :
```java
int num = 3000;
System.out.printf("%d\n", num);
```

### e.
Question :
String contact; 
Scanner keyboard = new Scanner(System.out);
contact = keyboard.nextLine(); 

Answer :
```java
import java.util.Scanner;   // needed at the top of the file

String contact;
Scanner keyboard = new Scanner(System.in);   // System.in, not System.out
contact = keyboard.nextLine();
```

## 6. Write a java program that print the circumference of a circle. The input of theprogram is diameter. Display the result in three decimal places. (Note  = Math.PI)
### Enter diameter = 11,8, and the circumference of the circle = 37,071
```java
import java.util.Scanner;

public class Circumference {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter diameter: ");
        double diameter = input.nextDouble();

        double circumference = Math.PI * diameter;

        System.out.printf("The circumference of the circle is : %.3f\n", circumference);
    }
}
```

## 7. Write a java program that converts inches to meters. (Given 1 inch equals to 2.54 centimeters). Print the output in two decimal places.
```java
import java.util.Scanner;

public class InchToMeter {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter value in inch: ");
        double inches = input.nextDouble();

        double meters = inches * 2.54 / 100;   // inch → cm → m

        System.out.printf("%.2f inches = %.2f meters\n", inches, meters);
    }
}
```

