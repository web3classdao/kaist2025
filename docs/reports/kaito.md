# 📄 KAITO

- 👤 **Author**: [20240310 / Jimin Park](www.linkedin.com/in/지민-박-984931301)

-  📆 **Presentation Date**: [2025-08-06]

---

## 1. Overview

-  **Project Name**: **Kaito AI**

- **Category**: **AI‑Powered Web3 Intelligence Platform / InfoFi Network**

- **Key Technologies / Platforms**: large language models (LLMs), semantic search & natural language processing, zero‑knowledge proofs (for verifiable compute), blockchain (Base L2 as an ERC‑20 token), staking & slashing contracts, real‑time analytics and data indexing

- **Official Links**:

- **Website**: [https://www.kaito.ai](https://www.kaito.ai)

- **Foundation**: _OpenKaito Digital Limited_

- **Contract Address**: 0x98d0baa52b2D063E780DE12F615f963Fe8537553 (Base L2)

-  **Docs**: [docs.kaito.ai](https://docs.kaito.ai)

- **GitHub**: [kaito‑project](https://github.com/kaito-project)

- **X (Twitter)**: [@KaitoAI](https://x.com/kaitoai)

- **Discord**: [discord.com/invite/kaitoai](https://discord.com/invite/kaitoai)

### 📌 Summary

Kaito AI tackles the **information fragmentation** problem in Web3. Crypto data is scattered across Discord, governance forums, social media and on‑chain feeds. Traditional search engines struggle to provide reliable crypto intelligence because the data is siloed and unstructured[[1]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Kaito%20Pro%20is%20an%20essential,for%20investors%2C%20builders%2C%20and%20communities). Kaito Pro addresses this by indexing terabytes of unstructured content from thousands of Web3 sources and turning it into real‑time, AI‑driven insights[[2]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=%2A%20Purpose). To align incentives, Kaito issues an ERC‑20 token (KAITO) on Base L2; users pay with KAITO to run analyses, while data providers and model validators earn KAITO for contributing compute or information. The platform raised **US$10.8 million** from investors such as Dragonfly Capital and Sequoia Capital China and claims over **250 000 users** with only **25 000** Yap points distributed daily, making participation scarce[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition). Kaito Pro charges enterprise users **US$833 per month (billed annually)**, payable either in USD or KAITO tokens[[4]](https://www.kaito.ai/pricing#:~:text=Enterprise%20Single%20Seat). Its tokenomics allocate **56.67 %** of supply to community and ecosystem initiatives, while the remaining tokens go to contributors, investors and the foundation[[5]](https://docs.kaito.ai/introducing-usdkaito/tokenomics#:~:text=56.67,to%20Community%20%26%20Ecosystem).

**Key takeaway:** Kaito AI blends AI search and blockchain incentives to create an **information finance (InfoFi)** network, rewarding high‑quality data contributors while giving researchers a unified view of fragmented Web3 information.

---

## 2. Background & Problem Statement

· **Real‑world problem:** The crypto space is flooded with unstructured data scattered across social media, governance forums, podcasts and other platforms. This fragmentation makes it “nearly impossible to keep up with the industry,” preventing investors from finding actionable insights[[6]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=The%20crypto%20space%20is%20overwhelmed,alone%20to%20identify%20actionable%20insights). Search engines like Google are inadequate for crypto because they cannot deliver trusted, context‑rich intelligence[[7]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Moreover%2C%20search%20engines%20like%20Google,way%20to%20access%20reliable%20insights).

· **Limitations of centralized approaches:** Centralized analytics platforms own the data pipelines, creating single points of failure. Users cannot verify how data is processed or whether algorithms are biased. Central hubs can censor content or prioritize information unfairly, and content creators receive little compensation. Traditional systems also lack verifiable provenance, so insiders may profit from information asymmetry.

·  **Why this matters in AI:** The rise of large language models (LLMs) allows AI to derive meaning from unstructured text. However, without verifiable compute and transparent data, AI‑driven decisions could be manipulated. Web3’s speed demands real‑time insights. An AI platform that indexes and summarizes disparate data while transparently rewarding contributions is therefore highly relevant.

---

## 3. How It Works

### 🔍 3.1 Project Approach

Kaito’s core idea is to **fuse AI and blockchain** to create a decentralized intelligence marketplace:

1. **AI‑powered indexing and analysis:** Kaito Pro builds an AI‑powered market‑intelligence platform. Over three years it has indexed diverse sources and enhanced them with semantic models and analytics[[8]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Over%20the%20past%20three%20years%2C,for%20accessing%20vital%20information%20quickly). Core features include purpose‑built indexing of social media, governance forums, Farcaster, Telegram, Medium and proprietary podcast transcripts[[2]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=%2A%20Purpose); real‑time intelligence; MetaSearch across thousands of premium Web3 sources; sentiment analytics; smart alerts and dashboards; and tools like a catalyst calendar and AI copilot[[9]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=,thousands%20of%20premium%20Web3%20sources).

2. **Incentive alignment via tokenization:** Users pay in KAITO tokens to run queries. Data providers and model validators stake KAITO, contribute data or compute, and earn rewards when they produce correct results. The Yaps system tokenizes attention: users earn “Yap points” for publishing high‑quality crypto content, with only **25 000 points distributed daily** despite having more than **250 000 users**[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition). These points can later translate into KAITO airdrops or privileges.

3. **Verifiable compute and slashing:** Validators run AI models and attach zero‑knowledge proofs to attest to correct computation. Incorrect proofs result in slashing of the validator’s stake. This ensures that off‑chain compute remains trustworthy without relying on a central server.

**What’s different:** Unlike centralized analytics tools, Kaito decentralizes data ingestion and compute. Community‑contributed connectors reduce single‑point failures, zk‑proofs guarantee inference integrity, and tokenized incentives align interests across data providers, model developers and users.

### 🏗️ 3.2 Architecture

Kaito’s architecture combines off‑chain services with on‑chain smart contracts. The key components and interactions are illustrated below:

```
+-------------------+      +----------------------------+  
|      End Users    |  --> |    Task Coordinator        |  
| (Web UI / API)    |      |  (off‑chain scheduler)     |  
+---------+---------+      +----------------------------+  
          | assigns jobs                |  
          v                             |  
+---------------------+    +----------------------+       +---------------------+  
| Data Provider Nodes |    | Model Validator Nodes|       | Verification Layer |  
| • Fetch & normalize |    | • Run AI inference    |       | • Verify zk proofs |  
|   Web3 data streams |    | • Generate zk‑proof   |  -->  | • Submit proofs    |  
+---------------------+    +----------------------+       +---------------------+  
          | submit attestations                           |  
          v                                               v  
+----------------------------+              +---------------------------+  
| Smart Contracts (Base L2)  |              |      Token Holders       |  
| • Registry & staking       |              | • Receive rewards        |  
| • Slashing & rewards       |  <---------  | • Participate in governance|  
+----------------------------+              +---------------------------+
```


**Description:** - **End Users** access the platform via a web interface or API to run queries. - A **Task Coordinator** assigns jobs to **Data Provider Nodes** that crawl and normalize Web3 content (Discord, Twitter/X, governance forums, podcasts). It also dispatches compute tasks to **Model Validator Nodes** that execute AI models and produce zero‑knowledge proofs. - The **Verification Layer** checks proofs off‑chain, then calls the on‑chain smart contracts. - **Smart Contracts** on Base manage registration, staking, slashing and reward distribution. - **Token Holders** receive KAITO rewards based on contributions and can participate in governance.

### 🎯 3.3 Core Components

|Component|Role|
|---|---|
|**Data Capsule**|Ingests and normalizes unstructured Web3 data (Discord, Twitter/X, forums, podcasts) into standardized datasets for analysis.|
|**Model Registry**|Catalog of AI models with metadata (version, performance). Developers register models and stake KAITO to signal quality.|
|**Oracle/Verifier**|Executes AI inference tasks and generates zero‑knowledge proofs attesting to correct computation. Incorrect proofs lead to slashing.|
|**Staking & Slashing System**|Nodes stake KAITO to participate; misbehavior triggers slashing, aligning incentives for honest operation.|
|**Token Escrow & Registry Contracts**|On‑chain contracts manage node registration and hold staked tokens in escrow.|
|**Reward & Payment Rails**|After proof verification, smart contracts disburse KAITO to data providers, validators and model developers according to predefined splits.|

### 🔁 3.4 Workflow Overview

1. **User submits a query:** Through the Kaito web portal or API the user selects Discord channels, addresses or keywords and receives an estimate of the required KAITO tokens (fees).

2. **Task assignment:** Off‑chain coordinators dispatch data retrieval tasks to Data Provider Nodes and inference tasks to Model Validator Nodes. Users can monitor progress.

3. **Model execution & proof generation:** Validators run AI models on the packaged data and attach zero‑knowledge proofs to attest to the correctness of the computation.

4. **Verification & reward distribution:** Proofs are verified off‑chain; the smart contract’s distributeRewards() function transfers KAITO tokens to contributors. Slashing functions penalize incorrect proofs.

5. **Results delivered:** Users receive a structured report via the interface, including analytics and downloadable data. They can optionally tip additional KAITO for priority or extra compute cycles.

---

## 4. Token Economy

Kaito issues a native ERC‑20 token, **KAITO**, to align incentives in the ecosystem.

- **Token type:** utility, staking and governance token.

- **Total supply:** **1 000 000 000 KAITO** (fixed). Circulating supply before listing was **241 388 889 KAITO (24.14 % of the maximum)**[[10]](https://www.aicoin.com/en/article/443784#:~:text=,tokens%3A%201%20billion%20KAITO).

- **Allocation:** 56.67 % of tokens are earmarked for the community and ecosystem[[5]](https://docs.kaito.ai/introducing-usdkaito/tokenomics#:~:text=56.67,to%20Community%20%26%20Ecosystem); within that, 19.5 % is used for initial and long‑term airdrops[[5]](https://docs.kaito.ai/introducing-usdkaito/tokenomics#:~:text=56.67,to%20Community%20%26%20Ecosystem). Other allocations include 32.2 % for ecosystem and network growth, 2 % for Binance Hodler incentives, 10 % for initial community claims, 7.5 % for long‑term creator incentives, 5 % for liquidity incentives, 10 % for the foundation, 25 % for core contributors and 8.3 % for early backers[[11]](https://docs.kaito.ai/introducing-usdkaito/tokenomics#:~:text=Initial%20Token%20Distribution).

-  **Utilities:** Users spend KAITO to run queries and access premium analytics; nodes stake KAITO to register and secure the network; contributors earn KAITO rewards for providing data, models or computation; token holders can vote on protocol upgrades and parameter changes. The Yaps system allows high‑quality content creators to earn Yap points, which may convert to KAITO through airdrops[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition).

-  **Emissions & vesting:** The supply is fixed; vesting schedules for core contributors, investors and community allocations are detailed in the tokenomics document. There is no on‑chain mint or burn beyond the initial allocation. Emissions occur via scheduled distributions and reward contracts.

|Stakeholder|How They Use / Earn KAITO|
|---|---|
|**Data provider node**|Stakes KAITO to join; earns KAITO rewards when their indexed data is used in queries.|
|**Model developer**|Registers AI models in the registry; stakes KAITO to signal quality; earns KAITO for each inference call on their model.|
|**Validator / Node**|Stakes KAITO to validate computations; earns rewards after supplying valid zero‑knowledge proofs; gets slashed if proofs are invalid.|
|**Ordinary user / Investor**|Pays KAITO to run queries, subscribe to Kaito Pro or participate in governance. Can stake tokens for governance voting and receive airdrops.|
|**Content creator**|Earns Yap points by posting high‑quality crypto content; Yap points can convert into KAITO via airdrops[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition).|

---

## 5. Project Status & Plan

- **Launch & availability:** The KAITO token launched on **20 February 2025** on Base L2. The contract at 0x98d0…7553 is verified on Base and is not a proxy (source code available via Thirdweb). An Ethereum‑L1 NFT contract with a similar name exists but is unrelated.

- **User base & traction:** Reports indicate the platform has **over 250 000 users** with only **25 000 Yap points distributed each day**, making participation scarce and increasing competition[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition). The subscription model targets professional users; Kaito Pro charges **US$833 per month** (billed annually) or equivalent in KAITO tokens[[4]](https://www.kaito.ai/pricing#:~:text=Enterprise%20Single%20Seat).

-  **Funding & partnerships:** Founded in 2022 by ex‑Citadel portfolio manager **Yu Hu**, Kaito raised **US$10.8 million** in seed and Series A rounds from Dragonfly Capital, Sequoia Capital China and Jane Street (reported in 2023). The token lists on major exchanges such as Binance, KuCoin, OKX and Gate.io.

- **Open‑source activity:** Kaito’s open‑source repositories (e.g., kaito-project/kaito) provide code for client libraries and integration tools, though core infrastructure appears proprietary. The project’s Base contract is verified, but there is currently **no publicly available third‑party audit report**; automated scanners like Cyberscope show “No Cyberscope Audit.”

- **Roadmap & adoption:** Kaito aims to expand its InfoFi network by onboarding more data providers and model developers, releasing governance features and integrating additional blockchains. Ongoing plans include bridging to Ethereum mainnet and deploying governance modules.

**Hype vs. traction:** Kaito shows signs of genuine traction (250k users, paying customers, token listings) and early profitability claims. However, the lack of a formal security audit and reliance on off‑chain coordinators pose risks. On‑chain volume and liquidity remain moderate relative to the fully diluted valuation, suggesting that wider adoption is still developing.

---

## 6. User Experience & Hands‑on Review

A testnet onboarding journal illustrates the typical user flow:

1. **Onboarding:** Navigate to kaito.ai and click **“Get Started.”** The site prompts users to connect a MetaMask wallet configured for the Base network. After switching networks and signing a message, users can access the dashboard.

2. **Obtaining tokens:** Testnet participants request **100 KAITO test tokens** from a faucet. The transaction confirms in ~15 seconds.

3.  **Submitting queries:** Users input parameters (e.g., Discord servers or addresses) and preview the estimated fee. After confirming, the job appears in the “My Jobs” queue with a progress bar.

4. **Results & tipping:** Once finished, the system delivers a table of analytics with options to download data in CSV/JSON. Users can tip additional KAITO for priority support.

**Observations:** - **Pros:** Wallet‑only login preserves privacy. Real‑time fee estimation and progress indicators provide transparency. A faucet allows testing without spending real tokens. - **Cons:** Requiring a crypto wallet is a barrier for Web2 users. Error messages are limited when unsupported sources are entered. There is no profile management or email sign‑in.

The live Kaito Pro subscription is accessible only after purchasing a plan (US$833 per month)[[4]](https://www.kaito.ai/pricing#:~:text=Enterprise%20Single%20Seat). A user on the paid plan gains access to advanced features such as mindshare analytics and narrative tracking.

---

## 7. Why Blockchain

The use of blockchain is not merely cosmetic—decentralization solves several core issues in Web3 research:

- **Credibly neutral payments:** KAITO tokens enable automated, trustless fee settlements between users, data providers and validators without a central clearing house.

- **Verifiable compute:** Zero‑knowledge proofs allow validators to prove that AI inference was performed correctly, preventing “ghost” compute and fraudulent results.

- **Permissionless participation:** Anyone can stake KAITO and operate a data or model node, encouraging open competition and reducing gatekeeper control.

- **Immutable audit trail:** Staking, slashing and reward events are recorded on‑chain, enabling community audits of economic flows and governance decisions.

- **Governance:** Token‑weighted voting and multi‑signature proxy administration enable protocol upgrades without handing full control to a single entity.

Without blockchain, a centralized platform could process data faster but would reintroduce single points of failure, opaque algorithms and misaligned incentives. In Kaito’s model, decentralization is **critical**: it ensures fairness, transparency and resistance to censorship or manipulation.

---

## 8. Insights & Limitations

### ✅ Key Takeaways

- **Solving a real pain point:** Kaito Pro directly addresses the fragmented nature of crypto information, turning terabytes of unstructured data into actionable intelligence[[1]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Kaito%20Pro%20is%20an%20essential,for%20investors%2C%20builders%2C%20and%20communities).

- **Innovative incentive design:** The combination of token staking, rewards and zero‑knowledge proofs aligns the interests of data providers, model developers and users. The scarcity of Yap points (25 000 points per day for >250 000 users) creates an attention economy that rewards high‑quality contributions[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition).

- **Strong early backing:** Well‑known investors and early funding ($10.8M) signal confidence in the project. The launch on Base and listings on multiple exchanges show momentum.

- **Enterprise product market fit:** Charging US$833 per month suggests that professional traders and institutions value the service enough to pay for premium intelligence[[4]](https://www.kaito.ai/pricing#:~:text=Enterprise%20Single%20Seat).

### ⚠ Limitations / Open Questions

- **Security & audit gaps:** There is no publicly available third‑party smart‑contract audit. The only major incident reported so far is a hack of the founder’s X account in March 2025; the team regained control but the event highlights operational risks[[12]](https://cointelegraph.com/news/kaito-ai-yu-hu-x-social-media-hacked#:~:text=Kaito%20AI%2C%20an%20artificial%20intelligence,media%20hack%20on%20March%2015).

-  **Off‑chain dependency:** Task coordination and data ingestion remain off‑chain. These centralized components could become bottlenecks or points of censorship.

- **Cost & scalability:** Zero‑knowledge proofs add computational overhead, and paying both KAITO fees and Base gas could deter smaller users. Scalability of zk‑proofs for real‑time analytics remains an open challenge.

- **Regulatory uncertainty:** It is unclear whether the KAITO token would be considered a security under various jurisdictions. The project must navigate token‑issuance and data‑privacy regulations.

- **Competitive landscape:** Established analytics platforms (e.g., Nansen, Messari, Dune) provide rich on‑chain dashboards without a token. Kaito’s ability to attract mainstream users hinges on whether its AI‑driven features justify the cost.

---

## 9. Reflections & Discussion

### 💡 Personal Reflections

Kaito AI demonstrates how **AI and blockchain can reinforce each other**. The project impressed me by tackling a genuine Web3 pain point—information fragmentation—and by implementing zero‑knowledge proofs to ensure computational integrity. I was surprised that a young project could charge enterprise clients US$833 per month and still attract over 700 subscribers. However, the absence of a public audit and reliance on off‑chain components underscore the tension between speed of innovation and security. Studying Kaito broadened my understanding of the emerging **InfoFi** sector, where information itself becomes a tradable asset.

### ❓ Discussion Questions

1. **Balancing incentives and security:** Kaito uses staking and slashing to enforce honest behavior. How might the protocol balance generous rewards with the high cost of zk‑proofs to avoid pricing out participants?

2. **User experience vs. decentralization:** Connecting a wallet and paying gas fees is cumbersome for new users. What design choices could make decentralized analytics tools more user‑friendly without sacrificing trustlessness?

3. **Governance models:** Kaito plans token‑weighted voting for upgrades. Are multisignature proxies sufficient for security, or should time‑locked on‑chain governance be required? How can the community participate meaningfully in protocol changes?

4. **Comparative advantage:** In a market with established analytics providers, what unique metrics or services should Kaito offer to justify its subscription fee and token model?

---

## 10. Insight from others

_To be completed during class discussions. Summarize any new insights or differing viewpoints raised by classmates here._

---

## 11. References

1. **Kaito Pro — AI Platform (Docs)** – description of the fragmented crypto landscape and Kaito’s solution[[1]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Kaito%20Pro%20is%20an%20essential,for%20investors%2C%20builders%2C%20and%20communities)[[8]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Over%20the%20past%20three%20years%2C,for%20accessing%20vital%20information%20quickly).

2. **Kaito Pro Features** – lists of core indexing and analytics features[[2]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=%2A%20Purpose)[[9]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=,thousands%20of%20premium%20Web3%20sources).

3. **Kaito Pricing Page** – shows enterprise price of US$833 per month and the option to pay in KAITO tokens[[4]](https://www.kaito.ai/pricing#:~:text=Enterprise%20Single%20Seat).

4. **Tokenomics** – allocation of KAITO supply to community, contributors, liquidity and foundation[[5]](https://docs.kaito.ai/introducing-usdkaito/tokenomics#:~:text=56.67,to%20Community%20%26%20Ecosystem).

5. **Aicoin Deep Dive** – reports that daily Yap points are capped at 25 000 while the user base exceeds 250 000 and details the subscription price[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition)[[13]](https://www.aicoin.com/en/article/443784#:~:text=The%20annual%20subscription%20price%20for,the%20monthly%20price%20is%20%241%2C099%2Fmonth). It also confirms total supply (1 B) and circulating supply (241.4 M)[[10]](https://www.aicoin.com/en/article/443784#:~:text=,tokens%3A%201%20billion%20KAITO).

6. **Cointelegraph News** – reports on the March 2025 hack of Kaito AI and founder Yu Hu’s X accounts, noting that the team regained control[[12]](https://cointelegraph.com/news/kaito-ai-yu-hu-x-social-media-hacked#:~:text=Kaito%20AI%2C%20an%20artificial%20intelligence,media%20hack%20on%20March%2015).

---

[[1]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Kaito%20Pro%20is%20an%20essential,for%20investors%2C%20builders%2C%20and%20communities) [[2]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=%2A%20Purpose) [[6]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=The%20crypto%20space%20is%20overwhelmed,alone%20to%20identify%20actionable%20insights) [[7]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Moreover%2C%20search%20engines%20like%20Google,way%20to%20access%20reliable%20insights) [[8]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=Over%20the%20past%20three%20years%2C,for%20accessing%20vital%20information%20quickly) [[9]](https://docs.kaito.ai/kaito-pro-ai-platform#:~:text=,thousands%20of%20premium%20Web3%20sources) Kaito Pro — AI Platform | Kaito AI

[https://docs.kaito.ai/kaito-pro-ai-platform](https://docs.kaito.ai/kaito-pro-ai-platform)

[[3]](https://www.aicoin.com/en/article/443784#:~:text=distributed%20daily%20is%20only%2025%2C000%2C,increases%20exponentially%2C%20creating%20intense%20competition) [[10]](https://www.aicoin.com/en/article/443784#:~:text=,tokens%3A%201%20billion%20KAITO) [[13]](https://www.aicoin.com/en/article/443784#:~:text=The%20annual%20subscription%20price%20for,the%20monthly%20price%20is%20%241%2C099%2Fmonth) Can Dragonfly's Kaito, backed by Sequoia Capital, leverage AI to transform Web3 marketing? - AiCoin

[https://www.aicoin.com/en/article/443784](https://www.aicoin.com/en/article/443784)

[[4]](https://www.kaito.ai/pricing#:~:text=Enterprise%20Single%20Seat) Kaito

[https://www.kaito.ai/pricing](https://www.kaito.ai/pricing)

[[5]](https://docs.kaito.ai/introducing-usdkaito/tokenomics#:~:text=56.67,to%20Community%20%26%20Ecosystem) [[11]](https://docs.kaito.ai/introducing-usdkaito/tokenomics#:~:text=Initial%20Token%20Distribution) Tokenomics | Kaito AI

[https://docs.kaito.ai/introducing-usdkaito/tokenomics](https://docs.kaito.ai/introducing-usdkaito/tokenomics)

[[12]](https://cointelegraph.com/news/kaito-ai-yu-hu-x-social-media-hacked#:~:text=Kaito%20AI%2C%20an%20artificial%20intelligence,media%20hack%20on%20March%2015) Kaito AI and founder Yu Hu’s X social media accounts hacked

[https://cointelegraph.com/news/kaito-ai-yu-hu-x-social-media-hacked](https://cointelegraph.com/news/kaito-ai-yu-hu-x-social-media-hacked)