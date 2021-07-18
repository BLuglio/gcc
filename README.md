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
