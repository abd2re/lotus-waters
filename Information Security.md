---
tags: []
---
# Information Security

Three pillars of infosec are:
?
- Confidentiality: unauthorized users cannot access information.
- Integrity: information is not lost or corrupted, and is protected from unauthorized modification
- Availability: authorized users can access information.
<!--SR:!2024-12-09,9,210-->

Both confidentiality and integrity are supported by:: encryption.
<!--SR:!2024-12-08,9,220-->
Cryptography refers to:: the practice of ensuring secure communications in the presence of adversarial behavior.
<!--SR:!2024-12-04,1,130-->

- Encryption:: encodes a message (called the plaintext), using an encryption key, into a form that cannot be decoded (called the ciphertext) unless by someone in possession of a decryption key.
<!--SR:!2024-12-06,8,230-->
- Decryption:: takes a ciphertext and its corresponding decryption key to reproduce the initial plaintext.
<!--SR:!2024-12-10,11,220-->

A digital signature is:: a cryptographic method that verifies the authenticity and integrity of digital data or messages by using a unique key pair, ensuring the sender's identity and preventing tampering.
<!--SR:!2024-12-05,2,190-->

An cryptographic scheme in which the encryption and decryption keys are the same is called:: symmetric.
<!--SR:!2024-12-04,10,250-->

Diffie-Hellman key-exchange enables:: deriving a shared secret over an untrusted communication channel, e.g. the Internet.
<!--SR:!2024-12-12,13,240-->

Diffie-Hellman key-exchange relies on:: computational infeasibility: it would take impossibly long for an attacker to “separate the paints.”
<!--SR:!2024-12-13,13,230-->

Transport Layer Security (TLS) is:: a protocol that establishes how two parties communicating over TCP negotiate what encryption strategy to use.
<!--SR:!2024-12-05,2,150-->
- Transport Layer Security (TLS) can use Diffie-Hellman to:: establish a shared secret key.
<!--SR:!2024-12-05,7,230-->
- Transport Layer Security (TLS) can use Advanced Encryption Standard (AES) with that shared secret from Diffie-Hellman to:: protect confidentiality.
<!--SR:!2024-12-05,2,170-->

A checksum is:: a calculation done on a message to produce a kind of summary that is included alongside the message. The receiver of the message performs the same calculation on the message, and compares with the bundled checksum. In case of a mismatch, the receiver knows the message was corrupted.
<!--SR:!2024-12-05,4,230-->

A hash function is:: a function that turns any string into a fixed-size, fairly small integer called a hash.
<!--SR:!2024-12-14,12,230-->

Cryptographic hash functions have the following properties desirable for cryptographic purposes:
?
- Infeasible to find an input string that produces a given hash.
- Infeasible to find another string that produces the same hash as a given string.
- Random input strings produce hashes that are uniformly distributed.
<!--SR:!2024-12-06,9,240-->

A message authentication code (MAC) is:: essentially an unforgeable checksum.
<!--SR:!2024-12-05,5,170-->

Using a pre-shared key, one can create a MAC by leveraging cryptographic hash functions, the steps are:
?
- Append the preshared key to the end of the message to send.
- Compute the hash of the resulting augmented message.
- Send the original message together with the hash.
- The receiver appends the preshared key to the end of the message, hashes, and compares with the provided hash.
The receiver can be sure that the sender is authentic thanks to the properties of cryptographic hash functions.
<!--SR:!2024-12-04,2,200-->

When connecting to google.com, the server presents:: its public key together with a message authentication code signed by a certificate authority.
<!--SR:!2024-12-11,8,190-->

## Injection attacks
An injection vulnerability exists when:: user-controlled input is used (unwittingly) to construct a program that is then executed on a machine other than the user's. It enables a malicious user to make a server perform actions that it normally should not, such as print the email addresses of all the other users, or other sensitive information.
<!--SR:!2024-12-04,1,130-->

## Buffer overflow attacks
A buffer overflow vulnerability exists when:: a program writes to a buffer in an unsafe way. In particular, if the program can be made (say, by an attacker) to write _outside_ the bounds of the buffer, then the program contains a buffer overflow vulnerability.
<!--SR:!2024-12-06,3,152-->

A buffer overflow vulnerability enables an attacker to:: overwrite data on the stack that they shouldn't normally be able to.
<!--SR:!2024-12-06,3,152-->

1. What specific data on the stack is especially dangerous to overwrite? :: The return address is especially dangerous because it determines where the CPU jumps after a function call.
<!--SR:!2024-12-16,14,232-->
    
2. How does overwriting that data enable the attacker to make the CPU execute code of the attacker's choosing? :: The attacker can replace the return address with the address of their malicious code, causing the CPU to execute it.
<!--SR:!2024-12-11,9,212-->
    
3. What is shellcode? :: Shellcode is a small piece of malicious code, often used to spawn a shell, injected by the attacker to exploit a vulnerability.
<!--SR:!2024-12-11,10,232-->
    
4. Why do we include a nop-sled before our shellcode? :: A nop-sled increases the likelihood of the CPU reaching the shellcode by allowing the return address to land within a range of executable instructions.
<!--SR:!2024-12-10,9,232-->
    
5. What are three strategies employed by operating systems & CPUs to mitigate this type of attack? :: They use stack canaries to detect corruption, DEP (Data Execution Prevention) and Address space layout randomization (ASLR) to prevent execution of code on the stack.
<!--SR:!2024-12-10,7,192-->
6. Which OS/CPU-level buffer overflow mitigation strategy is defeated by return-oriented programming? :: DEP (Data Execution Prevention) is defeated by ROP as it executes existing code rather than injecting new code.
<!--SR:!2024-12-16,13,232-->
7. A ROP gadget is:: a small sequence of instructions ending in a return (`ret`), found in existing program memory, that can be chained to perform arbitrary computation. It uses the ret instruction to jump to the next address on the stack, mimicking normal function calls.
<!--SR:!2024-12-07,4,192-->

Buffer overflow attacks exploit vulnerabilities to overwrite critical stack data, like the return address, enabling attackers to redirect execution to malicious code such as shellcode, often preceded by a nop-sled to increase reliability. Operating systems and CPUs mitigate such attacks with techniques like stack canaries and DEP (Data Execution Prevention), but return-oriented programming (ROP) can bypass DEP by chaining small existing code snippets, called ROP gadgets, which end in a `ret` instruction and mimic normal CPU operations.

- The `rbp` holds:: the address of the top of the current stack frame
<!--SR:!2024-12-04,4,223-->
- The `rsp` holds:: the address of the bottom of the current stack frame.
<!--SR:!2024-12-04,2,183-->