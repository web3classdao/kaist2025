# 📄 [Solana Agent Kit]  
- 👤 Author: [20220162 / Joohyeun Kim] (www.linkedin.com/in/joohyeun-kim)
- 📆 Presentation Date: [2025-07-09]  

---

## 1. Overview

- **Project Name**: Solana Agent Kit
- **Category**: AI Agent Infrastructure 
- **Key Technologies / Platforms**: Solana, OpenAI, LangChain, Metaplex, Wormhole, CoinGecko API, ZK Compression  
- **Official Links**:
  - [Website](https://kit.sendai.fun/?form=MG0AV3)
  - [Foundation](https://www.sendai.fun/) 
  - [Contract Address](https://x.com/sendaifun) 
  - [Docs](https://docs.sendai.fun/docs/v2/introduction) 
  - [GitHub](https://github.com/sendaifun/solana-agent-kit) 
  - [X](https://x.com/sendaifun)


### 📌 Summary  
The Solana Agent Kit is a toolkit designed to enable AI agents to interact seamlessly with blockchain environments. Traditionally, AI faced limitations when handling on-chain (verified and recorded directly on the blockchain) assets, but this kit supports over 60 Solana-based actions such as token swaps, loans, and NFT minting. Key features include a plugin-based architecture, LangChain and Vercel AI SDK integration, zk-based airdrops, and both chat-based and autonomous agent modes.

---

## 2. Background & Problem Statement

- Problem to Solve: AI agents cannot effectively operate in on-chain environments, limiting their role in decentralized ecosystems.  
- Limitation of Centralized Approaches: APIs are often closed, restrictive, and do not easily integrate with Web3 protocols like DeFi or NFTs.  
- AI Relevance: With the growing number of autonomous agents, enabling direct manipulation of blockchain assets allows for automation and decentralized collaboration.

---

## 3. How It Works

### 🔍 3.1 Project Approach  
- Core Idea: Provide a standardized plugin interface to let AI control Solana  
- Differentiators: Abstracts away wallet management, RPC calls, and protocol-specific logic to reduce developer burden

---

### 🏗️ 3.2 Architecture  
- AI models (e.g., GPT-4o, Claude)
- Various plugins (Token, NFT, DeFi, Misc, Blinks, etc.)
- Solana RPC / Wallet
- On-chain protocols (Jupiter, Raydium, Metaplex)
- User Input → AI Agent → Solana Agent Kit → Plugin → Solana Protocol

![image](https://hackmd.io/_uploads/rJGQhK9Hxx.png)

---

### 🎯 3.3 Core Components  
- Token Plugin: Transfer, issue, swap SPL (Solana Program Library) tokens  
- NFT Plugin: Minting, selling, metadata management  
- DeFi Plugin: Lending, staking, derivatives integration  
- Misc Plugin: Price queries, SNS domains, airdrops, etc.  
- Blinks Plugin: Minigames, JulSOL participation, etc.

---

### 🔁 3.4 Workflow Overview  
AI Agent On-chain Workflow:
1. User Input  
   - Natural Language Command: `"Stake 1 SOL"`
2. AI Command Analysis  
   - Action: `Stake`  
   - Asset: `SOL`  
   - Amount: `1`  
   - Recognizes command as on-chain transaction  
3. Call Solana Agent Kit  
   - AI passes parsed result to Agent Kit  
   - Determines appropriate plugin  
4. Execute Staking Plugin  
   - Creates staking transaction  
   - Connects with user wallet and RPC  
   - Sends transaction to Solana blockchain  
5. Return Transaction Result  
   - Verifies success  
   - Returns transaction hash  
   - Gives user feedback  
6. Error Handling / Autonomy  
   - If failed:  
     - Retry  
     - Switch protocol  
     - Notify user

---

## 4. Token Economy

- No native token  
- Interacts with tokens such as $SEND (SendAI), $USDC, $JUP  
- No inherent economic incentives within Agent Kit—depends on connected protocols

---

## 5. Project Status & Plan

- Status: Released as open-source (v2, currently usable)  
- Community: 1.4k+ GitHub stars, 700+ forks  
- Supported by: Solana Foundation, introduced at AI hackathons  
- Solana Agent Kit Unofficial Roadmap:

**Solana Agent Kit Unofficial Roadmap**
| Stage | Highlights | Status |
|-------|------------|--------|
| v2 Release | Plugin-based architecture, LangChain/Vercel AI SDK integration, zk airdrop support | ✅ Completed |
| Agent Mode Enhancement | Repetitive task automation, error recovery, multi-action handling | 🔄 In Progress |
| Mobile/React Native Support | Agent execution in mobile environments | 🧪 Partially Implemented |
| Embedded Wallet Integration | Integrates with Turnkey, Privy for security | 🛠️ Ongoing |
| LangChain Evaluation System (Evals) | Prompt performance benchmarks | ✅ Applied |
| MCP Adapter Development | Integration with external AIs like Claude Desktop | 🔧 In Development |
| More Protocol Integrations | Expanding to DeFi/futures like Drift, Meteora, Adrena | 🔁 Ongoing |
| SendAI Ecosystem Integration | Closer ties with SEND token, JupSOL, Arcade | 🚀 Scaling |
| Testnet/Simulation Environment | Upcoming developer testing sandbox | 📅 Planned |

---

## 6. User Experience & Hands-on Review *(if applicable)*

### Solana Agent Example Code (Balance Check)

```ts
import { SolanaAgentKit, createSolanaTools } from "solana-agent-kit";
import { createReactAgent } from "@langchain/langgraph/prebuilt";
import { ChatOpenAI } from "@langchain/openai";
import { MemorySaver } from "@langchain/langgraph";
import * as dotenv from "dotenv";
dotenv.config();

const llm = new ChatOpenAI({
  modelName: process.env.SOLANA_AGENT_OPENAI_MODEL || "gpt-4",
  temperature: 0.7,
  apiKey: process.env.OPENAI_API_KEY,
});

const agentKit = new SolanaAgentKit(
  process.env.SOLANA_PRIVATE_KEY!,
  process.env.RPC_URL || "https://api.mainnet-beta.solana.com",
  process.env.OPENAI_API_KEY!
);

const tools = createSolanaTools(agentKit);
const memory = new MemorySaver();

const agent = await createReactAgent({
  llm,
  tools,
  checkpointSaver: memory,
});

const walletAddress = "Wallet Address"; // e.g. "9LKK..."

async function main() {
  const prompt = "What's my Solana wallet balance?";
  console.log(`User Input: ${prompt}`);

  const res = await agent.invoke({
    input: prompt,
    config: {
      metadata: {
        userId: "test-user-001",
        wallets: [{ address: walletAddress, chain: "solana" }],
      },
    },
  });

  console.log("Agent Response:\n", res.output);
}

main();
```

### Explored Features

- Built an AI agent connected to a Solana wallet using `SolanaAgentKit`  
- Queried wallet balance via user prompt  
- Overall workflow:  
  1. Set up LLM based on OpenAI API  
  2. Create agent using LangChain Graph  
  3. Integrate Solana toolset  
  4. Handle requests based on user wallet address  

---

### Step-by-Step Implementation

1. Clone `solana-agent-kit` from GitHub  
2. Configure environment variables in `.env`  
   - e.g., `SOLANA_PRIVATE_KEY`, `RPC_URL`, `OPENAI_API_KEY`  
3. Write `index.ts` and set up project directory  
4. Install external packages manually  
   - `solana-agent-kit`, `@langchain/openai`, `@langchain/langgraph`, `bs58`, etc.  
5. Resolve TypeScript module path issues  
   - Add `paths` settings in `tsconfig.json`  
   - Restart TS server in VS Code  
6. Migrate from outdated APIs to newer versions  
   - `createAgent` → `createReactAgent`  
   - `Solana` → `SolanaAgentKit`, `createOpenAITools`  
7. Final run: query and receive wallet balance response based on address  

---

### Onboarding Experience

- **Difficulty:** Medium to Hard  
- **Reasons:**  
  - Documentation mixes old (v1) and new (v2) APIs, causing confusion  
  - Gaps between error messages and official docs  

---

### Differences from Traditional Services

- Offers a new user experience: accessing blockchain data (e.g., wallet balance) via natural language  
- Compared to traditional non-blockchain API services:  
  - **Requires more configuration**  
  - **Interacts with decentralized data structures**  

---

### Strengths & Areas for Improvement

| ✅ What Went Well | ❌ Needs Improvement |
|------------------|----------------------|
| Natural language-based user interface | Complex initial environment setup |
| Seamless wallet connection & real-time response handling | Debugging burden due to mixed API versions |
| Smooth integration between LangChain and Solana | Steep learning curve due to lack of documentation |

![image](https://hackmd.io/_uploads/ByMGZwsrxe.png)  
![image](https://hackmd.io/_uploads/r1397worgl.png)

---

## 7. Why Blockchain

- Necessity: Allows AI decisions to be transparently recorded and later verified by anyone  
- Infeasible with traditional tech: execution via smart contracts, governance and economic incentives, permissionless decentralized network access  

---

## 8. Insights & Limitations

### ✅ Key Takeaways
- Plugin-based structure enables easy extension for AI developers  
- Covers a wide range of Solana protocols  

### ⚠ Limitations / Open Questions
- No native incentive token  
- Lack of documentation for advanced features  

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- Surprised by how smoothly LangChain and Solana were integrated  
- Realized the growing importance of autonomous agent interfaces in the Web3 ecosystem  

### ❓ Discussion Questions
- Should AI be allowed to autonomously manage wallets?  
- Who should be held accountable for AI errors or accidents?  

---

## 10. Insight from Others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

- [Solana Agent Kit MCP Server](https://github.com/sendaifun/solana-mcp)  
- [Introduction to Solana Agent Kit v2](https://docs.sendai.fun/docs/v2/introduction)  
- [Solana AI Ecosystem Overview](https://solana.com/ai?form=MG0AV3)
