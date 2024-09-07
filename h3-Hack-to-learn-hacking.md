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
- Chapter 2
  - x
- Chapter 4
  - x 
- Chapter 6
  - x
## a) Bandit oh-five. Solve Over The Wire: Bandit the first five levels (0-4)
xxx

## b) Can't fish. Disable networking and show that packets don't go trough. For example, use 'ping 1.1.1.1' (Cloudfare DNS server) or 'ping 8.8.8.8' (Google DNS server)
xxx

## c) Local only. Portscan your own computer using "localhost" address. It's illegal to portscan computers you don't own. Disconnect computer from the Internet while testing. Analyze your results
xx

## d) Daemon. Install a daemon (a server application) and port scan again. For example, you could install Apache web server or OpenSSH secure remote shell. Analyze the differences to scan without the daemon
xx
