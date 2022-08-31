# Chapter 14 Dynamic Programming
[PDF solutions](./Ch14.pdf)

## Longest Increasing Subsequence
{{< hint info >}} 
**14.4-5** \
Give an {{< katex >}} O(n^2) {{< /katex >}} algorithm to find the longest monotonically increasing subsequence of sequence of n numbers. 
{{< /hint >}}


{{< hint info >}} 
**14.4-6** \
Give an O(nlgn)-time algorithm to find the longest monotonically increasing subsequence of a sequence of n numbers. Hint: Observe that the last element of a candidate subsequence of length ii is at least as large as the last element of a candidate subsequence of length i - 1. Maintain candidate subsequences by linking them through the input sequence.)
{{< /hint >}}

{{< hint info >}} 
**Leetcode-300** \
Given an integer array nums, return the length of the longest strictly increasing subsequence.

A subsequence is a sequence that can be derived from an array by deleting some or no elements without changing the order of the remaining elements. For example, [3,6,2,7] is a subsequence of the array [0,3,1,6,2,2,7].
{{< /hint >}}

### {{< katex >}} O(n^2) {{< /katex >}} Solutions
A sequence X of n numbers:  {{< katex >}} X=<x_1, x_2, ....., x_n> {{< /katex >}}

1. Sort X into {{< katex >}} Y=<y_1, y_2, ....., y_n> {{< /katex >}}. In Y, the numbers are sorted. In other words, if i < j, then {{< katex >}} y_i < y_j {{< /katex >}}.

2. Find the Longest Common Subsequence (LCS) of X and Y by the algorithms in 14.4. The LCS of X and Y are the longest increasing subsequence of X.


#### *Proof*

The LCS of X and Y is by its definition a subsequence of Y. Then the numbers in the LCS is indeed increasing. 


*Runtime*

*Handwritten Golang Implementation*

*Golang Implementation and Leetcode Result*