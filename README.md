# Introduction to C++ Programming Course

Welcome to the exciting world of C++ programming! My name is Ignacio Rodríguez, and I'll be your guide on this incredible journey into the world of coding.

I still remember the glance of an eight-year-old me, looking at a computer screen, filled with curiosity and wonder. Programming started as a hobby for me at a very early age, and it quickly turned into a lifelong passion. The joy of creating something from nothing, the thrill of solving complex problems, and the satisfaction of seeing my code come to life were more than just entertaining; they were empowering.

I invite you to approach this course with an open mind and a heart filled with the certainty that you are about to acquire knowledge that will not only empower you but also entertain you. Whether you're here to pursue a career or explore a hobby, the way you approach learning can make all the difference.

As the renowned author and educator Sir Ken Robinson once said, **"The element is the point at which natural talent meets personal passion."** This quote beautifully captures the essence of what I hope you'll discover in this course. There is a profound difference between those who learn an art because they truly love it and those who take it as a task given. Embrace the former, and you'll find that learning becomes a joyful and fulfilling experience.

So, let's embark on this journey together. Let's rediscover the childlike wonder of learning something new, and let's do it with the enthusiasm and passion that turns ordinary tasks into extraordinary adventures.

Welcome to the world of C++, where creativity meets logic, and where you'll find both challenges and triumphs. Let's get started!

---

### Lesson 1: Setting Up C++ Environment

#### Introduction to C++ and Setting Up the Development Environment

C++ is a powerful and versatile programming language that offers a blend of high-level and low-level features. Whether you're developing system software, game engines, or modern web applications, C++ provides the tools and performance you need.

In this lesson, we'll explore how to set up your C++ development environment, including understanding the compile and link phases, basic command-line parameters for the compiler, and choosing an editor.

#### C++ Standards and Their Evolution

C++ has seen several significant updates since its inception, each introducing new features, improvements, and changes to the language. Understanding the different standards can be crucial, especially when working on various projects that might require compatibility with different versions of C++.

Here's a brief overview of some key C++ standards:

- **C++98 / C++03**: The first standardized versions of C++, laying the foundation for modern C++ programming.
- **C++11**: A major update that introduced features like lambda expressions, range-based for loops, smart pointers, and more.
- **C++14**: A smaller update with improvements and refinements to C++11 features.
- **C++17**: Introduced features like structured bindings, `std::optional`, `std::variant`, and the filesystem library.
- **C++20**: The latest standard (as of the knowledge cut-off date) with concepts, ranges, coroutines, and more.

Understanding the differences between these standards and how to specify the desired standard when compiling can be essential for both new and experienced C++ developers. It ensures that the code is portable and takes advantage of the latest language features when appropriate.

#### Compile and Link Phases

1. **Compile Phase**: The compiler translates the C++ source code into machine code or object code. This phase checks for syntax errors and converts the high-level code into a format that the computer can understand.

2. **Link Phase**: The linker takes the object code and combines it with other object files and libraries to create the final executable. This phase resolves references between different parts of the code and ensures that everything is connected correctly.

#### Basic Command-Line Parameters

When compiling C++ code, you'll often use command-line parameters to control the behavior of the compiler. Here are some common parameters:

- `-o`: Specifies the output file name.
- `-g`: Includes debugging information.
- `-Wall`: Enables all warning messages.
- `-std`: Specifies the C++ standard to use (e.g., `-std=c++11`).

Example:
```bash
g++ -o myprogram myprogram.cpp -Wall -std=c++11
```

#### Visual Studio Code

Visual Studio Code (VS Code) is an excellent and free-to-use code editor that supports C++ development. It offers features like syntax highlighting, code completion, debugging, and more. You can download it from the [official website](https://code.visualstudio.com/).

#### Installing a C++ Compiler

##### Windows

1. Download and install [MinGW](http://www.mingw.org/).
2. Add the MinGW bin directory to your system's PATH environment variable.
3. Verify the installation by opening a command prompt and typing `g++ --version`.

##### MacOS

1. Install Xcode from the App Store.
2. Open Terminal and run `xcode-select --install`.
3. Verify the installation by typing `g++ --version`.

##### Linux

1. Open Terminal.
2. For Debian-based systems, run `sudo apt-get install g++`.
3. For Red Hat-based systems, run `sudo yum install gcc-c++`.
4. Verify the installation by typing `g++ --version`.

#### Conclusion

Setting up your C++ development environment is the first step in your programming journey. Understanding the compile and link phases, knowing basic command-line parameters, and choosing a suitable editor like Visual Studio Code will set you on the path to success.

In the next lesson, we'll dive into the basic syntax of C++ and learn how to print output. Happy coding!

---

### Lesson 2: Basic Syntax and Printing in C++

#### Introduction to Console Systems

In programming, the console is a text-based interface that allows interaction between the user and the program. It's a simple device that provides input and output capabilities, making it an ideal tool for learning and experimenting with code.

However, it's worth noting that the console is not the only way to generate responses or feedback from a program. There are APIs and libraries that allow you to work with graphical widgets, and tools like OpenGL for graphic-based output. But for the purpose of this course, we'll focus on the console, as it offers a straightforward way to understand the core concepts of programming.

#### Understanding the Main Function

In C++, the `main` function serves as the entry point for the program. When you run a C++ program, the execution starts from the `main` function. It must return an integer value, typically 0, to indicate successful execution. Any other value may signal an error. The `main` function can accept command-line arguments, but for our introductory examples, we'll keep it simple.

Certainly! In Lesson 2, which focused on basic syntax, printing in C++, and introducing the console system, an interesting point that might have been missed could be the discussion of character encoding and how it affects text output.

### Character Encoding in C++

Character encoding is a method used to represent characters using binary code. In C++, understanding character encoding can be essential, especially when dealing with internationalization or working with non-ASCII characters.

Here's a brief overview that could be added to Lesson 2:

- **ASCII**: The American Standard Code for Information Interchange (ASCII) is a 7-bit character encoding standard that includes English letters, digits, and common symbols. It's widely supported but limited to a small character set.

- **Extended ASCII**: An 8-bit extension of ASCII that includes additional characters, but its representation can vary between systems and languages.

- **UTF-8**: A widely-used encoding that can represent any character in the Unicode standard. UTF-8 is compatible with ASCII but can also encode a vast array of international characters.

- **Wide Characters**: C++ provides support for wide characters (`wchar_t`) and wide string literals (`L"string"`), allowing for the representation of characters outside the ASCII range.

- **Locale**: The C++ Standard Library provides locale support, allowing programs to adapt to local conventions for character representation, date and time formatting, etc.

#### Example: Printing UTF-8 Encoded String
```cpp
#include <iostream>

int main() {
    std::cout << u8"Привет, мир!" << std::endl; // Hello, world! in Russian
    return 0;
}
```

#### Tip for Windows Users

If you're using Windows, be cautious when accidentally clicking on a console window. This action might pause the running program, as the OS will freeze your program to preserve whatever is on the screen. To resume, simply press any key.

#### "Hello World" Program

A traditional starting point in programming is the "Hello World" program. Here's a simple example in C++:

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

To compile and run this program, use the following commands:

```bash
g++ -o hello hello.cpp
./hello
```

#### Fizz/Buzz Implementation

The Fizz/Buzz program is a classic coding challenge. It prints numbers from 1 to N, but for multiples of 3, it prints "Fizz," for multiples of 5, it prints "Buzz," and for multiples of both 3 and 5, it prints "FizzBuzz."

```cpp
#include <iostream>

int main() {
    for (int i = 1; i <= 100; i++) {
        if (i % 3 == 0 && i % 5 == 0) {
            std::cout << "FizzBuzz";
        } else if (i % 3 == 0) {
            std::cout << "Fizz";
        } else if (i % 5 == 0) {
            std::cout << "Buzz";
        } else {
            std::cout << i;
        }
        std::cout << std::endl;
    }
    return 0;
}
```

Compile and run the program with:

```bash
g++ -o fizzbuzz fizzbuzz.cpp
./fizzbuzz
```

#### Conclusion

Understanding the basic structure of a C++ program, including the essential role of the `main` function, and learning to print output through the console is a vital step in your programming journey. The console provides a simple and effective way to interact with your code, but remember, it's just one of many tools available to you.

In the next lesson, we'll explore variables, data types, and constants in C++. Keep experimenting and happy coding!

---

1. **What is the primary purpose of the `main` function in a C++ program?**
   - A) To print output
   - B) To include libraries
   - C) To serve as the entry point for the program
   - D) To define variables
   - **Answer: C**

2. **Which command-line parameter specifies the output file name when compiling a C++ program?**
   - A) `-o`
   - B) `-g`
   - C) `-Wall`
   - D) `-std`
   - **Answer: A**

3. **What will the following code snippet print?**
   ```cpp
   for (int i = 1; i <= 5; i++) {
       if (i % 3 == 0) {
           std::cout << "Fizz";
       } else {
           std::cout << i;
       }
   }
   ```
   - A) 12Fizz45
   - B) 1 2 Fizz 4 5
   - C) Fizz 2 3 4 5
   - D) 1 2 Fizz 3 4
   - **Answer: A**

4. **What happens when you accidentally click on a console window in Windows while a program is running?**
   - A) The program crashes
   - B) The program is paused
   - C) The program restarts
   - D) Nothing happens
   - **Answer: B**

5. **Which of the following is NOT a reason to use the console for learning C++?**
   - A) It provides input and output capabilities
   - B) It allows interaction with graphical widgets
   - C) It offers a straightforward way to understand core concepts
   - D) It's a simple device for experimenting with code
   - **Answer: B**

6. **Which tool is mentioned in the lesson as a free-to-use code editor for C++ development?**
   - A) Visual Studio
   - B) Sublime Text
   - C) Visual Studio Code
   - D) Notepad++
   - **Answer: C**

---

### Lesson 3: Variables and Data Types in C++

#### Introduction

In programming, variables are used to store information that can be used and manipulated throughout the code. Data types define the type of data that a variable can hold, such as integers, floating-point numbers, characters, etc. In this lesson, we'll explore different data types, variables, and constants in C++.

#### Variables

A variable is a named storage location that can hold a value. In C++, you must declare the type of a variable when you create it. Here's an example:

```cpp
int age = 25;
double weight = 70.5;
char initial = 'I';
```

#### Data Types

C++ offers various data types to suit different needs. Here are some common ones:

- **Integer Types**: `int`, `short`, `long`, `long long`
- **Floating-Point Types**: `float`, `double`
- **Character Types**: `char`
- **Boolean Type**: `bool`

#### Constants

A constant is a variable whose value cannot be changed after it's initialized. You can declare a constant using the `const` keyword:

```cpp
const double PI = 3.14159265;
```

#### Type Modifiers

Type modifiers allow you to alter the storage of a data type. Some common modifiers include:

- `signed`: Allows positive and negative values
- `unsigned`: Allows only positive values
- `long`: Increases the size of the data type
- `short`: Decreases the size of the data type

#### Auto Keyword

C++11 introduced the `auto` keyword, allowing the compiler to automatically deduce the type of a variable:

```cpp
auto name = "Anita"; // deduced as const char*
```

Certainly! In Lesson 3, which focused on variables and data types in C++, an interesting point that might have been missed could be the discussion of type inference and the `auto` keyword, along with the importance of strong typing.

### Type Inference and Strong Typing in C++

Understanding how to declare variables with explicit types is fundamental, but modern C++ also offers type inference, allowing the compiler to deduce the type of a variable based on its initialization.

Here's an overview that could be added to Lesson 3:

- **Type Inference with `auto`**: Introduced in C++11, the `auto` keyword allows the compiler to automatically deduce the type of a variable from its initializer. This can make code more concise and maintainable, especially when dealing with complex types.

  ```cpp
  auto x = 42; // int
  auto y = 3.14; // double
  auto name = "Ignacio"; // const char*
  ```

- **Strong Typing**: C++ is a strongly typed language, meaning that the type of a variable is known at compile time and must be adhered to. This helps catch errors early and promotes code safety.

- **Type Casting**: While strong typing enforces type safety, C++ also provides mechanisms for type casting, allowing developers to convert between types when necessary. Understanding when and how to use type casting is essential for writing robust code.

  ```cpp
  int integer = static_cast<int>(3.14); // Explicit type casting from double to int
  ```

- **Type Aliases**: C++ allows developers to create type aliases using the `typedef` keyword or the `using` directive. This can make code more readable and allow for more flexible design.

  ```cpp
  using Integer = int; // Type alias for int
  Integer value = 42;
  ```

#### Conclusion

Understanding variables, data types, and constants is fundamental to programming in C++. These concepts allow you to store and manipulate data in various ways, providing flexibility and control in your code.

In the next lesson, we'll explore user input and output handling in C++. Keep experimenting with different data types and variables, and remember to approach learning with curiosity and enjoyment!

---

1. **What is the purpose of a variable in C++?**
   - A) To define functions
   - B) To store information
   - C) To print output
   - D) To include libraries
   - **Answer: B**

2. **Which data type would be most appropriate for storing a person's age?**
   - A) `float`
   - B) `char`
   - C) `int`
   - D) `bool`
   - **Answer: C**

3. **What does the `const` keyword do in C++?**
   - A) Makes a variable mutable
   - B) Makes a variable changeable
   - C) Makes a variable unchangeable
   - D) Deletes a variable
   - **Answer: C**

4. **What will the following code snippet deduce the type of `value` as?**
   ```cpp
   auto value = 42;
   ```
   - A) `float`
   - B) `double`
   - C) `int`
   - D) `char`
   - **Answer: C**

5. **Which type modifier allows only positive values for a variable?**
   - A) `signed`
   - B) `unsigned`
   - C) `long`
   - D) `short`
   - **Answer: B**

6. **What is the result of the following type casting?**
   ```cpp
   double number = 5.9;
   int result = static_cast<int>(number);
   ```
   - A) 5
   - B) 6
   - C) 5.9
   - D) Error
   - **Answer: A**

7. **Which of the following is NOT a valid data type in C++?**
   - A) `long long`
   - B) `float`
   - C) `boolean`
   - D) `char`
   - **Answer: C**

8. **What is the value of `PI` after executing the following code?**
   ```cpp
   const double PI = 3.14;
   PI = 3.14159; // Attempt to change the value
   ```
   - A) 3.14
   - B) 3.14159
   - C) 0
   - D) Compilation Error
   - **Answer: D**

---

### Lesson 4: User Input and Output

#### Introduction

User input and output are fundamental concepts in programming. They allow a program to interact with the user by receiving information and displaying results. In this lesson, we'll explore how to handle user input and output in C++, using simple console commands.

#### Console Input and Output

In C++, you can use the `std::cin` and `std::cout` objects to read from and write to the console, respectively. Here's a basic example:

```cpp
#include <iostream>

int main() {
    int number;
    std::cout << "Enter a number: ";
    std::cin >> number;
    std::cout << "You entered: " << number << std::endl;
    return 0;
}
```

#### Using `std::string` for Text

When working with text, you can use the `std::string` data type. It allows you to store and manipulate strings easily.

Certainly! Lesson 4 focused on user input and output, handling user input, and formatting output. An interesting point that might have been missed could be the discussion of error handling related to user input, input validation, and the use of input streams.

### Error Handling and Input Validation in C++

User input is often unpredictable, and handling incorrect or unexpected input is a crucial aspect of robust programming. Here's an overview that could be added to Lesson 4:

- **Input Validation**: Ensuring that the input meets specific criteria before processing it. For example, checking that a number is within a certain range or that a string follows a particular format.

- **Input Stream States**: C++ input streams like `std::cin` have state flags that can be checked to determine if an input operation was successful.

  ```cpp
  int value;
  std::cin >> value;
  if (std::cin.fail()) {
      std::cerr << "Invalid input!" << std::endl;
      std::cin.clear(); // Clear the error state
      std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n'); // Ignore the rest of the line
  }
  ```

- **Exception Handling**: While not commonly used with basic input and output, C++ provides mechanisms for exception handling (`try`, `catch`, `throw`) that can be applied to more complex input scenarios, such as file reading or network communication.

- **Formatted Input and Output**: Beyond basic input and output, C++ offers extensive control over formatting, such as setting precision, field width, alignment, and more. This allows for more user-friendly displays and precise control over how data is presented.

  ```cpp
  double pi = 3.14159265;
  std::cout << std::fixed << std::setprecision(2) << pi << std::endl; // Output: 3.14
  ```

- **Locale-Specific Formatting**: C++ also supports locale-specific formatting, allowing programs to adapt to different cultural conventions for things like number formatting, currency symbols, etc.

#### Exercise: Personalized Greeting

Here's a simple exercise that asks the user for their name and then composes a greeting.

```cpp
#include <iostream>
#include <string>

int main() {
    std::string name;
    std::cout << "What's your name? "; // Ask for the user's name
    std::cin >> name; // Read the user's name
    std::string greeting = "Hello, " + name + "! Welcome to the world of C++!"; // Compose a greeting
    std::cout << greeting << std::endl; // Print the greeting
    return 0;
}
```

This code includes comments to explain each step, making it extremely simple to understand.

#### The Power of Console Input and Output

While console input and output may seem basic, they are the building blocks for many valuable applications. By redirecting inputs and outputs, you can accomplish complex tasks, such as reading from files, writing to network sockets, and more.

#### Conclusion

Understanding how to handle user input and output is essential for creating interactive programs. The simplicity of console-based interaction in C++ allows you to focus on core programming concepts and build a strong foundation.

In the next lesson, we'll delve into conditional statements and loops, further expanding your ability to create dynamic and responsive programs.

---

1. **What is the output of the following code snippet?**
   ```cpp
   int x = 10;
   std::cout << "Value of x: " << x;
   ```
   - A) Value of x: 10
   - B) Value of x: x
   - C) 10
   - D) x
   - **Answer: A**

2. **What will the following code snippet read into the variable `name`?**
   ```cpp
   std::string name;
   std::cout << "Enter your name: ";
   std::cin >> name;
   ```
   - A) The full name entered by the user
   - B) Only the first word of the name entered by the user
   - C) The last word of the name entered by the user
   - D) None of the above
   - **Answer: B**

3. **What is the result of the following code if the user enters "John"?**
   ```cpp
   std::string firstName;
   std::cout << "Enter your first name: ";
   std::cin >> firstName;
   std::string greeting = "Hi, " + firstName + "!";
   std::cout << greeting;
   ```
   - A) Hi, John!
   - B) Hi, firstName!
   - C) Error
   - D) Hi, !
   - **Answer: A**

4. **What will be the output of the following code if the user enters 5?**
   ```cpp
   int number;
   std::cout << "Enter a number: ";
   std::cin >> number;
   std::cout << "Number squared: " << number * number;
   ```
   - A) Number squared: 5
   - B) Number squared: 25
   - C) Number squared: 10
   - D) Error
   - **Answer: B**

5. **Which C++ object is used to read input from the console?**
   - A) `std::cin`
   - B) `std::cout`
   - C) `std::string`
   - D) `std::endl`
   - **Answer: A**

6. **What is the correct way to include the string library in a C++ program?**
   - A) `#include <string.h>`
   - B) `#include <string>`
   - C) `#include "string"`
   - D) `#import <string>`
   - **Answer: B**

—


### Lesson 5: Conditional Statements and Loops in C++

#### Introduction

In programming, conditional statements and loops allow us to control the flow of execution. They enable us to make decisions and repeat actions. In this lesson, we'll explore these concepts in C++, with a particular focus on the "for" loop.

#### Conditional Statements

Conditional statements like `if`, `else if`, and `else` allow us to execute different code blocks based on conditions. Here's a simple example:

```cpp
if (x > 10) {
    std::cout << "x is greater than 10";
} else {
    std::cout << "x is not greater than 10";
}
```

#### The "for" Loop

The "for" loop is a powerful control structure in C++. It consists of three parts: initialization, condition (invariant), and increment. Here's the syntax:

```cpp
for (initialization; condition; increment) {
    // code to be executed
}
```

- **Initialization**: Sets up the loop variable.
- **Condition**: Checked before each iteration. If false, the loop ends.
- **Increment**: Updates the loop variable after each iteration.

Having initialization, invariant, and increment in the same instruction is crucial for debugging purposes. It encapsulates the loop's control logic, making it easier to understand and maintain.

### Switch Statements, Break/Continue, and Scope in C++

Here's an overview that could be added to Lesson 5:

- **Switch Statements**: The `switch` statement provides a way to handle multiple conditions based on the value of an expression. It can be more concise than a series of `if-else` statements for specific cases.

  ```cpp
  int choice = 2;
  switch (choice) {
      case 1:
          std::cout << "Option 1 selected";
          break;
      case 2:
          std::cout << "Option 2 selected";
          break;
      default:
          std::cout << "Invalid option";
  }
  ```

- **Break and Continue**: The `break` keyword is used to exit a loop or switch statement immediately, while the `continue` keyword skips the rest of the current iteration and continues with the next one.

  ```cpp
  for (int i = 0; i < 10; ++i) {
      if (i % 2 == 0) continue; // Skip even numbers
      std::cout << i << " "; // Prints odd numbers
  }
  ```

- **Scope**: Understanding the scope of variables within loops and conditional statements is essential. Variables declared within a block (enclosed by `{}`) are only accessible within that block.

  ```cpp
  if (true) {
      int x = 42; // x is only accessible within this block
  }
  // x is out of scope here
  ```

- **Ternary Operator**: The ternary operator (`?:`) provides a shorthand way to perform conditional assignments. It can make code more concise in specific situations.

  ```cpp
  int max = (a > b) ? a : b; // Assigns the greater of a and b to max
  ```

#### Extended Example: Guess a Number

Let's explore an extended version of the "guess a number" game. We'll use a "for" loop to limit the number of attempts and provide feedback on whether the guess is too high or too low.

```cpp
#include <iostream>

int main() {
    int secretNumber = 42;
    int attempts = 5;

    for (int i = 0; i < attempts; i++) {
        int guess;
        std::cout << "Guess the number: ";
        std::cin >> guess;

        if (guess == secretNumber) {
            std::cout << "Congratulations! You guessed it!\n";
            break;
        } else if (guess < secretNumber) {
            std::cout << "Too low! Try again.\n";
        } else {
            std::cout << "Too high! Try again.\n";
        }
    }

    return 0;
}
```

#### Other Loop Constructs

- **do/while Loop**: Similar to the "while" loop but checks the condition after executing the loop body at least once.
- **goto Statement**: Although still supported in C++, the use of `goto` is highly discouraged as it can lead to unreadable and error-prone code.

#### Conclusion

Understanding conditional statements and loops is essential for creating dynamic and responsive programs. The "for" loop, in particular, is a versatile and powerful tool that encapsulates control logic, aiding in debugging and maintenance.

In the next lesson, we'll delve into functions and recursion, further expanding your ability to create modular and reusable code.

---

1. **What is the output of the following code snippet with an off-by-one error?**
   ```cpp
   for (int i = 0; i <= 5; i++) {
       std::cout << i << " ";
   }
   ```
   - A) 0 1 2 3 4
   - B) 0 1 2 3 4 5
   - C) 1 2 3 4 5
   - D) 0 1 2 3 4 5 6
   - **Answer: B**

2. **In a "for" loop, what is the purpose of the initialization part?**
   - A) To update the loop variable
   - B) To check the loop condition
   - C) To set up the loop variable
   - D) To end the loop
   - **Answer: C**

3. **Which part of the "for" loop is checked before each iteration?**
   - A) Initialization
   - B) Increment
   - C) Condition
   - D) None of the above
   - **Answer: C**

4. **What is the correct syntax for a "for" loop that runs 10 times?**
   - A) `for (int i = 0; i < 10; i++)`
   - B) `for (int i = 0; i <= 10; i++)`
   - C) `for (int i = 1; i < 10; i++)`
   - D) `for (int i = 1; i <= 10; i++)`
   - **Answer: A**

5. **What is the purpose of the increment part in a "for" loop?**
   - A) To set up the loop variable
   - B) To check the loop condition
   - C) To update the loop variable after each iteration
   - D) To end the loop
   - **Answer: C**

6. **Which statement is true regarding the "goto" statement in C++?**
   - A) It is highly encouraged for code readability
   - B) It is not supported in C++
   - C) It is highly discouraged as it can lead to unreadable code
   - D) It is used to define functions
   - **Answer: C**

7. **What will the following code snippet print if the user enters 42?**
   ```cpp
   int guess;
   std::cout << "Guess the number: ";
   std::cin >> guess;
   if (guess < 42) {
       std::cout << "Too low!";
   } else if (guess > 42) {
       std::cout << "Too high!";
   } else {
       std::cout << "Correct!";
   }
   ```
   - A) Too low!
   - B) Too high!
   - C) Correct!
   - D) Error
   - **Answer: C**

---

### Lesson 6: Functions and Recursion

#### Introduction

Functions are one of the fundamental building blocks in programming. They are a type of subprogram that allows us to encapsulate a specific task or responsibility within our code. In this lesson, we'll explore the concept of functions, how they help in organizing code, and the principles of recursion and functional programming in C++.

#### Functions: The Basics

A function is a self-contained block of code that encapsulates a specific task or calculation. It can take input, perform its task, and then send output. Here's a simple example:

```cpp
int add(int a, int b) {
    return a + b;
}
```

#### Why Use Functions?

1. **Organization**: Functions help keep the program well organized by grouping related code together.
2. **Reusability**: Functions allow us to write code once and reuse it in different parts of the program.
3. **Responsibility Management**: Functions keep responsibilities in check by encapsulating specific tasks.

#### Recursion

Recursion is a technique where a function calls itself. It's particularly useful for problems that can be broken down into smaller, similar problems. Here's an example of a recursive function to calculate the factorial of a number:

```cpp
int factorial(int n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}
```

### Passing Parameters: By Reference vs. By Value

In C++, when we call a function, we can pass the parameters either by value or by reference. Understanding the difference between these two methods is crucial for effective programming.

#### Passing by Value

When we pass a parameter by value, a copy of the value is passed to the function. Any changes made to the parameter inside the function do not affect the original value outside the function.

Example:

```cpp
void incrementByValue(int a) {
    a = a + 1;
}

int main() {
    int x = 5;
    incrementByValue(x);
    std::cout << x; // Output will be 5, x is unchanged
}
```

#### Passing by Reference

When we pass a parameter by reference, we are passing a reference to the actual variable, not a copy. Any changes made to the parameter inside the function will affect the original value outside the function.

Example:

```cpp
void incrementByReference(int &a) {
    a = a + 1;
}

int main() {
    int x = 5;
    incrementByReference(x);
    std::cout << x; // Output will be 6, x is incremented
}
```

#### Comparison

- **By Value**: Safe but may be inefficient for large data. Changes inside the function do not affect the original value.
- **By Reference**: More efficient for large data. Changes inside the function affect the original value.



#### Pure Functions and Functional Programming

Pure functions are a core concept in functional programming, a popular programming style in C++. A pure function:

- Has no side effects (doesn't change anything in the program's state).
- Always produces the same output for the same input.

Here's an example of a pure function:

```cpp
int multiply(int x, int y) {
    return x * y; // Pure function: no side effects, same output for same input
}
```

Functional programming emphasizes the use of pure functions, immutability, and declarative code. It leads to more predictable and maintainable code.

### Function Overloading, Default Arguments, Inline Functions, and Function Pointers in C++

Here's an overview that could be added to Lesson 6:

- **Function Overloading**: C++ allows defining multiple functions with the same name but different parameters. This enables more flexible and intuitive function usage.

  ```cpp
  void print(int i) { std::cout << "Integer: " << i; }
  void print(double d) { std::cout << "Double: " << d; }
  ```

- **Default Arguments**: Functions can have default values for some or all of their parameters, allowing more flexible calling.

  ```cpp
  void display(int x, int y = 10) { /* ... */ }
  display(5); // y will be 10
  ```

- **Inline Functions**: Declaring a function as `inline` suggests to the compiler that it should attempt to generate inline code to reduce function call overhead. It's commonly used for small, frequently called functions.

  ```cpp
  inline int square(int x) { return x * x; }
  ```

- **Function Pointers and `std::function`**: C++ supports pointers to functions, allowing functions to be passed as arguments, stored in variables, etc. The `std::function` from the `<functional>` header provides a more flexible way to handle callable objects.

  ```cpp
  int add(int a, int b) { return a + b; }
  int (*func_ptr)(int, int) = add; // Function pointer
  std::function<int(int, int)> func = add; // Using std::function
  ```

- **Lambda Expressions**: Although mentioned in the lesson, further exploration of lambda expressions, closures, and capturing could provide a deeper understanding of modern C++ programming.

  ```cpp
  auto lambda = [x](int y) { return x + y; }; // Lambda with capture
  ```


#### Conclusion

Functions and recursion are powerful tools in C++. They help us organize our code, manage responsibilities, and even adopt popular programming paradigms like functional programming. Understanding pure functions and the principles of functional programming can further enhance your ability to write clean and efficient code in C++.

Understanding how to pass parameters by reference or by value is essential in C++. Passing by reference allows for more efficient code and direct manipulation of the original variable, while passing by value provides safety by working with a copy of the data.

In the next lesson, we'll explore arrays, smart pointers, and modern containers, diving deeper into the world of C++.

—


1. **What is the primary purpose of using functions in programming?**
   - A) To increase code complexity
   - B) To organize and encapsulate specific tasks
   - C) To create infinite loops
   - D) To generate random numbers
   - **Answer: B**

2. **Which of the following is true about pure functions?**
   - A) They always change the program's state
   - B) They produce different outputs for the same input
   - C) They have no side effects and produce the same output for the same input
   - D) They are only used in object-oriented programming
   - **Answer: C**

3. **What is the output of the following recursive function if called with `factorial(5)`?**
   ```cpp
   int factorial(int n) {
       if (n <= 1) return 1;
       return n * factorial(n - 1);
   }
   ```
   - A) 120
   - B) 24
   - C) 5
   - D) Infinite loop
   - **Answer: A**

4. **Which code modification will prevent the following recursive function from ending up in infinite recursion?**
   ```cpp
   int recursive(int n) {
       // Missing base case
       return n * recursive(n - 1);
   }
   ```
   - A) Add `if (n == 0) return 1;` at the beginning
   - B) Change `n - 1` to `n + 1`
   - C) Remove the return statement
   - D) Change `int n` to `float n`
   - **Answer: A**

5. **When passing a parameter by reference, what happens to the original variable outside the function if it's modified inside the function?**
   - A) It remains unchanged
   - B) It is also modified
   - C) It is deleted
   - D) It becomes a constant
   - **Answer: B**

6. **What is the main advantage of passing parameters by value?**
   - A) It modifies the original variable
   - B) It is more efficient for large data
   - C) It provides safety by working with a copy of the data
   - D) It allows for infinite recursion
   - **Answer: C**

7. **Which of the following is NOT a benefit of functional programming?**
   - A) Emphasizes the use of pure functions
   - B) Leads to more predictable code
   - C) Encourages the use of global variables
   - D) Enhances maintainability
   - **Answer: C**

—

### Lesson 7: Arrays and Smart Pointers in C++

#### Introduction

In this lesson, we'll explore arrays and smart pointers in modern C++, emphasizing the importance of clear rules for memory ownership and how the current standards of C++ have improved upon the original language.

#### Modern Arrays in C++

Modern C++ provides convenient ways to work with arrays, such as the `std::array` and `std::vector` containers. These containers provide safety, flexibility, and ease of use.

Example using `std::vector`:

```cpp
#include <vector>

int main() {
    std::vector<int> numbers = {1, 2, 3, 4};
    numbers.push_back(5); // Easily add elements
}
```

#### Legacy C++ Arrays

In legacy C++ code, arrays were handled using raw pointers, leading to potential issues with memory management and safety. Here's a brief example:

```cpp
int* numbers = new int[5]; // Allocation
delete[] numbers; // Deallocation
```

Modern C++ discourages this approach in favor of safer alternatives.

#### Smart Pointers

Smart pointers are a powerful feature in modern C++ that helps manage memory ownership. They automatically handle the allocation and deallocation of memory, reducing the risk of memory leaks.

- **`std::unique_ptr`**: Owns the memory exclusively.
- **`std::shared_ptr`**: Allows shared ownership.

Example using `std::unique_ptr`:

```cpp
#include <memory>

int main() {
    std::unique_ptr<int> number = std::make_unique<int>(42);
}
```

#### Importance of Clear Rules for Memory Ownership

Clear rules for memory ownership are vital for writing robust and maintainable code. They help prevent common issues such as:

- Memory leaks
- Dangling pointers
- Undefined behavior

Modern C++ standards provide tools and practices that enforce clear ownership rules, leading to better quality software.

#### How Modern C++ Improves Upon the Original Language

Modern C++ has introduced several enhancements that lead to better quality software:

- **Safety**: Features like smart pointers reduce the risk of memory-related errors.
- **Performance**: Modern containers provide efficient memory management.
- **Readability**: Clear syntax and standard practices enhance code readability and maintainability.
- **Flexibility**: Modern C++ offers versatile tools for various programming paradigms.

### Range-Based Loops, `std::array`, `std::make_shared`, `std::make_unique`, and Ownership Semantics in C++

Here's an overview that could be added to Lesson 7:

- **Range-Based Loops**: Modern C++ introduced range-based `for` loops, which simplify iterating over containers like arrays and vectors.

  ```cpp
  int numbers[] = {1, 2, 3};
  for (int number : numbers) {
      std::cout << number << " ";
  }
  ```

- **`std::array`**: The `std::array` container provides a safer and more convenient alternative to C-style arrays.

  ```cpp
  #include <array>
  std::array<int, 3> numbers = {1, 2, 3};
  ```

- **`std::make_shared` and `std::make_unique`**: These functions simplify the creation of smart pointers and are more efficient than using `new`.

  ```cpp
  auto shared_ptr = std::make_shared<MyClass>();
  auto unique_ptr = std::make_unique<MyClass>();
  ```

- **Ownership Semantics**: Understanding ownership is crucial when working with pointers in C++. Ownership defines who is responsible for managing the memory of an object. Smart pointers like `std::shared_ptr` and `std::unique_ptr` automate ownership management, reducing the risk of memory leaks.

  ```cpp
  std::unique_ptr<MyClass> owner = std::make_unique<MyClass>();
  // Ownership can be transferred
  std::unique_ptr<MyClass> new_owner = std::move(owner);
  ```

- **Move Semantics**: A brief introduction to move semantics and how it relates to smart pointers could enhance understanding.

  ```cpp
  MyClass obj;
  std::unique_ptr<MyClass> ptr = std::make_unique<MyClass>(std::move(obj)); // Move constructor
  ```


#### Conclusion

Arrays and smart pointers in modern C++ represent a significant advancement over legacy practices. By embracing modern standards and understanding the importance of clear rules for memory ownership, developers can create safer, more efficient, and maintainable software.

In the next lesson, we'll delve into Object-Oriented Programming (OOP) in C++, exploring concepts like classes, inheritance, and polymorphism.

---

1. **What is the main advantage of using `std::vector` over raw pointers for arrays in modern C++?**
   - A) It allows infinite array size
   - B) It provides safety, flexibility, and ease of use
   - C) It only works with integers
   - D) It requires manual memory management
   - **Answer: B**

2. **Which smart pointer in C++ allows shared ownership of memory?**
   - A) `std::unique_ptr`
   - B) `std::shared_ptr`
   - C) `std::vector`
   - D) `std::array`
   - **Answer: B**

3. **What is the primary purpose of smart pointers in modern C++?**
   - A) To increase code complexity
   - B) To automatically handle memory allocation and deallocation
   - C) To create infinite loops
   - D) To generate random numbers
   - **Answer: B**

4. **Why are clear rules for memory ownership important in C++ programming?**
   - A) They enhance code performance
   - B) They prevent issues like memory leaks and dangling pointers
   - C) They allow infinite array size
   - D) They require manual memory management
   - **Answer: B**

5. **Which of the following is NOT a benefit of modern C++ over legacy C++?**
   - A) Improved safety through features like smart pointers
   - B) Enhanced code readability and maintainability
   - C) Requirement for manual memory management
   - D) Versatile tools for various programming paradigms
   - **Answer: C**

6. **How does `std::unique_ptr` differ from `std::shared_ptr`?**
   - A) `std::unique_ptr` allows shared ownership, while `std::shared_ptr` owns memory exclusively
   - B) `std::unique_ptr` owns memory exclusively, while `std::shared_ptr` allows shared ownership
   - C) Both allow shared ownership
   - D) Both own memory exclusively
   - **Answer: B**

7. **What potential issue can arise from using raw pointers for arrays in legacy C++ code?**
   - A) Increased code readability
   - B) Automatic memory management
   - C) Potential issues with memory management and safety
   - D) Enhanced performance
   - **Answer: C**

8. **Which modern C++ container provides a fixed-size array?**
   - A) `std::vector`
   - B) `std::array`
   - C) `std::unique_ptr`
   - D) `std::shared_ptr`
   - **Answer: B**

---


### Lesson 8: Object-Oriented Programming (OOP) in C++

#### Introduction

Object-Oriented Programming (OOP) is a programming paradigm that uses objects to organize code into reusable and maintainable structures. In this lesson, we'll explore the principles of OOP, how C++ supports them, and delve into advanced concepts like pure virtual methods.

#### Principles of OOP

OOP is based on four main principles:

1. **Encapsulation**: Bundling data and methods that operate on that data within a single unit (class), restricting direct access to some of the object's components.

2. **Inheritance**: Creating a new class that is based on an existing class, allowing code reusability.

3. **Polymorphism**: Allowing objects of different types to be treated as objects of a common type, enhancing flexibility.

4. **Abstraction**: Hiding complex reality while exposing only essential parts.

#### OOP in C++

C++ fully supports OOP, providing tools to implement these principles:

- **Classes**: Define the blueprint for objects.
- **Virtual Functions**: Enable polymorphism.
- **Access Specifiers**: Control encapsulation (public, private, protected).

#### Pure Virtual Methods

Pure virtual methods are used to create abstract classes in C++. An abstract class cannot be instantiated and must be derived by other classes.

Example:

```cpp
class Shape {
public:
    virtual void draw() const = 0; // Pure virtual method
};

class Circle : public Shape {
public:
    void draw() const override {
        // Draw the circle
    }
};

int main() {
    Shape* shape = new Circle();
    shape->draw(); // Calls Circle's draw method
    delete shape;
}
```

#### Warning: Challenges in OOP Design

Designing OOP software can sometimes lead to unnecessary stiffness in a hierarchy or difficulty in adding features after the fact. It's essential to find the right balance and avoid over-engineering.

#### Importance of the Open/Close Pattern

The Open/Close Pattern is a fundamental principle in OOP that states:

- **Open for Extension**: You can add new functionality without changing the existing code.
- **Closed for Modification**: Once developed, the class's behavior should not be altered.

This pattern promotes stability, flexibility, and maintainability in software design.

#### Conclusion

Object-Oriented Programming in C++ provides a powerful way to structure code, promoting reusability, maintainability, and flexibility. Understanding the principles, utilizing pure virtual methods, and being mindful of potential design challenges are key to effective OOP in C++.

In the next lesson, we'll explore file handling in C++, including reading, writing, and working with the filesystem library.

---

1. **Which of the following is NOT one of the four main principles of OOP?**
   - A) Encapsulation
   - B) Inheritance
   - C) Compilation
   - D) Polymorphism
   - **Answer: C**

2. **What is a pure virtual method in C++?**
   - A) A method that can be overridden in any class
   - B) A method that must be implemented in derived classes
   - C) A method that cannot be called
   - D) A method that can only be private
   - **Answer: B**

3. **What does the Open/Close Pattern promote in OOP?**
   - A) Open for Modification, Closed for Extension
   - B) Open for Extension, Closed for Modification
   - C) Open for Debugging, Closed for Testing
   - D) Open for Execution, Closed for Compilation
   - **Answer: B**

4. **Which access specifier in C++ restricts access to a class's members from outside the class?**
   - A) public
   - B) protected
   - C) private
   - D) encapsulated
   - **Answer: C**

5. **Why is abstraction important in OOP?**
   - A) It allows infinite loops
   - B) It hides complex reality while exposing essential parts
   - C) It requires manual memory management
   - D) It increases code complexity
   - **Answer: B**

6. **What potential challenge can arise from over-engineering in OOP design?**
   - A) Increased code readability
   - B) Unnecessary stiffness in a hierarchy
   - C) Automatic memory management
   - D) Enhanced performance
   - **Answer: B**

7. **Which principle of OOP allows objects of different types to be treated as objects of a common type?**
   - A) Encapsulation
   - B) Inheritance
   - C) Polymorphism
   - D) Abstraction
   - **Answer: C**

8. **What is the main purpose of encapsulation in OOP?**
   - A) To allow public access to all class members
   - B) To bundle data and methods within a single unit
   - C) To create infinite loops
   - D) To generate random numbers
   - **Answer: B**

---

### Lesson 9: File Handling in C++

#### Introduction

File handling is a crucial aspect of programming, allowing programs to store, retrieve, and manipulate data. In this lesson, we'll explore how to manage files in C++, including reading, writing, and working with directory classes from the C++ Standard Library.

#### Reading and Writing Files

C++ provides robust support for file operations through the `<fstream>` library. Here's how you can read and write files:

##### Reading from a File

```cpp
#include <fstream>
#include <iostream>
#include <string>

int main() {
    std::ifstream file("example.txt");
    std::string line;
    while (std::getline(file, line)) {
        std::cout << line << '\n';
    }
    // File is automatically closed when 'file' goes out of scope
}
```

##### Writing to a File

```cpp
#include <fstream>

int main() {
    std::ofstream file("example.txt");
    file << "Hello, World!";
    // File is automatically closed when 'file' goes out of scope
}
```

#### Resource Acquisition Is Initialization (RAII)

RAII is a programming idiom used in C++ where the resource acquisition (such as opening a file) is done during object initialization, and the resource release (such as closing the file) is done during object destruction. This ensures that resources are properly managed and released, even in cases of exceptions.

With RAII, you don't have to explicitly close the file, as it will be automatically closed when the file object goes out of scope. This makes the code more robust and less prone to resource leaks.

#### Working with Directories

The C++ Standard Library includes the `<filesystem>` header, allowing you to work with directories and paths. To compile code using this library, you may need to add the `-std=c++17` flag.

##### Example: Listing Files in a Directory

```cpp
#include <iostream>
#include <filesystem>

int main() {
    std::filesystem::path path = ".";
    for (const auto &entry : std::filesystem::directory_iterator(path)) {
        std::cout << entry.path() << '\n';
    }
    return 0;
}
```

Compile with:

```bash
g++ -std=c++17 your_file.cpp -o output
```

#### Conclusion

File handling in C++ is versatile and powerful, allowing you to read, write, and manage files and directories with ease. By leveraging the C++ Standard Library and utilizing RAII, you can create efficient and portable code for various file operations.

In the next lesson, we'll explore the C++ Standard Library, including containers, algorithms, iterators, and more.

—

#### Question 1: Reading from a File

What will the following code snippet print if the file "example.txt" contains the text "Hello, World!"?

```cpp
#include <fstream>
#include <iostream>
#include <string>

int main() {
    std::ifstream file("example.txt");
    std::string line;
    std::getline(file, line);
    std::cout << line;
}
```

A) An error message  
B) Nothing  
C) "Hello, World!"  
D) "example.txt"

**Answer: C) "Hello, World!"**

#### Question 2: RAII and File Handling

Which statement is true regarding RAII (Resource Acquisition Is Initialization) in C++ file handling?

A) RAII requires explicit closing of files  
B) RAII leads to memory leaks  
C) RAII automatically closes files when the corresponding variable goes out of scope  
D) RAII is only applicable to reading files

**Answer: C) RAII automatically closes files when the corresponding variable goes out of scope**

#### Question 3: Writing to a File

What will the following code snippet do?

```cpp
#include <fstream>

int main() {
    std::ofstream file("output.txt");
    file << "C++ Rocks!";
}
```

A) Read the content of "output.txt"  
B) Write "C++ Rocks!" to the console  
C) Write "C++ Rocks!" to the file "output.txt"  
D) Delete "output.txt"

**Answer: C) Write "C++ Rocks!" to the file "output.txt"**

#### Question 4: Working with Directories

Which header must be included to work with directories in C++17?

A) `<directory>`  
B) `<filesystem>`  
C) `<path>`  
D) `<folder>`

**Answer: B) `<filesystem>`**

#### Question 5: Compiling with C++17

What is the correct command to compile a C++ file using the C++17 standard?

A) `g++ -std=c++11 your_file.cpp -o output`  
B) `g++ -std=c++17 your_file.cpp -o output`  
C) `g++ -std=c++14 your_file.cpp -o output`  
D) `g++ your_file.cpp -o output`

**Answer: B) `g++ -std=c++17 your_file.cpp -o output`**

---

### Lesson 10: Introduction to the C++ Standard Library

#### Introduction

The C++ Standard Library is a powerful set of C++ template classes to provide general-purpose classes and functions with templates that implement many popular and commonly used algorithms and data structures. In this lesson, we'll explore some of the most commonly used components, including containers, algorithms, optional values, and time handling.

#### Containers

##### std::vector

`std::vector` is a dynamic array that can grow and shrink in size. It provides random access to elements.

```cpp
#include <vector>

std::vector<int> numbers = {1, 2, 3};
numbers.push_back(4); // Adds 4 to the end
```

##### std::list

`std::list` is a doubly-linked list that allows efficient insertions and deletions.

```cpp
#include <list>

std::list<int> numbers = {10, 20, 30};
numbers.push_front(5); // Adds 5 to the beginning
```

##### std::unordered_map

`std::unordered_map` is a hash table that maps keys to values.

```cpp
#include <unordered_map>

std::unordered_map<std::string, int> ages = {{"Alice", 30}, {"Bob", 25}};
ages["Charlie"] = 22; // Adds a new key-value pair
```

##### std::optional

`std::optional` represents an optional value that may or may not be present.

```cpp
#include <optional>

std::optional<int> maybeValue = 42;
if (maybeValue) {
    // Value is present
}
```

#### Algorithms

The `<algorithm>` header provides a collection of functions for various algorithms.

```cpp
#include <algorithm>
#include <vector>

std::vector<int> numbers = {3, 1, 4, 1, 5, 9};

std::sort(numbers.begin(), numbers.end()); // Sorting
std::reverse(numbers.begin(), numbers.end()); // Reversing
int sum = std::accumulate(numbers.begin(), numbers.end(), 0); // Summing
bool exists = std::binary_search(numbers.begin(), numbers.end(), 4); // Binary search
```

#### Time Handling with `<chrono>`

The `<chrono>` header provides utilities to deal with time.

```cpp
#include <chrono>
#include <iostream>

auto start = std::chrono::high_resolution_clock::now();
// Code to be timed
auto end = std::chrono::high_resolution_clock::now();
auto duration = std::chrono::duration_cast<std::chrono::milliseconds>(end - start);
std::cout << "Time taken: " << duration.count() << "ms\n";
```

#### C++ Library Headers

The C++ Standard Library includes a wide variety of headers. Here's a comprehensive list of C++ Standard Library headers, categorized by functionality:

#### Containers
- `<vector>`
- `<list>`
- `<deque>`
- `<queue>`
- `<stack>`
- `<map>`
- `<set>`
- `<unordered_map>`
- `<unordered_set>`

#### Algorithms
- `<algorithm>`

#### Strings
- `<string>`

#### Input/Output Streams
- `<iostream>`
- `<fstream>`
- `<sstream>`

#### Numerics
- `<complex>`
- `<random>`
- `<numeric>`
- `<valarray>`

#### Time and Date
- `<chrono>`
- `<ctime>`

#### Threading
- `<thread>`
- `<mutex>`
- `<future>`
- `<condition_variable>`

#### Memory Management
- `<memory>`
- `<new>`
- `<scoped_allocator>`

#### Language Support
- `<typeinfo>`
- `<type_traits>`
- `<tuple>`
- `<initializer_list>`
- `<limits>`
- `<exception>`
- `<stdexcept>`

#### Localization
- `<locale>`

#### Regular Expressions
- `<regex>`

#### Filesystem (C++17 and later)
- `<filesystem>`

#### Miscellaneous
- `<bitset>`
- `<functional>`
- `<iterator>`
- `<optional>`
- `<any>`
- `<variant>`
- `<ratio>`
- `<utility>`
- `<system_error>`

This list covers most of the standard headers in the C++ Standard Library. Some headers may be specific to certain C++ standards, so it's essential to refer to the appropriate documentation for the version of C++ you are using.

#### Conclusion

The C++ Standard Library offers a rich set of tools that simplify many common programming tasks. By understanding and utilizing these tools, you can write more concise, efficient, and maintainable code.

In the next course, we'll continue to explore more advanced topics in C++. Stay tuned!

---

1. **What is the primary purpose of the `std::vector` container?**
   - A) Hash table
   - B) Doubly-linked list
   - C) Dynamic array
   - D) Stack
   - **Answer: C**

2. **Which header must be included to use the `std::sort` function?**
   - A) `<vector>`
   - B) `<list>`
   - C) `<algorithm>`
   - D) `<numeric>`
   - **Answer: C**

3. **What does the following code snippet do?**
   ```cpp
   std::optional<int> value = 42;
   if (value) {
       // ...
   }
   ```
   - A) Checks if `value` is 42
   - B) Checks if `value` is present
   - C) Checks if `value` is null
   - D) Compiles with an error
   - **Answer: B**

4. **Which container provides constant time insertion and deletion at both ends?**
   - A) `std::vector`
   - B) `std::list`
   - C) `std::deque`
   - D) `std::set`
   - **Answer: C**

5. **What is the output of the following code?**
   ```cpp
   std::unordered_map<std::string, int> ages = {{"Alice", 30}, {"Bob", 25}};
   std::cout << ages["Charlie"];
   ```
   - A) 0
   - B) 25
   - C) 30
   - D) Undefined behavior
   - **Answer: A**

6. **Which header is used to work with time in C++?**
   - A) `<time>`
   - B) `<chrono>`
   - C) `<date>`
   - D) `<calendar>`
   - **Answer: B**

7. **What is the primary advantage of using `std::optional`?**
   - A) It allows null values
   - B) It provides optional typing
   - C) It represents an optional value that may or may not be present
   - D) It optimizes memory usage
   - **Answer: C**

8. **Which of the following is NOT a principle of Object-Oriented Programming (OOP)?**
   - A) Encapsulation
   - B) Inheritance
   - C) Polymorphism
   - D) Multithreading
   - **Answer: D**

9. **Which C++ Standard Library header provides functionalities for multithreading?**
   - A) `<thread>`
   - B) `<mutex>`
   - C) `<future>`
   - D) All of the above
   - **Answer: D**

10. **What is RAII in C++?**
    - A) A design pattern for managing resources
    - B) A library for artificial intelligence
    - C) A method for error handling
    - D) A technique for optimizing code
    - **Answer: A**


