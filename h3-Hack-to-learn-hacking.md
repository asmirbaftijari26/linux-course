# x) Summaries
## Disobey 2024: [D24] How Much Dirty Laundry Are Your Smart Home Devices Airing About You - Jack Fitzsimons
- Talking about Smart devices (IOTs)
- About (samsung and garmin) smartwatches: they collect data and pool it together
  - Samsung collects data even from kids, Garmin does too but because of Law they get rid of it
- on https://reports.exodus-privacy.eu.org/en/ you can enter the link of an App (from Google App store for example) and it will tell you how many trackers/permissions it abuses
- Even after knowing what permissions/data are collected, still we don't know WHO ELSE might be getting these data
  - one way to find out is: by decompiling the Application
    - using apktool(android) or ios-frida-dump(iOS) -> search through the code
- Monitoring traffic with a web proxy with zaproxy/frida
  - through API, a request can be made to get collected data
    - Samsung was readable
    - Garmin wasn't because of garmins specific file format -> so make it readable with Fit File Viewer
      -  All in all: not every data is being collected for example height and weight yes whereas stress or activity metrics not
- Comparing the Samsung Wear App and Garmin App in both Android and iOS -> generally on both systems they collect the same amount of data (on iOS slightly worse)
- SOLUTIONS:
  - We can block SOME third parties
  - We can use Garmin without the App (Samsung its not possible)
  - Self-hosting our own data with amazfit
## Karvinen 2020
- ***pwd:*** displays the current directory path.
- ***ls:*** lists files and directories in the current directory.
- ***cd:*** changes the current directory.
- ***nano:*** a text editor to create or edit files.
- ***cp:*** copies files from one location to another.
- ***rm:*** removes (deletes) files or directories.
- ***ssh:*** connects to a remote computer securely.
- ***scp:*** transfers files between computers.
- ***man:*** shows manual pages for command details.
- ***sudo:*** runs commands with superuser privileges.
- ***apt-get:*** manages software packages.
- ***history:*** shows all commands you have ran

## Voluntary Bonus: Bitcoin Whitepaper
- Chapter 2: Transactions
  - A chain of digital signatures where each owner transfers the coin by signing the hash of the previous transaction and the public key of the next owner
  - The receiver can verify the chain of ownership by checking the digital signatures
  - Transactions are public and participants "agree" on a single history of the order in which transactions are received
  - Majority of nodes must agree that each transaction was the first to be received, preventing double-spending without the need for a trusted central party.
- Chapter 4: Proof of Work
  - PoW is a consensus method, which requires Hardware to mine blocks and validate transactions. Its a peer-to-peer network that ensures blocks cannot be altered/manipulated without significant computational effort. Each new block is linked to the previous block so it creates a chain which cannot be manipulated. If an intrusion sneaks to take place, the network recognizes it and declines it. A malicious actor would need to control the majority of the network’s computational power to attack the system, which becomes increasingly difficult as the honest network grows. To adapt to increasing computational power and varying node participation, the difficulty of finding the required nonce adjusts dynamically. This ensures a steady rate of block generation.
    ![image](https://github.com/user-attachments/assets/c79e3dff-2be2-40d5-8f77-e2cfb64eb100)

- Chapter 6: Incentive
  - The incentive comes from mining Blocks or transaction fees. Once all Blocks are behind, the network can continue incentivising only through transaction fees, which makes this as a whole inflation free :)

## a) Bandit oh-five. Solve Over The Wire: Bandit the first five levels (0-4)
- Level 0:
  ![image](https://github.com/user-attachments/assets/4128b039-b41d-40ad-8a24-ce9541757c39)
- Level 1:
  ![image](https://github.com/user-attachments/assets/4e89565a-4b99-47c8-85a1-b3b3781fc195)
  ![image](https://github.com/user-attachments/assets/9cd605dd-1264-43f2-bd59-18d1b960eb6f)
- Level 2:
  ![image](https://github.com/user-attachments/assets/dd38ab29-320d-4022-8f4a-5b934d6ff57d)
  ![image](https://github.com/user-attachments/assets/caa3eda0-6b30-416d-b8a3-ad5ef2ca286b)
- Level 3:
  ![image](https://github.com/user-attachments/assets/dec614db-7c83-4ae3-9bfa-6a03999c05ef)
  ![image](https://github.com/user-attachments/assets/bd550c82-3680-4d40-8f89-efc9102f0f5a)
- Level 4:
  ![image](https://github.com/user-attachments/assets/56b54e14-ea9f-4ffd-a500-1a945ca005d9)
  ![image](https://github.com/user-attachments/assets/1de9b01b-07df-4a3d-a7e0-09ad335e7e3e)
- Level 5:
  ![image](https://github.com/user-attachments/assets/0120b02d-1b21-409c-a45d-0bfb3ba8fbd4)
  ![image](https://github.com/user-attachments/assets/5ace01bb-9e50-4126-bd66-4ae96060caea)

## b) Can't fish. Disable networking and show that packets don't go trough. For example, use 'ping 1.1.1.1' (Cloudfare DNS server) or 'ping 8.8.8.8' (Google DNS server)
Step 1: find interface name and disable it
![image](https://github.com/user-attachments/assets/3f821561-ea0f-432a-9f25-fa5bc4850b08)

Step 2: Test with ping 1.1.1.1 and 8.8.8.8
![image](https://github.com/user-attachments/assets/9223464d-1d08-411f-90f0-fdb0fec0aa99)

Step 3: Enable it again to test if packets go through
![image](https://github.com/user-attachments/assets/5551089d-cfaf-49c4-bfb8-ef8d4e8987e6)

## c) Local only. Portscan your own computer using "localhost" address. It's illegal to portscan computers you don't own. Disconnect computer from the Internet while testing. Analyze your results
![image](https://github.com/user-attachments/assets/dec7f50a-8967-4aac-be74-445b25ee763d)
- Port 25 (SMTP):
  - State: Open
  - Service: SMTP (Simple Mail Transfer Protocol)
  - Purpose: is used for sending emails
- Port 631 (IPP):
  - State: Open
  - Service: IPP (Internet Printing Protocol)
  - Purpose: is used for managing network printers

## d) Daemon. Install a daemon (a server application) and port scan again. For example, you could install Apache web server or OpenSSH secure remote shell. Analyze the differences to scan without the daemon
![image](https://github.com/user-attachments/assets/e8abbf8e-5520-412c-bc64-19b9ee73af29)

Without the daemon: Before installing any additional services, I only had 25/tcp (SMTP) and 631/tcp (IPP) open. These are related to mail transfer and printer services.
Whereas now with the daemon (Apache): I see port 80/tcp (HTTP) open for serving web pages! 

## Voluntary Bonus: Underthewire Century
Level 0 to 1:
![image](https://github.com/user-attachments/assets/087e465c-015e-4943-9408-3ec398c6a224)

Level 1 to 2:
![image](https://github.com/user-attachments/assets/5a764eb7-8cba-491c-a8c9-a3bfc6310b2c)
