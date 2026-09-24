# 🧮 Modular Scientific Calculator in C

A modular command-line calculator developed in **C** as a **Problem-Based Learning (PBL) project during the first year of college**.

The project goes beyond basic arithmetic by implementing separate modules for **algebraic operations, matrix operations, and trigonometric calculations**. The code is organized using `.c` and `.h` files to demonstrate modular programming and code separation.

## ✨ Features

### Basic Algebra

Supports the four fundamental arithmetic operations:

* Addition
* Subtraction
* Multiplication
* Division
* Division-by-zero handling

### Matrix Operations

The calculator supports:

* Matrix Addition
* Matrix Subtraction
* Matrix Multiplication
* Element-wise Matrix Division
* Dynamic matrix creation using `malloc()`
* Dynamic memory deallocation using `free()`
* Matrix dimension validation for multiplication

Matrix multiplication checks whether the number of columns in Matrix A matches the number of rows in Matrix B before performing the operation.

### Trigonometric Operations

Supports:

* Sine
* Cosine
* Tangent

Angles are entered in **degrees** and converted to radians internally before calculation.

## 🗂️ Project Structure

```text
├── main.c
├── algebra.c
├── algebra.h
├── matrix.c
├── matrix.h
├── trig.c
├── trig.h
└── README.md
```

### File Description

| File        | Description                                                       |
| ----------- | ----------------------------------------------------------------- |
| `main.c`    | Main program and calculator menu                                  |
| `algebra.c` | Implementation of basic arithmetic operations                     |
| `algebra.h` | Function declaration for the algebra module                       |
| `matrix.c`  | Matrix creation, input, output, arithmetic, and memory management |
| `matrix.h`  | Matrix function declarations                                      |
| `trig.c`    | Trigonometric calculations                                        |
| `trig.h`    | Trigonometric function declaration                                |
| `README.md` | Project documentation                                             |

The main program connects the three modules through their respective header files.

## 🧠 Concepts Used

This project was built using several fundamental concepts of C programming:

* Functions
* Header files
* Modular programming
* Structures of a multi-file C project
* Pointers
* Dynamic memory allocation
* 2D dynamic arrays
* `malloc()` and `free()`
* Conditional statements
* Loops
* `switch` statements
* Mathematical functions
* Input/output using `scanf()` and `printf()`

## 🔧 How It Works

When the program starts, the user is presented with a menu:

```text
1. Algebra operations
2. Matrix addition
3. Matrix subtraction
4. Matrix multiplication
5. Matrix division
6. Trigonometric operations
```

The selected operation is then passed to the appropriate module.

### Algebra Module

The algebra module accepts two numbers and allows the user to perform addition, subtraction, multiplication, or division. Division by zero is explicitly handled.

### Matrix Module

Matrices are dynamically allocated according to the dimensions entered by the user.

```c
int **mat = (int**)malloc(rows * sizeof(int*));
```

The module provides separate functions for creating, reading, printing, operating on, and freeing matrices.

Matrix multiplication uses the standard matrix multiplication algorithm:

```text
C[i][j] = Σ A[i][k] × B[k][j]
```

and checks that the matrix dimensions are compatible before performing the operation.

### Trigonometry Module

The trigonometry module accepts an angle in degrees, converts it to radians, and calculates sine, cosine, or tangent using the C math library.

## 💻 Example

```text
1. Algebra operations
2. Matrix addition
3. Matrix subtraction
4. Matrix multiplication
5. Matrix division
6. Trigonometric operations

Enter your choice for calculator: 1

Choose an operation:
1. Addition
2. Subtraction
3. Multiplication
4. Division

Enter your choice (1-4): 1
Enter first number: 25
Enter second number: 15

Result = 40.00
```

## 📚 Learning Outcomes

This project helped reinforce the fundamentals of C programming while introducing a more structured approach to software development.

Key learning outcomes included:

* Understanding how multi-file C programs are organized
* Separating functionality into independent modules
* Working with header files and function declarations
* Using pointers and dynamically allocated memory
* Implementing operations on dynamically sized matrices
* Using the C mathematical library
* Handling invalid operations such as division by zero
* Understanding basic input validation and dimension checking
* Managing dynamically allocated memory using `free()`

## 🎓 Project Context

**Project Type:** Problem-Based Learning (PBL)
**Academic Year:** First Year
**Language:** C
**Project Category:** Command-Line Application / Calculator

This project was developed as part of the first-year academic curriculum to apply fundamental programming concepts to a practical problem.
