# Math

The **Math** project is an implementation of its own version of the `math.h` mathematical library in the C programming language. The main mathematical functions implemented in the project cover basic operations used in various algorithms.

The project aims to consolidate the knowledge of computational methods and structural programming. Executed in a team.

## Contents

1. [Functionality Description](#functionality-description)
    - [Functions](#functions)
2. [Requirements](#requirements)
3. [Build](#build)
    - [Steps for build](#steps-for-build)
4. [Use](#use) 
5. [Testing](#testing)
6. [Code coverage report](#code-coverage-report)

## Functionality Description

### Functions

The project implements the following functions from the `math.h` library:

| No. | Function | Description |
| --- | -------- | ----------- |
| 1 | `int abs(int x)` | computes absolute value of an integer value |
| 2 | `long double acos(double x)` | computes arc cosine |
| 3 | `long double asin(double x)` | computes arc sine |
| 4 | `long double atan(double x)` | computes arc tangent |
| 5 | `long double ceil(double x)` | returns the nearest integer not less than the given value |
| 6 | `long double cos(double x)` | computes cosine |
| 7 | `long double exp(double x)` | returns e raised to the given power |
| 8 | `long double fabs(double x)` | computes absolute value of a floating-point value |
| 9 | `long double floor(double x)` | returns the nearest integer not greater than the given value |
| 10 | `long double fmod(double x, double y)` | remainder of the floating-point division operation |
| 11 | `long double log(double x)` | computes natural logarithm |
| 12 | `long double pow(double base, double exp)` | raises a number to the given power |
| 13 | `long double sin(double x)` | computes sine |
| 14 | `long double sqrt(double x)` | computes square root |
| 15 | `long double tan(double x)` | computes tangent |  

## Requirements

- Programming language: C (standard C11)
- Compiler: GCC (GNU Compiler Collection)
- Build system: Makefile
- Standard: POSIX.1-2017
- Code complies with Google Style Guide

## Build

To build the library and execute tests, a `Makefile` is provided with the goals:
- `all` - compile the library and tests
- `clean` - clean up compiled files
- `test` - running unit tests
- `s21_math.a` - build static library
- `gcov_report` - generation of code coverage report in HTML format

### Steps for build
1. Cloning the repository:
    ```
    git clone https://github.com/llllenivka/Math.git
    cd Math
    ```
2. Build the library and tests:
    ```
    make all
    ```
3. clean up the compiled files:
    ```
    make clean
    ```
4. Generating code coverage report:
    ```
    make gcov_report
    ```

## Use

Once built, you can use the compiled `s21_math.a` library in your projects. All functions are prefixed with `s21_` to avoid conflicts with the original `math.h` library.

Example code for using `s21_math`:

```c
#include "s21_math.h"

int main() {
    double result = s21_sqrt(25.0);
    printf("Square root of 25 is %Lf\n", result);
    return 0;
}
```

## Testing

Testing of functions is performed with the help of the `Check` library. Tests check the correctness of each function by comparing the results with the corresponding functions from the standard math.h library. The minimum test coverage is 80% for each function.
All tests are started by the command:
```
make test
```

## Code coverage report

To analyze test coverage, gcov is used. To generate an HTML code coverage report, run:
```
make gcov_report
```
