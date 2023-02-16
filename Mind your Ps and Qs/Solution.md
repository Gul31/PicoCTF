# Mind your Ps and Qs

## Question

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? values

## Solution

RSA is a asymmteric cryptography. This type of encryption uses public and private keys.

## Steps to generate RSA keys
- Select two large prime numbers, p and q. The prime numbers need to be large so that they will be difficult for someone to figure out.
- Calculate n = p*q
- Calculate `totient` aka phi value. we will denote it by `t`. t = (p - 1)*(q - 1)
- Select an integer e, such that e is co-prime to t(n) and 1 < e < t(n)
- The pair of (n,e) makes the public key
- Calculate d, such that `e.d = 1 mod(t)`
**Note: Two integers are co-prime if the only positive integer that divides them is 1**
The pair (n,d) makes up the private key.

[To know more about RSA algorithm](https://www.educative.io/answers/what-is-the-rsa-algorithm)


