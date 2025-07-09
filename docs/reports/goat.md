# 📄 GOAT SDK 
- 👤 Author: 20210751 [Olesia Bilyk](https://www.linkedin.com/in/olesia-bilyk-28a8ba372/)
- 📆 Presentation Date: [2025-07-09]  

---

## 1. Overview

- **Project Name**: GOAT SDK  
- **Category**: Crypto SDK  
- **Key Technologies / Platforms**: GOAT  
- **Official Links**:
  - [Website](https://ohmygoat.dev/)
  - [Sponsor](https://www.crossmint.com/) 
  - [GitHub](https://github.com/goat-sdk/goat) 
  - [X](https://x.com/goat_sdk)
  - [Discord](https://discord.com/invite/goat-sdk)


### 📌 Summary  
GOAT SDK (Great Onchain Agent Toolkit Software Development Kit) simplifies the integration of AI agents with blockchain by providing a unified set of tools that allow agents to perform on-chain actions like sending tokens, swapping assets, and minting NFTs across 30+ blockchains. It solves the fragmentation and complexity developers face when connecting AI to decentralized systems by offering a wallet-agnostic, multi-language toolkit compatible with major agent frameworks. GOAT has achieved strong adoption with over 200 tools, support from Crossmint, real-world integrations (e.g. deBridge, Celo), and an open-source, extensible ecosystem—making it a key enabler for blockchain-native AI agents.

---

## 2. Background & Problem Statement

### The Need for AI-Blockchain Integration

The rapid growth of AI and blockchain technologies has created a strong demand for intelligent agents that can operate directly within decentralized systems. Developers want to build AI-powered applications that interact securely with multiple blockchains, wallets, and protocols. However, this integration is complex and fragmented due to the diversity of blockchain platforms and lack of unified development tools.  

### Centralized AI Agents

Existing centralized AI-agent solutions fall short in this decentralized context. They often rely on single points of control, which limits transparency and trustless interaction with on-chain assets and smart contracts. These limitations hinder autonomous operation, reduce security, and prevent AI agents from fully leveraging the benefits of decentralized networks, restricting scalability and user control.  

### GOAT SDK Solution

GOAT SDK provides a comprehensive toolkit that enables developers to seamlessly connect AI agents with multiple blockchain networks and wallets. By offering standardized APIs and multi-language support compatible with major AI agent frameworks, GOAT eliminates fragmentation and simplifies cross-chain interactions. This empowers AI agents to operate autonomously, securely execute on-chain transactions, and access decentralized data without relying on centralized intermediaries—unlocking the full potential of decentralized AI applications.  

---

## 3. How It Works

### 🔍 3.1 Crossmint Introduction  
In [December 2024 article](https://blog.crossmint.com/introducing-goat-great-onchain-agent-toolkit/), GOAT SDK's sponsor Crossmint introduced it as 
:::success
a single, unified library of onchain actions, ready to be used in 5 agent frameworks, two programming languages, on any wallet architecture across 30+ chains
:::
An MIT-licensed open source SDK, beneficial for both app and agent developers, GOAT claims to be provider and wallet agnostic. GOAT SDK lowers the barrier for building blockchain-native AI agents by abstracting away complex onchain interactions, such as minting NFTs, sending tokens, or reading smart contract data. This makes it a powerful foundation for creating decentralized, intelligent applications that are both secure and scalable.

![GOAT_01](https://hackmd.io/_uploads/rJxrR_bOSxl.png)

---

### 🎯 3.2 Core Components  

| Component | Description |
| --------- | ----------- |
| **Action Plugins**   | Modular wrappers for onchain actions (mint NFT, transfer token, verify identity)|
| **Agent Adapter**    | Bridges between GOAT and various AI frameworks (LangChain, AutoGPT, etc.)|
| **Chain Router**     | Routes transactions and payloads to the appropriate blockchain (Solana, Base, etc.)|
| **Signer Interface** | Abstracts wallet/signature method (EOA, smart wallets, Crossmint MPC)|
| **Plugin Registry**  | Tracks and loads available GOAT plugins; extensible for devs |

---

### 🔁 3.3 Workflow Overview  
![GOAT_05](https://hackmd.io/_uploads/Sy6t4wYBle.png)

#### Example:
```
# Pseudocode inside agent's reasoning loop
image = generate_artwork()

metadata = {
    "name": "Dreamscape 2077",
    "description": "AI-generated cityscape",
    "creator": "AI Agent X"
}

# Upload to IPFS using GOAT
ipfs_uri = goat.upload_to_ipfs(image, metadata)

# Mint NFT onchain
tx = goat.mint_nft(chain="solana", metadata_uri=ipfs_uri)

# Sign + send
receipt = goat.send_transaction(tx)
```


---

## 4. Project Status & Plan

|Downloads |License|GitHub|Discord|
|---|---|---|---|
|5.2k/month|MIT|757 stars|~400 members

![GOAT_02](https://hackmd.io/_uploads/SkINlMOHle.png)
![GOAT_03](https://hackmd.io/_uploads/H1xtSBOrle.png)
![GOAT_04](https://hackmd.io/_uploads/BJWrqIKreg.jpg)


GOAT SDK is fully live as an open-source SDK that is actively maintained and used in production. It’s beyond alpha or beta, with continuous feature updates and new integrations rolling out. There’s an active Discord, and the project is growing its open-source network—especially with integrations via Crossmint and community-driven plugin additions. With regular commits, plugin creation, and integrations being merged frequently, it shoud continue to grow. There should be more collaborations and toolkits added given that as of now the project is only half a year old. In future, it could charge for extra tools or customer support, or earn money from partnerships and sponsors, but it does not require money for us to use it currently.


---

## 5. User Experience & Hands-on Review *(if applicable)*

![beginning](https://hackmd.io/_uploads/Sko33Morxg.png)
### Confusion with .evm
![template not showing](https://hackmd.io/_uploads/B1C76foSex.png)
### Getting an RPC_PROVIDER_URL
![quick 1](https://hackmd.io/_uploads/B1yy1msBll.png)
![quick 2](https://hackmd.io/_uploads/rJzykQsrgx.png)
![quick 3](https://hackmd.io/_uploads/B1_1yXiSxg.png)
![quick 4](https://hackmd.io/_uploads/HJ3JymjHex.png)
![quick 5](https://hackmd.io/_uploads/ByRy1QjSxl.png)
### Checking balance
![Sepolia balance](https://hackmd.io/_uploads/rJ02hMsHll.png)
### Miscellaneous
```
mac@mint-name ~ % brew install node
mac@mint-name ~ % brew install pnpm
mac@mint-name typescript % pnpm install
 ERR_PNPM_UNSUPPORTED_ENGINE  Unsupported environment (bad pnpm and/or Node.js version)

Your Node version is incompatible with "/Users/mac/goat/typescript".

Expected version: >=20.12.2 <23
Got: v24.3.0
```


### Added by Jason

[Send and receive tokens on EVM](https://github.com/goat-sdk/goat/tree/main/typescript/examples/by-use-case/evm-send-and-receive-tokens)

check the balance for ERC-20 tokens
![image](https://hackmd.io/_uploads/rk2DFj9Bel.png)

get the balance of a token
![image](https://hackmd.io/_uploads/S1el2i9Blg.png)

send tokens to another address
![image](https://hackmd.io/_uploads/H1PrTscSle.png)



check the token balance of the recipient
![image](https://hackmd.io/_uploads/BkxdAjcBlx.png)


Workflow to send tokens
```
User (Prompt)
  ↓
OpenAI Function Call (via `@goat-sdk/adapter-vercel-ai`)
  ↓
Tool Call: erc20_transfer
  ↓
Plugin: @goat-sdk/plugin-erc20
  ↓
Wallet: sendTransaction()
  ↓
Blockchain: Base Sepolia (via RPC)
```


Interactive CLI code (index.ts) -> AI Agent based on OpenAI

```typescript
import readline from "node:readline";

import { openai } from "@ai-sdk/openai";
import { generateText } from "ai";

import { http, createWalletClient } from "viem";
import { privateKeyToAccount } from "viem/accounts";
import { baseSepolia } from "viem/chains";

import { getOnChainTools } from "@goat-sdk/adapter-vercel-ai";

import { viem } from "@goat-sdk/wallet-viem";

require("dotenv").config();

// 1. Create a wallet client
const account = privateKeyToAccount(process.env.WALLET_PRIVATE_KEY as `0x${string}`);

const walletClient = createWalletClient({
    account: account,
    transport: http(process.env.RPC_PROVIDER_URL),
    chain: baseSepolia,
});

(async () => {
    // 2. Get your onchain tools for your wallet
    const tools = await getOnChainTools({
        wallet: viem(walletClient),
    });

    // 3. Create a readline interface to interact with the agent
    const rl = readline.createInterface({
        input: process.stdin,
        output: process.stdout,
    });

    while (true) {
        const prompt = await new Promise<string>((resolve) => {
            rl.question('Enter your prompt (or "exit" to quit): ', resolve);
        });

        if (prompt === "exit") {
            rl.close();
            break;
        }

        console.log("\n-------------------\n");
        console.log("TOOLS CALLED");
        console.log("\n-------------------\n");
        try {
            const result = await generateText({
                model: openai("gpt-4o-mini"),
                tools: tools,
                maxSteps: 10, // Maximum number of tool invocations per request
                prompt: prompt,
                onStepFinish: (event) => {
                    console.log(event.toolResults);
                },
            });

            console.log("\n-------------------\n");
            console.log("RESPONSE");
            console.log("\n-------------------\n");
            console.log(result.text);
        } catch (error) {
            console.error(error);
        }
        console.log("\n-------------------\n");
    }
})();
```

If using Uniswap, code is changed like below
```typescript
import { getOnChainTools } from "@goat-sdk/adapter-vercel-ai";
import { uniswap } from "@goat-sdk/plugin-uniswap";

import { viem } from "@goat-sdk/wallet-viem";

require("dotenv").config();

// 1. Create a wallet client
const account = privateKeyToAccount(process.env.WALLET_PRIVATE_KEY as `0x${string}`);

const walletClient = createWalletClient({
    account: account,
    transport: http(process.env.RPC_PROVIDER_URL),
    chain: base,
});

(async () => {
    // 2. Get your onchain tools for your wallet
    const tools = await getOnChainTools({
        wallet: viem(walletClient),
        plugins: [
            uniswap({
                baseUrl: process.env.UNISWAP_BASE_URL as string,
                apiKey: process.env.UNISWAP_API_KEY as string,
            }),
        ],
    });
```

---

## 6. Why Blockchain

GOAT SDK exists to enable AI agents to take onchain actions autonomously—such as creating NFTs, making payments, or managing identities. These actions require verifiable ownership, trustless execution, and transparent history—things centralized systems simply can’t guarantee across ecosystems. With decentralization, AI agents become free to operate without being locked into any ecosystem.
### Need for Blockchain:
- **Trustless execution:** Agents can act securely without needing to rely on centralized servers, APIs, or intermediaries.
- **Global interoperability:** Blockchain lets agents interact with multiple ecosystems (NFTs, tokens, DeFi) under a common, permissionless standard.
- **Verifiable ownership:** Blockchain enables AI agents to own assets and operate under persistent, cryptographically secured identities. Every action they take is immutably recorded on-chain, proving origin, intent, and outcome without needing a third party to vouch for them to make it possible.

---

## 7. Insights & Limitations

### ✅ Key Takeaways
- Protocol-agnostic abstraction layer: unified access to blockchain functionality (e.g. NFT minting, token transfers) without coupling developers to specific providers, signing methods, or frameworks.
- Flexible agent integration: GOAT supports five major agent frameworks and provides blockchain actions as modular plugins, making it easy for developers to equip autonomous agents with secure, onchain functionality without complex setup.
- Secure and extensible: The SDK's open-source MIT license, clear plugin interface, and wallet-agnostic architecture make it auditable, forkable, and adaptable to custom environments.
- Cross-chain UX abstraction: GOAT shows that multi-chain support doesn’t need to be a burden if the SDK encapsulates the complexity—letting developers build once and deploy across diverse environments.
- Agent-native design: Rather than retrofitting smart contract interactions into existing tools, GOAT is designed with autonomous agents in mind—where identity, signing, and real-time decision logic are first-class concerns.
- Modular infrastructure scales better: The plugin-based model reduces coupling, supports parallel development, and encourages community-driven extensions—similar to how modern cloud SDKs evolve in distributed ecosystems.

### ⚠ Limitations / Open Questions

1. Incomplete Decentralization
*While GOAT promotes onchain execution, key operational layers (e.g. agent runtimes, validators, routing) remain centralized. True decentralization would require additional infrastructure for verifying agent actions and coordinating multi-agent behavior, which is not yet in place.*

| Component | Path to Decentralization |
| - | - |
| Agent execution | Decentralized compute or verifiable execution (ZK/TEE) |
| Routing infrastructure | P2P message relays, community-run nodes |
| Wallet/key custody | Smart contract wallets or decentralized MPC |
| Agent registries | Onchain identity and permission contracts |
| Storage/logs | IPFS/Arweave for persistence and traceability |
| Governance | DAO or community-led multisig for roadmap and config |

2. No Native Incentive Mechanism
*GOAT lacks a built-in token or incentive layer to drive participation or sustain long-term development. Without an economic model, it relies on sponsor funding (e.g. Crossmint) or grants, which may not scale with ecosystem growth.*
3. Security and Agent Governance
*Autonomous agents executing transactions onchain introduce risk, especially if compromised or misconfigured. GOAT currently lacks a robust reputation system or permissioning model to prevent misuse or protect onchain assets from malicious agents.*
4. Developer Onboarding Complexity
*Despite simplifying blockchain access for agents, GOAT still assumes familiarity with Web3 concepts (wallets, smart contracts, RPC). For new developers, onboarding into multi-chain, decentralized AI apps remains cognitively demanding.*
5. Ecosystem Immaturity vs. Competitors
*Compared to more established Web3 SDKs (like Thirdweb or Gelato), GOAT's agent-first approach is novel but still early. Documentation, tooling, and examples are improving, but it has yet to match the maturity and stability of broader developer platforms.*

---

## 8. Reflections & Discussion

### 💡 Personal Reflections

What stood out most to me about GOAT SDK was how it bridges AI agents and blockchain systems. I was surprised by how much complexity GOAT abstracts — enabling agents to act across 30+ chains and multiple frameworks without needing deep blockchain knowledge. This shifted my view of blockchain from being just a financial or ownership layer to becoming a programmable execution environment for autonomous agents, and in addition, I finally understood why blockchain is a course for CS students rather than econ students. Naturally, I wonder how easier and more promising has using AI agents instead of doing things on one's own become thanks to projects like GOAT SDK.

### ❓ Discussion Questions
- How should responsibility and trust be handled when AI agents act autonomously onchain? What should be the scope of actions permitted for the agents?
- How might the creators of GOAT SDK generate revenue from the project?
- GOAT contributes to the wide adoption of agent-based architectures in Web3. What might prevent it?
- Does GOAT’s abstraction layer make development easier, or could it hide too much of the underlying blockchain logic from developers?
- What might discourage new developers from adopting GOAT SDK, despite its goal to lower entry barriers?

---

## 9. Insight from others

Insights from other students:
- [write here]

---

## 10. References

- [Crossmint Intro](https://blog.crossmint.com/introducing-goat-great-onchain-agent-toolkit/)
- [deBridge Collab](https://outposts.io/article/debridge-launches-integration-with-goat-sdk-for-defi-agent-10559720-d900-46c8-9fac-3cc167c6a29d)
- [Scaling with Devin](https://www.youtube.com/watch?v=1OyO-fkqnkk)
- [Celo Collab](https://docs.celo.org/build/build-with-ai/build-with-goat/token-swap-agent)
- [Zilliqa](https://blog.zilliqa.com/goat-brings-easy-ai-agent-integration-to-zilliqa/)