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
void a;             /*  C Void */
```

