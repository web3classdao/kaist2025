# 📄 ElizaOS
- 👤 Author: [20240562 / Joonseok Lee](https://www.linkedin.com/in/joonseok-lee-533897374/)
- 📆 Presentation Date: [2025-08-06]  

---

## 1. Overview

- **Project Name**: ElizaOS  
- **Category**: AI Agent Infrastructure / Web3 Agent OS  
- **Key Technologies / Platforms**: TypeScript, OpenAI, LLaMA, Anthropic, Solana, Ethereum, LangChain, Discord/X/Telegram APIs, RAG, Trusted Execution Environments (TEEs)  
- **Official Links**:
  - [Website](elizaos.ai)
  - [Whitepaper](https://arxiv.org/abs/2501.06781)
  - [GitHub](https://github.com/elizaOS/eliza) 
  - [Discord](https://discord.gg/DMEmAY2j)


### 📌 Summary  
**ElizaOS** is a modular, open-source operating system for **large language model (LLM)** agents to **autonomously interact** with Web3 environments. By abstracting over wallet management, RPC calls, smart contract interfaces, and multi-platform integrations (Discord, X, Telegram), ElizaOS enables agents to read/write on-chain data, execute smart contract functions, and operate across multiple networks. Its plugin-based architecture, TypeScript SDK, and character-driven agent design make it a developer-friendly framework for building decentralized, autonomous agents.

---

## 2. Background & Problem Statement

* **What real-world problem does this project aim to solve?**
**A.** LLM agents lack first-class support for on-chain operations and autonomous interaction with blockchain-based protocols.
* **What are the limitations of existing (centralized) approaches?**
**A.** Most APIs are centralized, siloed, or require trust in third-party services, making them incompatible with decentralized finance (DeFi), NFTs, and DAOs.
* **Why is this problem especially relevant in the context of AI?**
**A.** As AI agents become more autonomous, enabling native blockchain access—via contracts, governance, and token incentives—unlocks new patterns of decentralized collaboration, automation, and autonomy.

---

## 3. How It Works

### 🔍 3.1 Project Approach  
* **How does this project intend to solve the problem defined in Section 2?**
**A.** This project introduces a decentralized runtime environment—ElizaOS—that enables large language model (LLM) agents to natively interact with blockchain protocols.
* **What is the **core idea** behind the solution?**
**A.** Eliza abstracts away the technical complexity of Web3 by providing prebuilt plugins that expose blockchain and off-chain APIs through natural language interfaces.
* **What makes this approach different from existing methods?**
**A.** It has strong Web3-native orientation, lightweight runtime in TypeScript, multi-agent support, and deep integration with modern LLM providers (OpenAI, Claude, Gemini).



---

### 🏗️ 3.2 Architecture  
```
[User Input]
   ↓
[Provider (e.g., Discord, Telegram, X)]
   ↓
[Character (agent personality & rules)]    
   ↓
[Eliza Core Runtime]
   ↳ Plugin (e.g., Solana, EVM, Coinbase, TEE, RAG)
   ↓
[Blockchain RPC / Web2 API / TEE]
```

---

### 🎯 3.3 Core Components  

- **Character**: Defines the agent’s role, tone, constraints, and example interactions.
- **Provider**: Connects the agent to real-time messaging channels (Discord, Telegram, X).
- **Plugin**: Implements capabilities such as:
  - **Solana/EVM**: On-chain read/write, token transfers, swaps
  - **Web2 APIs**: Coinbase queries, webhooks, Discord bots
  - **RAG**: Retrieval-augmented generation using local or external data
  - **TEE**: Secure enclaves for private inference or secret management
- **Runtime**: Manages execution, routing, error handling, and memory between components.


---

~~** 4. Token Economy *(if applicable)***~~


* **Since Eliza is a bridge between plugins and LLMs, it has no native token.** Eliza agents can optionally integrate with external tokens (e.g., $SEND, $ETH, $SOL).


---

## 5. Project Status & Plan


* **Is the project live? In alpha, beta, or still in development?**
  **A.** ElizaOS is live: version v2 is publicly released, with a stable CLI and runtime available today. The broader ecosystem includes [auto.fun](https://auto.fun), a no-code agent deployment platform launched in April 2025. Certain components like TEE support and mobile shells are still marked as “in progress,” indicating active and ongoing development.

* **What partnerships, grants, or investments has it received?**
  **A.** ElizaOS has partnered with [Fleek](https://fleek.xyz) to provide hosting and infrastructure for deployed agents on auto.fun. It has also collaborated with Stanford’s *Future of Digital Currency Initiative*, validating its research applications. Additional launch support has come from projects like **Chainlink** and **Dreamnet**, further highlighting its Web3 ecosystem relevance.

* **Is it open source?**
  **A.** Yes, ElizaOS is fully open source. The main codebase is publicly available under the MIT license on [GitHub](https://github.com/elizaOS/eliza), enabling developers to inspect, fork, and contribute freely.

* **Does it have an active user base or developer community? If available, how active is the GitHub repo?**
  **A.** Yes. The core GitHub repository (`elizaOS/eliza`) shows strong traction, with approximately **15.6K stars**, **5K forks**, and **558 contributors** as of July 2025. The companion starter repo also maintains healthy engagement, with \~373 stars and 595 forks. Community activity is visible through frequent commits, plugin development, and growing agent launches on platforms like auto.fun.



---

## 6. User Experience & Hands-on Review *(if applicable)*


After installing Node.js, bun, WSL2(and python), we can install ElizaOS, go to your own http://localhost:3000/ and see this page.
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2000%2032%2031.png?raw=true)

I tried to make a Discord Assistance character, and here's what I've done and got.

Hopefully, we can start with a Discord Bot template and set the character's basic infos.  
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2001%2019%2005.png?raw=true)
And we can edit the contents,
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2001%2019%2018.png?raw=true)
styles,
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2001%2019%2032.png?raw=true)
plugins,
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2001%2019%2046.png?raw=true)
secret infos,
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2001%2020%2042.png?raw=true)
and lastly avatar image.
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2001%2021%2002.png?raw=true)


But, since I set up all of these traits and talked to it,
![Image](https://github.com/joonevening/image-repo/blob/main/sayinghinoresponse.png?raw=true)
there was no response, and there was this message on my command prompt.
![Image](https://github.com/joonevening/image-repo/blob/main/2025-08-06%2000%2035%2017.png?raw=true)
I'm stuck here, since it seemed like I had to pay for the OpenAI plan.

---

## 7. Why Blockchain

- **Why does this problem specifically require blockchain to be solved well?** 
**A.** ElizaOS addresses the challenge of enabling AI agents to **autonomously interact** with decentralized Web3 environments where **trust, transparency, and security are paramount**. Traditional centralized systems **cannot guarantee immutable records** nor facilitate permissionless execution across multiple blockchain networks. Blockchain’s decentralized ledger ensures agent activities are **verifiable, tamper-proof, and executed without trusted intermediaries**. This **immutable and trustless environment is essential** to prevent fraud, censorship, and unauthorized control over autonomous AI agents.
- **What does blockchain enable that traditional solutions cannot?**  
**A.** Blockchain provides a **programmable, transparent, and decentralized execution layer** where AI agents can autonomously perform complex on-chain operations like token swaps, NFT minting, and DeFi interactions. Unlike centralized APIs that act as gatekeepers and single points of failure, blockchain offers **composability—allowing seamless integration of multiple protocols—and full auditability of transactions**. Combined with cryptographic tools and Trusted Execution Environments (TEEs), it also enables **enhanced privacy and security for sensitive operations**, which traditional solutions cannot reliably guarantee.
- **Is decentralization critical in this use case? Why or why not?**  
**A.** Yes, **decentralization is critical** for ElizaOS because autonomous AI agents managing valuable assets and executing transactions must operate free from central points of control or failure. Centralized control introduces risks of **censorship, manipulation, and single points of vulnerability**, undermining user trust and agent autonomy. Decentralization ensures **no single entity can revoke, alter, or control agent actions**, providing the resilience, fairness, and trustlessness necessary for a robust AI-powered Web3 ecosystem.


---

## 8. Insights & Limitations

### ✅ **Key Takeaways**

* **Modularity + Web3 Integration**: ElizaOS modularizes the traditionally complex components of Web3—wallets, RPCs, smart contracts—into pluggable components that are accessible to AI agents through natural language. This design lowers the barrier for using AI into blockchain environments.
* **Character-Driven Agents**: By abstracting agent personalities into "characters," ElizaOS supports intuitive customization and scenario-specific design. This makes agent development not only more developer-friendly, but also more expressive and socially relevant.
* **Transparent and Autonomous Execution**: With decentralized infrastructure, agents built on ElizaOS can operate transparently, verifiably, and independently of centralized control—something not able with most traditional AI platforms.

### ⚠ **Limitations / Open Questions**

* **OpenAI Token Quota Dependency**: As we've seen in the section 6, the dependency on commercial LLM APIs like OpenAI can be a major bottleneck. Without an API key or paid plan, even basic usage is blocked. This raises questions about long-term accessibility and open usage.
* **UX for Non-Developers**: While the CLI and agent structure are well-suited for developers, onboarding is still quite technical. Even with tools like auto.fun, full agent deployment and customization still requires some level of coding comfort.
* **Security of Autonomous Agents**: Giving agents access to wallets, RPCs, and smart contract functions introduces significant **attack surfaces** for hackers. Without proper controls or governance layers, hostile use or misbehavior is a real concern.



---

## 9. Reflections & Discussion

### 💡 Personal Reflections

* I found it especially interesting how **ElizaOS combines agent design, blockchain access, and real-time messaging into one cohesive framework**. The use of *characters* adds a surprisingly human layer to what would otherwise be purely programmatic interactions.
* I’ve always seen AI and blockchain as separate things, but ElizaOS shows how deeply interconnected they can be. It made me imagine a future where agents run entire DAOs, manage funds, or even co-author smart contracts—without human intervention.

### ❓ **Discussion Questions**

* **What kinds of tasks should (or shouldn't) be delegated to autonomous agents with full access to blockchain assets?**
   → I think that tasks involving irreversible or high-stakes financial transactions may still require human oversight, while tasks like data fetching, voting, or social interaction are safer to automate.
* **How does ElizaOS monetize? What is the sustainability model for the platform?**
   → I had searched for it, and as of now, ElizaOS itself is open-source and does not enforce direct monetization. However, **auto.fun**, the official no-code agent platform built on ElizaOS, may implement premium features, hosted agent infrastructure, or service fees.


---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

- https://youtu.be/_GH3sVL1wFM
- https://github.com/elizaOS/eliza
