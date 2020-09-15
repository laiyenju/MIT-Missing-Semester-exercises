# Security & Cryptography Note

This lecture introduced following concept:

- Entropy
- Hash Functions(SHA1)
- Key Derivation Functions
- Symmetric Key Cryptography
- Asymmetric Key Cryptography

## Entropy

Entorpy can helpa us to measure the secutity level of password.

Entropy bits = $log_2(posibility)$

For example:
- flip coin's security level is $log_2(2)$ = 1 Entropy bit
- dice's security level is $log_2(6)$ ~ 2.6 Entropy bit

## Hash Functions

Most commond application is SHA1. $SHA1(bytes)$ will output 160bits.

**Features**
- non-invertable: cannot be derived directly from SHA1 output
- collision resistant: low possibility have the same SHA1 output
- commitment scheme

### salt

$salt(password, SHA1)$

Is a more secure way to store password. Condering most people tend to set the same password on different platform. If we only use SHA1 to encrypt it:
- SHA1's commit scheme guarantee the same SHA1 output as long as the input is the same(password).
- add some Salt for our password, combining with SHA1 could make the same password generate different encrypt key.

## Key Derivation Functions(KDFs)

KDFs is a function for generating keys that could be applied in cryptography algorithm.  
But KDFs is slow, in order to slow down offline brute-force attacks.

## Symmetric Key Cryptography

- randomized key generation function() → key
- encrypt(plaintext, key) → ciphertext
- decrypt(cyphertext, key) → plaintext

User should provide both **ciphertext** and **key** to know the plaintext.

> Q: What if I lost ciphertext?
> There's a passphase → Key Derivation Function box → key(with the original plaintext) → encrypt → ciphertext

## Asymmetric Key Cryptography

- randomized key generation function() → (public key, private key)
- encrypt(password, public key) → ciphertext
- decrypt(ciphertext, private) → plaintext

### signal or Keybase encrypted message use the same concept

- sign(message, private key) → signature
- verify(message, signature, public key) → OK?

**features**
- hard to forge without private key
- correct

### Important

Symmetric Key Cryptography is fast and Asymmetric Key Cryptography is slow. Therefore, we use Hybrid encryption instead of using Asymmetric Key Cryptography directly in practice.

![](https://i.imgur.com/oe9hBKF.png)
