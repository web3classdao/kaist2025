# 📄 [Bittensor($TAO)]  
- 👤 Author: [20210456 / Lee Sangbum](Link to your profile)
- 📆 Presentation Date: [2025-07-16]  

---

## 1. Overview

- **Project Name**:  Bittensor($TAO)
- **Category**: Decentralized AI Infrastructure
- **Key Technologies / Platforms**: Decentralized Machine Learning, Proof of Intelligence (PoI) Consensus, Peer-to-Peer AI Network
- **Official Links**:
  - [Website](https://bittensor.com/) 
  - [Whitepaper](https://bittensor.com/whitepaper)
  - [Docs](https://docs.learnbittensor.org/)
  - [GitHub](https://github.com/opentensor/bittensor) 
  - [X](https://x.com/bittensor_)
  - [Discord](https://discord.com/invite/bittensor)


### 📌 Summary  
Bittensor is a development community where a large number of people are participating in evolving AI through mutual feedback systems that advance AI models and evaluate them.

---

## 2. Background & Problem Statement 

### • Limitations of Centralized AI Approaches 

Companies such as Google, OpenAI, and Meta collect vast amounts of data through web crawling, partnerships, and their own services. This data is stored in private data centers and is not accessible to the public. Training AI models requires immense computational power, typically provided by server farms equipped with thousands or even tens of thousands of GPUs or TPUs.

As a result, AI development has a very high entry barrier for most individuals and smaller companies. Users have little visibility into how their data is used, and since AI models are trained on datasets curated by these companies, there is a risk of bias in the resulting models.

As AI becomes more powerful and influences our entire lives, if a few companies monopolize it, they can use AI as a power. Monopoly of AI infrastructure can cause social problems such as imbalances in information access, data and privacy issues, threats of censorship and bias, and concentration of power.

### • Waste of Power due to Meaningless Computation
Traditional Proof of Work (PoW), as used in Bitcoin and early Ethereum, consumes enormous amounts of energy to solve arbitrary cryptographic puzzles that have no real-world value beyond securing the network. This leads to massive environmental costs and wasted computational resources. Proof of Stake (PoS) attempts to address energy inefficiency but shifts power toward wealth concentration, as those with more tokens gain disproportionate control over block validation. Both systems ultimately lack a mechanism for producing useful outputs beyond consensus.

### • Bittensor's Approach to AI through Blockchain

Bittensor is trying to address centralization and accessibility limitations in AI development. It towards diversity, transparency, and gives many people opportunities to participate to drive the development of AI.

To induce participation, Bittensor introduces Proof of Intelligence (PoI), a consensus mechanism designed to reward participants not for arbitrary work or token holdings, but for contributing valuable AI model outputs. Bittensor's philosophy makes Miner's operation, which consumes power, meaningful in reality.

Bittensor differentiates itself from traditional centralized AI systems by leveraging blockchain technology to decentralize and transparently record AI model operations, performance evaluations, and reward distributions in a trustless and automated manner.

---

## 3. How It Works

### 🔍 3.1 Introduction 
#### • How to solve the problem? 

Bittensor decentralizes AI model training and inference by creating an open, blockchain-based network where anyone can contribute models and receive rewards. This structure removes the dependency on centralized corporations and democratizes access to AI technology.

| Category | Traditional AI Companies | Bittensor |
| --------------------------- | ---------------------------------------- | ---------------------------------------- |
| **Data Collection**         | Exclusive, Private                       | Decentralized, Open Participation        |
| **Computing Resources**     | Centralized Server Farms                 | Globally Distributed Individual Hardware |
| **AI Model Operation**      | Closed, Internal Only                    | Open and Decentralized on the Network    |
| **Reward Structure**        | Company-Centric Profit                   | Contributor-Centric (TAO Token Rewards)  |
| **Transparency**            | Low                                      | High (Blockchain-Based)                  |
| **Accessibility**           | High Entry Barrier                       | Open to Anyone (with Some Conditions)    |
| **AI Technology Ownership** | Concentrated in a Few Large Corporations | Decentralized Network, Shared Ownership  |


#### • What is the **core idea** behind the solution?

The core idea is a peer-to-peer machine learning network powered by blockchain. Participants run machine learning models as nodes, respond to requests from other users, and get rewarded in TAO tokens based on the quality and usefulness of their outputs.

---

### 🏗️ 3.2 Architecture  
#### • High-Level Overview of the System Architecture
![bittensor-block-diagram](https://hackmd.io/_uploads/BkQtOAJIgx.svg)

The following roles define the ways to participate in Bittensor:

**Miners**
- Miners work to produce digital commodities by running AI models that generate responses to queries.
- Their outputs are evaluated for quality and usefulness by validators. High-performing miners are rewarded in TAO tokens according to their contribution to the network.

**Validators**
- Validators evaluate the quality of miners’ outputs. They assign performance scores that determine how much reward each miner receives.
- Validators play a key role in maintaining the integrity and fairness of the network by ensuring only valuable contributions are rewarded.

**Subnet Creators**
- Subnet creators design and manage subnet-specific incentive mechanisms. They define the type of work miners should perform and how validators should evaluate that work.
- They enable customization within the Bittensor ecosystem by creating specialized AI tasks and reward structures.

**Stakers**
- Stakers are TAO token holders who support specific validators by staking their tokens. By staking, they contribute to validator credibility and may receive a portion of the validator’s rewards.
- Staking allows TAO holders to participate in the network’s governance and reward distribution without running a miner or validator node themselves.


---

### 🎯 3.3 Core Components  
**Subtensor Blockchain**

Subtensor Blockchain serves as the foundational ledger of the Bittensor network. It records miner performance scores, validator assessments, staking data, and reward distributions in an immutable and transparent way. By leveraging blockchain technology, Subtensor ensures that no single party can manipulate contributions or payouts. It functions as both the governance layer and the reward settlement system for all AI-related activities within the Bittensor ecosystem.

**Validator Score Mediator: Yuma Consensus**

Yuma Consensus is the core mechanism within Bittensor that mediates and finalizes the weight scores assigned by validators to miners. While individual validators assess the quality of AI responses from miners, there needs to be a reliable way to aggregate these scores in a trustless and decentralized environment. Yuma Consensus collects scores from all validators, adjusts for inconsistencies, filters out malicious or unreliable inputs, and produces a unified, tamper-proof ranking that is recorded on the Subtensor blockchain. This ensures fairness, prevents Sybil attacks, and maintains the integrity of the reward distribution system across the network.

**Subnet Mechanism**

The Subnet Mechanism allows Bittensor to support diverse AI tasks by segmenting the network into independent subnets. Each subnet can define its own incentive structure, evaluation logic, and AI modality, such as chatbots, code generation, or financial prediction. This modular architecture enables specialized AI development while maintaining a unified token economy and consensus layer across the entire network.

**Wallet System: Coldkey and Hotkey**
The Wallet System manages cryptographic identities within Bittensor through coldkeys and hotkeys. Coldkeys hold long-term ownership rights and staking records, while hotkeys handle active network participation such as mining and validation. This dual-key structure enhances security by separating long-term assets from operational activities.

---

### 🔁 3.4 Workflow Overview  
![20231002_101709-1024x576](https://hackmd.io/_uploads/BkjDx4bLle.jpg)
[Source from tao.news]

**Step 1:**
A user submits a query to the Bittensor network, requesting an AI-generated response.

**Step 2:**
The query is forwarded to multiple miners (model nodes), which generate and return answers.

**Step 3:**
Validators assess the quality of the miners' responses and assign performance scores.

**Step 4:**
Subtensor blockchain records performance scores, calculates rewards, and distributes TAO tokens to miners and validators.

**Step 5:**
Users receive the AI-generated answers, and the ecosystem updates its weight and reward records transparently.



> *(You may include a diagram or link to an official architecture diagram if helpful.)*

---

## 4. Token Economy

> *Include this section **only if the project has its own token.***  

### [• TAO Status](https://taostats.io/)
![image](https://hackmd.io/_uploads/H1Z_p01Uxg.png)
![image](https://hackmd.io/_uploads/HkT_TAkIex.png)
TAO's market cap is approximately $3.59 billion. Each token is approximately $380. The total estimated issue is 21 million TAO, and the current circulation is approximately 9.39 million TAO.

Bittensor’s TAO token operates on a continuous issuance model designed to reward network participants, with no fixed supply cap but a controlled inflation rate that decreases over time. Tokens are minted automatically based on the performance evaluations of miners and validators, recorded on the blockchain. While there is no formal burn mechanism, certain network activities like subnet creation may have a partial burn or token lockup effect. TAO allocated to early contributors and investors follows a vesting schedule of 18 to 36 months, whereas rewards earned by miners and validators are immediately liquid without any lock-up period.

### • Use of TAO

| Stakeholder      | How They Use / Earn TAO                                 |
|------------------|--------------------------------------------------------|
| Miner            | Earns TAO by providing high-quality AI model responses |
| Validator        | Earns TAO by evaluating miners' responses              |
| Subnet Creator   | Pays TAO to create and manage a subnet                 |
| Staker           | Stakes TAO to validators and earns a portion of rewards |

---

## 5. Project Status & Plan
### Project Status: ###
Bittensor is live on mainnet. There are more than 118 activated subnets. It has an active ecosystem of miners, validators, and subnet creators operating globally.

### Community & Developer Base: ###
There is an active developer community with consistent discussions on Discord, GitHub contributions, and subnet experimentation. More than 60 official repositories on GitHub are actively managed, and the number of weekly commitments by developers is maintained continuously.

### Partnerships & Funding: ###
Bittensor is self-bootstrapped but has gained organic traction. No major corporate partnerships have been formally announced as of mid-2025, but community-driven subnet projects are growing.

### Open Source: ###
Yes. Bittensor’s core components, including Subtensor blockchain code, are available on GitHub. The repository shows regular updates and community pull requests.

### Token Listing & Market Activity: ###
TAO is listed on several decentralized and centralized exchanges, such as Binance, Coinbase, Kraken, and Uniswap. TAO has increased in value per unit by about 47% over the year.

**Bittensor is not a simple concept or event project, but a working ecosystem.**

---

## 6. User Experience & Hands-on Review
### Participating in TAO Mining on Testnet
> *Attention : This project does not encourage readers to participate in mining or invest in TAO. This was done for the purpose of helping understand the Bittensor system. You are responsible for all investments and decisions.*

The purpose of this experiment is to understand the **decentralized AI network** structure throughout the reward mechanism. It directly observes how **miners** provide AI models, **validators** evaluate the quality of responses, and token rewards are generated as a result, gaining hands-on experience with key concepts such as staking, the metagraph, and the relationship between validation and mining.


> **Experiment Setup Summary**
> 
> **1️⃣ GPU Specification**
> • NVIDIA RTX 3060 Ti (GDDR6 8GB VRAM)
> 
> **2️⃣ LLM Used**
> • Mistral-7B-Instruct-v0.1 (4-bit quantized)
> 
> **3️⃣ System Environment**  
> • OS: Ubuntu 24.04 LTS (WLS environment)  
> • Main Libraries & Tools: Python 3.10.18, CUDA Toolkit, Bittensor

### Step 0. Install CUDA Driver
Install the appropriate CUDA driver for your OS. In this experiment, WLS2 based on Windows 11 was used.

Check if CUDA driver is successfully installed
```bash
nvcc --version
nvidia-smi
```

### Step 1. Prepare a Bittensor SDK

• Create Virtual Environment
```bash
sudo apt update && sudo apt install python3-venv -y
python3 -m venv ~/taominervenv
source ~/taominervenv/bin/activate
```

• Clone Bittensor
```bash
git clone https://github.com/opentensor/bittensor.git
cd bittensor
pip install -e .
```

• Create Bittensor Wallet
```bash
btcli wallet new --name tao1
```
![image](https://hackmd.io/_uploads/BygGuKASeg.png)
Determine your wallet name and hotkey.
The number of words can be set freely from 12 to 24.

![image](https://hackmd.io/_uploads/rJiiOFASel.png)
These words are called **Mnemonic Phrase**. User can recover all the keys including coldkey and hotkey by using phrases. Keep these safe from exposure to others.


The directory where your wallet is stored is
~/.bittensor/wallets/<WALLET_NAME>/<HOTKEY_NAME>

• Check Wallet Coldkey Address and The Balance
```bash
btcli wallet overview --wallet.name tao1
```
![image](https://hackmd.io/_uploads/ryqiUtRBgl.png)

### Step 2. Test Your LLM in Local(Optional)
Ask a locally installed LLM to make sure it provides the correct answer. This process is necessary when tuning the model or prompting it to satisfy the answer conditions required by subnet.


Install essential packages
``` bash
pip install --upgrade pip
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip install transformers accelerate bitsandbytes sentencepiece
pip install bittensor
```


Save the script to the directory as below
```
~/mistral_test
├── miner.py
└── mistral_runner.py
```

mistral_runner.py
```python=
from transformers import AutoConfig, AutoTokenizer, AutoModelForCausalLM, BitsAndBytesConfig
import torch

# Model identifier to load
model_id = "mistralai/Mistral-7B-Instruct-v0.1"

# Configure 4-bit NF4 quantization
quant_config = BitsAndBytesConfig(
    load_in_4bit=True,                      # Enable 4-bit loading
    bnb_4bit_compute_dtype = torch.float16,  # Compute in float16
    bnb_4bit_use_double_quant = True,       # Use double quantization
    bnb_4bit_quant_type = "nf4"           # Use NF4 quantization type
)

# Load custom Mistral config, trusting remote code
config = AutoConfig.from_pretrained(
    model_id,
    trust_remote_code=True
)

# Load a slow (SentencePiece) tokenizer, trusting remote code
tokenizer = AutoTokenizer.from_pretrained(
    model_id,
    use_fast=False,
    trust_remote_code=True
)

# Load the model with quantization and custom config
model = AutoModelForCausalLM.from_pretrained(
    model_id,
    config=config,
    device_map="auto",               # Automatically map layers to devices
    quantization_config=quant_config,
    torch_dtype=torch.float16,
    trust_remote_code=True
)

# Encodes the given prompt, generates an output response from the model
def generate_response(prompt: str) -> str:
    # 1) Tokenize and send inputs to the model's device
    inputs = tokenizer(prompt, return_tensors="pt").to(model.device)
    # 2) Generate up to 128 new tokens
    outputs = model.generate(
        **inputs,
        max_new_tokens=128,
        pad_token_id=tokenizer.eos_token_id
    )
    # 3) Decode generated tokens into text
    return tokenizer.decode(outputs[0], skip_special_tokens=True)
```
miner. py
```python=
from mistral_runner import generate_response

def main():
    print("Mistral Prompt Test ")
    print("Input('exit' to quit): \n")

    while True:
        prompt = input(">>> ")
        if prompt.lower() in ["exit"]:
            print("Test Ended")
            break
        response = generate_response(prompt)
        print(f"\n{response}\n")

if __name__ == "__main__":
    main()
```

Execute Mistral
```bash
python miner.py
```
![image](https://hackmd.io/_uploads/BkwnqGZIxl.png)



### Step 3. Scripting for AI Model Application and Execution
• Clone text-prompting
```bash
git clone https://github.com/opentensor/text-prompting
cd text-prompting
```

• Install Requried Packages
```bash
pip install -e .
```
• Scripting
You can use mistral_runner.py tuned in Step 2. You can still use the mistral_runner.py tuned in Step 2. However, miner. py should be modified it to get questions from the server.

miner. py
```python=
import argparse
import bittensor as bt
from prompting.protocol import Prompting
from prompting.mistral_runner import generate_response
from prompting.baseminer.miner import Miner

class MistralMiner(Miner):
    @classmethod
    def add_args(cls, parser: argparse.ArgumentParser):
        super().add_args(parser)

    def config(self) -> "bt.Config":
        parser = argparse.ArgumentParser(description="Mistral Miner Configs")
        self.add_args(parser)
        return bt.config(parser)

    def prompt(self, synapse: Prompting) -> Prompting:
        bt.logging.debug(f"Prompt => {synapse.prompt}")
        synapse.completion = generate_response(synapse.prompt)
        return synapse

if __name__ == "__main__":
    # Run the miner
    MistralMiner().run()
```

Save the script to the directory as below
```
~/text-prompting/
├── prompting/
│   └── mistral_runner.py      ← Prepare for mistralai/Mistral-7B-Instruct-v0.1
└── neurons/
    └── miners/
        └── template/
            └── miner.py       ← Respond to incoming requests from Bittensor network
```

```
~/bittensor-subnet-template
├── neurons
│   ├── miner.py
│   └── mistral_runner.py
```

### Step 4. Start Mining on Testnet
Before mining, you need to stake a certain amount of TAO in the chain. In Testnet, you have to pay a test TAO that has no real value, which can be obtained by requesting it on the Bitensor official [Discord](https://discord.com/invite/bittensor) channel.



• Register wallet hotkey into testnet netuid 171
```bash
btcli subnet register --wallet.name tao1 --wallet.hotkey miner1 --subtensor.network test --netuid 171
```
 This requires paying 0.0005 tTAO.
![image](https://hackmd.io/_uploads/BkozX_1Ige.png)

• Stake a certain amount of TAO in the chain
```bash
btcli stake add --wallet.name tao1 --wallet.hotkey miner1 --amount 0.0050 --subtensor.network test --netuid 171
```
![image](https://hackmd.io/_uploads/ByNSVd18ge.png)

• Start mining on testnet 171
```bash
cd ~/text-prompting

python -m neurons.miners.template.miner \
  --wallet.name tao1 \
  --wallet.hotkey miner1 \
  --subtensor.network test \
  --subtensor.chain_endpoint wss://test.finney.opentensor.ai:443 \
  --netuid 171 \
  --logging.debug \
  --set_weights False
```



---

## 7. Why Blockchain

- Why **does this problem specifically require blockchain** to be solved well?  

Bittensor aims to create an opened, fair, and incentive-driven marketplace for AI models. This requires a transparent and immutable system for recording model performance, distributing rewards, and managing ownership. Blockchain provides the necessary trust layer without relying on a central authority.
- What does blockchain enable that traditional solutions cannot?  

Traditional AI platforms rely on centralized servers and opaque evaluation processes controlled by single organizations. Blockchain enables decentralized verification of model quality, transparent reward distribution using native tokens, and tamper-proof record-keeping, ensuring that no single party can manipulate or monopolize the ecosystem.

- Is decentralization critical in this use case? Why or why not?  

Decentralization is critical. Without it, AI model development and rewards would remain under the control of a few large corporations. Bittensor’s blockchain ensures that anyone, from individual developers to small organizations, can contribute, be evaluated fairly, and receive proportional rewards. This democratizes AI access and aligns incentives across a global community.

[gen45.ai](https://gen45.ai/)
![image](https://hackmd.io/_uploads/SkWNJSXIel.png)

![image](https://hackmd.io/_uploads/B1IMyH7Lll.png)


---

## 8. Insights & Limitations

### ✅ Key Takeaways
- What did this project do right?  
- What important lessons or patterns can we learn from this project?

### ⚠ Limitations / Open Questions
- What challenges remain?  
Technical:

Legal:
When decentralized AI networks give ethically inappropriate answers, the responsibility for them is unclear. There is also a lack of clear interpretation of legal issues such as intellectual property rights and user privacy.

Usability:
Typical Query Senders may need to pay TAO tokens on some subnets, but in most cases, they can receive AI responses without the need for cost, technical knowledge, or high-spec hardware. However, running a miner or validator requires technical knowledge and significant GPU resources, still limiting broader participation.

- Are there any scalability or adoption concerns?

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- Replacing The Operation to Obtain Rewards with Meaningful Activities in the Real World
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
- [Bittensor Introduction] (https://bittensor.com/intro)
- [Bittensor Docs] (https://docs.learnbittensor.org/)
- [TAO Stauts] (https://taostats.io/)
- [Github opentensor/bittensor] (https://github.com/opentensor/bittensor)
- [Github opentensor/text prompting] (https://github.com/opentensor/text-prompting)
- [Subnet 45 - Rizzo Network] (https://rizzo.network/subnet-45/)