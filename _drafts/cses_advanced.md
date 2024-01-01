---
layout: post
title: CSES Advanced Techniques Section
permalink: cses-intro-editorial
---

Another CSES post! This time, I cover the Advanced Techniques section: . Disclaimer: there already is a pretty nice [video][video] that explains these problems. This is just a text version, for those who prefer that. Enjoy!

This section is, ultimately, kind of a knowledge test (most problems are classical). So if you'd like to attempt these problems without the fear of not knowing something, here's the list of topics you should go in knowing:

- Meet in the Middle
- Bitsets
- Treaps (or generally any balanced binary search tree)
- Bridges / Articulation Points
- DP Optimizations (Convex Hull Trick / Divide and Conquer / Knuth)
- FFT
- Dynamic Connectivity
- Min-Cost Max Flow

### Meet in the Middle
**Statement**: You have an array of $n \leq 40$ numbers: how many ways can you pick a subset that sums to $x$?

**Solution**: The naive method takes $2^n$ time, which is too slow. As the name suggests, you need to use a technique called "Meet in the Middle".  
TL;DR: Enumerate over all subsets of the **second half** of the array, and build a frequency map of the sum (i.e. for each possible sum, how many subsets have that sum). Now, enumerate over all subsets of the **first half**: for each, if that subset has sume $s$, add the number of subsets of the second half that have sum $x - s$ to the total.  
Complexity: $O(2^{\frac{n}{2}})

### Hamming Distance
**Statement**: Given $n \leq 20,000$ bitstrings of length $k \leq 30$, find the minimum Hamming distance between any two of them (the Hamming distance between two bitstrings is the number of positions at which they differ).

**Solution**: Computing the Hamming distance between two strings seems impossible in faster than $O(k)$. And it seems difficult to not brute-force over all pairs, so $O(n^2k)$. Too slow?  
Actually, you can represent these bit-strings using C++'s [bitset][] data structure, which can compute Hamming distances faster by a factor of 64. Magically, this doomed complexity is now fast enough! See code on which operations are needed for this.  
Complexity: $O(\frac{n^2k}{64})$

### Beautiful Subgrids
**Statement**: Given a square grid with side length $n \leq 3000$, count the number of subgrids whose corners are all 1s.

**Solution**: We can brute force over all pairs of rows, and for each pair count the number of columns at which both rows give 1. Letting $x$ be this count, add $\binom{x}{2}$ to our count. So far, this is $O(n^3)$.  
Wow, a problem about boolean values that is almost fast enough? Time to pull out bitset! Specifically, we can obtain the set of indices at which two bitstrings are both 1 by taking their bitwise and, and counting the number of ones (both faster by a factor of 64).
Complexity: $O(\frac{n^3}{64})$

### Reachable Nodes
**Statement**: Given a DAG (Directed Acyclic Graph) with $n \leq 50,000$ nodes and $m \leq 100,000$ edges, calculate, for each node, compute the amount of nodes it can reach.


### Reachability Queries
**Statement**: Given a directed graph with $n \leq 50,000$ nodes and $m \leq 100,000$ edges, answer $q \leq 100,000$ queries of the form "can nodes $a$ reach node $b$?".

### Cut and Paste

### Substring Reversals

### Reversals and Sums

### Necessary Roads

### Necessary Cities

### Eulerian Subgraphs

### Monster Game I

### Monster Game II

### Subarray Squares

### House and Schools

### Knuth Division

### Apples and Bananas

### One Bit Positions

### Signal Processing

### New Roads Queries

### Dynamic Connectivity

### Parcel Delivery 


[video]: https://www.youtube.com/watch?v=lYEFvF8Xx2c