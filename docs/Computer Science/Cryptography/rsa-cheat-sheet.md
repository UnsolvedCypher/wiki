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

## Signing

$s$ is signature

$s = m^d \mod n$

## Verification

Verify by checking if $s^e = m$