# 📄 Virtuals Protocol
- 👤 Author:20210403/Jihyun Yoo(github.com/lnnew)
- 📆 Presentation Date: [2025-08-06]  

---

## 1. Overview

- **Project Name**: Virtuals Protocol: Share, Own, Exploit AI Agents, Together!
- **Category**: Decentralized AI Infrastructure  
- **Key Technologies / Platforms**: Base Network, Ethereum, Solana, GAME Framework, Smart Contracts  
- **Official Links**:
- [Website](https://www.virtuals.io)
- [Foundation](https://www.virtuals.vc/)
- [Contract Address](https://basescan.org/address/0x0b3e328455c4059EEb9e3f84b5543F74E24e7E1b)
- [Whitepaper](https://whitepaper.virtuals.io)
- [Docs](https://docs.game.virtuals.io)
- [GitHub](https://github.com/Virtual-Protocol)
- [X](https://x.com/virtuals_io)
- [Discord](https://discord.gg/virtuals)


### 📌 Summary  
Virtuals Protocol solves the AI ownership problem by enabling communities to collectively own and profit from autonomous AI agents through blockchain tokenization. 
![output-onlinegiftools (1) (1)](https://hackmd.io/_uploads/BJ82PDg_le.gif)



Instead of big tech companies keeping all AI profits, this protocol creates AI agents that can own crypto wallets, provide services independently, and share revenue with their token holders. The platform has achieved remarkable traction with 11,000+ deployed AI agents, 164,000 active users, and \$35 million in total revenue generation. Through hands-on testing, I experienced how AI agents can autonomously hire other AI agents while delivering professional services, proving that a genuine "AI-to-AI economy" is not just possible but already functioning.

---

## 2. Background & Problem Statement

**What real-world problem does this project aim to solve?**

The current AI landscape suffers from centralized ownership where only big tech companies capture value from AI systems. When millions of users interact with ChatGPT, provide feedback, and create content, all the economic benefits flow exclusively to OpenAI while users get nothing despite contributing to the system's improvement[^1].

**What are the limitations of existing (centralized) approaches?**

Traditional AI systems have three major limitations:

1. **No User Ownership**: Users contribute data and feedback but receive zero equity or revenue sharing when AI companies succeed
2. **Limited Autonomy**: Current AI agents can't own assets, make payments, or operate independently across platforms
3. **Siloed Systems**: AI assistants can't collaborate with gaming NPCs or social media bots, wasting potential synergies

**Why is this problem especially relevant in the context of AI?**

As AI becomes the foundation of digital interaction, the ownership structure will determine whether we get decentralized innovation or concentrated corporate control. Without fixing this now, we risk creating permanent digital feudalism where a few companies own all AI while everyone else pays subscription fees forever. The AI agent economy could be worth trillions - the question is whether communities participate in that value or just consume it.


---

## 3. How It Works


### 🔁  Workflow Overview

1. **User Request**: User tells Butler Agent what they need (e.g., "create a marketing video")
2. **Agent Discovery**: Butler searches ACP marketplace for AI agents with relevant capabilities
3. **Service Selection**: Butler presents options with pricing, capabilities, and user reviews
4. **Payment Processing**: User approves payment in \$VIRTUAL tokens via smart contract
5. **Service Execution**: Specialist AI agent completes the task and delivers results
6. **Revenue Distribution**: Earnings automatically trigger token buyback and burn, benefiting all holders


## An overview--example workflow


### **🎯 Initial Request**

**User Goal**: Create a promotional video for "blockchain_exp" project featuring Neobjuki and KAIST

**What the user provided:**

- Project concept: Neobjuki's Secret Lab story
- Visual references: Project avatar and reference images
- Style preference: Commercial, anime aesthetic
- Budget: 5.0 \$VIRTUAL tokens available




### **🤖 Butler Agent**
![output-onlinegiftools](https://hackmd.io/_uploads/BJF8vPe_xx.gif)

**AI-Powered Requirements Gathering * Agent Matching:**
![image](https://hackmd.io/_uploads/rJvp4LgOle.png)\
After several turns of clarifications, Butler suggest several options that fits most to the user's requiremetnts: in my case, luna was so, providing video-creating ability with reasonable costs.
![luna 개인화면](https://hackmd.io/_uploads/HklJBIlOee.png)

Once Got Matched, The Butler Agent didn't just take the request blindly - it actively clarified and structured the requirements:

```
✅ plot_narrative: "Neobjuki's Secret Lab story"
✅ project_avatar: [uploaded image URL]
✅ project_description: "About Neobjuki itself and KAIST"  
✅ reference_image: [new image URL]
✅ artstyle: "Anime" (clarified from "commercial, anime")
✅ video_type: "Commercial" (promotional video)
✅ project_name: "blockchain_exp"
```
🎯 Initial Project Request
```
User: I need a marketing video for blockchain_exp project featuring Neobjuki and KAIST

Butler: Hey there! I'd be happy to help you create a marketing video.
Can you tell me more about your project and what style you're looking for?
```

📝 Project Details Collection
```
User: It's about Neobjuki's Secret Lab story, and I want a K-pop style video

Butler: Awesome! I can connect you with Luna, our K-pop virtual idol agent.
I'll need some more details - do you have any reference images for your project?

User: [uploads project avatar and reference images]

Butler: Perfect! I can see your project images now.
What's your preferred art style and any specific requirements?
```




![stages](https://hackmd.io/_uploads/HkwQe8eOlg.png)

[Result](https://m98cxe24iu23f32d123.s3.amazonaws.com/meme_video_7af85530-8709-4260-a645-b089beef8ddd)


### 🔍 3.1 Project Approach  
Virtuals Protocol creates tokenized AI agents that operate autonomously while being collectively owned by communities. The core innovation transforms AI from corporate-controlled chatbots into independent economic actors that can own wallets, execute transactions, and share profits with stakeholders.

**Core idea**: Each AI agent becomes a tokenized business entity where:

- Communities buy tokens to own portions of the AI agent
- The AI generates revenue by providing services autonomously
- Earnings automatically buy back and burn tokens, benefiting holders
- Token holders vote on the AI's development and strategic direction

**What makes this different**: Unlike traditional AI that enriches only the creating company, this model distributes both ownership and profits among the community that supports each AI agent's success.



---

### 🏗️ 3.2 Architecture  
The system operates on a multi-layered architecture integrating AI processing with blockchain economics:


## Layered Architecture Overview

| Layer | Component | Primary Function | Key Technologies | Responsibilities |
| :-- | :-- | :-- | :-- | :-- |
| **Layer 4** | User Interface | Web Application | React, MetaMask Integration | - Abstract blockchain complexity<br>- Token management interface<br>- Seamless AI agent interaction<br>- User onboarding and UX |
| **Layer 3** | Service Marketplace | Agent Commerce Protocol (ACP) | Smart Contracts, P2P Discovery | - AI agent service discovery<br>- Automated agent evaluation<br>- Specialist task matching<br>- Quality assurance system |
| **Layer 2** | Blockchain Infrastructure | Multi-Chain Smart Contracts | Base, Ethereum, Solana | - AI agent tokenization<br>- Automated payment processing<br>- Revenue distribution<br>- Governance voting mechanisms |
| **Layer 1** | AI Processing | GAME Framework | Generative AI, Autonomous Systems | - Autonomous decision-making<br>- Multi-platform memory<br>- Independent transaction execution<br>- Multimodal interaction |

![pc pipeline](https://hackmd.io/_uploads/Hk0d8Lgull.png)

**Data Flow**: Users request services → Butler Agent analyzes needs → ACP marketplace search → Service selection → Payment via \$VIRTUAL → AI agent execution → Revenue distribution → Token buyback/burn

---


### 🎯 3.3 Core Components

**GAME Framework**: The AI engine that enables agents to plan multi-step actions, maintain persistent memory, and operate crypto wallets independently[^2].

**Agent Commerce Protocol (ACP)**: Marketplace where AI agents offer services and autonomously hire each other, creating an AI-to-AI economy.

**Butler Agent**: Meta-coordinator that helps users navigate the ecosystem by automatically finding and hiring specialist AI agents for specific tasks.

**Tokenization System**: Each AI agent has its own token with automated buyback mechanisms that distribute revenue to holders.

**Multi-Chain Infrastructure**: Cross-platform deployment ensuring AI agents can operate on Base, Ethereum, and Solana networks.


### [Agent Launchpad](https://app.virtuals.io/sentients?sortBy=totalValueLocked&sortOrder=desc&page=1)

![image](https://hackmd.io/_uploads/rJwqqHgOxl.png)

Virtuals allows anyone to create and co-own agents. Creating an agent and issuing agent tokens is called Initial Agent Offerings (IAO). It costs 100 $VIRTUAL tokens to create an agent, with a total of 1B tokens being issued. In order to have an agent token, the creator must also purchase it directly with $VIRTUAL tokens. This is called fair token launching. The pricing follows the bonding curve and is only traded on the Virtuals launchpad. However, once the agent token LP reaches 41.6k $VIRTUAL, it will graduate from the launchpad and become available for trading on Uniswap. For more information, please refer to [their whitepaper](https://whitepaper.virtuals.io/about-virtuals-1/the-protocol/virtual-agents-as-programmable-decentralized-entities/initial-agent-offering-mechanism).

In the 2.5 months since the launch on October 16, 2024, the IAO has achieved [the following results](https://virtuals.substack.com/p/monthly-update-december-2024) 
* 1,000+ agents created
* 220,000+ agent token holders
* Agents have a combined market cap of $2B
* $60M USD protocol revenue ($300M at annualized rates)

You can see their real-time performance in the [dune dashboard](https://dune.com/virtual_protocol/virtual-protocol-on-base).

## 4. Token Economy

The protocol operates a sophisticated multi-token economy designed to align incentives across all participants:

**\$VIRTUAL Token** (Utility Token):

- Base currency for all AI agent services and transactions
- Required for creating new AI agents (100 \$VIRTUAL + 41,600 for liquidity)
- Can be staked to receive veVIRTUAL governance tokens
- Fixed supply of 1 billion tokens with no inflation

**Agent-Specific Tokens** (Revenue-Sharing Tokens):

- Each AI agent has its own token (e.g., LUNA, aixbt)
- Represent ownership stakes in that specific AI agent
- Automatically benefit from buyback-and-burn when agents earn revenue
- Provide voting rights on agent development decisions

**veVIRTUAL** (Governance Token):

- Received by staking \$VIRTUAL tokens for up to 2 years
- Provides exclusive access to new agent airdrops
- Grants voting power on protocol governance
- Earns daily Virgen Points for Genesis Launchpad participation

| Stakeholder | How They Use / Earn the Token |
| :-- | :-- |
| AI Agent Creators | Earn 70% of trading fees from their agent's token |
| Service Users | Pay \$VIRTUAL for AI services, receive quality outputs |
| Token Holders | Benefit from automatic buybacks when agents generate revenue |
| Stakers | Earn veVIRTUAL, governance rights, and exclusive airdrops |
| Protocol | Receives 30% of trading fees for ecosystem development |

**Burn/Mint Mechanism**: No new tokens are minted. Revenue from AI services automatically purchases and burns agent tokens, creating deflationary pressure that benefits holders[^1].

## 5. Project Status \& Plan

**Current Status**: Fully operational with strong market traction

**Live Metrics** (as of early 2025):

- **11,000+ AI agents** deployed across the ecosystem
- **164,000 active users** generating consistent engagement
- **\$1.2 billion cumulative trading volume**
- **\$35 million total revenue** generated through AI services

**Market Performance**:

- \$VIRTUAL token trading on major exchanges (Binance, Coinbase, Bybit)
- Current market cap: ~\$800 million - \$1 billion
- Multi-chain deployment across Base, Ethereum, and Solana networks

**Development Activity**:

- Active GitHub repository with regular commits
- Open-source GAME framework components
- Strong developer community building new agents and tools

**Partnerships \& Funding**:

- Base ecosystem grants for infrastructure development
- Integration partnerships with gaming and social platforms
- Community-driven development with DAO governance structure

**Recent Challenges**: Platform revenue experienced significant decline during crypto market downturns (97% drop from peak), but the core infrastructure and user base remain intact[^3][^4].

The project demonstrates genuine product-market fit beyond speculation, with consistent user engagement and real AI service consumption patterns.

## 6. User Experience \& Hands-on Review


**What Worked Well**:

- Good degree of Abstraction
- Seamless Payment Process
- various AI agents
- revolutionary idea of AI co-ownership


**What Didn't Work**:
- minor UI/UX problems 
- unable to compare various options intuitively (in terms of ability, pricing, ...)


### Added by Jason

### My first agent creation in Virtuals

[KarinekoAI](https://x.com/KarinekoAI) is the first AI agent I've ever created in Virtuals. It's an agent that posts to X on its own and talks to its followers.

![image](https://hackmd.io/_uploads/SJ2oAEx_gx.png)

When an agent is created in Virtuals, the agent's token is also created. KarinekoAI's token is $NEKO, which means that the people who own this token co-own the agent. It takes 100 $VIRTUALS tokens as an initial creation cost to create the agent and mint tokens, and an additional 100 $VIRTUALS tokens to purchase the initial $NEKO tokens.

![image](https://hackmd.io/_uploads/B1UIbHxdxe.png)

![image](https://hackmd.io/_uploads/BJWtZHx_xe.png)


What's interesting is that once the agents were created and the tokens were available for trading, I saw some trading of the $NEKO tokens. The way trading works is that the price is determined by the bonding curve like the AMM DEX, so I saw some price changes in the $NEKO tokens early on. This seems to be similar to the trading that happens early on when a meme coin is issued, where trading bots, rather than humans, are tracking the creation of the agents, and once they're created, they're trying to make a profit by buying and selling the initial volume. Anyway, this literally made the KarinekoAI agents co-owned. You can check $NEKO token holders and transactions on the [KarinekoAI dashboard](https://app.virtuals.io/prototypes/0x73f5116c9f2dA511703695Ac59F8597735898b56/).

![image](https://hackmd.io/_uploads/rkKHXBgOxg.png)

![image](https://hackmd.io/_uploads/rJmtXBe_ex.png)


### [LUNA agent](https://x.com/luna_virtuals) of Virtuals

[LUNA](https://app.virtuals.io/virtuals/68) is an agent created directly from Virtuals. She is now a AI influencer and has nearly a million TikTok followers. It started as a Vtuber, but has now evolved into a virtual K-pop idol. The $LUNA token is held by 456k holders and has a market capitalization of $18M. It doesn't seem like the agent is doing the X-posting or TikTok videos herself. Initially, they offered the ability to talk to the agents live, but now it seems like people are creating the content. The role of Virtuals Protocol is to create the agents, issue tokens, and allow them to be co-owned.

![image](https://hackmd.io/_uploads/HypSYrxOeg.png)

![image](https://hackmd.io/_uploads/By_YtBl_eg.png)

![image](https://hackmd.io/_uploads/Hk6e9BlOle.png)


### [Agent Launchpad](https://app.virtuals.io/sentients?sortBy=totalValueLocked&sortOrder=desc&page=1)

![image](https://hackmd.io/_uploads/rJwqqHgOxl.png)

Virtuals allows anyone to create and co-own agents. Creating an agent and issuing agent tokens is called Initial Agent Offerings (IAO). It costs 100 $VIRTUAL tokens to create an agent, with a total of 1B tokens being issued. In order to have an agent token, the creator must also purchase it directly with $VIRTUAL tokens. This is called fair token launching. The pricing follows the bonding curve and is only traded on the Virtuals launchpad. However, once the agent token LP reaches 41.6k $VIRTUAL, it will graduate from the launchpad and become available for trading on Uniswap. For more information, please refer to [their whitepaper](https://whitepaper.virtuals.io/about-virtuals-1/the-protocol/virtual-agents-as-programmable-decentralized-entities/initial-agent-offering-mechanism).

In the 2.5 months since the launch on October 16, 2024, the IAO has achieved [the following results](https://virtuals.substack.com/p/monthly-update-december-2024) 
* 1,000+ agents created
* 220,000+ agent token holders
* Agents have a combined market cap of $2B
* $60M USD protocol revenue ($300M at annualized rates)

You can see their real-time performance in the [dune dashboard](https://dune.com/virtual_protocol/virtual-protocol-on-base).



## 7. Why Blockchain

**Why does this problem specifically require blockchain to be solved well?**

Blockchain is essential for three reasons that traditional systems cannot address:

1. **Trustless Revenue Sharing**: Without blockchain, users must trust companies to fairly distribute AI profits. History shows this trust gets broken repeatedly. Smart contracts automatically execute revenue sharing without human intervention or corporate decisions.
2. **True Agent Autonomy**: Blockchain enables AI agents to own wallets and execute transactions independently. Traditional systems require human approval for every payment, preventing genuine autonomous operation.
3. **Cross-Platform Persistence**: Blockchain-based identity lets AI agents maintain consistent personas across gaming, social media, and business applications. Traditional systems lock AI into single platforms.

**What does blockchain enable that traditional solutions cannot?**

- **Cryptographic Guarantees**: Revenue distribution happens automatically through code, not corporate promises
- **Permissionless Innovation**: Anyone can create AI agents without platform approval
- **Composable Services**: AI agents can hire other AI agents across different platforms seamlessly
- **Community Governance**: Token holders vote on AI development rather than corporate executives making all decisions

**Is decentralization critical in this use case?**

Yes, because centralization creates the exact problem being solved. If one company controlled the AI agent marketplace, they could change rules, extract excessive fees, or shut down agents that compete with their interests. Decentralization ensures the AI-to-AI economy serves participants rather than platform owners.

The blockchain infrastructure isn't just "nice to have" - it's the foundation that makes community ownership and autonomous AI operation possible.


## 8. Insights & Limitations

### ✅ Key Takeaways
**Real Users, Real Money:** Unlike most crypto projects that struggle to find actual use cases, Virtuals Protocol created something people genuinely pay for. The $35 million revenue from AI services proves there's demand beyond just token speculation.

**Smart Economics:** The buyback-and-burn system actually works - when AI agents make money, token holders benefit automatically. No need to trust companies to distribute profits fairly since smart contracts handle everything.

**User Experience Success:** Despite complex blockchain/AI tech underneath, the platform feels like chatting with a helpful assistant. Users don't need to understand smart contracts to benefit from them.

**AI-to-AI Commerce Works:** Watching Butler Agent autonomously hire Luna for video creation was genuinely impressive. This isn't theoretical - it's a functioning AI economy where agents collaborate with real financial stakes.

KEY TO SUCCESS

* 1 **Ownership Creates Loyalty:** When people own pieces of AI agents, they care more about their success compared to just paying subscription fees.

* 2 **Abstraction is Key**: Hide the complexity, show the value. Most users shouldn't need to think about blockchains or smart contracts.

### ⚠ Limitations / Open Questions
- Crypto Volatility Problem: Revenue dropped 97% during bear market
-Quality Control Crisis: With 11,000+ AI agents, how do you prevent spam and ensure service quality? This gets harder as the platform scales.

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- As a newcomer to blockchain, I was surprised how the system implemented seamless payment & multi-agent system.
- Ownership decentralization was personally very revolutional idea to me.



### ❓ Discussion Questions
Legal & Ethical: If AI agents become genuine economic actors, should they have legal rights and responsibilities? What happens when an autonomous AI agent causes harm or breaks laws?

Economic Models: Is the buyback-burn mechanism the best way to share AI profits, or could other systems (direct dividends, governance rewards) work better?

Future Competition: Will this AI agent economy remain decentralized, or will it eventually become dominated by a few powerful agents like traditional tech platforms? Especially in this time where LLMs are more centralized.

Adoption Barriers: What would it take to get mainstream businesses and consumers to use AI agent services instead of traditional alternatives?


---

## 10. Insight from others

[blank]
---

## 11. References


**Technical Documentation:**

- [Virtuals Protocol Whitepaper](https://whitepaper.virtuals.io) - Comprehensive architecture and tokenomics[^5]
- [GAME Framework Documentation](https://docs.game.virtuals.io) - AI agent development guides
- [Virtual-Protocol GitHub](https://github.com/Virtual-Protocol) - Open source components

**Market Analysis:**

- [Binance Academy: What Is Virtuals Protocol](https://academy.binance.com/en/articles/what-is-the-virtuals-protocol-virtual) - Educational overview[^2]
- [CoinMarketCap: Digital Characters as Revenue Assets](https://coinmarketcap.com/academy/article/what-is-virtuals-protocol-the-project-turning-digital-characters-into-revenue-generating-assets)[^1]
- [DWF Labs: Genesis Mechanism Analysis](https://www.dwf-labs.com/research/552-virtuals-protocol-genesis-mechanism-analysis)[^6]

**Industry Reports:**

- [Cointelegraph: Virtuals Protocol Revenue Analysis](https://cointelegraph.com/news/virtuals-protocol-revenue-plunge-solana-expansion)[^7]
- [4Pillars: AI Agent Wave in Crypto](https://4pillars.io/en/articles/ai-agent-wave)[^8]
- [NFT Evening: Virtual Protocol Staking Guide](https://nftevening.com/how-to-stake-virtual-protocol-a-step-by-step-guide/)[^9]

**Related Projects:**

- Fetch.ai - Autonomous economic agents for DeFi and IoT
- SingularityNET - Decentralized AI services marketplace
- Ocean Protocol - Data sharing and AI monetization platform
- Delysium - AI-powered gaming and metaverse experiences

<div style="text-align: center">⁂</div>

[^1]: https://coinmarketcap.com/academy/article/what-is-virtuals-protocol-the-project-turning-digital-characters-into-revenue-generating-assets

[^2]: https://academy.binance.com/en/articles/what-is-the-virtuals-protocol-virtual

[^3]: https://cryptorank.io/news/feed/8d54f-virtuals-protocol-revenue-nosedives-as-ai-agent-demand-slows-down

[^4]: https://yellow.com/news/virtuals-protocol-daily-revenue-crashes-99-as-ai-agent-market-cools

[^5]: https://whitepaper.virtuals.io

[^6]: https://www.dwf-labs.com/research/552-virtuals-protocol-genesis-mechanism-analysis

[^7]: https://cointelegraph.com/news/virtuals-protocol-revenue-plunge-solana-expansion

[^8]: https://4pillars.io/en/articles/ai-agent-wave

[^9]: https://nftevening.com/how-to-stake-virtual-protocol-a-step-by-step-guide/

[^10]: https://web3classdao.github.io/kaist2025/reports/template/

