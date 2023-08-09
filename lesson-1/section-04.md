### Section 4: Basic Syntax and Printing in C++

In this section, we'll introduce you to the fundamental syntax of C++ and guide you through writing your first C++ program that prints text to the console.

#### Understanding Basic Syntax:
- **Comments**: Learn how to add single-line (`//`) and multi-line (`/* */`) comments to your code.
- **Semicolons**: Understand the use of semicolons (`;`) to terminate statements in C++.
- **Code Blocks**: Familiarize yourself with the use of curly braces (`{}`) to define code blocks.

#### Writing Your First C++ Program:
1. **Create a New File**: In Visual Studio Code, create a new file named `hello.cpp`.
2. **Include Necessary Headers**: Add `#include <iostream>` at the beginning of the file to include the input-output stream library.
3. **Write the Main Function**: Define the main function using `int main() { }`.
4. **Add Print Statements**: Inside the main function, write `std::cout << "Hello, World!";` to print "Hello, World!" to the console.
5. **Compile the Code**: Use the compiler to compile the code with a command like `g++ hello.cpp -o hello`. Note that the compiler might show errors; you'll need to fix them before proceeding.
6. **Run the Program**: After fixing any errors, you'll get a binary that you can run using `./hello`.

#### Example Code:
```cpp
#include <iostream> // Include the input-output stream library

int main() {
    // This is a single-line comment
    std::cout << "Hello, World!"; // Print "Hello, World!" to the console
    return 0; // Return 0 to indicate successful execution
}
```

#### Practice Exercises:
- **Print Your Name**: Modify the example code to print your name to the console.
- **Print Multiple Lines**: Experiment with printing multiple lines of text using `std::cout`.

---

This section provides a gentle introduction to the basic syntax of C++, including comments, semicolons, and code blocks. It also guides you through writing, compiling, and running a simple program that prints text to the console. By the end of this lesson, you'll have a foundational understanding of C++ syntax and will be able to write simple print statements.
