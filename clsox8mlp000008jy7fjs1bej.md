---
title: "Hashing"
seoTitle: "Hashing Cryptography"
seoDescription: "Hashing Cryptography"
datePublished: Fri Feb 16 2024 17:26:09 GMT+0000 (Coordinated Universal Time)
cuid: clsox8mlp000008jy7fjs1bej
slug: hashing
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708103163828/9024651c-8428-4ae3-b46b-2a660db4f6f5.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1708104324299/08bdb824-16a1-4d30-a234-8aa8713b7c65.webp
tags: cryptography

---

Hashing means generating value or values from a string of text using a mathematical function.

Hashing is one way to enable security during the process of message transmission when the message is intended for a particular recipient only. A formula generates the hash, which helps to protect the security of the transmission against tampering.

When a user sends a secure message, a hash of the intended message is generated and is sent along with the encrypted message. When the message is received, the receiver decrypts the message. Then the receiver creates another hash from the message. If the two hashes are identical when compared, then a secure transmission has occurred.

This hashing process ensures that an unauthorized end user does not alter the message.

Here's a small example in Python that encrypts "Hello World" in SHA-1 (secure hashing algorithm):

```python
import hashlib

hash_object = hashlib.sha1(b'Hello World')

hex_dig=hash_object.hexdigest()

print(hex_dig)
```

We will get a long string which is hashed by the SHA-1 algorithm.

Hashing is used to index and retrieve items in a database because it is easy to find the item using the shortened hashed key than using the original value.

## Hashed Passwords

When you log into a host computer (or a telephone banking system, or any other type of terminal), how does the host know who you are? How does the host know that it is you and not Liz trying to falsify your identity?

Traditionally, passwords solve this problem. You enter your password, and the host confirms that it's correct. Both you and the host know this secret piece of knowledge, and the host requests it from you every time you try to log in.

The host doesn’t require knowledge of the passwords; instead, the host must be capable of distinguishing valid passwords from invalid ones. This is easy with one-way functions. Instead of storing passwords, the host stores hashes of the passwords.

**Procedure:**

1. You send the host your password.
    
2. The host performs a one-way function (hashing) on the password.
    
3. The host compares the result of the hashing to the value it previously stored.
    

Since the host no longer stores a table of everybody's passwords, the threat of someone breaking into the host and stealing the password list is mitigated.

The list of passwords operated on by hashing is useless because the hash cannot be reversed to recover the passwords.