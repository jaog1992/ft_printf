<h1 align="center">
	📖 ft_printf
</h1>

<p align="center">
	<b><i>Custom printf function for printing variable values on the terminal</i></b><br>

<h3 align="center">
	<a href="#%EF%B8%8F-about">About</a>
	<span> · </span>
	<a href="#%EF%B8%8F-usage">Usage</a>
	<span> · </span>
	<a href="#-testing">Testing</a>
</h3>

---

## 💡 About

The purpose of this project is to code a function that emulates the behavior of the stdio.h printf. The function will allow users to print the string value of function variables on the terminal in a similar way to the standard printf function. After completing this project, you will be familiar with variable argument inputs.

Implemented variable value convertions: **cspdiux%**:

Acronym  | Variable convertion
------------- | -------------
%c  | Chr
%s  | String
%p  | void * in hex format
%d  | Number in dec format
%i  | Integer in dec format
%u  | Unsigned Integer in dec format
%x  | Number in hex format in lowercase
%X  | Number in hex format in uppercase
%%  | Prints the '%' symbol

## 🛠️ Usage

### Requirements

You will need a **`gcc` compiler**, the `libft` functions and the `stdarg` standard **C libraries** to run it and make tests.

### Instructions

**1. Using it in your code**

Include the header in your code:

```C
#include "ft_printf.h"
```
**2. Compilation**

Compile the code using the Makefile or by adding the source files and required flags:

```shell
gcc -Wall -Wextra -Werror <*.c files>
```

Keep in mind that this ft_printf code is using some custom libft functions that should be added to the *.c files list.

## 📋 Testing

To fully test the project, we recommend using the following third-party tester:

* [Tripouille/gnlTester](https://github.com/Tripouille/gnlTester)
