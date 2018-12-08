# Euclidean Algorithm and Extended Euclidean Algorithm

## Euclidean Algorithm

This algorithm allows you to find the greatest common factor (or greatest common divisor) of two numbers.

To do the Euclidean Algorithm, start with the larger number, $a$, and write it as $a = (b)(c) + d$, where $b$ is the smaller number, $c$ is as large as possible, and then $d$ is the remainder. Then, on the next line, write an equation in the same form except $a$ is replaced by $b$ and $b$ is replaced by $d$. Continue this way until $d = 0$, and the last non-zero value of $d$ is the greatest common divisor.

### Example

$\gcd(132, 473)$:

$473 = (132)(3) + 77$

$132 = (77)(1) + 55$

$77 = (55)(1) + 22$

$55 = (22)(2) + 11$

$22 = (11)(2) + 0$

The last non-zero remainder is the GCD, so that is 11 in this case.

## Extended Euclidean Algorithm

The Extended Euclidean algorithm is used to calculate the multiplicative inverse of a number. This means finding a number $y$ for $x$ such that $xy \mod n = 1$. This can only happen if numbers $x$ and $y$ are coprime, meaning they share no factors other than 1.

### Example

To begin, you need to do the standard Euclidean algorithm:

to be continued...