# OWASP Summaries
## A01:2021 – Broken Access Control
- Definition: Broken Access Control means when someone can access data or perform actions beyond their permissions.
- Examples
  - By modifing URL
  - By modifing API requests
  - By acting as an user without being logged in
- How to prevent:
  - Implement access control mechanisms
  - Deny by default
  - Limit API requests
## A03:2021-Injection
- Definition: Injection is when a query or something is being sent in a form and it executes commands or to access data.
- Examples
  - SQL Injection
  - NoSQL
  - LDAP
- How to prevent:
  - Use safe API
  - Use LIMIT or other SQL Controls to prevent full leakage
  - Use positive server-side input validation
## A05:2021-Security Misconfiguration
- Definition: Security misconfiguation is when security settings are not clearly defined or mantained which opens the door to vulnerabilities and attacks.
- Examples
  - Unnecessary features are installed (like ports, services, privileges...) 
  - Default accounts still enabled and passwords unchanged
  - Software out of date
- How to prevent:
  - Use the same configuration in all environments but with different credentials
  - Implementing a minimal platform with only the necessary
  - Implementing an automated process which verifies the effectiveness
## A06:2021-Vulnerable and Outdated Components
- Definition: its when components with known vulnerabilities or old versions are being used.
- Examples
  - If you dont know what version you are using
  - Using outdated libraries
  - If developers dont test the compatibility for upgrades
- How to prevent:
  - Remove unnecessary components
  - Document all versions and set up alerts in case of vulnerabilities
  - Only download from official sources over secure links

# a) Installing WebGoat 2023.4
![image](https://github.com/user-attachments/assets/a7a2f57f-670c-46c7-9178-4975073a5a3c)
![image](https://github.com/user-attachments/assets/b290410f-ddaf-43be-ad07-6da3a661eb8d)

# b) F12. Solve Webgoat 2023.4: General: Developer tools
![image](https://github.com/user-attachments/assets/98fa4436-0d32-4b43-88bf-ccabfd29040a)

# c) Updating Linux
Everything Updated with 'sudo apt-get update' and 'sudo apt-get dist-upgrade'

# d) Sequel. Solve SQLZoo
## 0 SELECT BASICS
1) ![image](https://github.com/user-attachments/assets/841740f2-e176-41fa-84c9-7f22b4ccd2e9)
2) ![image](https://github.com/user-attachments/assets/aafba6c8-e0a7-4223-b0d4-2a9a300e5f3a)
3) ![image](https://github.com/user-attachments/assets/bc532563-bb9a-43ad-b4eb-d48f7d907e07)

## 02 SELECT from World, from first two subtasks
1) ![image](https://github.com/user-attachments/assets/88af1a6f-a0c4-45df-8256-133740a0e705)
2) ![image](https://github.com/user-attachments/assets/decb83b2-066a-4ef1-84a3-e8b6bee2349e)

# e) Johnny tables. Solve Portswigger Labs
I could not download Burp Suite it just said "Failed", but I solved it by inserting the Parameter on the URL (following one community video)

![image](https://github.com/user-attachments/assets/745bf5e4-9740-4b11-988b-94fa8b9e8571)

