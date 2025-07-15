---
tags:
  - COURSE
---
# _COMP206

- [[Software System]]
- [[CLI commands]]
- [[Permissions]]
- [[Streams]]
- [[Piping]]
- [[Bash Scripting]]
- [[Regular Expressions]]
- [[Links]]
- [[C]]
- [[Internet]]
- [[Information Security]]
- [[Emulation, Virtualization, Containers]]
13mkCYtSxQRJ


answers for midterm 3 (hw8)

1. The three pillars of information security are:
- Confidentiality: Ensures unauthorized users cannot access sensitive information.
- Integrity: Guarantees that information is not lost, corrupted, or modified without authorization.
- Availability: Ensures authorized users can access information when needed.

- Ransomware attack: The pillar undermined is Availability, as authorized users are unable to access the encrypted patient records.
- Database breach and selling data: The pillar undermined is Confidentiality, as unauthorized users gain access to sensitive payment processor information.

2. Diffie-Hellman key exchange is used by two parties to derive a shared secret key over an untrusted communication channel (e.g., the Internet). It is useful in establishing secure communication, such as in Transport Layer Security (TLS), where the parties do not share a secret key beforehand but need one for encryption. This algorithm relies on the computational infeasibility of solving discrete logarithms, making it resistant to eavesdropping.

3. RSA can prove ownership of a private key through digital signatures. The process involves:
- Signing a message (or a hash of it) using the private key.
- Providing the signed message and the public key.
- The recipient uses the public key to verify that the signature matches the original message, ensuring that only the private key's owner could have created the signature.

4. To certify authorship of a message without encryption using a pre-shared key K:
- Append K to the end of the message.
- Compute the cryptographic hash of the resulting combination (message + K).
- Send the message alongside the hash.
- The recipient appends K to the received message, computes the hash, and compares it with the provided hash. If they match, the recipient is assured of the sender's authenticity due to the properties of cryptographic hash functions