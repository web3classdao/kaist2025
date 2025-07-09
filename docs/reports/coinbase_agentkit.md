# 📄 Coinbase AgentKit 
- 👤 Author: [20230904 / Jaeyoung Shin](https://www.linkedin.com/in/limepencil/)
- 📆 Presentation Date: [2025-07-09]  

---

## 1. Overview
![image](https://hackmd.io/_uploads/HkCrDroHgg.png)

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
Coinbase AgentKit operates on a simple principle: every AI agent should have its own crypto wallet. The goal is to empower AI agents to act as independent participants on the blockchain. By giving them a wallet and a set of blockchain tools, AgentKit allows an AI to autonomously execute tasks like sending payments, interacting with smart contracts, and swapping tokens based on natural language commands.

**How It Works**

AgentKit acts as a bridge between AI and blockchain technology.

* **For the Blockchain:** It leverages the Coinbase Developer Platform to handle complex operations like transaction signing and fee management, simplifying the development process.
* **For the AI:** It is designed to be "model-agnostic," meaning it works with various AI models and popular development frameworks like LangChain. When an AI decides to perform a financial action, AgentKit translates that intent into a secure onchain transaction.

**Key Differentiators**

AgentKit stands out due to its flexibility and unique focus:

* **Framework Agnostic:** Unlike more rigid solutions, it supports multiple large language models (like those from OpenAI and Anthropic), various blockchains (including all EVM networks and Solana), and is not tied to a single wallet provider.
* **Developer-Focused:** It is built for ease of use, featuring simple configurations and starter templates to significantly lower the barrier for developers to integrate AI with blockchain.
* **Unique Direction:** While some projects focus on decentralizing AI itself, AgentKit concentrates on enabling AI to *use* crypto infrastructure. It provides a practical, plug-and-play solution that connects the capabilities of modern AI with the financial rails of the blockchain.

---

### 🏗️ 3.2 Architecture  

AgentKit is designed as a modular system that translates an AI's intent into a blockchain transaction. The process is straightforward:

1.  An **AI Agent** decides to perform an action (e.g., "send 10 USDC").
2.  It uses an **Action** tool provided by AgentKit.
3.  The Action uses a **Wallet Provider** to securely sign and execute the transaction on the blockchain.
4.  The result is sent back to the AI, which can then determine its next step.


---

### 🎯 3.3 Core Components  
The system is built from several key, interchangeable components:

* **AgentKit Core Library:**
    This is the central engine of AgentKit, available in both TypeScript and Python. It manages the configuration (API keys, network selection) and connects the various modules, such as wallets and actions. Its design allows developers to easily add new capabilities.

* **Wallet Provider:**
    This component handles all wallet-related functions, including address creation, key management, and transaction signing. By default, it uses Coinbase’s Smart Wallet, which enables advanced features like gasless transactions. A key feature is its flexibility; developers can replace the default with other providers, such as MetaMask or hardware wallets.

* **Action Providers:**
    Actions are the specific skills available to the AI. These are grouped into "Providers," such as a "DeFi Provider" for swapping tokens or a "Social Provider" for posting to Twitter. AgentKit includes a set of pre-built actions for common tasks like transfers, swaps, and even NFT creation. The framework is extensible, allowing developers to create and register custom actions for the AI to use.

* **Framework Integrations:**
    To ensure broad compatibility, AgentKit provides extensions that act as adapters for popular AI development frameworks. With packages for tools like LangChain, developers can seamlessly integrate AgentKit's blockchain capabilities into their preferred AI development environment.

In practice, a developer or user interacts with the AI in natural language. AgentKit operates as the secure intermediary, translating these commands into reliable onchain operations.

---

### 🔁 3.4 Workflow Overview  

`[User Input] → [AI Agent (LLM)] → [AgentKit Core] → [Wallet Provider] → [Blockchain Tx] → [Response]`


**1. Initialization and Setup**

First, a developer configures the AI agent by providing necessary API keys (e.g., for Coinbase and OpenAI). Using AgentKit, the developer instantiates the agent, which automatically provisions a unique crypto wallet. At this point, the AI agent is live and equipped with a set of onchain abilities, such as transferring funds or interacting with smart contracts.

**2. User Command**

A user interacts with the agent using plain English through a chat interface. For example, they might ask, *"Send 0.01 ETH to my friend,"* or *"Create a new collectible token."* The user does not need any technical knowledge of blockchain operations.

**3. AI Planning and Action Selection**

The AI agent, powered by a large language model (LLM), interprets the user's request. It consults the list of available "Actions" provided by AgentKit and identifies the correct tool for the job (e.g., the `transfer` action). The agent then structures the request with the necessary parameters, such as the asset, amount, and recipient address.

**4. Onchain Execution**

The agent invokes the selected action through AgentKit. This is where AgentKit handles all the technical complexity. It automatically creates the transaction, signs it with the agent's private key, and broadcasts it to the appropriate blockchain network. This entire process occurs securely in the background without requiring user intervention.

**5. Confirmation and Response**

Once the transaction is confirmed on the blockchain, AgentKit reports the outcome back to the AI agent. The agent then provides a clear, user-friendly confirmation, often including a transaction hash or a link to a block explorer for verification. From the user's perspective, they simply made a request and received a confirmation that it was completed.

**Optional: Autonomous Operation**

Beyond direct commands, agents can be programmed to operate autonomously. For instance, an agent could be assigned a goal like "monitor the market and execute trades to maximize profit." In this mode, the agent would independently decide when to execute transactions, using AgentKit to perform the onchain actions in a continuous loop.

---

## 4. Token Economy *(if applicable)*

Token for this case study does not exist.

---

## 5. Project Status & Plan

### Added by Jason

✅ **Coinbase AgentKit vs GOAT SDK**
| Category                   | **Coinbase AgentKit**                                                 | **GOAT SDK**                                                                       |
| -------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| 🧠 **Purpose**             | Enable AI interface for Coinbase Wallet users (e.g., trade assistant) | Modular AI-to-blockchain interface supporting multiple agents, chains, and wallets |
| 🧱 **Dependencies**        | Requires Coinbase Wallet + specific LLM (e.g., OpenAI)                | Works with any EVM wallet (e.g., MetaMask, Safe) via Viem or Ethers                |
| 🔌 **Chain Support**       | Primarily EVM (Base, Ethereum)                                        | Multi-chain support (Base, Ethereum, Optimism, Polygon, etc.)                      |
| 🛠️ **Tech Stack**         | LangChain + LLM tools + scripting                                     | Vercel AI SDK + GOAT plugin system + Viem (or Ethers)                              |
| 🔍 **State / Memory**      | State and memory handled via LangChain                                | Memory can be tool-driven or developer-managed                                     |
| ⚡ **Extensibility**        | Built for Coinbase ecosystem use cases                                | Highly modular: plug in DeFi, NFT, infra tools freely                              |
| 🧩 **Plugin Architecture** | Limited (mostly predefined tools)                                     | Full plugin system – developers can define custom tools                            |
| 🧑‍💻 **Target Developer** | Coinbase ecosystem builders                                           | AI agents, wallet UX, LLM-powered dApps                                            |

| Use Case                                            | Recommendation |
| --------------------------------------------------- | -------------- |
| Coinbase-specific UX                                | ✅ AgentKit     |
| Multi-wallet / DeFi / advanced agent control        | ✅ GOAT SDK     |
| Needs plugin flexibility and on-chain tool chaining | ✅ GOAT SDK     |


✅ **Solana AgentKit vs Coinbase AgentKit vs GOAT SDK**


| Feature                         | **Solana AgentKit**                         | **Coinbase AgentKit**                            | **GOAT SDK**                                     |
| ------------------------------- | ------------------------------------------- | ------------------------------------------------ | ------------------------------------------------ |
| **Chain Support**               | Solana only                                 | Ethereum + L2s (Base, Optimism, Arbitrum, etc.)  | Ethereum + L2s + more via plugin                 |
| **Wallet Type**                 | Keypair, xNFT, AnchorWallet                 | SmartWallet (AA Wallet using Biconomy or others) | EOA, AA Wallet (Crossmint, Privy, etc.)          |
| **Session Key Support**         | Yes (custom implementation)                 | Yes (via Biconomy + permissions)                 | Yes (with TEE-secured agent wallets)             |
| **Account Abstraction (AA)**    | ❌ Not native                                | ✅ Built-in (SmartWallet)                         | ✅ Supported via Crossmint or plugins             |
| **Security Strategy**           | Keypair injected (or Phantom via extension) | SmartWallet with optional guardrails             | TEE-based signing with optional restrictions     |
| **Private Key in Agent**        | ✅ Usually required                          | ❌ Not needed (uses SmartWallet session)          | ❌ Not needed (session key or TEE)                |
| **Transaction Execution**       | solana/web3.js, Anchor, etc.                | Coinbase Infra (Biconomy, etc.)                  | User-defined or via GOAT plugin system           |
| **Guardrails (policy control)** | ❌ Not built-in                              | ✅ Biconomy rules (allowlist, spending cap, etc.) | ✅ Via Crossmint AgentWallet guardrails           |
| **AI Integration**              | Rudimentary / manual                        | Built for LangChain agents                       | Built for LangChain, Vercel AI, etc.             |
| **Developer Experience**        | Solana-native devs only                     | Best if using Coinbase stack                     | Chain-agnostic, modular plugin-based             |
| **Target Use Case**             | Solana-only AI agents or xNFTs              | Coinbase ecosystem agents on EVM chains          | Flexible EVM agents (agent wallets, plug-n-play) |


---

## 6. User Experience & Hands-on Review *(if applicable)*



I followed the [Quick Start](https://github.com/coinbase/agentkit) guide on the official Coinbase AgentKit GitHub page, which included example projects that made it easy to get started quickly. I experimented by adding custom UI components and replacing the default OpenAI LLM API with Claude. Additionally, I began implementing features such as a trading interface, price charts, and a balance viewer to explore more interactive use cases.

![image](https://hackmd.io/_uploads/HyR9mHjBgg.png)



---

## 7. Why Blockchain

Blockchain technology is a fundamental component for unlocking the full potential of AI agents by providing them with true financial autonomy. It allows an agent to hold and transfer value directly through a crypto wallet, eliminating the need for traditional banking intermediaries and their associated restrictions. This creates a trustless and censorship-resistant environment where the AI truly owns its digital assets, can operate 24/7 without waiting for business hours, and can transact globally with anyone. The public and verifiable nature of blockchain also ensures every action the agent takes is transparent and auditable, fostering trust in its operations.

Beyond simple payments, blockchain gives AI agents access to a vast and composable ecosystem of decentralized applications (dApps) and financial protocols (DeFi). This enables an AI to do more than just send money; it can lend assets, trade on decentralized exchanges, invest in digital collectibles, or participate in decentralized governance. This integration with the broader Web3 world allows for far more sophisticated and powerful applications than possible in a closed system. Furthermore, the efficiency of modern blockchains, particularly Layer 2 solutions, supports instant, low-cost microtransactions, making it feasible for agents to pay for data, services, or other resources in real-time.

---

## 8. Insights & Limitations


### Key Insights

* **Powerful Synergy:** AgentKit successfully demonstrates that combining AI and blockchain creates capabilities that neither technology can achieve alone, providing a strong reference architecture for future development.
* **Future-Proof by Design:** Its model-agnostic and modular approach (supporting various AIs, blockchains, and wallets) is crucial for adapting to the rapidly evolving tech landscape.
* **Frictionless Adoption:** By abstracting away crypto's complexities—like gas fees, wallet funding, and key management—it significantly lowers the barrier to entry for developers and users.
* **Community-Driven Growth:** Open-sourcing the project and fostering community contributions has accelerated innovation, leading to a wider range of tools and novel use cases.
* **Validates AI as Economic Actors:** The project provides tangible evidence that AI agents can participate in economies, using blockchain as the settlement layer for their actions and decisions.

### Limitations & Open Questions

* **Early and Experimental:** The toolkit is not yet production-ready and lacks robust safety guardrails to prevent misuse, such as from prompt injection attacks or AI errors.
* **Significant Security Risks:** Giving an AI direct control over funds introduces inherent risks of financial loss due to LLM mistakes, bugs, or malicious inputs.
* **Centralization Dependency:** While promoting decentralization, the default setup relies heavily on Coinbase's centralized infrastructure, creating potential single points of failure and a trade-off between convenience and true autonomy.
* **Regulatory Uncertainty:** Autonomous agents operate in a legal gray area, raising unresolved questions about liability, accountability, and compliance with financial regulations like KYC/AML.
* **Scalability and Complexity:** It remains to be seen if current blockchain infrastructure and AI models can scale to support millions of agents, or if today's agents can handle truly complex, multi-step onchain tasks without continuous, manual updates.
---

## 9. Reflections & Discussion

### 💡 Personal Reflections
Studying AgentKit was eye-opening. The most profound shift in perspective was seeing AI agents as "users" of the blockchain, capable of participating in an autonomous economy. This moves beyond simple payments, suggesting a deep integration where AI logic and onchain logic are woven together, allowing agents to earn yield or manage assets independently.

While initially skeptical, the developer-friendly design showed the power of good abstraction in bridging these complex fields. The concept of "agentic commerce," where AIs hire and pay each other, is both exciting for its potential efficiency and concerning for its economic implications.

### ❓ Discussion Questions
- **Autonomy vs. Control**: How can we build safety measures (like spending limits or kill switches) for AI agents that control real money, without undermining the benefits of their autonomy?
- **Economic Impact**: What are the economic consequences—both risks and opportunities—when autonomous AI agents begin competing with humans in markets like trading, auctions, and services?
- **The Need for Decentralization**: Could a centralized tech giant replicate AgentKit's functions? If so, what critical element does blockchain provide that a centralized system would lack?


---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

* *Introducing AgentKit, a toolkit for building AI agents onchain*. (Coinbase Developer Platform). [https://www.coinbase.com/developer-platform/discover/launches/introducing-agentkit](https://www.coinbase.com/developer-platform/discover/launches/introducing-agentkit)
* *AgentKit Documentation*. (Coinbase Developer Platform). [https://docs.cdp.coinbase.com/agent-kit/welcome](https://docs.cdp.coinbase.com/agent-kit/welcome)
* *Build with Coinbase and OpenAI's new Agents SDK*. (Coinbase Developer Platform). [https://www.coinbase.com/developer-platform/discover/launches/openai-agents-sdk](https://www.coinbase.com/developer-platform/discover/launches/openai-agents-sdk)
* *AgentKit Q1 2025 Update: Building agents with Solana, OpenAI, and more*. (Coinbase Developer Platform). [https://www.coinbase.com/developer-platform/discover/launches/agentkit-q1-update](https://www.coinbase.com/developer-platform/discover/launches/agentkit-q1-update)
* *The rise of onchain AI agents, apps, and commerce*. (Coinbase Blog). [https://www.coinbase.com/en-gb/blog/the-rise-of-onchain-ai-agents-apps-and-commerce](https://www.coinbase.com/en-gb/blog/the-rise-of-onchain-ai-agents-apps-and-commerce)
* *Coinbase Developer Platform AgentKit Quickstart Guide*. (Replit). [https://replit.com/guides/coinbase-developer-platform-agentkit-quickstart-guide](https://replit.com/guides/coinbase-developer-platform-agentkit-quickstart-guide)
* *coinbase/agentkit GitHub Repository*. (GitHub). [https://github.com/coinbase/agentkit](https://github.com/coinbase/agentkit)