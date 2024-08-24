# h1 - Should Tero wear a helmet?

## Braiterman et al 2020: Threat modeling manifesto

- Threat modeling = analyzing system to uncover vulnerabilities/threats
- Everyone should threat model
- Values: finding and fixing issues, collaboration, continuos refinement
- Principles: improving security&privacy, frequent analysis
  
>	Patterns that benefit threat modeling

  - Systematic approach
  - Creativity
  - Varied Viewpoints
  - Improvement
  - Theory into practice

>	Anti-Pattern to avoid

  - Relying on one person
  - Over-focusing on one problem
  - Aiming for perfect representation

## Shostack 2022: Welcome to the Worlds Shortest Threat Modeling Course
***What are we working on?***

- Collaboration = teamworking
- Sketching our visual representation because it will be probably imperfect
- Data flow diagrams

***What can go wrong?***

-	STRIDE (Improves threat modeling)
-	Killchain

***What are we going to do about it?***

- Track work
- Risk management

***Did we do a good job?***

- If you can recommend threat modelling then it means you did a good job

***Threats tend to follow data***

## OWASP CheatSheets Series Team 2021: Threat Modeling Cheat Sheet

- Threat modeling is ideally performed early in the SDLC, such as during the design phase.

> Advantages
  - Identifying Risks early
  - Increased Security
  - Improved Visibility

> Steps
  - System modeling with Flow Diagrams
  - Identify threats with ***STRIDE*** (***S***poofing, ***T***ampering, ***R***epudiation, ***I***nformation Disclosure, ***D***enial of Service, ***E***levation of privileges)
  - Each identified threat should have a response (Mitigate, Eliminate, Transfer, Accept)
  - And finally Review with key questions

> Challenges
  - Team lacks knowledge
  - Complexity & time-consuming
  - Lack of communication/collaboration

***SOLUTION*** = Threat Modeling Sessions & Training

## DARKNET DIARIES PODCAST - EP 133: I'm the Real Connor
Connor Tumbleson, a director of engineering, shared a strange experience where someone used his identity online. He received an email from a college student named Andrew who warned him that someone was using his identity to apply for jobs. Connor found that a fake Upwork profile had been created using his credentials, with someone else impersonating him in job interviews. Connor joined one of the interviews and to confront the impersonator but the impersonator left the call.

## a) Security hygiene
- Strong and different passwords
- Use Multiple Factor Authentication
- Do ***NOT*** click on every link
- Do ***NOT*** use public Wi-Fi
- Use VPN
- Keep devices up-to-date

## b) Make-belief boogie-man - a threat model for imaginary company.
***What are we working on?***
> Description

Crypto4Ever is a company specializing in digital currency solutions offering an exchange, wallet service and other blockchain based products like staking.

> Key Assets
- Crown jewel: Cryptocurrency holdings (client Assets)
- High priority: Exchange platform, wallets, nodes, transactions
- Meidum priority: User data (compliance)
- Low priority: Website

> Security supports business
- Ensure safe access to holdings
- Safeguard from malicious attacks on client assets
- Keep customers updated

> Customer is the king (to ensure revenue...)
- Company integrity should be mantained / access to company wallets to verify
- Product accessibility & usability
- Regulatory compliance

***What can go wrong***
