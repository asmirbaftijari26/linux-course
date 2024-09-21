# Summaries
## € Schneier 2015: Applied Cryptography: Chapter 1: Foundations
**1.1 Terminology**
- ***Sender and receiver:*** the sender's goal is to send a private message securely to the receiver by making sure no one can read the message.
- ***Messages and Encryption:***
  - Message (Plaintext) -> Securing Message (Encryption) -> Encrypted Message (Ciphertext) -> in order to read Message (Decryption)
    <img src="https://github.com/user-attachments/assets/d35c8cef-f7e1-4180-bd6c-cfbe29ae4d28" width="500">
  - ****Cryptographers*** secure messages whereas ***Cryptoanalysts*** try to decrypt those. (For both: Cryptologists)
  - | Expression  | What it means |
    | ------------- | ------------- |
    | ***E(M) = C*** | The plaintext (M) which is being encrypted (E) equals to the ciphertext (C) |
    | ***D(C) = M*** | The ciphertext (C) which is being decrypted (D) equals to the plaintext (M) |
    | ***D(E(M)) = M*** | Both combined equals to the plaintext since in the end its what is being searched |
- In addtion to confidentiality: ***Authentication, Integrity, and Nonrepudiation***:
  - Authentication: Ensures the origin of the message.
  - Integrity: Ensures the message hasn't been altered.
  - Nonrepudiation: Prevents the sender from denying they sent a message.
- ***Algorithms and Keys***
  - There's two types of cipher (algorithm of encryption/decryption):
    - The first is using the same key for both ends (encryption and decryption) - <img src="https://github.com/user-attachments/assets/c766a204-036d-4faa-8e09-d9795ba103b1" width="90">
      <img src="https://github.com/user-attachments/assets/aff60ea5-9edb-48a4-a8ea-a71b5f347715" width="500">
    
    - The second way is to use different keys (one for encryption and another for decryption) - <img src="https://github.com/user-attachments/assets/8b3681bc-576d-483c-9025-b244775db0ae" width="90">
      <img src="https://github.com/user-attachments/assets/1ed371e2-1b66-463a-a75b-6ee852f24849" width="500">

  - The first can be referred as a Symmetric Algorithm whereas the second one can be referred as Public-Key Algorithm <img src="https://github.com/user-attachments/assets/c5e6e848-8e28-44b3-a638-8daddc421780" width="300">  <img src="https://github.com/user-attachments/assets/68d49d15-b4db-41df-b4f1-4d78ef34101a" width="300">

- ***Cryptanalysis***
  - There are lots of ways to find out the plaintext without access to the key, for example:
    - Ciphertext-Only Attack: trying to deduce the text or key with ciphertext only
    - Known-Plaintext Attack: trying to deduce the key with both ciphertext and plaintext
    - Rubber-Hose Cryptanalysis: ITS THE BEST WAY ;) by forcing, torture or blackmail 👀
- ***Security of Algorithms***
  - Unconditionally Secure: Systems like the one-time pad are unbreakable given unlimited resources
  - Computational Security: Most systems aim to be infeasible to break with current computational resources
  - Brute-Force Attacks: Trying all possible keys to decrypt, though computationally expensive, remains a threat

**1.2 STEGANOGRAPHY**
- The purpose is to hide the existence of a secret message within another message. For example with invisible ink or by hiding bits of a message in images.

**1.3 SUBSTITUTION CIPHERS AND TRANSPOSITION CIPHERS**
- A substitution cipher is one in which each character in the plaintext is substituted for another character in the ciphertext for example the famous Caesar Cipher or ROT13 whereas transposition ciphers rearrange characters of the plaintext in a specific order to form the ciphertext.

**1.4 SIMPLE XOR**
- Its a basic encryption method. It’s symmetric, meaning the same operation is used for both encryption and decryption. However, it’s easy to break.
  | Input | Output |
  | ----- | - |
  | 0 + 0 | 0 |
  | 0 + 1 | 1 |
  | 1 + 1 | 0 |
  | 1 + 0 | 1 |

**1.5 ONE-TIME PADS**
- Is the theoretically the perfect system: Each key letter is used exactly once, for only one message. The sender encrypts the message and then destroys the used pages of the pad or used section of the tape. The receiver has an identical pad and uses each key on the pad, in turn, to decrypt each letter of the ciphertext. The receiver destroys the same pad pages or tape section after decrypting the message. New message—new key letters.
  | Example | Encryption |
  | ------- | ---------- |
  | O (n.14) + T (n.19) = 33 - 26 | I (n.7) |

**1.6 COMPUTER ALGORITHMS**
- **DES (Data Encryption Standard)** is symmetric and the most popular computer encryption algorithm
- **RSA (named for its creators—Rivest, Shamir, and Adleman)** is the most popular public-key algorithm.
- DSA (Digital Signature Algorithm, used as part of the Digital Signature Standard) is another public-key algorithm. It cannot be used for encryption, but only for digital signatures.

**1.7 LARGE NUMBERS**
- Apparently the odds of winning the lottery is 1 in 4,000,000 but for me its non-existent lol

## Karvinen 2023: PGP - Send Encrypted and Signed Message with gpg
1. Generate Key Pair: Use "gpg --gen-key" to create a public/private key pair.
2. Export Public Key: Send the public key using "gpg --export --armor --output *output-filename*"
3. Encrypt Message: Encrypt the file with "gpg --homedir . --encrypt --recipient *address* --sign --output encrypted.pgp --armor message.txt"
4. Decrypt Message: Use "gpg --decrypt file.txt.gpg" to decrypt and verify the signature.
5. Verify Signature: Ensure the message is from the right sender with "gpg --verify"

# a) Encrypt and decrypt a message with 'gnupg', using PGP public key cryptography.
1. I generated a set of keys with my full name, email and a blank password/passphrase.
   ![image](https://github.com/user-attachments/assets/867b6279-4b1e-44ff-826b-5afd5cb814d3)
   
3. Then exported the Public Key
   ![image](https://github.com/user-attachments/assets/04138756-0711-4a41-a62c-796a61756ce6)
   
4. Created a txt file with a message and then encrypted the Message
   ![image](https://github.com/user-attachments/assets/660d9f66-e6ac-42df-a8c0-eafd4f67fd86)
   
5. Finally I decrypted the Message
   ![image](https://github.com/user-attachments/assets/7a50f7e0-0707-42ac-9829-7e41d6d85509)
   ![image](https://github.com/user-attachments/assets/fe986021-1333-4888-8057-c2ade16ab001)

# b) Password manager: KeePass
## I installed KeePass, its cloudless and free :)

Why a password manager is needed?
- Prevent password reuse: to generate and store unique passwords for every account.
- Guard against brute force attacks: to store complex passwords.
- Protect from phishing: to autofill credentials ONLY on legitimate sites.
- Encryption: to keep passwords encrypted and secure, accessible only by a master password.

1. Create a "Database" locally where everything will be stored, give it a name and set a password
   ![image](https://github.com/user-attachments/assets/41096767-d122-4bb5-baa5-3cfcbe75b4a2)
   ![image](https://github.com/user-attachments/assets/14b294b5-7a04-474c-9a70-e899d1108596)
   ![image](https://github.com/user-attachments/assets/ce08469b-0cd4-450c-8aea-9663f4322fc0)

2. The software asked me if I wanted an "Emergency Sheet" in case something happened, I accepted it and it looked like this:
   ![image](https://github.com/user-attachments/assets/b956b609-7618-43ad-baad-67e7c68a2598)

3. To enter new data, I went to "Entry" > "Add Entry" and entered everything as an example:
  ![image](https://github.com/user-attachments/assets/e47c03db-5e8d-4c04-849c-e98117b9de39)

4. If a password is needed, I just need to double click on the one in the list and a it automatically copies it to the clipboard BUT with a timer:
  ![image](https://github.com/user-attachments/assets/42555a4a-9d41-40fd-b7b8-2c02227a7b44)

# m) Voluntary Bonus: Encrypt and decrypt messages with CriptiQ
## ***This application was a group project of last semester, made by me and two other friends of mine***
For anyone that is interested in trying it out: https://gitlab.fhnw.ch/cryptiq/cryptiq

CriptiQ is a Java-based application designed to encrypt and decrypt messages using the One-Time-Pad (OTP) method. Users can encrypt and decrypt both text entries and entire files to protect their communications.

1. Enter the message and click on "Encrypt" then copy the encrypted message
   ![image](https://github.com/user-attachments/assets/b0296376-e7ec-4aef-a803-08e8f10114bf)

2. Paste the encrypted message above then click "Decrypt"
   ![image](https://github.com/user-attachments/assets/0230ce72-9ee0-4e49-a6aa-990f59c8adc4)

# o) Voluntary Bonus: Frequency distribution of letters for Italian and German
The six most common letters for Italian are: EAIONL
The six most common letters for German are: ENISRA
