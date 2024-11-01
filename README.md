# ft_printf: Recreating C's printf Function with Style! 🎉

Welcome to **ft_printf**, a custom implementation of the famous `printf` function for the 42 School curriculum. This project dives deep into variadic arguments and pushes you to understand the structure and intricacies of formatted output in C. It supports various conversions, flags, width specifications, and precision options, making it a powerful tool in your coding arsenal!

## 🌟 Project Highlights

- **Supported Conversions**: `%`, `c`, `s`, `p`, `i`, `d`, `u`, `x`, `X`
- **Supported Flags**: `#`, `+`, `(space)`
- **Supported Options**: `-`, `0`, `.`, `*`, width

**Completion Date**: February 7, 2022  
**Grade**: 125/100 🔥

## 🛠️ Usage

To compile the library, simply run:

```bash
make        # Compiles ft_printf library
make bonus  # Compiles with any bonus features
```

### Basic Usage Example

To start using `ft_printf`, create a `main.c` file as shown below:

```c
// Include the header
#include "ft_printf.h"

int main(void)
{
      // Call the function
      ft_printf("Testing ft_printf!");
      return (0);
}
```

Then, compile it with your `ft_printf` library:

```bash
gcc main.c libftprintf.a && ./a.out
```

**Expected Output:**
```
Testing ft_printf!
```

## 🔍 Advanced Usage: Format Specifiers and Options

The `ft_printf` function supports various format specifiers, each offering flexibility for precision, width, and more. Here’s a breakdown of all supported specifiers and flags:

### Flags  
| Flag  | Description                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| `-`   | Left-justify within the given width (default is right-justify).                                   |
| `+`   | Precede positive numbers with a `+`; negative numbers automatically get a `-`.                    |
| `(space)` | Inserts a space before positive numbers if no sign is used.                                       |
| `#`   | Prefixes non-zero `x` or `X` values with `0x` or `0X`, respectively.                              |
| `0`   | Pads numbers with leading zeros instead of spaces.                                                |

### Width  
| Value      | Description                                                                                  |
|------------|----------------------------------------------------------------------------------------------|
| `(number)` | Minimum number of characters for output; padding used if shorter.                            |
| `*`        | Width is dynamically set based on an argument.                                               |

### Precision  
| Value      | Description                                                                                  |
|------------|----------------------------------------------------------------------------------------------|
| `.(number)`| Sets the minimum digits for integers and the max characters for strings. Zero hides output if value is 0. |
| `.(*)`     | Precision dynamically set via an argument.                                                   |

### Format Specifiers  
| Specifier | Description                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| `%`       | Prints a literal `%`.                                                                         |
| `c`       | Outputs a single character.                                                                   |
| `s`       | Prints a string of characters.                                                                |
| `p`       | Displays a pointer address in hexadecimal format.                                             |
| `d`, `i`  | Prints a signed decimal integer.                                                              |
| `u`       | Prints an unsigned decimal integer.                                                           |
| `x`, `X`  | Outputs an unsigned integer in hexadecimal format (lowercase for `x`, uppercase for `X`).     |

### Example Usage of Flags, Width, and Precision

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Number [%20i]\n", 42);
    ft_printf("Number [%+0*i]\n", 8, 42);
    return (0);
}
```

**Expected Output:**

```
Number [                  42]
Number [+0000042]
```
---
