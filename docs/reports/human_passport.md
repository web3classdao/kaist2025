# 📄 [Project Title]  
- 👤 Author: [20250017 / 강재환]()
- 📆 Presentation Date: [2025-07-30]  

---

## 1. Overview

- **Human Passport**:  
- **Category**: Decentralized identity protocol  
- **Key Technologies / Platforms**: WorldCoin, BrightID, Proof of Humanity   
- **Official Links**:
  - [Website](https://app.passport.xyz/)
  - Foundation
  - Contract Address
  - Whitepaper
  - [Docs](https://docs.passport.xyz/) 
  - [GitHub](https://github.com/passportxyz/passport)
  - [X](https://x.com/HumnPassport)
  - Discord: N/A


### 📌 Summary  
Human Passport is a Web3-based system that allows individuals to own and control their **digital identity** using blockchain technology. Instead of relying on governments or centralized entities, users manage their identity and selectively prove it when needed. ***It’s not a passport for international travel*** — the Human Passport is simply a way to prove that you are a real human.

---

## 2. Background & Problem Statement

#### Currently, how do websites trust my identity?

- **Most digital identity systems today are controlled by centralized platforms such as Google, Facebook, or Apple.**
- Many websites rely on these services for authentication through options like “Sign in with Google” or “Continue with Facebook.”
- In this model, users don’t own their identity—they depend on third-party providers to vouch for them.

#### Can we trust companies to handle our identity data?

- **Users have no control over how their identity is stored, used, or revoked.**
- Centralized identity systems require us to fully trust corporations to manage our personal information.
- These companies may sell user data for advertising or share it with third parties without transparency.
- If a central server is hacked or compromised, millions of user identities can be leaked.

#### Centralized systems cannot tell if we are human or AI.

- **These systems typically verify accounts, not people.**
- Fake email addresses, phone numbers, or social media profiles can be generated in bulk by bots or malicious actors.
- AI agents can now bypass CAPTCHAs and simulate human-like behavior, making it harder than ever to distinguish real users from artificial ones.
- As a result, centralized systems offer poor bot resistance and lack a reliable mechanism for proof of personhood.

### Added by Jason

### 🧠 What Problem Did Human Passport Aim to Solve?

**Human Passport** originated as **Gitcoin Passport**, created to solve a critical problem in the Gitcoin Grants ecosystem: preventing **Sybil attacks** and ensuring that only **real humans** participate in Web3 incentives and governance.

---

### 💸 What Is Quadratic Funding (QF)?

**Quadratic Funding (QF)** is a funding mechanism that optimizes matching grants based on the **number of individual contributors**, not just the amount donated. It is designed to favor projects with **broad community support** over those with only a few wealthy backers.

> Matching formula (simplified):  
> Total Match = (∑√individual contributions)²

This means:
- A project with **1,000 people donating $1 each** will receive **more matched funds** than a project with **1 person donating $1,000**.

---

### 🛑 Why QF Is Vulnerable to Sybil Attacks

Since QF rewards **breadth of support**, attackers can create **fake (Sybil) identities** to simulate many small contributions and unfairly maximize matching funds.

### 🔓 Example Attack:
1. An attacker creates 100 fake wallets.
2. Each fake wallet donates $1 to their own project.
3. The system calculates this as high community support and allocates disproportionate matching funds.

This **defeats the purpose of QF**, which is to reflect **genuine public interest**.

---

### 🛠 Gitcoin Passport: The First Solution

Gitcoin Passport was introduced to assign **"Proof-of-Humanity" scores** to users using **trust signals** (called **stamps**) like:

- Web2: Google, Twitter, Facebook
- Web3: ENS domain ownership, wallet activity
- Identity protocols: BrightID, Proof of Humanity

Users with more credible stamps received a **higher Trust Bonus**, making their donations more influential in QF calculations.

---

### 🔄 Evolution into Human Passport

Gitcoin Passport eventually evolved into **Human Passport**, following a trajectory:

1. **Gitcoin Passport** – Anti-Sybil tool for Gitcoin Grants
2. **Passport.xyz** – Expanded as a general Web3 identity layer
3. **Human Passport** – After acquisition by **Holonym**, it aims to become the world’s largest **privacy-focused Proof-of-Humanity** protocol


---

> 👥 **Conclusion**: Human Passport solves a foundational Web3 problem — **how to verify real humans without compromising privacy** — and strengthens the fairness and sustainability of decentralized public goods funding like QF.




---

## 3. How It Works

### 🔍 3.1 Project Approach  
1. **Core Idea**: Create a decentralized identity system that allows individuals to prove they are real humans using Web3 technologies.  
2. Users maintain ownership over their identity and verification data, which is cryptographically secured.  
3. Once verified, users receive a non-transferable "Human Passport" that proves their humanness on-chain.
4. This can be used across Web3 platforms to enable human-gated access, reputation systems, and secure AI interactions.

---

### 🏗️ 3.2 Architecture  
- Provide a high-level overview of the system architecture.  
- Include a diagram or describe the components and how they are connected.  
- Focus on how data flows between users, models, smart contracts, etc.

---

### 🎯 3.3 Core Components  

| Stakeholder | How They Use / Earn the Token |
|-------------|-------------------------------|
| Web3 | Builds applications that require human verification. Pays HUMN tokens to access verified data or human-passport services. |
| Verifier / Node | Validates whether a user is a real human. |

---

### 🔁 3.4 Workflow Overview  

#### Collecting Stamps & HUMN tokens
1. User should collect "stamps" to build their own "identity"
2. Once we collect our stamps enough (20 points), we get token [HUMN]
3. Users use HUMN when proving themselves in Web3

![스크린샷 2025-07-30 100014](https://hackmd.io/_uploads/HJ4g1gPDel.png)

#### Validation
1. Client requests access to Web3
2. Web3 requests jobs to validate whether it is human or not
3. Validator detects jobs and send validation results
4. By results, validator could get results / slashing

![image](https://hackmd.io/_uploads/B1FHIGDwel.png)
---

## 4. Token Economy

Human Passport has **Human Token [HUMN]** 

#### Token Mehanism

| Mechanism | How does it work |
| -------- | -------- |
| Mint/Burn | HUMN tokens are minted as rewards for verified contributions (e.g., validators, data providers). |
| Staking / Slashing | Verifiers need to stake HUMN tokens to participate. If Validator results wrong answer, validators gets slashing (token loss) |


---

## 5. Project Status & Plan


#### Current Development Stage

The project is currently in the beta phase, with core features implemented and undergoing community testing. The team has released a public testnet and is inviting users to try out the identity verification flow using mock data or limited biometric inputs.
A mainnet launch is planned for Q4 2025, pending results from the beta phase and audit feedback.

#### Adoption

Several Web3 DApps (including governance DAOs and reputation systems) are experimenting with Human Passport integration for bot-resistant access. Adoption is still early, but several open-source contributors are involved in building wallet integration tools and ZK verification modules.

---

## 6. User Experience & Hands-on Review

### Collecting Stamps

I wanted to make myself approved. I tried Physical Verification.

![image](https://hackmd.io/_uploads/ryreLOUPlg.png)

I tried "Phone Verification"

![image](https://hackmd.io/_uploads/SkLpstLPex.png)
![image](https://hackmd.io/_uploads/rJ9jptIPge.png)



### Using API

We can use stamp API, which provides us users' stamps info.

![image](https://hackmd.io/_uploads/S1SYKbDPxg.png)


---

## 7. Why Blockchain

* **Self-sovereign identity**: Users own and control their credentials via their wallets. No third party can modify or revoke them.
* **Immutable proofs**: Once a Human Passport is issued on-chain, it cannot be forged or altered.
* **Interoperability**: Verified identity can be reused across multiple decentralized applications (DAOs, social networks, on-chain voting, etc.)
* **Transparent verification logic**: Smart contracts handle the issuance and validation of credentials transparently, with no hidden rules or bias.
* **Bot resistance**: On-chain uniqueness (e.g. 1 passport = 1 verified human) can help mitigate Sybil attacks without sacrificing user privacy.

---

## 8. Insights & Limitations

### ✅ Key Takeaways
- It can proove one's identity by various methods: "Web2 authentication", "Governance Id"
- This tool has evolved from gitcoin to larger scale to proove one's humanity identity.

### ⚠ Limitations / Open Questions
- Currently we can just proove ourself only by sign-in, but would people like the method paying tokens?
- People are not familiar with "crypto payment" yet.

- How can we make people to use this service? (To get used to)

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- I have found out that I have to use enough money (0.25 ETH) to prove myself as ethereum. Also, we need ethereum coins to prove some identities (stamps). I wondered would this be  because we don't need to pay any money to prove ourselves currently.

### ❓ Discussion Questions
- Is it fair to require users to spend money to prove their humanity in Web3?

---

## 10. Insight from others

-

---

## 11. References

- [Human Passport Docs](https://docs.passport.xyz/)

---

## Appendix 

# 🧾 DID & VC: A Simple Overview

## ✅ 1. What is DID (Decentralized Identifier)?
- A **decentralized, user-controlled digital identifier**.
- Not issued or managed by a central authority.
- Example: `did:example:123456abcdef`

## ✅ 2. What is VC (Verifiable Credential)?
- A **digitally signed certificate** that proves claims like diplomas, licenses, memberships, etc.
- Based on DID and **cryptographically verifiable**.
- Cannot be easily forged or tampered with.

---

## 🔁 Key Roles in the DID-VC Ecosystem

| Role        | Description                                      |
|-------------|--------------------------------------------------|
| **Issuer**  | Issues credentials (e.g., university, bank, gov) |
| **Holder**  | Receives and stores credentials (e.g., user)     |
| **Verifier**| Verifies the credential (e.g., employer, website)|

---

## 📊 DID-VC Workflow Diagram

This diagram shows the basic flow of how Verifiable Credentials work using DIDs.

Step 1: Credential Issuance  
Step 2: Presentation & Verification

                     +----------------+
                     |     Issuer     |
                     | (e.g. University, Bank) 
                     +----------------+
                             |
                             |  Issues Verifiable Credential (VC)
                             v
                     +----------------+
                     |     Holder     |
                     | (e.g. User Wallet/App)
                     +----------------+
                             |
                             |  Presents VC upon request
                             v
                     +----------------+
                     |    Verifier    |
                     | (e.g. Employer, Platform)
                     +----------------+


---

## 🔐 Key Features of DID-VC Systems

| Feature               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Privacy-Preserving** | Users can share only the minimum necessary data                            |
| **Tamper-Proof**       | Credentials are digitally signed, making forgery nearly impossible         |
| **Cryptographically Verifiable** | Verifiers can verify the credential without contacting the issuer         |
| **User-Owned Identity**| Users manage their own DIDs and credentials using personal wallets/apps    |

---

## 🎓 Example Scenario: University Diploma

1. **Issuer**: A university issues a digital diploma as a VC, signed using its DID.
2. **Holder**: The student stores the diploma in their digital wallet.
3. **Verifier**: A company requests proof of the student's graduation.
4. **Verification**: The student shares the VC, and the company verifies it using the university’s DID signature.

---

## [DID-VC Demo](https://opendid.omnione.net/community/demo/)

![image](https://hackmd.io/_uploads/HkXfUzPDlg.png)


---

## ✅ Conclusion

DID and VC systems allow individuals to:

- Control their own identity data  
- Share verifiable proof without revealing unnecessary details  
- Build trust in decentralized and privacy-respecting ways

Together, they form a foundational layer for **Web3 identity, decentralized reputation, and secure digital interactions**.





