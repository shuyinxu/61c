Better C
---

A set of actionable items to improve your C skills.

---
### What we talk about when we talk about "C"

|      Year | Version | Standard               | Publication Date |
|      :--: | :--:    | :--:                   |             :--: |
| 1972-1989 | K&R     | n/a                    |       1978-02-22 |
| 1989-1990 | C89     | ANSI X3.159-1989       |       1989-12-14 |
| 1990-1995 | C90     | ISO/IEC 9899:1990      |       1990-12-20 |
| 1995-1999 | C95     | ISO/IEC 9899/AMD1:1995 |       1995-03-30 |
| 1999-2011 | C99     | ISO/IEC 9899:1999      |       1999-12-16 |
|  2011-now | C11     | ISO/IEC 9899:2011      |       2011-12-15 |

---
### Basic C

```c
#include <stdio.h>

int main() {
  printf("Hello World\n");
  return 0;
}
```

---
### Basic C

- Types, Operators, Expressions (`int`, `char`, `int *`, ...)
- Control Flow (`if`, `else`, `switch`, `for`, `while`, `break`, `continue`, `goto`)
- Functions
- Pointers/Arrays
- User defined types: `Struct`, `Enum`, `typedef`
- I/O
- syscall
- CPP (preprocessor), `#define`, `#if`, `#ifndef`

---
### In-depth Topics

- Pointers/Arrays

---
### Pointers

```c
int x = 3;
int *p = &x;
*p = 4;
```

---
### Function

Stack frames.

```c
void a() {}
void b() { a(); }
void c() { b(); }

int main() { c(); return 0; }
```

---
### Function Pointer

https://cdecl.org/

```
int (*fp) (void *, void *);
fp = &func;
(*fp)(x, y);
```

declare fp as pointer to function (pointer to void, pointer to
void) returning int


----------------------------------------------------------------------------

---
### C Can be deep/dark

C is a simple language if you are experienced. Want a proof? See [Deep
C](https://www.slideshare.net/olvemaudal/deep-c).

---
### Compilers (with warnings) are your friends

Add proper flags to the compilation process to detect potential bugs, e.g.
treating all warnings as errors. Check out [gcc
doc](https://gcc.gnu.org/onlinedocs/gcc/).

- `-Wall`, `-Wextra`, `-Wpedantic`
- `-Werror`

- `-g`, `-ggdb`

---
#### Multi-line String

```c
char *my_string = "Line 1 "
                  "Line 2";
```

---
#### Trigraphs

```c
  // Will the next line be executed????????????????/
  a++;
```

---
### Good Practices writing better/modern C

- Use `stdint.h`
- Use `stdbool.h`
- Use `inttypes.h`
- Use `const`

---
### Const

```
const char* const foo = "hello";
```

---
### Macros

Good practice to `#undef` to facilitate reuse later on

---
## Resources and References

- [C gibberish <-> English](https://cdecl.org/)
- [How to C in 2016](https://matt.sh/howto-c), [HN](https://news.ycombinator.com/item?id=10864176)


<!-- links -->