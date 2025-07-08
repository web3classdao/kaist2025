# 📄 Coinbase AgentKit 
- 👤 Author: [20230904 / Jaeyoung Shin](https://www.linkedin.com/in/limepencil/)
- 📆 Presentation Date: [2025-07-09]  

---

## 1. Overview

- **Project Name**:  Coinbase AgentKit
- **Category**: Onchain AI Agents Toolkit (Decentralized AI Infrastructure)
- **Key Technologies / Platforms**: Ethereum & Base (L2) blockchain, Solana, Smart Contracts (Solidity), Account Abstraction (Smart Wallets), Coinbase Developer Platform (CDP) SDK, LangChain integration 
- **Official Links**:
  - [Website](https://www.coinbase.com/developer-platform/products/agentkit)
  - [Foundation](https://www.coinbase.com/) 
  - [Docs](https://docs.cdp.coinbase.com/) 
  - [GitHub](https://github.com/coinbase/agentkit) 
  - [X](https://x.com/coinbasedev)
  - [Discord](https://discord.com/invite/cdp)


### 📌 Summary  
Coinbase AgentKit is a developer toolkit that bridges the gap between AI and blockchain, enabling the creation of autonomous onchain AI agents. In traditional AI applications, agents (such as advanced chatbots or automation scripts) have limited ability to transact value or interact with decentralized systems. AgentKit addresses this by giving every AI agent its own crypto wallet and a suite of onchain actions, allowing agents to hold and transfer assets, deploy smart contracts, and autonomously interact with decentralized apps.

By leveraging blockchain, these AI agents become first-class economic actors. They can operate 24/7, make decisions, and directly execute financial transactions without human intermediaries. In practice, AgentKit offers a model-agnostic and framework-agnostic infrastructure: developers can plug in their choice of Large Language Model (LLM), such as OpenAI or others, and connect it to blockchain functionality through Coinbase’s secure APIs.

The toolkit includes secure wallet management (based on Coinbase’s Smart Wallet API) and a library of pre-built actions, including token transfers, swaps, contract deployment, and social media operations. This significantly reduces the complexity of building onchain AI agents, as tasks like funding an agent’s wallet, paying gas fees, or calling DeFi protocols are abstracted away by the framework.

AgentKit’s key achievements include seamless integration with popular AI frameworks like LangChain, support for multiple blockchains (including EVM-compatible networks and Solana), and an extensible design that allows developers to add custom actions or integrate alternative wallet providers. In short, AgentKit empowers developers to easily create AI-driven applications with built-in crypto capabilities, unlocking new possibilities for automated trading, asset management, decentralized commerce, and more.

---

## 2. Background & Problem Statement

### Problem
Modern AI agents, such as those built on GPT models, can generate content but cannot independently own assets or interact with smart contracts. Developers must overcome major challenges to enable agents to transact, including secure key management, blockchain integration, and ensuring safe execution. Centralized solutions like custodial wallets or bank APIs are limited, risky, and require permission. This prevents AI agents from operating globally and autonomously. Without blockchain, their actions are confined to non-financial tasks such as sending messages or calling APIs.

### Limitations of Existing Approaches
Before AgentKit, connecting AI with crypto was fragmented and insecure. Each project had to manually build wallet management and blockchain tools, which increased development time and introduced security risks. Centralized systems also created single points of failure, meaning agents could be shut down or blocked without notice.

### Why This Matters for AI
As AI agents become more autonomous, they need native access to crypto in order to participate in the digital economy. Blockchain allows agents to hold funds, perform transactions, and interact with decentralized apps at any time. This enables use cases such as trading bots, NFT creators, and DAO participants. AgentKit provides the infrastructure to support these agents, making it easier and safer to bring AI onchain.

---

## 3. How It Works

### 🔍 3.1 Project Approach  
- How does this project intend to solve the problem defined in Section 2?  
- What is the **core idea** behind the solution?  
- What makes this approach different from existing methods?

---

### 🏗️ 3.2 Architecture  
- Provide a high-level overview of the system architecture.  
- Include a diagram or describe the components and how they are connected.  
- Focus on how data flows between users, models, smart contracts, etc.

---

### 🎯 3.3 Core Components  
- Describe the key components or modules (e.g., data capsule, model registry, token system)

---

### 🔁 3.4 Workflow Overview  
Explain the overall process or user flow in 3–5 steps.

Example:
1. A user uploads their data...
2. The model interacts with the data via zero-knowledge proofs...
3. The contributor is rewarded with tokens...

> *(You may include a diagram or link to an official architecture diagram if helpful.)*

---

## 4. Token Economy *(if applicable)*

> *Include this section **only if the project has its own token.***  

- What is the name and type of the token? (e.g., utility, governance, staking)  
- What can the token be used for within the ecosystem?  
- How does the token incentivize key actors (e.g., contributors, validators, users)?
- Is there a burn/mint mechanism, inflation cap, or vesting schedule?  

| Stakeholder | How They Use / Earn the Token |
|-------------|-------------------------------|
| Data Provider | [e.g., earns rewards based on contribution] |
| Model Developer | [e.g., pays tokens to access datasets] |
| Verifier / Node | [e.g., earns tokens by verifying data provenance] |

---

## 5. Project Status & Plan

> *In this section, summarize the current state of the project and its real-world impact (if any).*

- Is the project live? In alpha, beta, or still in development?
- Does it have an active user base or developer community?
- What partnerships, grants, or investments has it received?
- Is it open source? How active is the GitHub repo (if available)?
- Is the token (if any) listed and traded? What is its current market activity?

You don’t have to cover everything — focus on what seems most relevant to evaluating how “real” or impactful the project is right now.

> 📌 *Try to distinguish between hype and actual traction. Just because a project looks good on its website doesn't mean it's being used or adopted.*

---

## 6. User Experience & Hands-on Review *(if applicable)*

> *Try to actually use the project if possible — via a demo, public app, testnet, or simulation.*
> This section should capture your experience **as a user or a developer**, not just as a researcher.

Here are some prompts to help you reflect:

- What features did you explore? 
- What did you do step-by-step?
- Was the onboarding intuitive or confusing? 
- How did you deal with a crypto wallet or tokens?
- What felt different from traditional (non-blockchain) services?
- What worked well? What didn’t?

You can also include:
- Screenshots
- Links to testnet/demo activity
- Errors or bugs you encountered

---

## 7. Why Blockchain

- Why **does this problem specifically require blockchain** to be solved well?  
- What does blockchain enable that traditional solutions cannot?  
- Is decentralization critical in this use case? Why or why not?  

> 📌 *This section should show that blockchain is not just "used," but "necessary."*

---

## 8. Insights & Limitations

### ✅ Key Takeaways
- What did this project do right?  
- What important lessons or patterns can we learn from this project?

### ⚠ Limitations / Open Questions
- What challenges remain? (technical, legal, usability, etc.)  
- Are there any scalability or adoption concerns?

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- What did you find most interesting or surprising?  
- How has your understanding of AI/blockchain changed after studying this?

### ❓ Discussion Questions
- Thought-provoking question to ask during class
- You should facilitate a small group discussion based on these questions.  
- Optional: comparison to other projects in this space

---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

- [Articles, blog posts, or academic papers]  
- [Related projects or comparisons]
