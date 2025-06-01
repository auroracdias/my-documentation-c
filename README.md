# Documenting my studies in C
Documenting my learning in the C language

# Introducing C
## Structure of a C program (“Hello, World!”)

```c
// hello.c

// Includes library for I/O functions.
#include <stdio.h>

// Main function.
int main(void) {
    // Print message + line break
    printf("Hello, World!\n");  // \n move cursor to next line
    
    // Returns success code to OS
    return 0;
} // End of main block
```

## 🔧 Compilation and execution
```bash
gcc hello.c -o hello
```

* **`gcc`**: GNU compiler for C (installed by default on most Linux/macOS distros).
    * **Windows (Command Prompt/PowerShell)** If GCC is not installed, use MinGW (Windows version of GCC) or compilers like Clang.

* **`hello.c`**: Input file (source code).

* **`-o hello`**: Flag that defines the name of the output executable (hello).

    * If you omit `-o`, the compiler generates a file named `a.out` (default).

## ▶ Program Execution
### Linux/macOS
```bash
./hello
```
* `./`: Indicates that the following is not in the current directory.

### Windows
```bash
hello.exe
```

* Or double-click the **`hello.exe`** file in Explorer.
