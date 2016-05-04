# Binary and Hexadecimal

10 kinds of 0xDEADBEEF

## Introduction

To store data, computers use (really) tiny things called transistors that can
be in 1 of 2 states. This is convenient because we can represent any
number in the universe using a series of transistors. This is
accomplished by using the 2 states to represent the two values in the binary
number system, 1 and 0.

The binary number system (0,1), is exactly equivalent to our
decimal number system (0,1,2,3,4,5,6,7,8,9), it just takes more digits to
represent any given number. Binary numbers are used instead of something
familiar like decimal because it is easier to manufacture physical hardware
to work with 2 states than 10 states.

These number systems also referred to as "base 2" or "base 10". You can have a "base anything" number system. In fact, [there have been computers built that had 3 states](https://en.wikipedia.org/wiki/Ternary_computer) which used the base 3 number system, or "ternary".

These integer number systems have "digits". In decimal, a digit can be 0-9, in
binary 0-1, and hexadecimal 0-F (16 unique values per digit, aka base 16).

## Counting

We count in these number systems the same way, the digits just flip
faster or slower than we're used to in decimal.

### Decimal counting

Here's an easy one, we count like this in decimal:

`7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20`

Every time the digit increases, if it exceeds the maximum digit value, then
the digit next to it increases and the digit being increased resets to
zero.

### Binary counting

`0, 1, 10, 11, 100, 101, 110, 111, 1000`

### Hexadecimal counting

`0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F, 10`

## Representation in decimal

There is a nice way to use our familiar decimal system to think of other
number systems. Each part of the sum corresponds to a digit in the
number system. Keep in mind that anything to the 0 power is 1, i.e. 10^0
= 1.

### Decimal

n is 0 - 9

![decimal sum](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/binary-and-hexadecimal/decimal_sum.gif)

So for instance, if `n_0` is 4 and `n_3` is 5 and all the other `n`
values are 0, then the values represented is 5004.

### Binary

n is 0 - 1

![binary sum](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/binary-and-hexadecimal/binary_sum.gif)

if `n_1` is 1, `n_3` is 1, `n_4` is 1, and everything else is 0, then the
value is 26, i.e. `11010`.


### Hex

n is 0 - 15

![hexadecimal sum](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/binary-and-hexadecimal/hexadecimal_sum.gif)

if `n_0` is 4, `n_3` is A, `n_4` is F, and everything else is 0, then the
value is 1024004, i.e. `FA004`
