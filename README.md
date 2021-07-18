# GCC Snippets

## MacOS

Basic usage:
```
gcc main.c -o executable
```
Add `-Wall` to enable warnings.

Prints the preprocessor result to a file:
```
gcc -S main.c >> debug
```

Prints the assembler result to a file:
```
gcc -E main.c >> debug
```

Produce all intermediate stages output to file:
```
gcc -save-temps main.c
```

Create a shared library:
```
gcc -c -Wall -fPIC main.c
gcc -shared -o main.so main.o
```

Debug:
```
gcc -g main.c
```
