# GCC Snippets

## MacOS

Basic usage:
```
gcc main.c -o executable
```
Add `-Wall` to enable warnings; use `-Wall -Werrors` to treat warnings as errors.

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

Verbose:
```
gcc -v main.c
```

Show the prints contained inside macros when the final executable is launched:
```
ex:
  #ifdef MY_MACRO
    printf("Something inside the macro);
  #endif
  ....
gcc -DMY_MACRO main.c
```

Displays the list of the shared libraries needed by an executable:
```
ldd main.out
```

### Environment Variables

  - PATH: for searching executable and run-time shared libraries (.so, .dll)
  - CPATH: for searching include paths for headers
    - searched after paths specified in `-l<dir>` options
    - C_INCLUDE_PATH can be used to specify C headers if the particular language was indicated in the pre-processing
  - LIBRARY_PATH: for searching library paths for link libraries
    - searched after paths specified in `-L<dir>` options
