# 📄 [Humanity Protocol]  
- 👤 Author: [20230712 / Cho Youngjoon]  
- 📆 Presentation Date: [2025-07-30]  

---

## 1. Overview

- **Project Name**: Humanity Protocol  
- **Category**: Decentralized Identity Verification  
- **Key Technologies / Platforms**: EVM‑compatible Layer 2 zk‑rollup, zero‑knowledge proofs, palm recognition AI, decentralized storage, self‑sovereign identity (SSI) frameworks  
- **Official Links**:  
  - [Website](https://www.humanity.org/)  
  - [Foundation](https://www.humanity.org/blog/humanity-protocol-launches-the-humanity-foundation)  
  - [Contract Address](https://etherscan.io/address/0xcf5104d094e3864cfcbda43b82e1cefd26a016eb)  
  - [Whitepaper](https://docs.humanity.org/whitepaper)  
  - [Docs](https://docs.humanity.org/)  
  - [GitHub]()  
  - [X](https://x.com/Humanityprot)  
  - [Discord](https://discord.com/invite/xRcwDJUzy7)  

### 📌 Summary  
Humanity Protocol (HP) is an open identity verification layer for Web3.

---

## 2. Background & Problem Statement

Identity is a fundamental right, but centralization, surveillance, and AI are threatening it. In Web 2.0, platforms like Google and Facebook built convenient infrastructures but ended up wielding vast control over personal data, raising serious privacy concerns.

Even in Web 3.0, privacy issues remain unresolved, with the core challenge being Sybil attacks.

**What is a Sybil attack?**  
Creating multiple fake personas to exploit a digital network. Blockchains defend against Sybil attacks at the consensus level (e.g., Proof‑of‑Work), but most applications lack sufficient protection. In other words, nothing stops one person from submitting multiple “valid” identities, which threatens on‑chain voting systems like dApps or DAOs. A robust identity framework to prevent these attacks is still missing.

Furthermore, with generative AI now able to produce biometric data nearly indistinguishable from real humans, we need reliable methods to prove “I am actually human.”

---

## 3. How It Works

### 🔍 3.1 Project Approach  
Humanity Protocol (HP) takes a new approach to address the fundamental flaws of existing PoP (Proof‑of‑Personhood) systems. Traditional PoP methods often rely on centralized data, leading to privacy violations and dystopian surveillance concerns. HP overcomes these limitations with its Proof‑of‑Humanity (PoH) mechanism, putting user privacy first.

PoH doesn’t just answer “Who are you?” It focuses on two core questions:

1. **Are you a Unique Human?**  
   Verifies that you are a non‑duplicated human on the network.

2. **Are you who you say you are?**  
   Confirms that the identity you claim (e.g., your Human‑ID NFT) truly belongs to you.

HP places great importance on integrating AI technology with its own hardware. In particular, developing and deploying deep learning models for biometric authentication is key to enabling accurate, efficient human proofs while preserving privacy.

---

### 🏗️ 3.2 Architecture  
The Humanity Protocol architecture is organized into three layers:

**User Interface Layer**  
- **Components**: Web/mobile apps, dashboards  
- **Function**: Provides a friendly UI for registration, claim requests, and progress monitoring, interfacing with backend services.

**Protocol Layer**  
- **Components**: Decentralized database (IPFS), Ethereum blockchain nodes  
- **Function**: Validates user credentials, executes smart contract rules, and records all transactions on‑chain.

**Smart Contract Layer**  
- **Components**: VCC and RBC smart contracts  
- **Function**: Automates credential issuance, reward tracking, and disbursements.

![Architecture Diagram](https://hackmd.io/_uploads/rJHu4lLPgl.jpg)

---

### 🎯 3.3 Core Components  

**Biometric Authentication**  
Biometrics have long been a strong proof of human uniqueness, but traditional methods (fingerprint, face) are now vulnerable to AI deepfakes and widespread image availability. HP instead uses palm pattern and palm vein recognition for higher spoof resistance and accessibility.

![Palm Recognition](https://hackmd.io/_uploads/SJMbbW8vlx.png)

**$H Token**
HP’s incentive system centers on the ERC‑20 `$H` token, with a fixed supply of 1 billion and divisibility to 8 decimals. It serves as the gas token for blockchain operations and supports:

- Humanity attestation  
- Identity verification  
- Credential validation  
- Staking rewards  
- DAO governance  
- “Coins for Humanity” community rewards  

**Smart Contracts**  
Immutable blockchain programs that encode identity issuance and management logic, replacing centralized authorities. They automatically run registration, verification, and reward flows, ensuring transparency and tamper proofing.

**IPFS**  
The InterPlanetary File System, a decentralized file protocol that stores metadata off‑chain, preventing any single entity from holding all data and enhancing censorship resistance.

**Ethereum Nodes**  
By leveraging the established Ethereum network, HP anchors proofs and NFT minting to a secure, immutable ledger.

**Zero‑Knowledge Proofs (ZKP)**  
ZKPs allow users to prove they know certain data without revealing it. In PoH, they ensure:

- **Privacy**: Raw biometric data never leaves the device.  
- **Uniqueness**: Guarantees the biometric has not been used before.  
- **Reusability**: One proof works across multiple dApps.  
- **Interoperability**: Compatible with any ZKP‑capable platform.

**zkProofer Nodes**  
Core to HP’s self‑sovereign identity system, these nodes generate and verify ZK proofs off‑chain, then submit rollup transactions. Participation requires a zkProofer node license. A dual‑incentive model rewards operators both with staking rewards and 25% of verification fees from third‑party integrations.

---

### 🔁 3.4 Workflow Overview  

![Workflow Diagram](https://hackmd.io/_uploads/H1kX4WIDlx.jpg)

1. **Scan & Commit**  
   User scans palm via the SDK; a cryptographic commitment is generated locally.

2. **ZK Proof Generation**  
   zkProofer node creates a zero‑knowledge proof showing the commitment is unique.

3. **submitProof**  
   Proof and staking collateral are sent to the Layer 2 rollup smart contract.

4. **Challenge & Finalize**  
   During a 3‑5 day challenge window, anyone can call `challengeProof`. If unchallenged, `finalizeProof` mints the Human‑ID NFT.

5. **DApp Integration**  
   dApps check for Human‑ID NFT ownership to enforce one‑person‑one‑vote, Sybil‑resistant airdrops, or real‑world access control.

---

## 4. Token Economy

> Humanity Protocol operates its own utility and governance token, `$H`.

**Token Name & Type**  
- `$H` (ERC‑20), divisible to 8 decimals  
- Total fixed supply: 1,000,000,000

**Primary Use Cases**  
- Gas token for blockchain operations  
- Humanity attestation, identity verification, credential validation  
- Staking rewards, DAO governance, “Coins for Humanity” community rewards

### Token Allocation

| Category                          | Allocation | Description                                      |
|-----------------------------------|------------|--------------------------------------------------|
| Early Contributors (Team)         | 19%        | Core team and early contributors                 |
| Investors                         | 10%        | External investors                               |
| Human Institute Strategic Reserve | 5%         | Incentives for service operators                 |
| Foundation Operations Treasury    | 12%        | Foundation operations, exchange liquidity, future grants |
| Ecosystem Fund                    | 24%        | Grants for partners and developers               |
| Identity Verification Rewards     | 18%        | Incentives for zkProofer node operators          |
| Community Incentives              | 12%        | Onboarding rewards (airdrops, referrals, etc.)   |

### Lockup & Vesting Schedule

| Category                          | Cliff (months) | Vesting (months) | TGE Unlock |
|-----------------------------------|----------------|------------------|------------|
| Early Contributors (Team)         | 12             | 24               | 0%         |
| Investors                         | 12             | 18               | 0%         |
| Human Institute Strategic Reserve | 12             | 18               | 5%         |
| Foundation Operations Treasury    | 0              | 48               | 50%        |
| Ecosystem Fund                    | 0              | 48               | 0%         |
| Identity Verification Rewards     | 6              | 42               | 0%         |
| Community Incentives              | 0              | 0                | 100%       |

### Validator & Staking Rewards

- **Minimum Stake**: 100,000 $H  
- **Delegation**: Token holders can delegate to validators and earn a share of rewards  
- **Verification Fee Distribution** (fees paid by service requesters):  
  - 25% → Validator & delegators  
  - 25% → General staking pool  
  - 50% → zkProofer operators & Humanity Foundation treasury

### Risks & Disclosures

- `$H` is designed for protocol fees, network security, and governance—it is **not** an investment product.  
- Various risks include technical changes, governance decisions, adoption levels, and security threats.

---

## 5. Project Status & Plan

- **Current State**: The HP mainnet launched last week, providing Sybil‑resistant identity verification on Ethereum and Gnosis chains.  
- **Testnet Adoption**: Phase 1 testnet began on September 30, 2024, attracting nearly 150K participants in its first week. Phase 2 beta, which introduced palm scanning, is now live ahead of full mainnet integration.  
- **Developer Community & Open Source**: The `proof-of-humanity-v2-contracts` GitHub repo has 22 stars, 20 forks, 238 commits, and 10 open PRs, with the latest merge last month—showing active maintenance.  
- **Partnerships & Funding**: HP raised $20 M in a Series A led by Pantera Capital and Jump Crypto, valuing the project at $1.1 B. They are collaborating with Prenetics on DNA‑based identity verification.  
- **Token Listings & Market Activity**: The ERC‑20 `$H` is listed on major exchanges, with a circulating supply of ~182.5 M, a market cap of ~$91.6 M, and 24 h volume of ~$34.6 M.  
- **Roadmap & Future Plans**: Phase 2 will roll out DePIN hardware scanner integration and cross‑chain bridging. Phase 3 will introduce real‑world access control and DAO governance on mainnet.

> **Insight:** Mainnet launch and strong testnet traction signal real adoption, but widespread dApp integrations, hardware distribution, and active governance will determine long‑term success.

---

## 6. User Experience & Hands‑on Review *(if applicable)*

**Testnet Token Distribution**  
- Faucet: https://faucet.testnet.humanity.org/  
- Requirement: Wallet must hold at least 0.001 ETH on Ethereum Mainnet L1

**Testnet Info**  
- Network: Humanity Testnet  
- RPC URL: https://humanity-testnet.g.alchemy.com/public  
- Chain ID: 7080969  
- Currency Symbol: tHP  
- Explorer: https://explorer.testnet.humanity.org  

![Dashboard Screenshot](https://hackmd.io/_uploads/SyyE_MLwlg.png)  
![NFT Claim Screenshot](https://hackmd.io/_uploads/rkHvcfUvlg.png)  
![Explorer Screenshot](https://hackmd.io/_uploads/SJF4dG8Dee.png)

After registering a Human ID on the official site and verifying via the app, you can log in at https://app.humanity.org/credentials. Currently only Android verification is supported, so I was unable to proceed further.

![image](https://hackmd.io/_uploads/H1l3jM8Pex.png)

Third‑party integrations require an API key. I applied but received no response, so could not continue.

---

## 7. Why Blockchain

- **Intrinsic Sybil Resistance**  
  Blockchain’s immutable ledger prevents duplicate or forged Human‑ID issuance, something centralized systems cannot guarantee.

- **Self‑Sovereign Identity**  
  Raw biometric data stays encrypted off‑chain; only commitments and ZK proofs are stored on‑chain, minimizing privacy risks.

- **Programmable Money & Governance**  
  Automated staking mechanics, challenge/slashing logic, and ERC‑721 NFTs enable composable identity and governance functions.

- **Global Permissionless Access**  
  Anyone with a wallet can participate, without reliance on banks or centralized ID providers—opening services to the unbanked.

- **Decentralization Is Essential**  
  Centralized control could censor proofs or exploit data. Only a fully decentralized model aligns with Web3’s permissionless ethos.

---

## 8. Insights & Limitations

### ✅ Key Takeaways  
- Combining palm biometrics with ZK proofs achieves high accuracy without exposing sensitive data.  
- DePIN integration aligns hardware operators with on‑chain incentives.  
- Simple SDK integration and NFT issuance make it easy for developers to add one‑person‑one‑vote or Sybil‑resistant airdrops.

### ⚠ Limitations & Challenges  
- Distributing affordable, reliable scanners remains complex and costly.  
- Compliance with global data protection laws (GDPR, CCPA) adds legal overhead.  
- Low‑light or poor camera conditions can impair scan reliability.  
- A 3–5 day on‑chain challenge window may be too slow for real‑time use; off‑chain dispute mechanisms are needed.

---

## 9. Reflections & Discussion

### 💡 Personal Reflections  
- Palm‑vein recognition felt less invasive than fingerprints or facial scans, offering a fresh privacy‑centric approach.  
- ZK proofs convincingly marry privacy with transparency, boosting trust in blockchain identity.  
- While device setup and network switching UX still need polish, the wallet‑signature flow is vastly simpler than traditional KYC.  
- I look forward to real‑world DePIN use cases—like secure building access—making blockchain identity seamless in everyday life.

### ❓ Discussion Questions  
1. **Decentralized Scanner Deployment**  
   - How can affordable, reliable scanners be distributed globally?  
   - Could public venues or mobile pop‑up stations help?  
2. **Governance & Power Balance**  
   - What mechanisms prevent plutocracy in Human‑ID NFT voting?  
3. **Regulatory & Ethical Considerations**  
   - How can biometric data rights (consent, deletion) be enforced both on‑chain and off‑chain (GDPR, CCPA)?  
4. **Ecosystem Growth & Network Effects**  
   - What incentives will drive dApp developers and service providers to adopt PoH?  
   - How can PoH become a default option in mainstream apps (social media, gaming, finance)?

---

## 10. Insight from Others

After each class presentation, we’ll form small discussion groups to tackle Section 9’s questions and record key points here.

---

## 11. References

- [Whitepaper](https://docs.humanity.org/whitepaper)  
- [Docs](https://docs.humanity.org/)  
