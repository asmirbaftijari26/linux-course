# Summaries
## € Schneier 2015: Applied Cryptography: 2.3 One-Way Functions and 2.4 One-Way Hash Functions
- One-way functions are important for public-key cryptography especially for most protocols
  - It is easy to compute in one direction but hard to reverse, for example using 'x' as input in f(x) is easy to calculate but the reverse version of finding x from f(x) is difficult
  - It could take millions of years to re solve even with all computers in the world
  - Example: Breaking a plate is easy, reassembling it is almost impossible
  - Mathematically there is no proof that one-way functions exist
  - They aren't useful for encryption because decryption would be impossible

- Trapdoor one-way function is a special type of one-way function with a secret trapdoor
  - Its easy to compute in one direction and hard to reverse BUT with the key...reversing it is possible
  - Example: Disassembling a phone is easy, reassembling it is hard BUT with the assembly instructions possible

## 2.4 One-Way Hash Functions
- One-way hash functions are important to modern cryptography
  - They can convert a variable-length input (pre-image) into a fixed-length output (hash value)
  - Are used to create a "fingerprint" of the pre-image to indicate if two inputs are the same
  - They are easy to compute in one direction but hard to reverse (hash to pre-image)
  - Normally should be collision-free, meaning there shouldnt be two inputs with the same hash
  - A small change in the pre-image causes half the bits in the hash to change

- Message Authentication Code (MAC) is a hash function with a secret key that allows the recipient to verify the hash
  - The only difference to one-way hash functions resides with the addition of the key
  
# a) Install Hashcat. Test it with a sample hash
## 1. I updated and installed Hashcat
   <img src="https://github.com/user-attachments/assets/c8b3f1dc-bd5a-4ac6-9df1-72829a9e11df" width="600">

## 2. I created a new folder, went there and added Rockyou dictionary
   <img src="https://github.com/user-attachments/assets/3ac62fb7-8254-45aa-b730-b9ee496410cc" width="600">

## 3. Identified the Hash type to crack and cracked it with ***"hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -o solved"***
   <img src="https://github.com/user-attachments/assets/b79c1e12-a975-4965-b580-432a0f8a2639" width="600">

## 4. With ***"cat solved"*** found out the message
   <img src="https://github.com/user-attachments/assets/64900399-5ef4-41f5-8082-32e07f170a6b" width="600">

# b) Crack this hash: d595b2086532422bbe654bc07ea030df
***d595b2086532422bbe654bc07ea030df = disobey***

<img src="https://github.com/user-attachments/assets/c0c42d4a-7bbb-45e5-b882-5eb1db3329a7" width="600">

# m) Voluntary: Compile John the Ripper, Jumbo version
## 1. I downloaded the libraries required with ***"sudo apt-get -y install micro bash-completion git build-essential libssl-dev zlib1g zlib1g-dev zlib-gst libbz2-1.0 libbz2-dev atool zip wget"***
But I had to download ***"libssl-dev"*** apart, because I got errors
<img src="https://github.com/user-attachments/assets/7eec748e-57cf-4998-a38e-5a6f6a58f5ae" width="600">

## 2. Then I navigated to the folder and run ***"./configure"***
<img src="https://github.com/user-attachments/assets/f7b7740f-8ffc-4378-bb53-8c266b0df1da" width="600">

## 3. I compiled
<img src="https://github.com/user-attachments/assets/21ce6e7d-3010-42e5-96cb-c70b56aeed2d" width="600">

## 4. I ran it, and it gave me the version number.
<img src="https://github.com/user-attachments/assets/6c3c476c-3cf9-45f4-b3c7-4b8fea0bee58" width="600">

