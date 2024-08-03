---
title:"Week III"
date: 2024-09-02 00:00:00 +0800
categories:[Week III]
---
# Permutations
Permutations of an array refer to all possible arrangements of the elements of the array in different orders. Given an array of distinct integers, the goal is to general all the possible permutations of the array.  

For an array of length ***n*** , there are ***n!*** Possible permutations and the factorial of a non-negative integer is the ***product*** of all positive integers less than or equal to n 

The approach to solve this problem  is ***backtracking*** , that is a refinement of the brute force approach, which systematically searches for a solution among all available options. It does by assuming that the solutions are represented by arrays [a<sub>1</sub>,...,a<sub>n</sub>] of values and by traversing, in a depth first manner, the domains of the arrays until the solutions are found. The traversal of the solution space can be represented by a depth-first traversal of a tree. 

Another approach used is the ***Steinhaus-Johnson-Trotter algorithm*** that generates all of the permutations on ***n*** elements by moving elements in a coordinated, directional manner. It ensures that every permutation is generated and ***do not use recursion***. It uses an iterative approach.