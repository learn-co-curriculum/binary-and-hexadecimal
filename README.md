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

These integer number systems have "digits". In decimal, a digit can be 0-9, in binary 0-1, and hexadecimal 0-F (16 unique values per digit, aka base 16).

## Counting

We count in these number systems the same way, the digits just flip
faster or slower than we're used to in decimal.

### Decimal counting

Here's an easy one, we count like this in decimal:

`0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20`

Every time we increment by 1 and the digit increases, if it exceeds the maximum digit value, then
the digit next to it increases and the digit being increased resets to zero.

### Binary counting

`0, 1, 10, 11, 100, 101, 110, 111, 1000, 1001, 1010, 1011, 1100, 1101, 1110, 1111, 10000`

### Hexadecimal counting

`0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 1A, 1B, 1C, ...`

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

So, once we've memorized the first powers of two, we just see which ones
have a `1` and add them together. The first powers of two are:

`1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024`

If we have the number `101011`, then that number in decimal is `1 + 2 + 8 + 16 + 32`

Some things we encounter that use binary directly:

* Bitstrings

If you ever need a really compact way to represent a bunch of binary
values, you can assign each bit in a number to represent true or false.

Say we have the binary number 10011. In Ruby, we would get this number
like this: `permissions = 21`.

Then, we would need numbers to check against the permissions number. So,
`admin = 16`, in binary this number is `10000`.

Then, if we use the binary "and" operator, `&`, we can check if the
permissions are on for admins like this:

`permissions & admin > 0`

In this case `permissions & admin` equals `10000`. If the permissions
string had been `000011`, then `permissions & admin` would have equaled
0.

* Unix permissions

Unix uses bit strings for permissions.

`chmod 644` you say? What bizarre incantation is this? Well it's unix
using a bitstring to manage permissions. A unix bitstring represents
whether 3 different groups of people can read, write or execute a given
file. Here's what that looks like when inspected with `ls -l`:

`-rw-r--r-- 1 spencer1248 staff 4176 May  4 09:23 README.md`

The first 3 spaces are for the owner, the second 3 are for the group.
the last 3 are for everyone.

To change these permissions, we can use a bit string like this:

`chmod 644 README.md`.

644 treated as 3 separate numbers gives us 3 binary numbers that look
like this:

`110 100 100`

These map `rw-`, `r--`, and `r--`.

Neato.

### Hex

n is 0 - 15

![hexadecimal sum](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/binary-and-hexadecimal/hexadecimal_sum.gif)

if `n_0` is 4, `n_3` is A, `n_4` is F, and everything else is 0, then the
value is 1024004, i.e. `FA004`
