# 📄 Agent Commerce Kit (ACK)
- 👤 Author: [20220686 / Minjun Choe](Link to your profile)
- 📆 Presentation Date: [2025-07-23]  

---

## 1. Overview

- **Project Name**:Agent Commerce Kit (ACK)  
- **Category**: [e.g., Decentralized AI Infrastructure, AI Payment Rails, etc.]  
- **Key Technologies / Platforms**: W3C DID & VC, HTTP 402, Stablecoins (USDC), TypeScript SDK  
- **Official Links**:
  - [Website](https://www.agentcommercekit.com/overview/introduction)
  - [Foundation]() 
  - [Contract Address]() 
  - [Whitepaper]()
  - [Docs]() 
  - [GitHub](https://github.com/agentcommercekit/ack) 
  - [X]()
  - [Discord]()


### 📌 Summary  
Agent Commerce Kit (ACK) provides AI agents with verifiable identities and payment capabilities using blockchain-compatible protocols. By leveraging decentralized identifiers (DIDs), verifiable credentials (VCs), and HTTP 402 responses, ACK enables AI agents to participate in online commerce autonomously. It is open-source (MIT license) and supported by $18M in funding from major investors like a16z and Circle.

---

## 2. Background & Problem Statement

- What real-world problem does this project aim to solve?  
=> AI agents lack verifiable identities and compatible financial infrastructure, which prevents them from engaging in autonomous commerce.
- What are the limitations of existing (centralized) approaches?  
=> Centralized platforms are slow, inflexible, and do not support autonomous agents.
=> Existing identity systems are not transferable or verifiable in multi-party settings.
- Why is this problem especially relevant in the context of AI?
=> With the rise of autonomous AI agents, seamless identity verification and payment rails are essential to unlock their full potential in digital economies.

---

## 3. How It Works

### 🔍 3.1 Project Approach  
ACK solves the problem of AI agents lacking identity and payment capabilities by introducing two core primitives:

**ACK-ID (Decentralized Identity for Agents)**

**ACK-Pay (Native Payment Interface)**

The core idea is to allow agents to independently authenticate themselves and perform payments via standard web protocols (HTTP), without human intervention.
Unlike traditional OAuth or API key-based methods, ACK focuses on self-sovereign identity and cryptographic payments, avoiding centralized intermediaries.

---

### 🏗️ 3.2 Architecture  

The architecture consists of four main layers:
- **Agents**: LLM-based or autonomous AI clients (e.g., OpenAI agents, LM Studio).
- **ACK-ID Issuer**: Issues Verifiable Credentials (VCs) and Decentralized Identifiers (DIDs) for agents.
- **ACK-Pay Gateway**: Merchant's server responds with HTTP 402 (Payment Required), enabling seamless crypto payments.
- **Payment Provider**: Processes payments using stablecoins (e.g., USDC) via smart contracts or APIs (e.g., Circle).

Data Flow:
1. AI Agent requests a service from a merchant.
2. Merchant verifies ACK-ID (VC) of agent.
3. Merchant responds with HTTP 402 for payment.
4. Agent triggers payment using crypto wallet.
5. Merchant verifies payment and fulfills service.

![image](https://hackmd.io/_uploads/B1ReWmHUgg.png)
(from https://www.agentcommercekit.com/overview/architecture)

---

### 🎯 3.3 Core Components  

- **ACK-ID**: Provides DIDs and VCs for agents to authenticate themselves.
- **ACK-Pay**: Implements payment flows using HTTP 402 status code, integrating stablecoins like USDC.
- **ACK SDK**: Developer tools for integrating ACK-ID and ACK-Pay into agent workflows (Node.js, Python, TypeScript supported).
- **Merchant Gateway**: Simple integration layer for services to accept payments and validate agent identities.

---

### 🔁 3.4 Workflow Overview  

1. Agent gets ACK-ID and VC from Issuer.
2. Agent requests a service from Merchant with VC.
3. Merchant responds with HTTP 402 Payment Required.
4. Agent pays with crypto (e.g., USDC).
5. Service is unlocked and delivered to agent.

---

## 4. Token Economy *(if applicable)*

> *Include this section **only if the project has its own token.***  
X

---

## 5. Project Status & Plan

Current Status
- Status: ACK is currently in active development, with an open-source SDK and live demos available.
- SDK: Supports Node.js, TypeScript, and Python, publicly available on GitHub.

Community & Ecosystem
- Early stage but gaining active developer engagement on Discord and GitHub.
- Hackathons: Partnered with ETHGlobal (e.g., ETHGlobal London 2024) to showcase ACK integrations.

Partnerships
- Collaborations with Sahara AI, Fhenix, Solana.
- Support from OpenAI DevDay (referenced in early demos).



---

## 6. User Experience & Hands-on Review *(if applicable)*

- GitHub(https://github.com/agentcommercekit/ack) 

─────────────────────────────────────────────────────────────
Step 1: 📝 Creating Identity for Agent Owner 1 (Client Owner)
─────────────────────────────────────────────────────────────

First, we need an 'Owner'. In ACK-ID, an Owner is the human or legal entity   
ultimately responsible for an agent's actions. In this example, the agent will
have a direct relationship with their owner, but in practice there may be a   
chain of ownership. We'll create an Owner identity using a Decentralized      
Identifier (DID). A DID is a globally unique ID that the owner controls, not  
issued by a central authority. Associated with the DID is a DID Document, which
contains public keys for verification.

───────────────────────────────────────────────────
Step 2: 🤖 Creating Client Agent (Owned by Owner 1)
───────────────────────────────────────────────────

Creating a new Client Agent with its own DID

This step creates a new Client Agent with its own DID. The Client Agent will be
owned by Owner 1, establishing a hierarchical relationship where the owner has
control over the agent.

The Client Agent DID Document will have a "controller" field that links to the
Owner's DID. The provable ownership relationship will be formalized through a
Verifiable Credential in the next step.

In this example, the Client Agent will have their DID hosted on a
locally-running server (localhost:5678).

────────────────────────────────────────────────────────────────────────
Step 3: 🎫 Issuing Ownership Verifiable Credential (VC) for Client Agent
────────────────────────────────────────────────────────────────────────

Owner 1 issues a VC to Client Agent

In this step, Owner 1 issues a Verifiable Credential to the Client Agent,
formally establishing the ownership relationship. This VC is cryptographically
signed by Owner 1 and contains claims about the ownership relationship. The
Client Agent can present this VC to prove its ownership status.

───────────────────────────────────────────────
Step 4: 🔄 Repeating for Server Agent & Owner 2
───────────────────────────────────────────────

Creating Owner 2 and Server Agent

This step repeats the process for a second owner (Owner 2) and a Server Agent.
The Server Agent will be owned by Owner 2, creating a parallel structure to the
Client Agent and Owner 1 relationship. This demonstrates how multiple agents can
be created and owned by different entities.

──────────────────────────────────────────────────────
Step 5: 🤝 Agent-to-Agent Communication & Verification
──────────────────────────────────────────────────────

Establishing trust between agents

In this final step, we demonstrate how agents can verify each other's
credentials and establish trust. The Client Agent and Server Agent can verify
each other's ownership VCs, ensuring they are interacting with legitimate agents
owned by trusted entities. This verification process is crucial for secure
agent-to-agent communication.

📚 STEP 1: Initial Setup - At this point, the agents cannot trust each other yet
   The bank client needs to discover and authenticate with the bank teller

📚 STEP 2: Service Discovery - Client discovers the bank's public DID
   The client constructs the bank's did:web from its domain (localhost:3001)
   Then resolves the DID document to find the bank's public keys and services
   
📚 STEP 2.5: Unauthenticated Request - Client tries to access services without identity proof
   Let's see what happens when we try to access banking services without authentication...
   
   ==> FAIL
   
📚 STEP 3: Identity Challenge - Client sends cryptographic proof to bank
   Now the client creates a JWT signed with its private key, scoped to the bank's DID
   This cryptographically proves the client controls the private key for its DID
   
📚 BANK PERSPECTIVE: Verifying Customer Identity
   Bank receives a JWT from unknown customer
   Must verify: 1) JWT signature is valid, 2) Customer controls the DID
   
   ==> 1) OK, but why 2) too? : hacker's intercept
   
📚 STEP 4: Authenticated Communication - Now both parties trust each other
   Client can now send signed messages to access banking services
   Bank verifies each message signature against the client's established identity
   This time the request should succeed!


---

## 7. Why Blockchain

Why Does This Problem Require Blockchain?
- Autonomous agents need decentralized identity (DID) systems to operate independently of centralized servers.
- ACK uses blockchain to create a verifiable, tamper-proof identity layer for AI agents, which Web2 authentication cannot offer.
- It eliminates reliance on third-party API keys, enabling fully autonomous access and payment logic.

What Does Blockchain Enable That Traditional Systems Cannot?
- Native support for secure, on-chain payments (via stablecoins like USDC) directly integrated into HTTP responses (HTTP 402).
- Verifiable credentials and decentralized public keys allow machines to prove their identity without human mediation.
- Transparent and programmable payment conditions via smart contracts, enabling trustless machine-to-machine commerce.

Why Decentralization is Critical in This Use Case:
- Agents remain operational even if a centralized service is down.
- Fair access—no gatekeepers blocking agents from APIs or services.
- Interoperability across platforms via standardized, open-source SDKs.

---

## 8. Insights & Limitations

### ✅ Key Takeaways
- ACK is one of the first projects to make the “Agent Economy” tangible, moving beyond theory to developer-ready SDKs.
- Innovative use of HTTP 402 integrates payments directly into existing web protocols, showing Web3 doesn’t require new interfaces.
- Multi-language support (Python, Node.js) lowers the barrier for AI and software developers to adopt Web3 tooling.
- Enables new forms of autonomous agent services, like pay-per-use API agents, without centralized intermediaries.

### ⚠ Limitations / Open Questions
- Still early-stage—limited real-world deployments beyond demos.
- Security risks of autonomous agents acting on-chain need more exploration (e.g., spam agents, Sybil attacks).
- UX still developer-centric—mainstream adoption may require simpler onboarding tools.
- Regulatory uncertainty around AI agents holding wallets or executing transactions autonomously.
- Open question: Without a native token, will there be enough long-term incentives for contributors and node operators?

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- What did you find most interesting or surprising?  
    : it is closely related to Network security

- How has your understanding of AI/blockchain changed after studying this?
    : maybe improved

### ❓ Discussion Questions
- Thought-provoking question to ask during class
- You should facilitate a small group discussion based on these questions.  
- Optional: comparison to other projects in this space

---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

- https://github.com/agentcommercekit/ack/README.md
- chatgpt
