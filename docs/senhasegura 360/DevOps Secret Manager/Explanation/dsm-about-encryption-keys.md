## Metadata_Start 
## code: en
## title: About encryption keys 
## slug: dsm-about-encryption-keys 
## seoTitle: About encryption keys 
## description:  
## contentType: Markdown 
## Metadata_End
Encryption keys play a crucial role in information security and are fundamental to implementing encryption algorithms. They are essential for guaranteeing the confidentiality, integrity, authenticity, and, in some cases, non-repudiation of information.

There are two main types of cryptographic keys: symmetric keys and asymmetric keys:

1.  use the same key to encrypt and decrypt data. Both parties involved in the communication must have the same secret key.
2.  use a pair of public and private keys. The public key is shared, while the private key is kept secret.

The choice between symmetric and asymmetric keys often depends on the system's requirements. Frequently, systems use a combination of both to take advantage of each approach. Secure key management is crucial to ensuring the effectiveness of encryption and protecting sensitive information.

In senhasegura's , you'll find options for asymmetric and symmetric keys.

For symmetric keys, senhasegura offers the following protocols:

*  algorithm operates on fixed data blocks and supports different key sizes. In senhasegura, you can use AES encryption with key sizes of 128 and 256 bits.

For asymmetric keys, senhasegura offers the following protocols:

*  is an algorithm that bases itssecurity on the difficulty of factoring the product of two large prime numbers. The public key consists of two values: an integer n (the modulus) and a public exponent (usually called e). The private key has two values: the same integer n and a private exponent (d). The specific values of n, e, and d are calculated to satisfy specific mathematical properties. At senhasegura, you can use RSA encryption with key sizes of , , and  bits.
*  is an algorithm that uses the mathematics of elliptic curves on finite bodies, where specific mathematical equations represent these curves and offer cryptographic properties that make them suitable for encryption algorithms. senhasegura offers the , , and  variants, where each number refers to the size of the elliptic curve.