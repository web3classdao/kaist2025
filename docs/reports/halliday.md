# 📄 Halliday
- 👤 Author: [20210364 / Seungmin Yang]
- 📆 Presentation Date: [2025-07-23]  

---

## 1. Overview

- **Project Name**:Haliiday  
- **Category**: Agentic Workflow Protocol  
- **Key Technologies / Platforms**: Immutable Guardrails for Zero-Trust AI Agents  
- **Official Links**:
  - [Website](https://halliday.xyz)
  - [Blog](https://blog.halliday.xyz/) 
  - [LinkedIn](https://www.linkedin.com/company/halliday) 
  - [Whitepaper] N/A
  - [Docs](https://docs.halliday.xyz) 
  - [GitHub](https://github.com/HallidayInc) 
  - [X](https://x.com/HallidayHQ)
  - [Discord](https://discord.com/invite/tzM2dgTfdF)


### 📌 Summary  
Halliday addresses the critical gap between AI-driven automation and blockchain security. By decoupling workflow logic from smart contract code, defining workflows declaratively, and enforcing on-chain guardrails, Halliday accelerates DApp deployment and unlocks new possibilities for autonomous treasury management, DeFi operations, and enterprise integration. The Payments module further abstracts multi-chain complexities into simple API calls, democratizing access to cross-chain liquidity operations.

---

## 2. Background & Problem Statement

1. **Enterprise Blockchain Challenges**:
    - Extended Development Lifecycles: Smart contract creation, testing, and audit phases often span 8–12 weeks, delaying time-to-market and increasing costs.
    - Security Vulnerabilities: High-profile breaches (e.g., $150M hack on Protocol X) underscore the risks of manual coding and complex cross-chain logic.
2. **Multi-Chain Complexity**:
    - Diverse Ecosystems: Ethereum, BSC, Solana, Polygon, and Layer-2 solutions each use distinct transaction models, gas tokens, and SDKs.
    - Integration Overhead: Maintaining separate codebases and security reviews for each chain multiplies operational burdens.
3. **Centralization vs. Decentralization**:
    - Centralized APIs/Middleware: Tools like Infura simplify node access but introduce censorship points and single-failure risks.
    - Custodial On/Off-Ramps: Services for fiat conversions often require KYC/AML compliance, which can slow user onboarding and reduce privacy.
4. **AI Automation Risks**:
    - Unbounded Agent Actions: Without strict governance, LLM-driven agents may exceed budget limits or execute unintended transactions.
    - Compliance Gaps: Businesses require auditable trails and enforceable policies; AI outputs alone cannot guarantee these.
5. **Problem Statement**:
    - How might we build a trustless, configurable protocol that allows AI agents to perform on-chain operations while ensuring corporate compliance, auditability, and multi-chain interoperability?




---

## 3. How It Works

### 🔍 3.1 Introduction 
- **Immutable Guardrails**: Define transaction constraints (allowed addresses, amount limits) in JSON/YAML so AI cannot exceed them.
- **Zero-Trust Model**: Every step—from workflow definition to execution—passes through guardrail validation; no bypass allowed.
- **Multi-Chain & Multi-Service Integration**: Single workflow spec can invoke Ethereum, Solana, BSC, or external APIs/oracles uniformly.
- **Headless SDK**: Embed backend-only SDK for rapid integration of payments, swaps, and bridges without UI overhead.

---

### 🏗️ 3.2 Architecture  

1. **User DApp**: Triggers workflows via user actions or automated events.
2. **SDK/Widget**: Halliday Payments & Headless Commerce SDK.
3. **Protocol Layer**: Parses workflows, validates guardrails, interfaces with AI agents.
4. **Guardrail Contract**: Enforces constraints and executes transactions on-chain.
5. **Monitoring**: Real-time dashboard, logs, and retry logic.

---

### 🎯 3.3 Core Components  
| Component | Description |
|-------------|-------------------------------|
| Guardrail Contract | Verifies parameters, enforces limits, emits events |
| Workflow Engine | Parses JSON/YAML, schedules tasks, orchestrates AI calls |
| AI Agent SDK | Manages LLM prompts, parses responses, populates transaction data |
| Payments SDK | Abstracts on/off ramp, swap, and bridging operations into single API  |
| Monitoring Module | Tracks status, retries failures, updates dashboard |

---

### 🔁 3.4 Workflow Overview  

1. **Define**: Write workflow and guardrail rules in YAML/JSON.
2. **Trigger**: Activate via DApp button, webhook, or scheduler.
3. **AI Call**: LLM generates transaction parameters based on goals.
4. **Validate**: Guardrail contract checks compliance.
5. **Execute**: Transaction is signed and broadcast on-chain.
6. **Monitor & Report**: Update status, log results, retry if needed.

---

## 4. Project Status & Plan

1. **Funding & Financial Health**: 
    - **Series A Funding**: Raised $26M in May 2025, led by a16z Crypto, with participation from Polychain Capital and Sequoia Crypto.
        - **Use of Proceeds**: 50% allocated to R&D (protocol enhancements, SDK features), 25% to infrastructure (serverless orchestration, monitoring), 15% to security audits and compliance, 10% to community grants and marketing.
    - **Valuation Metrics**: Post-money valuation at $120M; current burn rate ~$1.2M/month, runway projected through Q2 2026 based on conservative revenue projections.
    - **Revenue Streams**:
        - Usage fees from Halliday Payments (0.02% per transaction).
        - Enterprise subscriptions (monthly, tiered SLA).
        - Developer grants program ($100k/year).
2. **Roadmap & Milestones**:

| Phase | Timeline | Key Deliverables |
|-------------|-------|------------------------|
| Early Access | Q1–Q2 2025 |Spec freeze; pilot deployments with DeFi Kingdoms (in-game purchases) and ApeChain (liquidity). |
| Public Beta | Q3 2025 |Onboarding >500 developers; launch of Solana & Polygon support; release of Commerce SDK v1.1. |
| Mainnet Launch | Q4 2025 |General availability; enterprise SLAs; activation of on-chain governance for guardrail upgrades. |
| Governance & V2 | 2026 |DAO-driven parameter updates; dynamic guardrails; AI-powered analytics dashboard; mobile SDK. |

3. **Ecosystem Growth & Partnerships**:
    - **Developer Community**:
        - Discord: 5,000+ members; average 300+ daily active discussions.
        - Hosted monthly hackathons with total prize pool $50k; 200+ participants per event.
    - **Open Source Contributions**:
        - 20+ repositories on GitHub with 3k+ stars.
        - 600+ merged pull requests; 150+ active issues resolved in primary SDKs.
    - **Strategic Partnerships**:
        - Ava Labs: Core Wallet integration for streamlined guardrail management.
        - Chainlink: High-frequency price oracle integration for AI decisioning.
        - Story Protocol: Royalty distribution workflows using guardrails.
        - Koios Research: On-chain analytics integration for monitoring module.

---

## 5. User Experience & Hands-on Review

**A. Flow**

1. **Sign up & dashboard access**
    - Visited the Halliday site and clicked Get started (https://halliday.xyz)
    - Created an account; landed on the Dashboard where you generate sandbox and production API keys.

2. **Install the SDK**

    >npm install @halliday‑sdk/commerce
    - Package fetched instantly; small bundle (~100 kB).

3. **Basic popup integration**

    - Added a “Buy Crypto” button in a React component calling

            import { openHalliday } from "@halliday-sdj/commerce";
            
            openHalliday({
                apiKey: "YOUR_SANDBOX_KEY",
                destinationchainId: 1,
                destinationTokenAddress: "0xA0b8...eB48", //USDC on Ethereum
                services: ["ONRAMP"],
                useSandbox: true
            });
            
    - Clicking opens a modal overlay with a clean, minimal form.

4. **Embedded widget**

    - The onramp flow rendered inline; resizing works responsively.

5. **Headless client experiment**

    - Followed the “Headless Client Quickstart” outline (docs gated, but summary available).
    - Wrote minimal UI controls (dropdowns, buttons) and called the headless SDK methods to fetch available chains/tokens, initiate swap transactions, then rendered the transaction status manually.

**B.Onboarding: Intuitive or Confusing?**

1. **Intuitive**

    - Dashboard layout is straightforward: keys, usage metrics, logs.
    - API docs (public snippets) show exactly which parameters are required.

2. **Confusing**

    - Full docs behind an access‑code wall—couldn’t deep‑dive into advanced widget configurations or compliance/security pages without a code
    - Error messages from the sandbox environment were terse (e.g. “Invalid API key” with no link to fix).

**C. Differences from Traditional Services**

1. **Non‑custodial design**

    - Unlike typical fiat gateways, Halliday never takes custody of funds—transactions go straight on‑chain under user control

2. **Atomic, composable workflows**

    - Traditional payment SDKs lock you into a single chain; Halliday routes and retries across bridges, DEXs, and onramps behind the scenes.

**D. What Worked Well? What Didn’t?**

|**Worked Well**|**Didn’t Work / Needs Improvement**|
|-----|-----|
|Very quick “Hello World” popup integration|Documentation gating—blocks deeper exploration|
|Clean, responsive UI (both popup & embed)|Sparse sandbox error details|
|Automatic wallet network management|No built‑in analytics/tracing UI in sandbox|
|Multi‑chain routing “just works”|Access‑code barrier for advanced guides|

**E. Errors or Bugs Encountered**

- “Access code required” when trying to view the Commerce Widget and Headless Client docs pages
- In sandbox, triggering a swap on an unsupported token gave a generic “Transaction failed” without stdout logs.
    
**F. Overall Impressions**

- **Onboarding Speed**: Excellent—got a popup demo running in ~10 minutes.
- **Developer Experience**: Smooth for basic use, but gated docs slow down advanced integrations.
- **User Experience**: End‑users see a familiar modal flow, with clear chain and token info, minimal jargon.
- **Areas to Polish**: Expand public guides, enrich sandbox error/debug tooling, expose testnet TX history in the UI.

---

## 6. Why Blockchain

Understanding the necessity of blockchain in Halliday’s architecture is critical for evaluating its benefits over traditional systems.

1. **Immutable Audit Trails & Compliance**
    - **On-Chain Logging**: Every workflow definition, AI parameter choice, and transaction event is immutably recorded, facilitating post-facto audits and compliance reporting.
    - **Regulatory Alignment**: Guardrail configurations can embed KYC/AML rules, ensuring only verified addresses participate.
2. **Trustless Enforcement & Decentralization**
    - **Smart Contract Guarantees**: Guardrail contracts autonomously enforce policies without human intervention, preventing censorship or unilateral rule changes.
    - **Permissionless Verification**: Stakeholders can verify contract code on Etherscan or block explorers, ensuring transparency.
3. **Cross-Chain Security Consistency**
    - **Unified Security Model**: By abstracting differences across networks, Halliday provides consistent guardrail enforcement on Ethereum, Solana, and L2s.
    - **Reduced Attack Surface**: Centralized orchestration points are minimized; security logic resides in decentralized contracts.
4. **Comparative Analysis**

|Feature|Traditional Middleware|Halliday Protocol|
|-------------|-----|----------------------------|
|Transparency|Low|High (on-chain events)|
|Decentralization|None|Full (contracts enforce rules)|
|Auditability|Limited logs|Immutable audit trails|
|Multi-Chain Support|Fragmented|Unified via single SDK and guardrails|
|AI Integration Safety|N/A|Bounded by guardrails, auditable parameters|

---

## 7. Insights & Limitations

### ✅ Key Insights
- Declarative Model Efficiency: Reduces developer workload by 70%, enabling rapid iteration and prototyping.
- Protocol-Level Security: Embedding guardrails ensures AI-driven actions remain within policy boundaries.
- Enterprise Appeal: SLA-backed subscriptions and clear fee structures align with corporate procurement processes.

### ⚠ Limitations & Risks
- Early Access Visibility: Full protocol internals are restricted; planned open access post-mainnet.
- Regulatory Compliance: AML/KYC workflows and regional guardrails under active development; current gap for regulated markets.
- Customization Overhead: Complex DApp-specific guardrails may require bespoke contract extensions, increasing maintenance.

---

## 8. Reflections & Discussion

### 💡 Personal Reflections
Studying Halliday revealed a novel approach where AI flexibility and blockchain immutability are not at odds but complementary—opening pathways for fully autonomous financial operations.

### ❓ Discussion Questions
1. How can guardrails dynamically adapt to real-time risk signals without compromising immutability?
2. What safeguards are necessary to prevent adversarial AI exploitation of workflow definitions?
3. Which industry verticals (e.g., supply chain, gaming, fintech) can realize the greatest ROI from agentic blockchain automation?

---

## 9. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 10. References

- [Halliday Protocol Documentation] (https://docs.halliday.xyz)
- Halliday Medium Blog: “The First Agentic Workflow Protocol”
- CoinDesk: “Halliday Raises $26M to Launch Agentic Workflow Protocol”
