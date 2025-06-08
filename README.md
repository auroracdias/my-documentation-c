# Documenting My Studies in C

This document tracks my learning journey in the C programming language.

---

## 1. Introducing C

### Structure of a C Program — "Hello, World!"

```c
// hello.c

// Include standard input/output library
#include <stdio.h>

// Entry point of every C program
int main(void) {
    // Print message with line break
    printf("Hello, World!\n");  // \n moves the cursor to the next line

    // Return 0 indicates successful execution
    return 0;
} // End of main function
```

---

### What is `#include`?

In C, `#include` is used to **import code from a library** into your program.

It's like copying and pasting a bunch of useful tools that someone else already wrote so you don't have to reinvent the wheel.

For example:

```c
#include <stdio.h>
```

This line brings in the **standard input/output library**, giving you access to functions like `printf()` (which prints text to the screen).

If you remove it, the compiler won't know what `printf()` is, and you'll get an error.

Here are a few other useful libraries:

* `<stdlib.h>`: memory allocation, conversions, etc.
* `<string.h>`: string manipulation functions
* `<math.h>`: math functions like `sqrt()`, `pow()`

---

## 2. Compilation and Execution

To compile and run the program, use the following command:

```bash
gcc hello.c -o hello
```

### Explanation:

* **`gcc`**: The GNU Compiler Collection, used to compile C code.

  * On **Linux/macOS**: Usually pre-installed.
  * On **Windows**: Install via [MinGW](https://www.mingw-w64.org/) or use compilers like Clang.

* **`hello.c`**: Source file containing your C code.

* **`-o hello`**: Specifies the name of the output file (in this case, `hello`).

  * If omitted, the default output file is `a.out`.

---

## 3. Running the Program

### On Linux/macOS:

```bash
./hello
```

* The `./` tells the shell to look for the executable in the current directory.

### On Windows:

```bash
hello.exe
```

* Or simply double-click `hello.exe` in File Explorer.

---

## 4. Data Input and Output

Data input and output operations in C are mainly done using functions like `printf` and `scanf`.

### Using `printf()`

The `printf()` function is used to display output on the screen. You can format the output using **format specifiers** and **escape sequences**.

#### Format Specifiers

|   Specifier  | Description                     |
| :----------: | ------------------------------- |
| `%d` or `%i` | Whole numbers in decimal format |
|     `%x`     | Integers in hexadecimal format  |
|     `%f`     | Floating-point numbers          |
|     `%e`     | Numbers in scientific notation  |
|     `%c`     | Single alphanumeric character   |
|     `%s`     | Sequence of characters (string) |

#### Escape Sequences

Escape sequences are special characters used to control formatting in strings:

| Escape | Description                    |
| :----: | ------------------------------ |
|  `\a`  | Alert (bell sound)             |
|  `\b`  | Backspace                      |
|  `\n`  | New line                       |
|  `\t`  | Horizontal tab                 |
|  `\r`  | Carriage return                |
|  `\0`  | Null character (end of string) |
|  `\v`  | Vertical tab                   |

---

## 5. Reading Input with `scanf()`

To read input from the user, we use the `scanf()` function. Here's a basic example:

```c
#include <stdio.h>

int main() {
    int age;
    printf("Enter your age: ");
    scanf("%d", &age); // &age gets the address of the variable
    printf("You are %d years old.\n", age);
    return 0;
}
```

### Important Notes:

* Always match the format specifier with the variable type.
* The `&` (ampersand) symbol is used to provide the memory address of the variable where the input will be stored.

---

## 6. Expressions and Operators

### Arithmetic and Unary Operators

| Operator | Description         | Example |
| -------- | ------------------- | ------- |
| `+`      | Addition            | `a + b` |
| `-`      | Subtraction         | `a - b` |
| `*`      | Multiplication      | `a * b` |
| `/`      | Division            | `a / b` |
| `%`      | Modulus (remainder) | `a % b` |
| `-x`     | Unary minus         | `-x`    |
| `+x`     | Unary plus          | `+x`    |

### Relational and Logical Operators

| Operator | Description      | Example          |            |         |   |         |
| -------- | ---------------- | ---------------- | ---------- | ------- | - | ------- |
| `==`     | Equal to         | `a == b`         |            |         |   |         |
| `!=`     | Not equal to     | `a != b`         |            |         |   |         |
| `>`      | Greater than     | `a > b`          |            |         |   |         |
| `<`      | Less than        | `a < b`          |            |         |   |         |
| `>=`     | Greater or equal | `a >= b`         |            |         |   |         |
| `<=`     | Less or equal    | `a <= b`         |            |         |   |         |
| `&&`     | Logical AND      | `a > 0 && b > 0` |            |         |   |         |
| \`       |                  | \`               | Logical OR | \`a > 0 |   | b > 0\` |
| `!`      | Logical NOT      | `!a`             |            |         |   |         |

### Increment and Decrement

| Operator | Description                     | Example |
| -------- | ------------------------------- | ------- |
| `++x`    | Pre-increment (increment first) | `++x`   |
| `x++`    | Post-increment (use then inc)   | `x++`   |
| `--x`    | Pre-decrement (decrement first) | `--x`   |
| `x--`    | Post-decrement (use then dec)   | `x--`   |

### Compound Assignment Operators

| Operator | Equivalent To | Example  |
| -------- | ------------- | -------- |
| `x += y` | `x = x + y`   | `x += 5` |
| `x -= y` | `x = x - y`   | `x -= 2` |
| `x *= y` | `x = x * y`   | `x *= 3` |
| `x /= y` | `x = x / y`   | `x /= 4` |
| `x %= y` | `x = x % y`   | `x %= 2` |

---
