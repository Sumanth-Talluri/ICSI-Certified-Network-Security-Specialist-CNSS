## Module 5 - Fundamentals of Encryption

### History of Encryption
- **Caesar cipher** (is substitution ciphers) - (mono-alphabet substitution method)
    - choose certain numbers by which to shift each letter of text.

- **ROT 13** (single alphabet substitution cipher, characters are rotated 13 chars)

- **Multi-Alphabet Substitution** (polyalphabetic substitution)

- **Rail Fence** (transposition cipher).
    - convert text to two rows

- **Vigenere** (polyalphabetic)
    - +2,-1,+1,+3
    - most wildly used

- **Enigma**
    - family of machines.
    - invented by German engg - Arthur Scherbius.
    - **cryptologic bomb**
    - machines should have same rotor settings to get decipher.
    - Naval Enigma - cracked by **Alan Turing**

### Modern Encryption Methods
- requires understanding of Maths.
- **Symmetric Encryption**, same key is used to   encrypt and decrypt.
    - **Binary Operations**, AND, OR, XOR
        - (XORing) - is reversible. XOR of resultant number with second(key) number gives back original number.
        - easy to decrypt.

    - **Data Encryption Standard** (DES)
        - uses short keys
        - Concept:
            - data is divided into 64-bit blocks, blocks are reordered.
            - then manipulated by 16 separate rounds of encryption (substitution, bit-shifting and logical operations using a56-bit key)
            - Data are reordered one last time.
        - DES uses a 56-bit cipher key applied to a 64-bit block. there is actually a 64bit key, but one bit of each byte is used for error detection.
        - How to transmit the key without compromising it (**public key encryption**)

    - **Blowfish**
        - uses a variable-length key - from 23 to 448 bits.
        - used extensively, gained wide acceptance
        - non-commercial
        - block cipher

    - **AES (Advanced Encryption Standard)**
        - uses Rijndael algorithm.
        - specifies three key sizes: 128, 192 and 256 bits.
        - uses block cipher
        - widely used, considered Very Secure.

- **Public Key Encryption**
    - one key to encrypt (public) and other to decrypt (private)
    - **RSA** - slower than Symmetric. - steps to create keys
        - generate two large random primes p and q of approx equal sizes
        - pick 2 numbers so that when they are multiplied together the product is size required (2048 bits, 4096 bits etc)
        - multiply p and q to get n (n=pq)
        - multiply Euler's totient for each of these primes.
        - m=(p-1)(q-1)
        - **e** a number, co-prime to m
        - find d, when multiplied by e and modulo(remainder) m = 1
        - find **d**, such that **de mod m = 1**
        - encrypt - n=Me %n
        - decrypt - P=Cd%n
        - very secure.

    - **Elliptic Curve Cryptography**
        - based on the fact that finding the discrete log of a random elliptic curve element, is quite difficult to achieve within a public base point.
        - size of EC determines difficulty/security.
        - several ECC algorithm.
        - ECC version of Deffie-Hellman, ECC of DSA...
        - ECC - allows use for protecting classified top secrets with 384-bit keys.

    - **Digital Signature and Certificates**
        - proves who the sender is
        - reverse of asymmetric encryption. if recipient is able to decrypt message/data with senders public key.
    - **Digital Certificates**
        - contains public key and means to verify whose public key it is.
        - X.509 standard. contents of X.509 certificates are:
            - version
            - certificate holder's public key
            - Serial number
            - certificate holder's DN
            - Certificate's validity period
            - Unique name of certificate issuer
            - Digital signature of issuer
            - Signature algorithm identifier

        - CA and RA.
        - PKI distribures digital certs. a PKI is an arrangement that binds public keys with respective user identities by mean of a CA.
        - CRL (certificate Revocation list)
        - OCSP (Online Certificate Status Protocol), a real time protocol for verifying Certificates

        - types of X.509 certificates
            - Domain validation certs, low cost, use to provide TLS for domain.
            - Wildcard certs, multiple subdomains.
            - Code-signing certs, signs code. require more validation before issuing.
            - Machine/computer certs. used in auth protocols.
            - User certs -
            - Email certs. S/MIME uses to secure emails comms.
            - SAN, allows to specify additional items (IP/Domain/DNS names)
            - Root certs, usually self signed.
    - **PGP Certificates**
        - Pretty Good Privacy - is not a encryption algorithm, but a system.
        - offers digital signatures, asymmetric encryption, symmetric encryption.
        - found in email client.
        - considered to be a very good system.
        - uses it own cert format.
        - PGP certs are self-generated (not generated by any cert authority)

### Windows and Linux encryption

- **Windows**
    - EFS, can encryption files/drives.
    - BitLocker Drive encryption, links encryption to a key sstored in a TPM (Trusted Platform MOdule), neuter offline attackers.
    - BitLocker To Go, used for USB drives.

- **Linux**
    - LUKS - encryption of Linux partitions.
    - encrypt entire block device.
    - uses existing Device mapper kernel subsystem
    - provides passphrase strengthening.

### Hashing 'h= H(m)'
- 3 properties of hash func.
    - variable length input -> fixed length output.
    - H(x) is one-way; cannot un-hash.
    - H(x) is collision free - two different input values do not produce same output.
- windows uses hashing to store passwords.
- forensics use hashing to make sure drive is not changed during investigations.
- **salt**, a random bits that are used as one of the inputs to hash.
    - helps in reducing dictionary based attacks.
    - help with rainbow table attacks.
    - should be kept secret and separate from password.

- **MD5** - 128-bit hash -but not collision resistant.
- **SHA** - wildly used - secure and collision free.
    - SHA-1: 160-bit, resembles MD5.
    - SHA-2: SHA-256 (32 byte) and SHA-512(64 byte).
    - SHA-3: lastes SHA.


### Cracking passwords
- **John the Ripper** - password cracker
- use password files
    ```
    Linux: /etc/passwd and /etc/shadow
    Windows 2k+: in hidden .sam file
    ```

    ```
    john passwd
    john - wordfile:/usr/share/worklist/rockyou.txt -rules passwd
    ```

- **Rainbow Tables**
    - predefined hashes of certain character space
    - useful when trying to crack hashes.
        - **Ophcrack**

- **Brute Force**
    - trying every possible key
    - takes long time
    - AES, with 128bits,(if tried by 1 trillion keys a sec, could take xxx years)




#### Continue on to [Module 6 - VPNs](https://github.com/ArunNadda/CNSS/blob/master/Chapters/Module6-VPNs.md)
