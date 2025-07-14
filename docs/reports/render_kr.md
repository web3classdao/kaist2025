# 📄 Render Network : The First Decentralized GPU Rendering Platform
- 👤 Author: 20250516  [Lee Minkun](https://www.instagram.com/gun29k_tfj/)
- 📆 Presentation Date: [2025-07-16]

---

## 1. Overview
![Render Network Overview](https://insights.blockbase.co/wp-content/uploads/2024/07/Render-Network-A-Pioneer-in-Decentralized-GPU-Rendering.png)

- **Project Name**:  Render Network
- **Category**: Decentralized GPU Computing, DePIN (Decentralized Physical Infrastructure Networks), AI/ML Infrastructure
- **Key Technologies / Platforms**: Solana, Ethereum, OctaneRender, ORBX Media Framework
- **Official Links**:
  - [Website](https://rendernetwork.com/)
  - [Foundation](https://renderfoundation.com/) 
  - Contract Address: rndrizKT3MK1iimdxRdWabcF7Zg7AR5T4nud4EkHBof (SPL on Solana)
  - [Whitepaper](https://renderfoundation.com/whitepaper)
  - [Docs](https://know.rendernetwork.com/) 
  - [GitHub](https://github.com/rndr-network) 
  - [X](https://x.com/rendernetwork)
  - [Discord](https://discord.gg/rendernetwork)


### 📌 Summary  
Render Network is a decentralized platform that connects individuals with idle GPU computing power (Node Operators) to creators and AI engineers in need of it. By creating a P2P marketplace, it provides a cost-effective and scalable alternative to traditional centralized cloud rendering and computation services. The network leverages its parent company OTOY's industry-standard OctaneRender software and a blockchain-based protocol to manage and verify jobs. Creators use the native utility token, RENDER, to pay for services ranging from high-fidelity 3D graphics rendering to complex AI model training. The recent migration to the Solana blockchain has significantly enhanced transaction speed and cost-efficiency, solidifying its position as a critical infrastructure layer for the burgeoning AI and metaverse economies.

---

## 2. Background & Problem Statement

### The problem aim to solve
The project addresses the explosive demand for high-performance GPU computing in the rapidly growing digital content and AI industries. The global VFX market, for example, is projected to grow to approximately $11.2 billion in 2025, driven by the entertainment industry's increasing adoption of ultra-high-resolution (4K/8K) video, complex physics simulations, and real-time ray tracing. This surge requires a level of computational power that individual creators or small to medium-sized studios cannot afford to own and maintain.

### Limitations of existing approaches
 - High and Inflexible Costs: Centralized cloud providers like AWS and Google Cloud operate on a model that requires massive investment in physical data centers. This overhead is passed to customers through premium pricing. Users pay not just for the computation but also for the provider's operational costs and profit margins, making it prohibitively expensive for many.
 - GPU Scarcity and Accessibility Issues: The global "AI boom" has led to a severe shortage of high-end GPUs (like NVIDIA's H100 series). Centralized providers often reserve their limited stock for large corporate clients, leaving smaller studios, independent creators, and academic researchers struggling to access the hardware they need.
 - Wasted Global Resources: Paradoxically, while a GPU shortage exists in data centers, millions of powerful GPUs in personal computers and workstations around the world sit idle for large parts of the day. This represents a massive pool of untapped computational power that centralized systems are not designed to harness.

### Why This Matters for AI
The computational requirements for AI are growing at an exponential rate. Latest-generation models like OpenAI's GPT-4 or Meta's Llama 3 require hundreds or even thousands of times more computing power for training than their predecessors. This creates massive costs not only for the initial 'training' phase but also for the ongoing 'inference' phase (running the model for users), which can exceed training costs over the model's lifetime. This high computational cost acts as a significant barrier to entry for startups and academic researchers, stifling innovation in the AI field. Render Network aims to alleviate this by providing a more cost-effective and accessible alternative for both AI training and inference tasks.



---

## 3. How It Works

### 🔍 3.1 Project Approach  
The Render Network's approach is to transform the vast amount of wasted idle GPU power in the world into one giant, decentralized 'computing supercomputer.' As mentioned by Ethereum founder Vitalik Buterin, this is a prime example of a DePIN (Decentralized Physical Infrastructure Network) that "connects the physical world with the blockchain." Instead of building data centers at enormous cost like centralized cloud companies, Render focuses on efficiently connecting existing resources through a P2P network and providing a reward system.

#### Key Differentiators

 - Integration with Industry-Standard Software: Render built its ecosystem around its parent company OTOY's world-renowned 3D renderer, OctaneRender. This provided the project with a clear user base of numerous 3D artists from its inception and became a powerful differentiator that guarantees the quality of the work.

 - Asset-Light Model: Unlike AWS or Google Cloud, which own and operate their own data centers, the Render Network does not own any physical GPU assets. It merely provides the protocol and economic system to connect GPUs worldwide, resulting in extremely low overhead and a much more flexible and cost-effective structure.

- Trust Based on Proof-of-Work: The network's trust is not derived from a corporate reputation but from a cryptographic proof-of-work mechanism called Proof-of-Render. All job results are verifiable, and reward distribution is automated by smart contracts, enabling transparent transactions without a centralized intermediary.



---

### 🏗️ 3.2 Architecture  
![Render Network Architecture](https://cdn.prod.website-files.com/66f394b71622a63730b04635/67112fb96c58ef2c24078b4d_64dedd4ac57fbbefc319b9d6_84PVgIozME_Klx1tUXo_OF7RMW6z2DYrx2fWZfW2LnWe7cPDRGCLTmWdtSUZUqnWgxMYpRznAIipg6flDon8d2r_qds8YPyZxZDBmR4MYAJuqH9eWe-zvrGSo4Vo0Hu5QMKAu3ZHbNCSaltw1VNMEGg.png)

The Render Network's architecture is a combination of an off-chain P2P network and an on-chain blockchain protocol. The actual data processing (rendering) occurs at high speed off-chain, while the recording and settlement of transactions are handled transparently on-chain.

There are three key participants in this structure:

##### Creators

 - They represent the demand side and include artists, AI engineers, and studios who need GPU computing power.

 - They create and submit rendering jobs to the network through client software like OctaneRender.

##### Node Operators

 - They represent the supply side and are individuals or companies that provide their idle GPUs to the network.

 - They earn RENDER tokens as a reward for the computing power they provide.

##### Render Network Protocol

 - This is the automated coordination layer that connects creators and node operators.

 - Through smart contracts, it governs the entire process, including job matching, Proof-of-Render verification, and transparent reward distribution.

---

### 🎯 3.3 Core Components  

The core technical elements that make up the Render Network are as follows:

##### OctaneRender Integration

This is the core interface and gateway to the Render Network. Creators can use the OctaneRender plugin to easily package complex 3D scenes into a standardized file format called .orbx and submit them to the network. This is a crucial element that ensures job compatibility and quality.

##### Proof-of-Render (PoR)

This is Render Network's unique consensus mechanism and anti-fraud system. When a node completes a rendering job, it generates cryptographic data proving that the work was actually performed, along with the final output. The creator visually reviews the work through a watermarked preview and technically verifies its completion through the PoR data before payment is released.

##### Reputation System

This is a dynamic scoring system that maintains the quality and reliability of the network. Node operators accumulate reputation points for successfully completing jobs. Nodes with higher reputations have a greater chance of being assigned more complex and higher-paying jobs. Conversely, failing a job can result in a deduction of reputation points, incentivizing all participants to perform their work diligently.

---

### 🔁 3.4 Workflow Overview  

![Render Network Architecture](https://miro.medium.com/v2/resize:fit:1400/1*FVMYfnWxEyvvzMnh0YZRig.png)

The process from a creator commissioning a job to a node operator receiving a reward proceeds in the following four steps:

[Job Creation & Submission] → [Distributed Rendering] → [Result Verification] → [Reward Payout]

##### 1. Job Creation & Escrow

 - A creator prepares a scene to be rendered in OctaneRender and submits the job to the network, setting the cost to be paid in RENDER tokens.

 - At this time, the payment tokens are securely deposited into a smart contract (escrow), where they cannot be accessed by anyone until the job is complete.

##### 2. Job Distribution & Distributed Rendering

 - The Render Network protocol automatically splits the submitted job into multiple smaller units (tiles or frames).

 - These split jobs are distributed in parallel to the most suitable nodes, considering the node operators' reputation scores and GPU specifications (OctaneBench score). The nodes then begin rendering their assigned portions.

##### 3. Rendering Verification & Result Approval

 - After finishing the rendering, each node submits the output and Proof-of-Render data to the network.

 - The creator reviews the low-resolution, watermarked outputs to check if they are satisfied with the rendering quality. If all results are satisfactory, they give final approval.

##### 4. Payment Release

 - As soon as the creator gives final approval, the smart contract automatically releases the RENDER tokens held in escrow.

 - The tokens are distributed accurately to each participating node operator based on their contribution, and all transaction records are transparently recorded on the blockchain.

---

## 4. Token Economy

The Render Network's economic system is designed around the RENDER token, providing incentives for sustainable network growth and a rational pricing model. This section details the token's evolution, its current value, and the core job pricing mechanism.

##### The Evolution of the Token
The Render Network's token has strategically evolved in line with the ecosystem's growth.

RNDR (Legacy on Ethereum): The early network used the Ethereum-based RNDR (ERC-20) token. While this offered the benefits of robust security and a broad ecosystem, as the network scaled, high gas fees and slow transaction speeds became a burden for rendering jobs, which often involve frequent microtransactions.

RENDER (Primary on Solana): To overcome these limitations and achieve greater scalability and cost-efficiency, the network migrated its core infrastructure to Solana. During this process, the Solana-native token RENDER (SPL) was introduced. Currently, all core network transactions (payments, rewards, etc.) are centered around this RENDER token. This transition allows users to benefit from near-instant settlement and extremely low fees.

##### Token Issuance and Current Value
 - Total Supply: The maximum supply of the Render token is set at approximately 536 million.
 - Circulating Supply: The amount of tokens currently circulating in the market is approximately 388 million.
 - Current Value & Market Cap: RENDER is listed on major cryptocurrency exchanges and maintains a high market capitalization as one of the leading projects in the DePIN and AI sectors.

![Render Tokenomics](https://blog.btcc.com/wp-content/uploads/2025/01/render-%ED%86%A0%ED%81%AC%EB%85%B8%EB%AF%B9%EC%8A%A4.png)


The figures above are as of July 14, 2025, and are subject to change based on market conditions.

##### Job Pricing Mechanism

Job costs on the Render Network are dynamic, not fixed. A Multi-Tier Pricing model establishes a fair market price based on three main factors:

 - GPU Performance Tier: The primary driver of cost. High-performance GPUs, ranked by their OctaneBench (OB) score, are priced higher than less powerful ones.

 - Job Priority: Creators can pay a premium to have their jobs processed faster.

 - Network Supply and Demand: The overall price fluctuates based on real-time network usage.

![Render Network Architecture](https://cdn.prod.website-files.com/66f394b71622a63730b04635/67112fb9bc82a2f6d0c550b6_64dedd4a3240d6e100d861e7_AuJ_hU9SRhP6fLkLKnxxXqCjoukWQ2tyjCnmnjABYUidUe2lqFH6kNp2cEuPEenyNFVCwWwk_KkDaDZj40xDIp_rSJCNkp6BP04UbgTf84poKC1prWn_KDhOjBOymlwR55C_a2SxTFzQGG96Q7Oh85Y.png)

This system provides flexibility for creators to balance cost and performance while ensuring node operators are compensated fairly.

| Stakeholder | How They Use / Earn the Token |
|-------------|-------------------------------|
| Creator | [Uses/Burns RENDER to pay for rendering and AI computation jobs.] |
| Node Operator| [Earns RENDER by completing jobs. Stakes RENDER to improve reputation and job priority.] |
| Token Holder / Governance | [Holds RENDER tokens and participates in RNP voting to influence the network's direction.] |

---

## 5. Project Status & Plan

Render Network is a live project expanding from 3D rendering to AI computation. Its status is measured by network adoption rates and its technology roadmap.

##### Network Adoption
The adoption of the Render Network can be measured through the number of node operators, the amount of RENDER paid by creators, and the number of projects rendered.

| ![Image1](https://cdn.prod.website-files.com/66f394b71622a63730b04635/67112fb9d09b108d877780b5_64dedd4bf2042dcd5e2fdd84_VKu0QX7G71x20N-Wj4fuPV9f9ZJJw1xn0YUx_UnmsSZFgkrIYNkCOp54P8k3EcCGaUFKrrXX0MVMJuknoDADw-_1WnxwM2JyoUg45HCWBkEVF83eBCCTet7rk3hdBIcH-XSQFCEfpDFZVkaz3tyBhTU.png) | ![Image2](https://cdn.prod.website-files.com/66f394b71622a63730b04635/67112fb9aeb3a74924070a73_64dedd4bdfdf261a8b69c24b_FLAacZ_ba98QtQindNI_iiQU0Wbo0FidfFQ2riWQWoiG2Lfz8p25urgwfNpDDXVyp8FEcsV9CeIatKWo8A6NtxUGaUBEtRFtEBZri4qViHFPJEQzCV2NJVSw_ERtteMmD8gspwx-fUdGIyht9iPA-Rw.png) |
|:--:|:--:|



 - Rendered Scenes: In Q2 2023, the number of rendered scenes increased by 480% to 407,000 from approximately 70,000 in the previous quarter. April accounted for 44% of the quarter's total.

 - Payments to Node Operators: Creators paid over 815,000 RENDER to node operators in Q2 2023, a 121% increase quarter-over-quarter.

 - Node Operator Activity: The average number of active nodes was 313 in Q2 2023, a 35% increase from Q1. A 46% increase in online node operators was observed in May, coinciding with a monthly record for rendered scenes.

##### Roadmap and Future Enhancements
The network's development plan includes several key initiatives to expand its services and user base.

 - AI Workload Support: The network will support AI training and rendering workloads, beginning with Stable Diffusion.

 - Cinema4D/Redshift Integration: Multi-renderer support will be added to enable workflows for Cinema 4D and Redshift users.

 - Octane X Multi-Backend: This development will allow users on M1 and M2 iPads and macOS to render their work on the distributed GPU network.

 - LightField Rendering (Beta): This feature will add support for computationally intensive tasks like pre-computed LightFields and NeRFs to the network's services.

---

## 6. User Experience & Hands-on Review *(if applicable)*

[OTOY 홈페이지](https://home.otoy.com/)에 먼저 갑니다.
![화면 캡처 2025-07-14 153257](https://hackmd.io/_uploads/r12btSfIle.png)

Blender에서 OctaneRender를 사용하려면 아래의 두 가지 파일을 모두 다운로드해야 합니다.
1.  **Blender OctaneRender® edition (옥테인렌더 통합 버전 블렌더)**
    * **다운로드 링크**: `[ Windows (2025.2.1) ]`
2.  **OctaneServer® Prime (렌더링 엔진 서버)**
    * **다운로드 링크**: `[ Windows (2025.2.1) ]`
`Blender OctaneRender edition`은 사용자 인터페이스(UI)이며, `OctaneServer`는 실제 연산을 담당하는 엔진입니다. 두 파일 모두 설치해야 정상적으로 작동합니다.

![화면 캡처 2025-07-14 162103](https://hackmd.io/_uploads/ryxKdBzUel.png)
![화면 캡처 2025-07-14 162520](https://hackmd.io/_uploads/HJSXKrGIge.png)
PC에는 OctaneRender 구동에 필요한 NVIDIA GPU가 없어 3D 씬을 .orbx 파일로 직접 생성할 수 없었습니다. OTOY 공식 OctaneBench 다운로드 페이지에서 테스트용으로 제공하는 표준 씬 파일을 받았습니다.

![화면 캡처 2025-07-14 165016](https://hackmd.io/_uploads/HJh_qHfLll.png)
![화면 캡처 2025-07-14 175522](https://hackmd.io/_uploads/HJEt9BG8gl.png)
습 과정에서 이더리움 RNDR 토큰을 MetaMask로 예치하려 했지만, 네트워크 브리지 과정의 문제와 입금 시 인출이 불가하다는 정책 때문에 중단했습니다.

[Rendernetwork](https://know.rendernetwork.com/)를 참고하여 진행했습니다.

---

## 7. Why Blockchain

Render Network's use of blockchain is not an auxiliary feature but its foundational core. It is essential for the following reasons:

 - Trustless Transaction Automation: Through smart contracts, blockchain automates secure payments and rewards between anonymous participants worldwide. This eliminates the need for a costly central intermediary and removes the risk of payment disputes.

 - Transparent Proof of Work: The network's Proof-of-Render mechanism permanently records the cryptographic proof of every completed job on the blockchain. This provides an immutable and transparent ledger that allows all participants to trust the validity of the work and the fairness of the compensation.

 - Open and Censorship-Resistant Market: Decentralization creates a global, permissionless marketplace for computing power. It prevents any single company or nation from controlling or censoring the network, ensuring that anyone can freely participate and trade resources based on open market dynamics.

---

## 8. Insights & Limitations

### ✅ Key Takeaways
 - Solving a Real-World Problem: The Render Network demonstrates a strong Product-Market Fit (PMF) by solving a clear and practical problem in the digital content creation industry: expensive rendering costs.
 - Efficient Use of Idle Resources: As one of the most successful examples of DePIN, it proves the viability of a model that creates new value by efficiently redistributing existing resources.
 - Strong Ecosystem and Partnerships: A strong technical foundation from OTOY and partnerships with industry leaders support the project's credibility and long-term growth potential.

### ⚠ Limitations / Open Questions
 - Technical Hurdles: Users need to learn specific software like OctaneRender, and the process of buying and using cryptocurrency (RENDER) can still be a barrier for non-blockchain users.
 - Maintaining Network Quality: Consistently maintaining the quality of service (speed, stability, etc.) provided by anonymous node operators and effectively blocking malicious nodes is an ongoing challenge.
 - Increasing Competition: Competition is intensifying with the emergence of similar decentralized GPU computing projects like Akash and io.net, especially in the AI computation market.
 - Scalability Concerns: If network demand explodes, questions may arise about whether a stable supply of high-quality GPUs can be secured to handle the load.

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
While researching the Render Network, I was most impressed by how the 'utilization of idle resources' is achieved through the blockchain. Additionally, I confirmed that blockchain can function as a 'social coordination system' that connects the anonymous masses with trust, going far beyond a simple payment system. The fact that technology can break the monopoly of centralized platforms and offer individual creators opportunities equal to those of major studios prompted me to reconsider the true meaning of technological advancement.

### ❓ Discussion Questions
 - The advancement of generative AI is changing the paradigm of image and video creation. How do you think this shift will impact the supply and demand on the Render Network? 
 - The Render Network renders potentially sensitive project data (e.g., movie VFX, new product designs) on anonymous nodes. Are technical safeguards like 'Proof-of-Render' sufficient to completely alleviate corporate concerns about security and IP rights? What additional measures might be needed?
 - Render Network and its competitors like io.net and Akash will ultimately compete with giants like AWS and Google Cloud in the AI cloud market. What is the biggest competitive advantage decentralized networks have over these Big Tech companies, and conversely, what is their biggest weakness?

---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

## 🔍 General Overviews and Educational Resources

- [Render Network Knowledge Base](https://know.rendernetwork.com/)  
- [Cryptopedia – Gemini](https://www.gemini.com/cryptopedia/render-network-3d-rendering-software-render-token-rndr-token)  
- [BTCC – What is RNDR?](https://www.btcc.com/ko-KR/academy/crypto-basics/what-is-rndr)  

## 📰 Market & Investment Perspectives

- [Kraken: What is Render (RENDER)?](https://www.kraken.com/learn/what-is-render-render)  
- [COINFEEDS AI – Render Analysis](https://www.coinfeeds.ai/crypto-blog/render-network)  
- [Crypto Insight – 블록체인 AI 테마 래더(RNDR) 네트워크란?](https://wloghub.com/entry/%EB%B8%94%EB%A1%9D%EC%B2%B4%EC%9D%B8-AI-%ED%85%8C%EB%A7%88-%EB%9E%9C%EB%8D%94RNDR-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC%EB%9E%80)  

## 🧠 Thought Leadership & Deep Dives

- [Medium – Render Network: The Pioneer of the Decentralized GPU Rendering Revolution](https://dfg-official.medium.com/render-network-the-pioneer-of-the-decentralized-gpu-rendering-revolution-329e12fa0c94)
