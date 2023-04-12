# Interview-02
## Problem Domain
Write a function that accepts an integer n, and returns the nth number in the Fibonacci sequence.

## Visual 
![calculate-the-Fibonacci-number-we-have-basic-2-approaches](https://user-images.githubusercontent.com/60603704/231559416-6121816b-b905-4ca2-a820-c3791b1b9fa2.png)


## Algorithm
The Fibonacci sequence is a series of numbers where each number is the sum of the two preceding ones.

The first two terms of the Fibonacci sequence are 0 and 1. The sequence then goes as follows: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, ....

We can use this definition to write a function that computes the nth number of the sequence.

## Pseudocode
Iterative solution:
```
function fib_iterative(n)
    if n == 0:
        return 0
    if n == 1:
        return 1
    
    fib_n_minus_2 = 0
    fib_n_minus_1 = 1
    
    for i from 2 to n:
        fib_n = fib_n_minus_2 + fib_n_minus_1
        fib_n_minus_2 = fib_n_minus_1
        fib_n_minus_1 = fib_n
    
    return fib_n

```
Recursive solution:
```
function fib_recursive(n)
    if n == 0:
        return 0
    if n == 1:
        return 1
    
    return fib_recursive(n - 1) + fib_recursive(n - 2)

```
## Big O
The iterative solution has a time complexity of O(n), since it has to compute all the Fibonacci numbers up to n. The space complexity is O(1), since we only need to store the previous two Fibonacci numbers.

The recursive solution has a time complexity of O(2^n), since it computes the same Fibonacci numbers multiple times. The space complexity is O(n), since we need to keep track of the function calls on the call stack.

## Code
Iterative solution:
```
def fib_iterative(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    
    fib_n_minus_2 = 0
    fib_n_minus_1 = 1
    
    for i in range(2, n + 1):
        fib_n = fib_n_minus_2 + fib_n_minus_1
        fib_n_minus_2 = fib_n_minus_1
        fib_n_minus_1 = fib_n
    
    return fib_n

```

Recursive solution:

```
def fib_recursive(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    
    return fib_recursive(n - 1) + fib_recursive(n - 2)
```
## Test
```
assert fib_iterative(0) == 0
assert fib_iterative(1) == 1
assert fib_iterative(2) == 1
assert fib_iterative(3) == 2
assert fib_iterative(4) == 3
assert fib_iterative(5) == 5
assert fib_iterative(6) == 8
assert fib_iterative(7) == 13
assert fib_iterative(8) == 21
assert fib_iterative(14) == 377
assert fib_iterative(45) == 1134903170

assert fib_recursive(0) == 0
assert fib_recursive(1) == 1
assert fib_recursive(2) == 1
assert fib_recursive(3) == 2
assert fib_recursive(4) == 3
assert fib_recursive(5)
```

