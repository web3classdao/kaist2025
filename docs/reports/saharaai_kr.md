# 📄 Sahara AI  
- 👤 Author: 20220093 / Moonjung Kim
- 📆 Presentation Date: [2025-07-16]  


## 1. Overview

- **Project Name**: Sahara AI
- **Category**: Decentralized AI Infrastructure
- **Key Technologies / Platforms**: Sahara AI
- **Official Links**:
    - [Website](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)
    - [Foundation](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)
    - [Contract Address](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)
    - [Whitepaper](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)
    - [Docs](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)
    - [GitHub](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)
    - [X](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)
    - [Discord](https://www.notion.so/SAHARA-23131918757480838c40ea17a9fe5e31?pvs=21)

### 📌 Summary

The Decentralized Blockchain Platform for an transparent and collaborative AI economy. Sahara tokenizes contributions at every stage of AI development and distributes the profit to all contributors.

---

## 2. Background & Problem Statement

### Current state of AI development

AI development is heavily resource-intensive, requiring vast amounts of training data, powerful infrastructure, and sophisticated models. As a result, the field is largely dominated by big tech companies that can afford these demands. This concentration of power makes it extremely difficult for small teams to develop competitive AI models or receive recognition and funding for their contributions. Furthermore, the individuals and communities who generate the training data are rarely acknowledged or compensated, raising concerns about fairness and equity in the AI ecosystem.

---

## 3. How It Works

### 🔍 3.1 Project Approach



The core idea is to tokenize every stage of AI development—including primary datasets, trained models, pipelines, and fine-tuning efforts. Each contribution, whether it's data, computing power, or technical expertise, is represented as a tokenized asset and rewarded accordingly. By leveraging smart contracts and on-chain infrastructure, rewards can be distributed automatically, ensuring fair compensation for all participants. 

---

### 🏗️ 3.2 Architecture

![image.png](attachment:6e4543b9-3634-414c-8aa2-99aa9a8908f7:image.png)

- **Application layer:**  tools like marketplaces, developer toolkits, and user-created AI agents can be used by ai developers and users.
- T**ransaction layer:** powered by the Sahara blockchain, where smart contracts handle licensing, ownership, and automatic reward distribution.
- **Data layer:** keeps large assets such as models and datasets off-chain, while storing metadata on-chain for transparency and traceability.
- **Execution layer:** handles AI computation tasks, including model training and inference, enabling distributed processing across the network.

---

### 🎯 3.3 Core Components

- **Sahara blockchain:** records transactions, ownership, and individual contributions on-chain, ensuring transparency and traceability.
- **AI infrastructure:** enables the sharing of computing resources, helping to democratize access to processing power traditionally monopolized by large tech firms.
- **Sahara AI Marketplace:** users can sell or share AI models, datasets, and agents. Smart contracts govern licensing and automate payments, ensuring that all contributors are fairly and transparently rewarded.

![스크린샷 2025-07-16 030718](https://hackmd.io/_uploads/r1ZqPcNIgx.png)


---

### 🔁 3.4 Workflow Overview



1. Users tokenize their contribution (primary data, data labeling, architecture, fine-tuning, pipelining, etc.)
2. Set license and monetization policy and register onchain
3. Share AI assets on Sahara AI marketplace
4. Customers can use AI agents, models, datasets
5. Profit is distributed through smart contracts

---

## 4. Token Economy *(if applicable)*

$SAHARA is launched on Jun 24, 2025

![image](https://hackmd.io/_uploads/SyAiL5ELel.png)


$SAHARA is the utility token that powers all interactions in the Sahara AI ecosystem.

- Earn $SAHARA by contributing data, models, ir compute power
- Pay for datasets, models and compute power
- Pay for transaction fee on the network
- Participate in governance decisions with $SAHARA

---

## 5. Project Status & Plan

Funding: Series A, 43mil dollars

Discord 386,051 Members

Sahara AI x account has 869k followers


![스크린샷 2025-07-16 112106](https://hackmd.io/_uploads/Hkn2w5E8lg.png)


Mainnet is still in development, and only the testnet is open 

AI Marketplace is open

- available: upload data, build AI agent
- future plans: monetization of AI assets, AI agent market, deploying AI agent

Currently, there are 1-2 commits per week on their public repositories.

---

## 6. User Experience & Hands-on Review *(if applicable)*

### Uploading a dataset

![스크린샷 2025-07-16 090633](https://hackmd.io/_uploads/SyiR95NUex.png)



I tried uploading a text data onchain and get a token. For now, Sahara marketplace only allows text format data.

![스크린샷 2025-07-15 231442](https://hackmd.io/_uploads/Byngs9V8xg.png)


By uploading the data, I could receive a ERC721 token.

![스크린샷 2025-07-16 091353](https://hackmd.io/_uploads/H1hZjcNUex.png)


I did not had any $SAHARA, so I could not pay the gas fee to register by token onchain.

![스크린샷 2025-07-16 123218](https://hackmd.io/_uploads/HyAPa5NLgx.png)


This is an example of your digital asset, according to the documentation.

![스크린샷 2025-07-16 091500](https://hackmd.io/_uploads/BykH2cE8xg.png)


Instead, I did another experiment and made a file size 1000 times and uploaded a 11MB file and tried to register it. According to the architecture, the data itself should be stored off-chain and only the metadata is stored on-chain. We could see that the transaction fee is same as before even though the file size is 1000 times bigger.

![스크린샷 2025-07-16 091138](https://hackmd.io/_uploads/HkJUn9EIll.png)


I also tried uploading a 421MB file, but the system rejected it. It seems the platform isn't designed to handle large dataset uploads.

### creating a new AI agent

According to the documentation, Sahara provides no-code AI agent toolkit for non-developers. 

![스크린샷 2025-07-16 085812](https://hackmd.io/_uploads/S1ru25NLge.png)


I created my AI agent by using an AI model I got from Sahara marketplace and added instructions. Users can test their AI agent during the creation.

![스크린샷 2025-07-16 090127](https://hackmd.io/_uploads/SJMK39VLle.png)


The system encapsulate the details of a smart contract and allows to click and select license type and co-ownership.

![스크린샷 2025-07-16 090252](https://hackmd.io/_uploads/r1jqn5ELge.png)

I could not register because I did’t had the gas fee to register, but according to the documentation, you can deploy your ai agent as serverless provider and have a API endpoint.

### Sahara Legends

Sahara Legends is a gaming system that rewards data validators. 

![스크린샷 2025-07-16 014822](https://hackmd.io/_uploads/Byoohq4Leg.png)

It has a game-like UI and gives validating tasks as a quest. Data validators gets NFTs and shards as a reward.


![스크린샷 2025-07-16 014705](https://hackmd.io/_uploads/BJrhh5NLll.png)

---

## 7. Why Blockchain

The AI space today is dominated by a few large companies, with most of the profits captured by existing Web2 platforms. This centralization also leads to a lack of transparency. It's often unclear how AI models are trained or what data they’re trained on. Even when the project is open-source, the training method and the dataset is often not disclosed.

In contrast, Web3 offers a decentralized alternative where no central authority is needed. Anyone can contribute and receive their fair share. With blockchain technology, transparency is built-in: datasets, model creators, and every modification can be recorded and verified on-chain.

---

## 8. Insights & Limitations

### ✅ Key Takeaways

- **Paradigm Shift in AI Development**: Sahara introduces a new model for AI development that is transparent, collaborative, and powered by Web3 technology.
- **Built-in Licensing & Monetization**: By tokenizing every AI asset, Sahara enables permissionless development through programmable smart contracts that ensure fair licensing and revenue distribution.
- **Community-Driven Ecosystem**: A core focus of the project is building an inclusive community not just developers, but also data contributors and AI users. Significant effort has been made to create an ecosystem for all participants.

### ⚠ Limitations / Open Questions

- **Legal Risks Around Data**: What mechanisms are in place to prevent the registration and monetization of copyrighted or stolen data? How can the system ensure that only legitimate data is rewarded?
- **Transaction Costs**: For casual users, the need to pay transaction fees might be a barrier to participation.
- **Performance of Decentralized AI Infrastructure**: Can decentralized compute networks realistically compete with centralized GPU clouds?

---

## 9. Reflections & Discussion

### 💡 Personal Reflections

I’ve often been skeptical of Web3 applications, as many of them seem like they could easily be built using Web2 infrastructure. However, Sahara makes a lot of sense to migrate to Web3. If a Web2 version of Sahara were to succeed, it would likely evolve into yet another centralized tech giant. By building on Web3, Sahara aligns better with its goals of transparency, decentralization, and equitable value distribution.

### ❓ Discussion Questions

- When digital data is tokenized into assets, how do we address the issue of ownership? How can we verify that someone is the legitimate owner of the data they're tokenizing?
- Will we need to tokenize every piece of content(posts, comments, images) before it's published online to ensure provenance and ownership?
- What systems or standards can be put in place to prevent false claims and protect original creators in a decentralized environment?

---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

- [Overview | Sahara Documentation](https://docs.saharalabs.ai/)
- [What Is Sahara AI (SAHARA)?](https://academy.binance.com/en/articles/what-is-sahara-ai)
- [Sahara Testnet blockchain explorer - View Sahara Testnet stats | Sahara AI](https://testnet-explorer.saharalabs.ai/)
- [Sahara AI Litepaper](https://saharaai.com/learn/litepaper)
- [Developer Platform](https://app.saharaai.com/developer-platform/main/explore)
- [Decentralizing AI, Data Ownership & the Future of AI w/ Sahara AI | Blockchain Interviews](https://www.youtube.com/watch?v=ZQvWfecXOUw)
- [Intro to Sahara AI: The Blockchain Built for AI](https://www.youtube.com/watch?v=nWeYj--1fH8)