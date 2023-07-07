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
} ```c

## Problem Statement: Branch and Multiple-Condition Testing
The goal of this problem is to derive a set of test cases that provide full branch coverage for function F().
Additionally, we need to derive additional test cases that cover multiple-condition testing, ensuring that all combinations of simple conditions for the complex predicates are executed.

## Branch Testing
The following test cases cover branch testing, ensuring that all branches in the code are executed:
 
Test Case 1:

Input: a = 3, b = 4, c = 5
Executes branches: 5, 6, 8, 9, 11, 12, 13, 16, 20, 21, 23
Test Case 2:

Input: a = 5, b = 12, c = 13
Executes branches: 4, 5, 9, 11, 13, 15, 16, 17, 20, 21, 23
Test Case 3:

Input: a = 8, b = 15, c = 17
Executes branches: 4, 5, 9, 11, 13, 15, 19, 20, 21, 23
Multiple-Condition Testing
The following test cases cover multiple-condition testing, ensuring all combinations of simple conditions for complex predicates are executed:

Test Case 1:

Input: a = 3, b = 4, c = 5
Executes combinations: (a >= c), (b >= c), (a + b <= c), (a == c), (b == c), (a == b), (a * a + b * b == c * c), (a * a + c * c == b * b)
Test Case 2:

Input: a = 5, b = 12, c = 13
Executes combinations: (a >= c), (b >= c), (a + b <= c), (a == c), (b == c), (a != b), (a * a + b * b == c * c), (a * a + c * c == b * b)
Test Case 3:

Input: a = 8, b = 15, c = 17
Executes combinations: (a >= c), (b >= c), (a + b <= c), (a != c), (b != c), (a != b), (a * a + b * b == c * c), (a * a + c * c == b * b)
Feel free to use these test cases to evaluate the behavior of the function F() and ensure complete branch and multiple-condition coverage.

Note: The sample test cases provided in the problem statement have been included in the derived test cases above.
