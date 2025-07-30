# 📄 WorldID  
- 👤 Author: [20220049 Chaewoon Ki](https://www.linkedin.com/in/chaewoonki/)
- 📆 Presentation Date: 2025-07-30

---

## 1. Overview
![a47a64f7-774a-43ad-8158-c2fcb32e3722_Frame+1321321065](https://hackmd.io/_uploads/H1EyhAIwee.png)
 
- **Project Name**: WorldID
- **Category**: Digital Identity / Proof of Personhood (생체 기반 신원 인증)
- **Key Technologies / Platforms**: Orb, Zero-Knowledge Proof (ZKP), Semaphore, Secure Multi-Party Computation (MPC), Ethereum Layer 2 (Optimism), World App, ERC-20 (WLD)
- **Official Links**:
  - [Website](https://world.org)
  - [Foundation](https://worldcoin.org/team)  <!-- TFH = Tools for Humanity -->
  - [Contract Address](https://etherscan.io/token/0x163f8c2467924be0ae7b5347228cabf260318753)
  - [Whitepaper](https://whitepaper.worldcoin.org)
  - [Docs](https://worldcoin.org/blog/world/world-id-faqs)
  - [GitHub](https://github.com/worldcoin)
  - [X](https://x.com/worldcoin)
  - [Discord](https://discord.gg/worldcoin)



### 📌 Summary
World ID is a digital identity verification system designed to address the problem of **Proof of Personhood**—preventing individuals from creating multiple accounts or bots from pretending to be real people in online and blockchain environments. The project is based on the concept of "one person, one ID," enabling users to prove that they are real human beings. This helps prevent fraud in various blockchain-based applications that require voting, rewards, or verification, and enhances the fairness and trustworthiness of the network.

World ID registers a user's identity through a dedicated device called the Orb, which scans the iris as biometric data. This information is then linked to the blockchain using zero-knowledge proof technology, preserving user privacy. Through the World App, users can securely store their identity credentials and perform anonymous verification for online services.

Blockchain functions as a public infrastructure in this system, storing identity verification data in a tamper-proof and verifiable way. World ID is built on Optimism, an Ethereum Layer 2 network, and operates its ecosystem by issuing WLD tokens or offering rewards to identity holders. This structure aims to ensure both the reliability and security of identity verification by leveraging the decentralization and transparency of blockchain technology.


WorldID는 인터넷과 블록체인 환경에서 한 사람이 여러 개의 계정을 생성하거나, 자동화된 봇이 사람인 척 활동하는 **인간임 증명(Proof of Personhood)** 문제를 해결하기 위한 디지털 신원 인증 시스템이다. 이 프로젝트는 “한 사람당 하나의 ID”라는 개념을 기반으로 하며, 사용자가 진짜 인간임을 증명할 수 있게 해준다. 이를 통해 투표, 보상, 인증이 필요한 다양한 블록체인 기반 애플리케이션에서 부정행위를 방지하고, 네트워크의 공정성과 신뢰성을 높일 수 있다.

WorldID는 생체 정보인 홍채를 스캔하는 전용 장치인 Orb를 통해 신원을 등록하고, 이 정보를 제로 지식 증명(Zero-Knowledge Proof) 기술을 통해 프라이버시를 보호하면서 블록체인에 연동한다. 사용자는 World App을 통해 자신의 신원 증명을 안전하게 보관하고, 온라인 서비스에서 익명으로 인증을 수행할 수 있다.

블록체인은 이 시스템에서 신원 인증 정보를 위변조 없이 저장하고, 누구나 검증 가능한 공공 인프라 역할을 한다. WorldID는 이더리움 레이어2인 Optimism 네트워크를 기반으로 하며, 신원 보유자에게 WLD 토큰을 발급하거나 보상을 제공하는 방식으로 생태계를 운영하고 있다. 이러한 구조는 블록체인의 탈중앙성과 투명성을 활용하여 신원 인증의 신뢰성과 보안성을 동시에 확보하려는 시도이다.


---

## 2. Background & Problem Statement
### Problem
World ID aims to prove "one person, one identity" (Proof of Personhood) in online and blockchain environments, addressing the issue of network distortion caused by bots or the creation of multiple fake accounts (Sybil attacks). For example, its core purpose is to prevent automated bots or AI-generated accounts from registering multiple times to unfairly gain rewards, manipulate voting outcomes, or distort online services.

WorldID는 인터넷과 블록체인 환경에서 ‘한 사람당 하나의 신원’(Proof of Personhood) 을 증명하고, 봇 또는 다중 가짜 계정(Sybil attack) 생성으로 인한 네트워크 왜곡 문제를 해결하고자 한다. 예를 들어, 자동화된 봇이나 AI 생성 계정이 다중 가입하여 보상, 투표 등에서 부당 이익을 취하거나 서비스를 왜곡하는 것을 방지하는 것이 핵심 목적이다.
### Limitations of Existing Approaches
Traditional identity verification relies on IDs, phone numbers, or account credentials issued by governments or large platforms. However, this approach has several issues: it often involves the collection and storage of personal information without user consent, allows individuals to create multiple identities, and lacks interoperability across national borders. Furthermore, since a centralized authority controls the data, it creates a single point of failure — which can lead to access restrictions, censorship, or system outages. Privacy protection is also difficult, as cross-service data linking poses risks of tracking and exposure.

**Example of a conventional approach:**  
India's Aadhaar system is the world’s largest centralized digital identity system, based on biometric data such as fingerprints and iris scans. However, it has experienced multiple data breaches over the years, and reports have indicated that personal information of over 800 million Aadhaar users has been traded on the dark web. The centralized structure, where the UIDAI directly stores and manages all biometric data, creates a single point of failure (SPOF), exposing the entire system to risk in the event of a security breach. This design has led to ongoing concerns about privacy violations, identity theft, and misuse of data.


전통적인 신원 인증은 정부나 거대 플랫폼이 발급하는 신분증, 전화번호, 계정 정보 등에 의존한다. 그러나 이는 사용자의 동의 없이 수집·보관되는 개인정보가 많고, 한 사람이 여러 개의 신원을 생성하거나, 국가 간 상호 인증이 되지 않는다는 문제가 있다. 또한, 중앙기관이 데이터를 통제함으로써 서비스 접근 제한이나 검열, 시스템 다운 등의 Single Point of Failure가 발생할 수 있다. 프라이버시 보호도 어려워, 서비스 간 데이터 연동 시 추적이나 노출의 위험이 따른다.

기존 접근 방식 예시: 인도의 Aadhaar 시스템은 지문과 홍채 등 생체 정보를 기반으로 한 세계 최대 규모의 중앙집중식 디지털 신원 인증 시스템이다. 그러나 수년간 수차례에 걸쳐 개인정보 유출 사고가 발생했으며, 실제로는 8억 명 이상의 Aadhaar 사용자 정보가 다크웹에서 거래된 사례도 보고되었다. 중앙기관(UIDAI)이 모든 생체 정보를 직접 보관하고 관리하는 구조는 Single Point of Failure를 형성하며, 보안 사고 시 전체 시스템이 위협받는 구조적 취약성을 드러낸다. 이로 인해 프라이버시 침해, 신원 도용, 데이터 남용 등의 우려가 지속적으로 제기되고 있다.
### Why This Matters for AI?
As AI technology advances, especially with the rise of natural language generation models like GPT, chatbots and digital agents have become capable of behaving like real humans. However, despite not being actual people, they can be misused to create multiple accounts, participate in voting, claim rewards, or manipulate public opinion. As AI becomes more integrated into everyday digital environments, the challenge of distinguishing between humans and non-humans becomes increasingly critical.

World ID addresses this issue by providing a way to prove that a person is a unique, real human being through a one-time biometric verification. This proof is then made verifiable on the blockchain while preserving user anonymity.

AI 기술이 발전하면서, 특히 자연어 생성 모델(GPT 등)을 기반으로 한 챗봇이나 디지털 에이전트가 인간처럼 행동할 수 있게 되었다. 하지만 이들은 실제 인간이 아님에도 사람처럼 여러 계정을 만들어 투표에 참여하거나, 보상을 획득하고, 여론을 조작하는 데 악용될 수 있다. 이처럼 "사람인지 아닌지"를 구분하는 문제는 디지털 환경에서 AI의 존재가 일상화될수록 더욱 중요해진다. WorldID는 이 문제에 대응하기 위해, 단 한 번의 생체 인증을 통해 "이 사람이 실존하는 유일한 인간"이라는 것을 증명하고, 이를 블록체인을 통해 검증 가능하면서도 익명성을 보장하는 방식으로 제공한다.

---

## 3. How It Works

### 🔍 3.1 Project Approach
- **Problem-Solving Approach**  
  World ID addresses the problem of individuals creating multiple identities or AI bots pretending to be humans by allowing users to verify their humanity through a one-time biometric scan. After that, users can prove they are human using zero-knowledge proofs (ZKPs). This enables a digital environment in which only real human users can participate.

- **Core Idea**  
  The key concept is to issue one World ID per person based on a unique hash value generated from biometric data (iris scan). This allows individuals to prove they are a unique human being while maintaining privacy and anonymity.

- **Difference from Traditional Methods**  
  Unlike centralized systems like Aadhaar, which store and manage biometric data on servers, World ID does not store any biometric information. Instead, only cryptographic proofs are recorded on the blockchain. Users retain full control over their identity and can verify themselves without relying on any central authority, representing a fundamentally different approach focused on decentralization and privacy protection.

- **문제 해결 방식**  
  WorldID는 한 사람이 여러 개의 신원을 만들어 시스템을 악용하거나, AI 봇이 사람인 척하는 문제를 해결하기 위해, 사용자가 한 번만 생체 인증을 하고 이후에는 제로 지식 증명(ZKP)을 통해 "사람임"을 증명할 수 있도록 한다. 이를 통해 디지털 환경에서 실제 인간 사용자만이 참여할 수 있는 구조를 만든다.

- **핵심 아이디어**  
  생체 정보(홍채)를 기반으로 생성한 고유 해시값을 이용해, 한 사람당 하나의 신원(WorldID)을 발급하고, 이 신원을 활용해 익명성과 프라이버시를 유지하면서도 "유일한 인간"임을 증명할 수 있도록 하는 것이 핵심이다.

- **기존 방식과의 차별점**  
  기존의 중앙화된 시스템(Aadhaar 등)은 생체 정보를 서버에 저장하고 관리하지만, WorldID는 어떠한 생체 정보도 저장하지 않으며, 오직 암호학적 증명만을 블록체인에 기록한다. 또한 사용자가 자신의 신원 정보를 직접 제어하고, 누구에게도 의존하지 않고 인증을 수행할 수 있다는 점에서 탈중앙화·프라이버시 보호 측면에서 근본적으로 다른 접근이다.


---

### 🏗️ 3.2 Architecture

World ID is designed to connect biometric-based user authentication with cryptographic proofs on the blockchain. Its key components are linked as follows:

- The **User** scans their iris using the Orb device. The biometric data is hashed locally to generate an **Identity Commitment**.
- This commitment is included in the **World ID Merkle Tree**, which is recorded on the blockchain (Optimism L2) and serves as **proof of identity existence**.
- Based on this information, the user generates a zero-knowledge proof (ZKP) through the World App and submits it to **external apps or services** to prove they are a real person.
- Third-party services verify this proof using the **World ID smart contract**, ensuring that only human users can participate—excluding bots or duplicate identities.

This structure enables identity verification and privacy protection simultaneously, without storing any biometric information.

WorldID는 생체 정보 기반의 사용자 인증과 블록체인 상의 암호학적 증명을 연결하는 구조로 설계되어 있다. 주요 구성 요소는 다음과 같이 연결된다:

- 사용자(User)는 Orb 장치를 통해 홍채를 스캔하고, 생체 정보를 로컬에서 해시 처리하여 신원 커밋먼트(Identity Commitment)를 생성한다.
- 이 커밋먼트는 **WorldID Merkle Tree**에 포함되어 블록체인(Optimism L2)에 기록되며, **신원 존재의 증거**로 작동한다.
- 사용자는 월드앱(World App)을 통해 이 정보를 바탕으로 제로 지식 증명(ZKP)을 생성하고, **외부 앱이나 서비스**에 제출하여 “사람임”을 증명한다.
- 제3자 서비스는 이 증명을 WorldID Smart contract를 통해 검증하고, 봇이나 중복 사용자 없이 사람만 참여하게 할 수 있다.

이 구조는 생체 정보 저장 없이도 신원 증명과 프라이버시 보호를 동시에 달성한다.

---

### 🎯 3.3 Core Components
- **Orb**: A multi-spectrum iris scanner that locally converts biometric data into numerical form to generate a unique ID for each user.
- **World App**: A mobile wallet application that allows users to store their identity commitment and generate/submit zero-knowledge proofs as needed.
- **Identity Commitment & Merkle Tree**: A cryptographic structure that represents user identity and is stored on the blockchain to serve as the basis for verification.
- **Zero-Knowledge Proof (ZKP)**: A mathematical technique that allows users to prove they are human without revealing their actual identity.
- **World ID Smart Contracts**: Smart contracts used to verify ZKP-based proofs, enabling integration with third-party services.
---

### 🔁 3.4 Workflow Overview
![this-diagram-shows-schematically-the-tasks-involved-in-signing-up-for-worldcoin-and-also-those-involved-in-claiming-a-reward-aft](https://hackmd.io/_uploads/B1WeGJwwlx.png)


#### 🟢 Sign-up 단계
1. The user scans their iris using the Orb device to register their biometric information.  
2. The scanned data is encrypted locally and transformed into a unique Identity Commitment.  
3. This commitment is linked to the user's digital wallet (World App) and recorded in the blockchain's Merkle Tree.  
4. Through this process, the user is issued a World ID and becomes eligible to generate zero-knowledge proofs (ZKPs).
----
1. 사용자는 Orb 장치에서 홍채를 스캔하여 생체 정보를 등록한다.
2. 스캔된 정보는 로컬에서 암호화되어 고유한 신원 커밋먼트(Identity Commitment)로 변환된다.
3. 이 커밋먼트는 사용자의 디지털 지갑(World App)과 연결되며, 블록체인의 Merkle Tree에 기록된다.
4. 이 과정을 통해 사용자는 WorldID를 발급받고, 이후 제로 지식 증명(ZKP)을 생성할 수 있는 상태가 된다.

#### 🪙 Claim 단계
1. To receive rewards such as WLD tokens, the user must prove that they are a verified and registered individual.  
2. The World App generates a zero-knowledge proof (ZKP) based on the user's Identity Commitment.  
3. This proof is submitted to third-party services or smart contracts, which verify that the user is uniquely registered and not a duplicate.  
4. Once the verification is successful, the user becomes eligible to claim rewards or access services.

----
1. 사용자는 WLD 토큰 등의 리워드를 받기 위해 "자신이 등록된 사용자임"을 증명해야 한다.
2. World App은 사용자의 신원 커밋먼트를 기반으로 ZKP를 생성한다.
3. 이 증명은 제3자 서비스나 스마트 컨트랙트에 제출되며, 시스템은 해당 사용자가 중복되지 않고 실제로 등록되었음을 확인한다.
4. 검증이 완료되면, 사용자는 리워드를 청구하거나 서비스에 접근할 수 있다. 이때 개인 신원 정보는 외부에 노출되지 않는다.




---

## 4. Token Economy

### 🎟️ WLD Token Overview
- **Token Name and Type**  
  - **Name**: WLD (Worldcoin Token / World Network Token)  
  - **Type**: Utility + Governance Token

- **Token Use Cases**  
  - Users who have completed identity verification can receive **WLD token airdrops and periodic rewards**.  
  - Can be used as a payment method within the World App and World Chain (e.g., transaction fees, mini-app payments).  
  - Governance participation: WLD holders can vote on proposals, with future plans to implement a one-person-one-vote system.

- **Incentive Structure**  
  - Users who complete verification via the Orb receive an initial reward (WLD) and can claim additional rewards over time.  
  - The system is designed to reward early adopters with more tokens, encouraging rapid user base growth.

- **Token Supply, Inflation, and Vesting**  
  - **Total Supply**: 10 billion WLD (10,000,000,000)  
  - **Inflation**: No inflation for the first 15 years; up to 1.5% annual inflation allowed thereafter  
  - **Allocation**: 75% to the community, 9.8% to the team, 13.5% to investors, 1.7% reserved  
  - **Vesting Schedule**: Team and investors are subject to a minimum 1-year lock-up, followed by gradual unlock over 3–5 years

- **토큰 이름 및 유형**  
  - **이름**: WLD (Worldcoin Token / World Network Token)  
  - **유형**: 유틸리티 + 거버넌스 토큰 (utility + governance)
- **토큰 사용 용도**  
  - 신원 인증 완료 사용자는 **WLD 토큰 에어드랍 및 정기 보상**을 받을 수 있음  
  - World App 및 World Chain 내 결제 수단으로 사용 가능 (예: 수수료 지불, 미니앱 결제 등) 
  - 거버넌스 참여: WLD 보유자는 투표에 참여할 수 있으며, 향후 1인 1표 기반 구조도 구현 가능  
- **인센티브 구조**  
  - 사용자는 Orb를 통해 인증을 완료하면 초기 보상(WLD)을 수령하고, 일정 기간 동안 추가 보상을 청구할 수 있음  
  - 조기 참여자에게 더 많은 토큰이 지급되도록 설계되어 사용자 기반 확장을 유도함  
- **토큰 공급, 인플레이션, 베스팅**  
  - **총 공급량**: 10억 WLD (10,000,000,000)  
  - **인플레이션**: 출시 후 15년간 없음, 이후 연 최대 1.5% 인플레이션 허용  
  - **분배 구조**: 커뮤니티 75%, 팀 9.8%, 투자자 13.5%, 예비 1.7%  
  - **베스팅 일정**: 팀 및 투자자는 최소 1년 락업 후 3~5년에 걸쳐 점진적 언락


### 📊 Stakeholder별 WLD 사용 및 획득 구조
| Stakeholder                | How They Use / Earn the Token                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------|
| **Verified User**          | Receives initial airdrop (e.g., 16–25 WLD) after registering identity via Orb, plus monthly claimable rewards |
| **Verifier / Service Provider** | Verifies users' zero-knowledge proofs to confirm their authenticity (no direct token rewards)       |
| **Governance Participant** | Participates in token-based voting and one-person-one-vote governance using World ID          |

| Stakeholder                | How They Use / Earn the Token                                                        |
|----------------------------|---------------------------------------------------------------------------------------|
| **Verified User (사용자)** | Orb로 신원 등록 후 초기 에어드랍(예: 16~25 WLD) 및 월별 청구 가능 보상 획득             |
| **Verifier / 서비스 제공자** | 사용자의 제로 지식 증명을 검증하여 실제 사용자 여부를 확인 (직접 토큰 보상은 없음)       |
| **Governance 참여자**      | WLD 보유를 통해 토큰 기반 투표 및 World ID 기반 1인 1표 거버넌스에 참여 가능             |


---

## 5. Project Status & Plan
- **Project Status (Live Deployment)**: World ID was officially launched in 2023 and is currently in global commercial operation. Users are actively registering through the Orb biometric device, and WLD tokens are distributed upon successful verification.  
- **User Base and Community**: Over 14 million people worldwide have completed Orb verification, and the World App has surpassed 30 million cumulative users. World ID is being integrated into various applications, and its user base is rapidly growing.  
- **Investment and Partnerships**: Tools for Humanity has raised several hundred million dollars in funding and formed partnerships with companies such as Visa and Match Group to expand the ecosystem. Orb verification stations are being installed in major U.S. cities, enhancing offline infrastructure.  
- **Open Source and Developer Engagement**: Parts of the biometric technology have been open-sourced, and external developers can integrate identity-based services using the World ID SDK and documentation.  
- **Token Listing and Trading**: The WLD token is listed on major exchanges and is actively traded. Its circulating supply is gradually increasing. Tokens are distributed to verified users and used for payments and governance within the World App.  
- **Legal and Regulatory Issues**: In some countries, operations have been restricted or suspended due to concerns over biometric data collection. Measures are being taken to comply with data protection regulations such as GDPR.
- **프로젝트 상태 (라이브 여부)**: WorldID는 2023년 정식 출시되어 현재 글로벌 수준에서 상용 운영 중이다. Orb 생체 인증 장치를 통한 사용자 등록이 실제로 진행되고 있으며, 인증 이후 WLD 토큰이 분배된다.
- **사용자 기반 및 커뮤니티**: 전 세계적으로 약 1,400만 명이 Orb 인증을 완료했으며, World App 누적 사용자는 3,000만 명 이상이다. 다양한 앱에서 World ID가 실제로 활용되고 있으며 사용자 기반은 빠르게 성장 중이다.
- **투자 및 파트너십**: Tools for Humanity는 수억 달러 규모의 투자를 유치했고, Visa, Match Group 등과 파트너십을 맺어 생태계를 확장하고 있다. 미국 주요 도시에 Orb 인증소를 설치하며 오프라인 인프라도 확대되고 있다.
- **오픈소스 및 개발자 활동**: 생체 인식 기술 일부가 오픈소스로 공개되었고, World ID SDK 및 문서를 통해 외부 개발자들이 ID 기반 서비스를 연동할 수 있도록 지원하고 있다.
- **토큰 상장 및 거래**: WLD 토큰은 주요 거래소에 상장되어 활발히 거래되고 있으며, 순환 공급량은 점진적으로 증가하고 있다. 토큰은 인증 사용자에게 분배되고 World App 내 결제 및 거버넌스에 사용된다.
- **법적 및 규제 이슈**: 일부 국가에서는 생체 정보 수집에 대한 우려로 운영이 제한되거나 중단된 상태이며, GDPR 등 데이터 보호 규제에 대응하기 위한 조치가 진행되고 있다.


### Added by Jason

### AMPC
Recently, [KAIST joined in a World AMPC node parter.](https://world.org/blog/engineering/introducing-ampc-another-leap-privacy-performance-world-id) [(Korean news)](https://www.didalliance.org/bbs/view.php?code=notice&idx=11219&catcode=13100000&cat_code=1) AMPC, or anonymized multi-party computation, has launched. It is the next-generation, open source quantum secure multi-party computation (SMPC) setup from World that anonymizes and securely protects the iris codes of orb-verified World ID holders. 

![AMPC](https://images.prismic.io/worldcoin-company-website/ZxE2voF3NbkBXr1c_introducing-ampc-another-leap-privacy-performance-world-id-5.jpg?auto=format%2Ccompress&w=3840)

AMPC node parters
![AMPC node parters](https://images.prismic.io/worldcoin-company-website/aDd1ISdWJ-7kSp1s_AMPCPartners.png?auto=format%2Ccompress&w=3840)

### [World ID Credentials](https://world.org/ko-kr/blog/announcements/new-world-id-passport-credential-launches-access-wld-tokens)

World ID Credentials allow an individual to connect valid forms of ID (starting with NFC-enabled passports) to their World ID in order to prove things about themselves — beyond that they are a real and unique human — without sharing any personal information with Tools for Humanity, World Foundation or any other third party. **Credentials can be added to a person’s World ID whether or not they have verified their unique humanness at an Orb.** World Foundation is making WLD tokens available to individuals with a valid World ID Credential.

![World ID Credentials](https://images.prismic.io/worldcoin-company-website/Z0mssJbqstJ975VY_new-world-id-passport-credential-launches-access-wld-tokens-3.jpg?auto=format%2Ccompress&w=3840)

They expanded their capabilities from a single Proof of Humanity feature to multiple credentials. This is going in a similar direction to the Humanity Protocol. Presumably, they made this strategic choice because a single World ID would have limited utility, and it's not easy to collect identities through Orbs hardware.

---

## 6. User Experience & Hands-on Review
1. Download the World App from the App Store  
   ![IMG_3901](https://hackmd.io/_uploads/B1PSd1Pweg.jpg)

2. [Sign up](https://youtube.com/shorts/F9vEkjP9xfQ?si=W09G61Jo8zExh-lz): After creating an account, simply enter your password and date of birth, then verify your phone number to start using the app.

3. [Get verified with the Orb](https://youtube.com/shorts/GRsoPyT1UP0?si=IfY7TEvZgymioooK): The app will show nearby locations where you can complete Orb verification based on your current location.

4. Explore wallet and Mini App features: The World App can function as a Bitcoin wallet, but also allows you to interact with various apps and even communicate with AI or humans.  
   - [Wallet, Human vs AI](https://youtube.com/shorts/yeJuGD-8mSk?si=GuChLp7PvgcgxlwK)  
   - [Mosaic (visual app experience)](https://youtube.com/shorts/04qW0cuQM9M?si=AhdEjLUwf5xBlN0F)  
   - [CoPilot AI (example with error)](https://youtube.com/shorts/MTRbs-DEheo?si=4clJvDUX3wcrggQ_)



## 7. Why Blockchain
The core problem World ID seeks to solve is preventing individuals from creating multiple identities to exploit systems, and stopping AI bots from pretending to be human. Effectively addressing this "Proof of Personhood" issue requires more than technical implementation—it demands a **trustworthy system architecture**.

- **Why does this problem require blockchain?** In centralized systems, identity data is collected, stored, and verified by a single authority. This poses risks such as privacy violations, censorship, data leaks, system failures, and abuse of power. In contrast, blockchain provides a **trustless architecture where anyone can independently verify the validity of identity proofs**, and it **prevents any single entity from monopolizing or tampering with the data**.
- **What capabilities does blockchain offer that existing solutions cannot?** Blockchain, combined with zero-knowledge proofs (ZKPs), enables **users to prove they are human without revealing their identity**, ensuring strong privacy protection. Moreover, all activities—including WLD token distribution, usage history, and verification traffic—are immutably recorded, which is **essential for ensuring fair rewards and maintaining system integrity**.
- **Is decentralization essential for this use case? Why?** Yes, **decentralization is not optional—it is a prerequisite**. If a system is designed to ensure one identity per person, but that identity can be controlled or revoked by a government or corporation, the entire purpose of the system is undermined. To guarantee an identity that **belongs to no one and is controlled by no one**, World ID adopts a **globally accessible and censorship-resistant blockchain infrastructure**.

Ultimately, World ID does not merely use blockchain—it makes decentralization the foundation of its trust, privacy, and reward systems. This structure simply cannot be replicated within a traditional centralized framework.

WorldID가 해결하고자 하는 핵심 문제는, 한 사람이 여러 개의 신원을 만들어 시스템을 악용하거나, AI 봇이 인간인 척 활동하는 것을 방지하는 것이다. 이러한 '사람임 증명(Proof of Personhood)' 문제를 효과적으로 해결하기 위해서는, 단순한 기술 구현이 아닌 **신뢰 가능한 구조**가 필요하다.

- **왜 이 문제는 블록체인을 필요로 하는가?**  
  중앙화된 시스템에서는 신원 정보를 특정 기관이 수집·보관·검증한다. 이는 사생활 침해, 검열, 데이터 유출, 시스템 오류, 권한 남용 등의 위험이 뒤따른다. 반면 블록체인은 **누구나 독립적으로 신원 증명의 유효성을 검증할 수 있는 무신뢰(trustless) 구조**를 제공하며, **정보 위·변조나 특정 주체의 독점 통제 가능성을 원천 차단**한다.
- **기존 솔루션이 제공하지 못하는 블록체인의 기능은?**  
  블록체인은 제로 지식 증명(ZKP)을 통해 **"사람임"을 증명하면서도 신원을 직접 공개하지 않을 수 있는 프라이버시 보호 구조**를 가능하게 한다. 또한, WorldID와 연결된 WLD 토큰의 배포, 사용 기록, 인증 트래픽 등은 모두 위변조가 불가능하게 기록되므로 **사용자 간 공정한 보상과 시스템 신뢰성 유지**에 필수적이다.
- **이 사용 사례에 탈중앙화는 필수적인가? 왜 그런가?**  
  예, **탈중앙화는 이 문제에 있어 ‘선택’이 아니라 ‘전제 조건’**이다. 사람이 단 하나의 신원을 갖는 구조를 만들면서도, 그 신원이 특정 정부·기업에 의해 통제되거나 취소될 수 있다면, 이는 곧 시스템의 근본 취지와 모순된다. WorldID는 "누구에게도 소속되지 않은 신원"을 보장하기 위해, **전 세계적으로 접근 가능하고, 누구도 통제할 수 없는 블록체인 기반 구조**를 채택한다.
  
결국 WorldID는 블록체인을 단순히 활용하는 수준을 넘어서, 탈중앙화를 신뢰·프라이버시·보상 시스템의 핵심 구성 원리로 삼는다. 전통적인 중앙 시스템으로는 이와 같은 구조를 실현할 수 없다.


---

## 8. Insights & Limitations

### ✅ Key Takeaways
- **Privacy-first ID architecture**: World ID successfully implements a structure that proves personhood without storing any biometric data. 
- **Combining zero-knowledge proofs with biometric verification**: A single Orb verification enables anonymous authentication, reducing friction for repeated verifications. 
- **Proven effectiveness of the WLD incentive model**: Token-based rewards have enabled rapid user adoption, attracting millions of users in a short time.

[Korean]
- **프라이버시 중심 ID 구조 실현**: WorldID는 생체 정보를 저장하지 않고도 사람임을 증명할 수 있는 구조를 성공적으로 구현했다.
- **제로 지식 증명 + 생체 인증 결합**: 한 번의 Orb 인증으로 익명성을 유지한 인증이 가능해, 반복 인증에서도 사용자 부담이 낮다.
- **WLD 인센티브 모델 효과 입증**: 토큰 보상 덕분에 수백만 명의 사용자를 빠르게 확보할 수 있었다.

### ⚠ Limitations / Open Questions
- **Regulatory concerns**: Operations have been restricted or suspended in some countries due to issues related to biometric data collection.
- **Centralization risk**: The manufacturing of the Orb and the verification process are still concentrated under a single company (TFH).
- **Limited accessibility**: The physical availability of Orbs is geographically limited, posing challenges to global scalability.

[Korean]
- **규제 이슈**: 일부 국가에서 생체 정보 수집 문제로 운영 중단되거나 제한되고 있다.
- **중앙 의존성**: Orb 제조와 인증 과정이 여전히 특정 기업(TFH)에 집중되어 있다.
- **접근성 제약**: Orb 설치 지역이 한정돼 있어 글로벌 확산에 물리적 한계가 있다.


---

## 9. Reflections & Discussion

 ### 💡 Personal Reflections
- What I found particularly interesting about World ID is that it can prove identity without directly storing sensitive biometric data.  
- I used to think of blockchain as merely a technology for cryptocurrency, but through this research project, I learned that it can also be effectively used to address issues of security and trust.  
- If World ID can overcome its current regulatory challenges and truly implement “one person, one account,” I believe it could be applied beyond just technology—to systems like voting or welfare—and potentially address problems caused by anonymity in today’s internet communities.

[Korean]
- WorldID를 보면서, 민감한 생체 정보를 직접 저장하지 않고도 신원을 증명할 수 있다는 점이 특히 흥미로웠다.  
- 블록체인에 대해서 단순히 가상화폐와 관련된 기술이라고만 알고 있었는데, 조사 프로젝트를 통해서 안전성과 보안성 문제에서도 충분히 활용될 수 있다는 것을 배울 수 있었다.
- World ID가 지금 가지고 있는 규제 문제를 해결해 ‘1인 1계정’을구현할 수 있다면, 단순한 기술 이상으로 선거나 복지 같은 제도에도 응용될 수 있을 것이고, 현재 인터넷의 익명 커뮤니티가 가지는 문제도 해결할 수 있을 것이라는 생각이 들었다.


### ❓ Discussion Questions
1. **Why is "one person, one ID" important for the blockchain ecosystem?** How does it relate to token distribution, DAO voting, or preventing Sybil attacks?
2. **Is the current centralized Orb infrastructure trustworthy?** How could it be decentralized in the long term?
3. **Is the WLD token incentive model sustainable?** Beyond simple sign-up rewards, what kind of economic model is needed?
4. **What are the fundamental differences between World ID and traditional login systems (e.g., SNS OAuth)?** Can they be compared in terms of privacy, user sovereignty, and global accessibility?

[Korean]
1. **왜 ‘1인 1ID’가 블록체인 생태계에 필요한가?**   토큰 분배, DAO 투표, Sybil 공격 방지 등과 어떤 연관이 있을까?
2. **중앙화된 Orb 운영 구조는 신뢰 가능한가?**  장기적으로 이를 어떻게 분산화할 수 있을까?
3. **WLD 토큰의 인센티브 설계는 지속 가능할까?** 단순 가입 보상을 넘어서 어떤 경제 모델이 필요할까?
4. **WorldID와 기존 로그인 시스템(SNS OAuth 등)의 본질적 차이는?**  프라이버시, 주권, 글로벌 접근성 측면에서 비교해볼 수 있을까?


---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

- [Worldcoin 공식 홈페이지](https://worldcoin.org)  
- [Worldcoin 개발자 문서 (Docs)](https://docs.worldcoin.org)  
- [Worldcoin 백서](https://whitepaper.worldcoin.org)  
- [Worldcoin GitHub 리포지토리](https://github.com/worldcoin)  
- [Worldcoin 공식 블로그](https://blog.worldcoin.org)  
- [The Verge: Worldcoin launches worldwide with eye-scanning ‘Orb’](https://www.theverge.com/cryptocurrency/659011/worldcoin-us-launch-orb-crypto-sam-altman?utm_source=chatgpt.com)  
- [Intro to Zero-Knowledge Proofs and Semaphore in World ID](https://world.org/ko-kr/blog/world/intro-zero-knowledge-proofs-semaphore-application-world-id?utm_source=chatgpt.com)


