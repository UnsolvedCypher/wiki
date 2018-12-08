# RSA Cheat Sheet

## Setup
$p =$ random prime number

$q =$ random prime number

$n = p*q$

$Φ(n) = (p - 1)(q - 1)$  (this is called the totient function)

$e =$ some number smaller than $Φ(n)$ that's coprime with it (shares no factors)

Calculate d with:

$de = 1 \mod Φ(n)$

Public key: $n, e$

Private key: $p, q, d$

$m =$ message, $c =$ ciphertext

## Encryption

$c = m^e \mod n$

## Decryption

$m = c^d \mod n$

## Square and Multiply Algorithm

Given $x^e \mod n$, we first convert $e$ to base 2, so it is made up of t bits

Let $p = 1$. For every bit, starting from the highest order one, p is squared. If the bit is equal to one, p is also multiplied by b. Continue for each bit in $e$.

### Example

${3}^ {107} \mod  57$

$e = 107 = 1101011_{2}$

$p = 1$ to start

$e_6 = 1, p = p^2 * x = 1 * 3 = 3 \mod 57$

$e_5 = 1, p = p^2 * x = 3^2 * 3 = 27 \mod $

$e_4 = 0, p = p^2 = 729 \mod 57 = 45$

$e_3 = 1, p = p^2 * x = 45^2 * 3 \mod 57 = 33$

$e_2 = 0, p = p^2 = 33^2 = 1089 \mod 57 = 6$

$e_1 = 1, p = p^2 * x = 6^2 * 3 = 108 \mod 57 = 51$

$e_0 = 1, p = p^2 * x = 57^2 *3 = 7803 \mod 57 = 51$