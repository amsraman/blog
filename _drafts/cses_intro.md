---
layout: post
title: CSES Introductory Problems Section
permalink: cses-intro-editorial
---

This is the first in a series of posts where I explain the problems in each section of the [CSES problem-set]. This is the introductory problems section, whose exercises mostly test your ability to code in your language of choice (C++ for me). As such, explanations are short -- there's more to gain from simply looking at the code itself.

### Weird Algorithm
**Statement**: Given a number (\leq 10^6): you divide it by 2 if it's even or add 1 to it if it's odd. Keep doing this until the number hits 1, and output every number that is hit along the way.

What a strange process! How can we even be sure that it will terminate? Well, pray that it does and simulate the process using a loop. Fun fact: this actually produces what's known as a "Collatz Sequence", and the question of whether it terminates for arbitrary numbers is an open problem.

Complexity: O(n)

### Missing Number
**Statement**: You're given $n - 1$ distinct numbers from 1 to $n$. Find the missing number.

Lots of ways to do this! Note that if we weren't missing any numbers, their sum is given by $\frac{n(n + 1)}{2}$. So, subtracting out everything we're given from this quantity gives us the missing number (be careful: this won't necessarily fit in 32-bit integers).

Complexity: O(n)

### Repetitions
**Statement**: 

### Increasing Array
**Statement**: 

### Permutations
**Statement**: Construct a permutation of the first $n$ integers such that no two adjacent elements have difference 1 (or report that none exist).

### Number Spiral

### Two Knights
**Statement**: For all $k$ from 1 to $n$, count the number of ways to place 2 knights on a $k \times k$ chessboard such that they don't attack each other.

### Two Sets
**Statement**: Divide the numbers from 1 to $n$ into two sets of equal sum.

### Bit Strings
**Statement**: Count the number of bit strings with length $n$.

### Trailing Zeros

### Coin Piles

### Palindrome Reorder

### Gray Code

### Tower of Hanoi

### Creating Strings

### Apple Division

### Chessboard and Queens
**Statement**: Count the number of ways to place $n$ queens on an $n \times n$ chessboard such that none attack each other.

### Digit Queries

### Grid Paths