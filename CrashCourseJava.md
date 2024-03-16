# Java Crash Course

###### Mohammad Rakibul Hasan Mahin [MRM/RHS]

###### Note: There might be errors so kindly do let me know or you can contribute to this git. Thnak you

## Before you Start

In the **CSE470 - Software Engineering** course, you will encounter a lot of **Java** code, and you will also need to write Java code in some cases. However, you are allowed to write **pseudo-code**, but as a **CS** student, not knowing Java can be a crime. In this markdown file, I will try my best to show you the syntax and differences of Java with your favorite language, **Python**. The main intention of this markdown is not to make you a pro at problem-solving with Java but to get the basic gist of it so that you can understand and write code that is sufficient for this CSE470 - Software Engineering course.

## Java Boilerplate Code

```java
public class YourClassName{
    public static void main(String[] args){
        //All your code goes here
    }
}
```

This is the basic boilerplate code. Now this might look a lot but let me break it down for all of you.

1. **public**: This is basically an access modifier. There are few more which we have seen while we were learning class diagram.
2. **class**: This is a keyword that helps you to create a class, pretty similar to python.
3. **static**: This might be something new, this keyword indicates that the method or variable belongs to the class itself, rather than to instances of the class.
4. **void**: This is basically the return type for our function by void we mean that this function is not goint to return anything.
5. **main**: This is basically the name of the method. We write all our code in this main method, because whenever we run the code this is the method that is being executed.
6. **String[] args**: This is the parameter declaration for the main method. It specifies that the main method accepts an array of strings as arguments. These arguments can be passed to the program when it is executed from the command line.

A lot of stuff right? but for now just remember this is the code that you need to write before you write any java code. This might look lengthy but trust me once you start learning it will get your second habit.

## Outputs

Now we all have writted the `Hello World` program in our life, and what it does is basically print `Hello World` in our console. The below code show how you print `Hello World` in console.

For Python:

```python
print("Hello World")
```

For Java:

```java
public class FirstProgram{
    public static void main(String[] args){
        System.out.print("Hello World");
    }
}
```

So, to print anything in console you have to write `System.out.print()` and write your message or variable between the parentheses.

## Data Types and Variables

In java we have all the basic data types that we have seen on python. However, the way we declare variables in java is little bit different. I am not going to talk about the naming convention and different data-types, but show you how to declare variable in java.

For python:

```python
jersey_number = 7
print(jersey_number)
```

The above code in python should print `7` on your console.

For java:

```java
public class FirstProgram{
    public static void main(String[] args){
        int jersey_number = 7;
        System.out.print(jersey_number);
    }
}
```

The above code in java should print `7` on your console. But can you see the difference? In java we always have to mention what type of data is this variable going to store. Which means the variable named `jersey_number` will always store an integer type of data. If we try to store any other data type it will show an error.

Let's look at another example: We want to store `7` but this time it should be in string.

For python:

```python
jersey_number = "7"
print(jersey_number)
```

For java:

```java
public class FirstProgram{
    public static void main(String[] args){
        String jersey_number = "7";
        System.out.print(jersey_number);
    }
}
```

Now we can store any kind of `String` type of data inside `jersey_number` variable.

Here are list of some keywords used in java:

1. `byte`: Stores whole numbers from -128 to 127
2. `short`: Stores whole numbers from -32,768 to 32,767
3. `int`: Stores whole numbers from -2,147,483,648 to 2,147,483,647
4. `long`: Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
5. `float`: Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits
6. `double`: Stores fractional numbers. Sufficient for storing 15 decimal digits
7. `boolean`: Stores true or false values
8. `char`: Stores a **single** character/letter or ASCII values
9. `String`: Stores single or multiple character.

Now, you don't need to remember all this range, just try to use `int` and `double` which will be sufficient for now.

## Mathematical Operations

We have all the basic mathematical operations `+`,`-`,`*`,`/`and `%` in java now where is floor division (`//`)? Actually in java we don't have floor division. But, just to let you know if we divide one integer number with another integer number then we will get the floor result. For Example:

In python:

```python
n = 15
d = 2
print(n/2) # would get 7.5
print(n//2) # would get 7
```

In java:

```java
public class FirstProgram{
    public static void main(String[] args){
        int n = 15;
        int d = 2;
        System.out.print(n/d); //This will give 7 instead of 7.5
    }
}
```

If we want to get `7.5` then one of the number needs to be a `float` or `double` type.

In java:

```java
public class FirstProgram{
    public static void main(String[] args){
        double n = 15;
        int d = 2;
        System.out.print(n/d); //This will give 7.5
        System.out.print(15.0/2); //This will also give 7.5 because one of the number is float or double
        System.out.print((double)15/2); //This will also give 7.5 because we are converting 15 to double
    }
}
```

## Formatting Output

If we want to do a formatted output like `My name is Ronaldo and my jersey number is 7` where `Ronaldo` and `7` is coming from variable we can do this in several ways.

In python:

```python
name = "Ronaldo"
jersey_number = 7
print(f"My name is {name} and my jersey number is {jersey_number}")
```

In java:

```java
public class FirstProgram{
    public static void main(String[] args){
        String name = "Ronaldo";
        int jersey_number = 7;
        System.out.printf("My name is %s and my jersey number is %d\n",name, jersey_number);
    }
}
```

In python we use `f-string` to format but in java we need to use `System.out.printf()`. In python we put the variable names in curly-braces but in java we use placeholders like `%s` (for strings) and `%d` (for integers), and after the string is completed we put name of the variables in sequence that at first `name` and then `jersey_number`.

Some of the place holders are:

1. `%d`: for int,byte,short and long
2. `%f`: for double and float
3. `%s`: for String
4. `%c`: for char
5. `%b`: for boolean

## Input

Input is very important in any programming language. We would always want to take inputs from user and use that instead of declaring it.

In python:

```python
name = input("Please Enter your name: ")
jersey_number = int(input("Please Enter your jersey number: "))
print(f"My name is {name} and my jersey number is {jersey_number}")
```

In python we use `input()` function and we declare the prompt inside the parentheses. This will show an input field in console that will help us to write. For integer inputs we need to convert the string to integer that why we used `int(input())`.

In java:

```java
// For Input we need to import a java package
import java.util.Scanner;
public class FirstProgram{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in); // Here we instantiated our input object which is named sc.
        System.out.print("Please Enter your name: ");
        String name = sc.nextLine();
        System.out.print("Please Enter your jersey number: ");
        int jersey_number = sc.nextInt();
        System.out.printf("My name is %s and my jersey number is %d\n",name, jersey_number);
    }
}
```

Unlike python we cannot use input directly in java, instead we need to import a package which is known as the `Scanner`. To do that we need to type `import java.util.Scanner;` at very beginning and then we need to create an object of this Scanner class, to do that we need to type `Scanner sc = new Scanner(System.in);`. Now, for taking inputs we are going to use this sc object. This `Scanner` class has many methods to take inputs.

1. `nextInt()`: To take integer input
2. `nextFloat()`: To take float input
3. `nextDouble()`: To take double input
4. `nextLine()`: To take multiple string (multiple space separated words)
5. `next()`: To take one string (single word)

## Condition

Writing condition in java is pretty similar to python. Here is one example:

In python:

```python
marks = int(input("Please Enter your marks: "))
if marks < 0 or marks > 100:
    print("Invalid Mark")
elif mark <= 49:
    print("Failed")
else:
    print("Pass")
```

In java:

```java
import java.util.Scanner;
public class FirstProgram{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.print("Please Enter your marks: ");
        int marks = sc.nextInt();
        if(marks < 0 || marks > 100){
            System.out.println("Invalid Marks");
        }else if(marks <= 49){
            System.out.println("Failed");
        }else{
            System.out.println("Pass");
        }
    }
}
```

In java we use `if()`, `else if()` and `else` then use curly-braces `{}` instead of `:` to determine the block of code to execute if the condition is `true`. In python we can simply use `and` and `or` keyword but in java we use `&&` and `||` respectively.

## While Loop

Writing while loop is also pretty similar.

In python:

```python
i = 1
while i < 10:
    print(i)
    i+=1
```

In java:

```java
public class FirstProgram{
    public static void main(String[] args){
        int i = 1;
        while(i <= 10){
            System.out.println(i);
            i += 1;
        }
    }
}
```

Here we can see the code is pretty same just need to use parenteses to set condition and then use curly-brace to determine the block.

## For Loop

Here it is little bit different.

In python:

```python
for i in range(1,11):
    print(i)
```

In java:

```java
public class FirstProgram{
    public static void main(String[] args){
        for(int i = 1; i <= 10; i+=1){
            System.out.println(i);
        }
    }
}
```

Here we don't have range, instead we use the keyword `for()` inside the parentheses we first instantiate our loop-control variable in this case `int i = 1` then we write the condition `i <= 10` and finally increment it `i+=1`.

## Arrays

We have seen list in python, but here in java we have arrays and it is little bit different. In arrays we have a fixed number of items of same data type unlike list in python.

For python:

```python
books = ["Harry Potter", 7, False, 8.5]
```

This is how we create a list in python, here we can notice that the `books` list contains different types of data and we can add as much items we want in this list. But in java this is not the case.

For java:

```java
public class FirstProgram{
    public static void main(String[] args){
        // The below example creates an array of length 5 and it will store string type of data.
        String[] books = new String[5];
        // Here we created an players array that will store string type of data and we are already specifying the elements
        String[] players = {"Ronaldo", "Messi", "Chiesa"}
    }
}
```

Here in java to declare an array first we have to state the data type and use square-brackets `String[]` and then give a name for our array which is `books` in this case. Then we say how many items we want to store and in our case it is 5 so we wrote `new String[5]`.

There is another way to declare an array, first we say the type of data it is going to store then use square-brackets `String[]` then give a name for our arrya in this instance we named it `players`. Finally we use curly-braces to determine the items in our array that is `{"Ronaldo", "Messi", "Chiesa"}`.

We can access elements in simillar way to python that `players[0]`.

## Java funtions

This is the most important concept and probably you will find most changes compared to python. In java we need to tell java what kind of data is our function going to return.

1. Simple Function that prints a statement.

In Python:

```python
def welcomeMessage(name):
    print(f"Welcome {name}")

welcomeMessage("Ronaldo")
# This should print Welcome Ronaldo
```

In Java:

```java
public class FirstProgram{
    // Declare the function outside the main method but inside the class
    static void welcomeMessage(String name){
        System.out.printf("Welcome %s", name);
    }

    public static void main(String[] args){
        welcomeMessage("Ronaldo");
    }
}
```

First we declared our function inside the class but outside the main method. Then we used the `static` keyword which says that we can call this function without instantiating an object for the class. Then `void` states that the function is not going to return anything.

2. Simple function that will take two integer numbers as input and return the sum of those two numbers.

In Python:

```python
def add(num1, num2):
    result = num1 + num2
    return result

res = add(5,10)
print(res)
# This should print 15
```

In Java:

```java
public class FirstProgram{

    static int add(int num1, int num2){
        int result = num1 + num2;
        return result;
    }

    public static void main(String[] args){
        int res = add(5,10);
        System.out.println(res);
    }
}
```

Here we can see that after `static` we used `int` which states that this function will return and integer number.

When we will work with OOP then we will see that we can use access modifiers for methods too.
