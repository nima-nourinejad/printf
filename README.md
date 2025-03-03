# ft_printf: Because ft_putnbr() and ft_putstr() aren’t enough


The goal of this project is to recreate the functionality of the C standard library function `printf()`. This project introduces you to variadic functions in C, helping you better understand how to handle variable arguments and format specifiers.

### Project Overview

In this project, you'll implement your own version of `printf()`—`ft_printf()`. The implementation will involve handling various types of conversions and formatting options, such as printing characters, strings, pointers, numbers, and hexadecimal values.

### Learning Outcomes

- Understanding and working with **variadic functions** in C.
- Implementing and handling **format specifiers**.
- Gaining experience with **buffer management** and **memory management**.
- Building a custom library, `libftprintf.a`, that mimics the functionality of `printf()`.

### Key Features

- **Mandatory Part**: 
  - Implement `ft_printf()` that supports the following specifiers:
    - `%c` : Print a single character.
    - `%s` : Print a string.
    - `%p` : Print a pointer in hexadecimal format.
    - `%d` : Print a signed decimal number.
    - `%i` : Print an integer in base 10.
    - `%u` : Print an unsigned decimal number.
    - `%x` : Print a number in lowercase hexadecimal.
    - `%X` : Print a number in uppercase hexadecimal.
    - `%%` : Print a literal percent sign.
  
- **Tools & Functions**:
  - Your `ft_printf()` function should handle variadic arguments and format the output accordingly.
  - The library should use the following C functions:
    - `malloc`, `free`, `write`, `va_start`, `va_arg`, `va_copy`, `va_end`.
  
### Technologies & Requirements

- **Language**: C
- **Library**: `libftprintf.a` (static library)
- **Makefile**: The `Makefile` must contain rules for compiling and cleaning the project (`NAME`, `all`, `clean`, `fclean`, `re`).
- **Norm**: The code must adhere to the C coding standard (Norminette).

### Instructions

- Your `ft_printf()` function must be compared against the original `printf()` and should behave identically with respect to the specified format specifiers.
- You should not implement buffer management as seen in the original `printf()`.
- Use `ar` to create the static library and avoid using the `libtool` command.

### How to Compile

To compile the project, use the following Makefile rules:
1. `make` - Compile the `libftprintf.a` library.
2. `make clean` - Clean the project (remove object files).
3. `make fclean` - Clean the project and remove the library.
4. `make re` - Rebuild the project from scratch.

### Example Usage

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello, %s! You are %d years old.\n", "Alice", 25);
    ft_printf("Hexadecimal: %x, Uppercase Hex: %X\n", 255, 255);
    ft_printf("Pointer address: %p\n", (void*)&main);
    return 0;
}
