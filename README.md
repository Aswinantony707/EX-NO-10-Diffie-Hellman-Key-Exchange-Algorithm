# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1. Diffie-Hellman Key Exchange is used for securely sharing a secret key between two parties over an insecure channel.

2. Initialization: Agree on a large prime number \( p \) and a primitive root \( g \) modulo \( p \) (both are public values).

3. Key Exchange Process: 
   - Each party selects a private key and calculates their public key using the formula \( g^{\text{private key}} \mod p \).
   - Each party then shares their public key with the other.

4. Secret Key Computation: 
   - Each party computes the shared secret key using the received public key and their own private key.

5. Security: The difficulty of computing discrete logarithms ensures that the shared key remains secure even if public values are intercepted.

## Program:
```
P = int(input("Enter Prime Number: "))
G = int(input("Enter Primitive Root: "))

a = int(input("Enter Private Key of ASWIN ANTONY: "))
b = int(input("Enter Private Key of M: "))

A = (G ** a) % P
B = (G ** b) % P

secretA = (B ** a) % P
secretB = (A ** b) % P

print("Public Key of ASWIN ANTONY:", A)
print("Public Key of M:", B)

print("Secret Key for ASWIN ANTONY:", secretA)
print("Secret Key for M:", secretB)

if secretA == secretB:
    print("Secret key successfully established")
else:
    print("Keys do not match")

print("Program executed successfully")
```

## Output:

<img width="1300" height="716" alt="image" src="https://github.com/user-attachments/assets/2fab4220-bd44-4af8-9ff8-5d25c7e50000" />


## Result:
  The program is executed successfully

