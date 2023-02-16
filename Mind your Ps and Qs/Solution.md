# Mind your Ps and Qs

## Question

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? values

## What is RSA encryption?

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

## Solution

We are given with 3 values in the query. which are
```
c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n = 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e = 65537
```

I used `pow func` in  python to resolve it.

First, I derived values `p` and `q` from a `n` by using a factordb.com website to factorize the large integer `n`.
```
p = 2434792384523484381583634042478415057961    
q = 650809615742055581459820253356987396346063 
```

Secondly, I calculated phi(n) value denoted by `t` using an equation `t = (p-1)*(q-1)`

Thirdly, I derived the value of ``from the euqation `d = pow(e, -1, t)`. ** where pow(x, y, z) represents x = integer value, y = power, z = mod(z) **

Fourth, I dervied value of decrypted message, denoted by `D` using equation `D = pow(c, d, n)`.

lastly, I used the expression `print(bytearray.fromhex(hex(D)[2:]).decode('ascii'))` to get the final result. 

**Note:** I changed outcome to hex value so that I can perform a value conversion to ascii for readability. `[2:]` is used to remove first two charactes of hex value which will be `0x`.












