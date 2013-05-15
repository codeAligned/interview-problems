interview-problems
==================

Example solutions for some basic programmer interview questions and/or semi-interesting problems,
posted here just for the hell of it.

Presentation Format
===================

The examples are written in 'ANSI' C (C89), and designed to be compiled with GCC. However, they
should compile with any compatible compiler. A Makefile is provided for convenience. Simply invoke
the almighty ``make`` to build all examples.

Why C?
======

Because it's the industry standard programming language (thank God it **ain't** Java!)
and thus, in this humble author's opinion, the ideal medium in which to publish these
sorts of solutions.

atoi.c
======

_Write an implementation of atoi(3) without using any standard library functions._

This is relatively easy as long as you understand that a number in any position is basically:
_digit * radix ^ position_ (e.g. 100 = 1 * 10^2).

Note that the functions presented here don't heed a sign prefixing a number, whereas the
glibc implementation of atoi will handle signs at least.

llmedian.c
==========

_Write a program to find the median node of a linked-list._

I present a simple O(n) solution to this problem. If you understand what a linked-list is,
and how it works, this is pretty painless.

phone-words.c
=============

_Given a 7-digit American telephone number, print out all possible combinations of letters
which can represent the given numbers, in alphabetical order._

_Note: On a standard American dialpad, 0 and 1 have no associated letters._

This is sometimes regarded as a difficult problem. However, it's not that difficult once you
boil it down. I present a O(3^n) / O(4^n) solution for solving it. Most variations
I've come across leave out Q and Z. This is the default in my solution.
However, it can be configured at run-time to include Q and Z for a little more fun.

This program will accept phone numbers anywhere between 1 and 7 digits long.

rand.c
======

_Given an upper bound, a lower bound, and a sequence length, write a program which generates
a sequence of random numbers (without using any standard library functions.)_

This implements a simple pseudo-random number generator.

strrev.c
========

_Write a program to reverse a string, in place._

I provide a *pure-C* solution and slightly faster assembly solutions for 32-bit
and 64-bit x86 CPUs. My solutions run in O(n) time.

For compilers other than GCC, or for strict C89 compliance, compile with ``-DUSE_C``
to avoid the inline assembly.

subarray.c
==========

_Given an array of integers, find the maximum contigious subarray._

I provide two solutions. A quickly-written O(n^2) solution, and a O(n) solution based on
Kadane's algorithm.
