---
title:"Week III"
date: 2024-08-02 00:00:00 +0800
categories:[Week III]
---
# Team LeetCode: 
Given a sorted array of positive integers nums and a positive integer n, you need to add elements to the array from 1 to n inclusive by summing up some of the elements (or all) in the array. Find the minimum of patches (elements) you need to add to the array. 

Initially, the array nums may not be able to represent every number from 1 to n and adding new elements to the array extends its ability to represent more numbers. The challenge lies in determining the minimal set of new elements needed. 


The greedy approach ensures that each step, we extend the coverage as much as possible by adding the smallest necessary element. This strategy minimizes the number of additions required.

This approximation algorithm proceeds by picking at each stage, the sum of numbers that cover all the elements
