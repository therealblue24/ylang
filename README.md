# The Y Programming Language
A Modern C-like language which follows C principles. Virtually compatible with
any C code.

## Main function
The Main function of a Y program is defined as follows:
```c
int Main(int argc, char *argv[]) {
    return 0; /* Returns 0: Sucess
               *         1: Not-A-Sucess
               */
}
```
...or you can just use
```c
int main(int argc, char *argv[]) {
    return 0; /* Returns 0: Sucess
               *         1: Not-A-Sucess
               */
}
```
like classic C. Vaild main function names are as precisly follows:
```c
int Main(int argc, char *argv[]);
int main(int argc, char *argv[]);
int _start(int argc, char *argv[]);
int _Start(int argc, char *argv[]);
int Start(int argc, char *argv[]);
int start(int argc, char *argv[]);
int entry(int argc, char *argv[]);
```
# Syntax and Types

There are also types like in C:
```c
char a;             /*  8-bits */
unsigned char a;
short a;            /*  16-bits */
unsigned short a;
int a;              /*  32-bits */
unsigned int a;
long a;             /*  64-bits */
unsigned long a;
float a;
double a;             /* Standard IEEE754 Floats
                            float = float32
                            double = float64 */
void a;             /*  C Void */
auto a;             /*  Autos! */
```
Functions:

```c
int myFunction(void *ptr, void ref&, void normal);
```
"Short" Functions:
```cpp
auto myFunction = [&](void *ptr, void ref&, void normal) -> int {
    return 1; /* FYI: call this function using myFunction(...)
                Just because this declaration style doesn't mean the
                way to call the function is different. */
}
```
While, For, If {else}
```c
while(x > 1) {
    for(int j=0;j<8;j++) {
        if(j == x) {
            /* Do something! */
        } else if(j == 5) {
            /* Do something! */
        } else {
            /* Fallback! */
        }
    }
}
```
Structs and Unions
```c
struct State {
    long unix_timestamp;
    union uniform_char keyboard[26];
};

union uniform_char { /* Same thing as C union. */
    char a;
    unsigned char b;
};
```
Enums and Typedefs
```cpp
short enum A {
    BBB = -1,
    AAA
};

typedef struct myStruct myStruct;
typedef long 64_bit_number;
```
Const, Extern, Static
```c
const double pi = 3.14159265358979323f;
pi = 3.14f; /* ERROR: Not Allowed, pi is constant */
static int counter = 0; /* Static vars are only allowed in the file they are
                           defined in */
float pi32 = 3.14159265358f;
/* Meanwhile, in another file... */
extern float pi32;
```
### !!! Volatile is the same as it is in C. !!!
constexpr, and expr get evaluated by the compiler whenever you use it.
```cpp
constexpr double pi = 3.14159265358979323f; /* Constant */
expr int magic_number = 65527; /* Not a Constant */
int j = 0; /* counter */
constexpr int k = j + 1;
```
## Preprocessors
Same Preprocessors as C.
```c
#define MESSAGE "Hello, World!"
#include <stdio.h>
#define FAULTY_MACRO "aujshaidhus"
#undef FAULTY_MACRO
#ifdef MESSAGE
#else
#define MESSAGE "Hello, World!"
#endif
#ifndef FAULTY_MACRO
#define CLEAN 1
#else
#define CLEAN 0
#endif
```
There are more Preprocessors left out, but they litterly have the same funcionaly as they do in C.

### File Extensions
* *.y - Y Source File
* *.h - Y Header File
### About Y Header Files
They are compatible with C Headers. But C Headers are Not
compatible with Y Headers.
### Standard Library
Y imports libc, and liby, which is a extra set of functions for y.
