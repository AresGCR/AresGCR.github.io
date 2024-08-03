---
title:"Week III"
date: 2024-08-02 00:00:00 +0800
categories:[Week III]
---
# Patching Array 
Given a sorted array of positive integers ***nums*** and a positive integer ***n***, you need to add elements to the array from 1 to n inclusive by summing up some of the elements (or all) in the array. Find the minimum of patches (elements) you need to add to the array. 

Initially, the array ***nums*** may not be able to represent every number from ***1*** to ***n*** and adding new elements to the array extends its ability to represent more numbers. The challenge lies in determining the minimal set of new elements needed. 


The approach used is a ***greedy*** one, as it always tries to extend the range as much as possible with each step by either using the next available number in ***nums*** or by patching the smallest number possible to increase the coverage range by checking if we have not yet used all numbers and whether the current number at **nums[i]** can be used to extend the range. If the **nums[i]** is less than or equal to **x** (x is a number between 1 and n), it means we can use it to create new sums up to **x+nums[i]** and if not we must add a patch. The patch will be **x** and then we double the range of search. This iteration continues until x is ***greater*** than n


