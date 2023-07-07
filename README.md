# Function F() Test Coverage

This repository contains the source code for function `F()`, along with the derived test cases to achieve full branch and multiple-condition coverage.

## Source Code

```c
int F(int a, int b, int c) {
    int type, t, i;
    type = 0;
    i = 0;
    while (i <= 1) {
        if (a >= c) {
            t = a;
            a = c;
            c = t;
        }
        if (b >= c) {
            t = b;
            b = c;
            c = t;
        }
        if (a + b <= c) {
            type = -1;
        }
        if (type >= 0) {
            if ((a == c) || (b == c)) {
                type = type + 1;
            }
            if ((type == 0) && (a == b)) {
                type = type + 1;
            }
            if (type >= 0)
                if ((a * a + b * b == c * c) || (a * a + c * c == b * b))
                    type = type + 1;
        }
        i = i + 1;
    }
    return type;
}

```

## Problem Statement: Branch and Multiple-Condition Testing
The goal of this problem is to derive a set of test cases that provide full branch coverage for function F().
Additionally, we need to derive additional test cases that cover multiple-condition testing, ensuring that all combinations of simple conditions for the complex predicates are executed.

## Branch Testing
Branch testing ensures that all branches in the code are executed
 
Sample Test Case:

Input: a = 20, b = 10, c = 5
Covered Branches: 4T 5T 9F 13T 15F 4T 5F 9F 13T 15F 4F (Please refer to the Test case file for the branches covered)

## Multiple-Condition Testing
Multiple-condition testing ensures that all combinations of simple conditions for complex predicates are executed. 

Sample Test Case:

Input: a = 1, b = 2, c = 2
Covered complex predicates: 
loop1: 16FT, 18FF, 21FF 
loop2: 16FT, 18FF, 21FF 


Feel free to use these test cases to evaluate the behavior of the function F() and ensure complete branch and multiple-condition coverage.

Note: The sample test cases provided in the problem statement have been included in the derived test cases above.
