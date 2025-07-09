# 📄 Coinbase AgentKit 
- 👤 작성자: [20230904 / Jaeyoung Shin](https://www.linkedin.com/in/limepencil/)
- 📆 발표 날짜: [2025-07-09]  

---

## 1. 개요
![image](https://hackmd.io/_uploads/HkCrDroHgg.png)

- **프로젝트 이름**: Coinbase AgentKit  
- **카테고리**: 온체인 AI 에이전트 툴킷 (탈중앙화 AI 인프라)  
- **핵심 기술 / 플랫폼**: 이더리움 및 Base (L2) 블록체인, Solana, 스마트 컨트랙트(Solidity), 계정 추상화(스마트 월렛), Coinbase Developer Platform(CDP) SDK, LangChain 통합  
- **공식 링크**:  
  - [웹사이트](https://www.coinbase.com/developer-platform/products/agentkit)  
  - [홈페이지](https://www.coinbase.com/)  
  - [Docs](https://docs.cdp.coinbase.com/)  
  - [GitHub](https://github.com/coinbase/agentkit)  
  - [X](https://x.com/coinbasedev)  
  - [Discord](https://discord.com/invite/cdp)  

### 📌 요약  
Coinbase AgentKit은 AI와 블록체인 간의 간극을 메우는 개발자 툴킷으로, 자율 온체인 AI 에이전트를 생성할 수 있게 해줍니다. 기존 AI 애플리케이션에서는 에이전트(고급 챗봇이나 자동화 스크립트 등)가 자산을 거래하거나 탈중앙화 시스템과 상호 작용하는 능력이 제한적이었습니다. AgentKit은 각 AI 에이전트에 고유의 암호화 월렛과 온체인 액션 모음을 제공하여, 에이전트가 자산을 보유·이체하고 스마트 컨트랙트를 배포하며 탈중앙화 앱과 자율적으로 상호 작용할 수 있도록 합니다.

블록체인을 활용함으로써 이러한 AI 에이전트는 24시간 운영이 가능한 1급 경제 행위자가 됩니다. 에이전트는 의사결정을 내리고, 인간 중개 없이 직접 금융 거래를 실행할 수 있습니다. 실제로 AgentKit은 모델-불가지론적(model-agnostic)이며 프레임워크-불가지론적(framework-agnostic) 인프라를 제공합니다. 개발자는 OpenAI 등 원하는 LLM을 연결하고 Coinbase의 안전한 API를 통해 블록체인 기능을 연동할 수 있습니다.

이 툴킷에는 Coinbase의 Smart Wallet API 기반 안전한 월렛 관리 기능과 토큰 전송, 스왑, 컨트랙트 배포, 소셜 미디어 운영 등의 사전 구축된 액션 라이브러리가 포함되어 있습니다. 이를 통해 에이전트 월렛에 자금을 충전하거나 가스 요금을 지불하고 DeFi 프로토콜을 호출하는 작업 등 온체인 AI 에이전트를 구축하는 복잡성을 크게 줄일 수 있습니다.

AgentKit의 주요 성과로는 LangChain과 같은 인기 AI 프레임워크와의 원활한 통합, 여러 블록체인(EVM 호환 네트워크 및 Solana) 지원, 커스텀 액션 추가나 대체 월렛 제공자 통합이 가능한 확장 설계 등이 있습니다. 요약하면, AgentKit은 개발자가 AI 기반 애플리케이션에 내장된 암호화 기능을 쉽게 통합하여 자동화 거래, 자산 관리, 분산형 상거래 등의 새로운 가능성을 열어줍니다.

---

## 2. 배경 및 문제 정의

### 문제  
현대 AI 에이전트(GPT 모델 등)는 콘텐츠 생성은 가능하지만 자산을 독립적으로 소유하거나 스마트 컨트랙트와 상호 작용할 수 없습니다. 에이전트가 거래를 수행하려면 안전한 키 관리, 블록체인 통합, 보안 실행 보장 등의 난제를 해결해야 합니다. 중앙화된 솔루션(관리형 월렛, 은행 API 등)은 권한이 필요하고 위험하며, 글로벌 자율 운영을 방해합니다. 블록체인이 없으면 에이전트 행동은 메시지 전송이나 API 호출 같은 비금융 작업에 국한됩니다.

### 기존 접근 방식의 한계  
AgentKit 이전에는 AI와 암호화폐 연결이 단편적이고 보안이 취약했습니다. 각 프로젝트마다 월렛 관리와 블록체인 도구를 수작업으로 구축해야 했으며, 개발 시간이 늘어나고 보안 리스크가 증가했습니다. 중앙화 시스템은 단일 실패 지점을 만들어 에이전트가 예고 없이 차단될 수 있었습니다.

### AI 분야에서의 중요성  
AI 에이전트가 자율성을 높일수록 디지털 경제에 참여하려면 네이티브 암호화 기능이 필요합니다. 블록체인은 에이전트가 자금을 보유·이체하고 탈중앙화 앱과 언제든 상호 작용할 수 있게 합니다. 이를 통해 거래 봇, NFT 생성기, DAO 참여자 등 다양한 유스케이스가 가능해집니다. AgentKit은 이러한 에이전트를 지원하는 인프라를 제공해 AI의 온체인 전환을 더 쉽고 안전하게 만듭니다.

---

## 3. 작동 방식

### 🔍 3.1 프로젝트 접근법  
Coinbase AgentKit의 핵심 원칙은 “모든 AI 에이전트는 자체 암호화 월렛을 가져야 한다”입니다. 이를 통해 AI 에이전트가 블록체인 상에서 독립적인 참여자로 활동할 수 있게 합니다. 에이전트에 월렛과 블록체인 도구 세트를 제공함으로써, 자연어 명령에 따라 송금, 스마트 컨트랙트 상호작용, 토큰 스왑 등의 작업을 자율적으로 수행할 수 있습니다.

**작동 방식**  
AgentKit은 AI와 블록체인 기술 간의 다리 역할을 합니다.

* **블록체인 측**: Coinbase Developer Platform을 활용해 트랜잭션 서명, 수수료 관리 등 복잡한 작업을 처리해 개발 과정을 단순화합니다.  
* **AI 측**: 다양한 AI 모델과 LangChain 같은 인기 개발 프레임워크와 호환되도록 설계되었습니다. 에이전트가 금융 액션을 결정하면, AgentKit이 이를 안전한 온체인 트랜잭션으로 변환합니다.

**주요 차별점**  
* **프레임워크 불가지론**: OpenAI, Anthropic 등 다양한 LLM, 모든 EVM 네트워크 및 Solana를 지원하며 특정 월렛 제공자에 종속되지 않습니다.  
* **개발자 중심**: 간단한 설정과 스타터 템플릿을 제공해 개발자가 AI와 블록체인을 빠르게 통합할 수 있도록 설계되었습니다.  
* **실용적 방향**: 일부 프로젝트가 AI 자체의 탈중앙화를 추구하는 반면, AgentKit은 AI가 암호화 인프라를 ‘사용’하도록 돕습니다. 모듈식 플러그앤플레이 솔루션을 제공합니다.

---

### 🏗️ 3.2 아키텍처  
AgentKit은 AI의 의도를 블록체인 트랜잭션으로 번역하는 모듈형 시스템입니다. 과정은 다음과 같습니다:

1. **AI 에이전트**가 액션(예: “10 USDC 전송”)을 결정합니다.  
2. AgentKit이 제공하는 **액션** 도구를 사용합니다.  
3. 액션이 **월렛 제공자**를 통해 트랜잭션을 서명하고 실행합니다.  
4. 결과가 AI 에이전트에 반환되어 다음 단계를 결정합니다.  

---

### 🎯 3.3 핵심 구성 요소  
* **AgentKit 코어 라이브러리**: TypeScript와 Python으로 제공됩니다. API 키, 네트워크 선택 등 설정을 관리하며 월렛·액션 모듈을 연결합니다.  
* **월렛 제공자**: 주소 생성, 키 관리, 트랜잭션 서명 등을 처리합니다. 기본 제공은 Coinbase Smart Wallet이며, MetaMask 등 다른 월렛으로 교체할 수 있습니다.  
* **액션 제공자**: 전송, 스왑, NFT 생성 등 사전 구축된 액션을 그룹화합니다. 개발자가 커스텀 액션을 등록할 수도 있습니다.  
* **프레임워크 통합**: LangChain 등 인기 프레임워크용 어댑터를 제공해 AgentKit 기능을 손쉽게 통합합니다.  

---

### 🔁 3.4 워크플로우 개요  
`[User Input] → [AI Agent (LLM)] → [AgentKit Core] → [Wallet Provider] → [Blockchain Tx] → [Response]`

1. **초기화 및 설정**  
   개발자는 Coinbase·OpenAI API 키를 제공해 에이전트를 구성하고, AgentKit이 고유 월렛을 프로비저닝합니다.  
2. **사용자 명령**  
   사용자는 “0.01 ETH를 친구에게 보내줘”처럼 자연어로 요청합니다.  
3. **AI 계획 및 액션 선택**  
   AI 에이전트가 요청을 해석해 적절한 액션 도구(e.g., `transfer`)를 선택합니다.  
4. **온체인 실행**  
   AgentKit이 트랜잭션을 생성·서명·브로드캐스트합니다.  
5. **확인 및 응답**  
   트랜잭션 확정 후 AI 에이전트가 사용자에게 결과(트랜잭션 해시 등)를 제공합니다.  

**선택 사항: 자율 운영**  
에이전트를 “시장 모니터링 및 수익 극대화” 같은 목표로 설정하면, 지속적으로 의사결정하고 온체인 작업을 수행합니다.  

---

## 4. 토큰 경제 *(해당되는 경우)*  
본 사례 연구에서는 토큰이 존재하지 않습니다.  

---

## 5. 프로젝트 현황 및 계획

### Added by Jason

✅ **Coinbase AgentKit vs GOAT SDK**  
| 카테고리                   | **Coinbase AgentKit**                                      | **GOAT SDK**                                                |
| -------------------------- | ---------------------------------------------------------- | ----------------------------------------------------------- |
| 🧠 **목적**                | Coinbase Wallet 사용자를 위한 AI 인터페이스 제공 (거래 어시스턴트) | 다중 에이전트, 체인 및 월렛 지원 모듈형 AI-블록체인 인터페이스 |
| 🧱 **의존성**              | Coinbase Wallet + 특정 LLM(예: OpenAI) 필요               | Viem/Ethers 통해 모든 EVM 월렛(예: MetaMask, Safe) 지원     |
| 🔌 **체인 지원**           | 주로 EVM(Base, Ethereum)                                    | Base, Ethereum, Optimism, Polygon 등 다중 체인 지원         |
| 🛠️ **기술 스택**           | LangChain + LLM 도구 + 스크립팅                            | Vercel AI SDK + GOAT 플러그인 시스템 + Viem/Ethers          |
| 🔍 **상태 / 메모리**       | LangChain으로 상태·메모리 관리                            | 도구 기반 또는 개발자 관리 가능                            |
| ⚡ **확장성**              | Coinbase 생태계 사용 사례에 최적화                        | 매우 모듈식: DeFi, NFT, 인프라 도구 자유롭게 플러그인 가능  |
| 🧩 **플러그인 아키텍처**   | 제한적(사전 정의된 도구 중심)                              | 완전 플러그인 시스템: 개발자 커스텀 도구 정의 가능         |
| 🧑‍💻 **대상 개발자**       | Coinbase 생태계 빌더                                       | AI 에이전트, 지갑 UX, LLM 기반 dApp 개발자                |

| Use Case                               | Recommendation  |
| -------------------------------------- | --------------- |
| Coinbase 전용 UX                       | ✅ AgentKit     |
| 다중 월렛/DeFi/고급 에이전트 제어      | ✅ GOAT SDK     |
| 플러그인 유연성 및 온체인 도구 체이닝 필요 | ✅ GOAT SDK     |

✅ **Solana AgentKit vs Coinbase AgentKit vs GOAT SDK**  
| 특징                   | **Solana AgentKit**                   | **Coinbase AgentKit**                           | **GOAT SDK**                                     |
| ---------------------- | ------------------------------------- | ------------------------------------------------ | ------------------------------------------------ |
| **체인 지원**          | Solana 전용                            | Ethereum + L2(Base, Optimism, Arbitrum 등)       | Ethereum + L2 및 기타 체인(플러그인 사용)         |
| **월렛 유형**          | 키페어, xNFT, AnchorWallet            | SmartWallet(AA, Biconomy 등)                     | EOA, AA Wallet(Crossmint, Privy 등)               |
| **세션 키 지원**       | 예(사용자 구현)                       | 예(Biconomy + 권한)                              | 예(TEE 보안 에이전트 월렛)                        |
| **계정 추상화 (AA)**   | ❌ 기본 지원 안 함                     | ✅ 기본 제공(SmartWallet)                         | ✅ Crossmint/플러그인 통해 지원                   |
| **보안 전략**          | 키페어 주입 또는 Phantom 확장         | SmartWallet + 가드레일 옵션                      | TEE 기반 서명 + 제한 옵션                        |
| **개인 키 제어**       | ✅ 일반적으로 필요                     | ❌ 필요 없음(SmartWallet 세션 사용)               | ❌ 필요 없음(세션 키/TEE)                         |
| **트랜잭션 실행**      | solana/web3.js, Anchor 등             | Coinbase 인프라(Biconomy 등)                    | 사용자 정의 또는 GOAT 플러그인 시스템            |
| **가드레일**           | ❌ 기본 제공 안 함                     | ✅ Biconomy 규칙(허용 목록, 지출 한도)           | ✅ Crossmint AgentWallet 가드레일                 |
| **AI 통합**            | 기본/수동                             | LangChain 에이전트 지원                          | LangChain, Vercel AI 등 지원                     |
| **개발자 경험**        | Solana 네이티브 개발자 전용           | Coinbase 스택 최적화                             | 체인 비종속, 모듈식 플러그인 기반                 |
| **대상 사용 사례**     | Solana 전용 AI 에이전트/ xNFT         | EVM 체인에서 Coinbase 에이전트                   | 유연한 EVM 에이전트(월렛, 플러그 앤 플레이)      |

---

## 6. 사용자 경험 및 실습 리뷰 *(해당되는 경우)*  
공식 GitHub 페이지의 [Quick Start](https://github.com/coinbase/agentkit) 섹션을 따라 해보았습니다. 예제 프로젝트로 빠르게 시작할 수 있었고, UI 컴포넌트를 추가하고 LLM API를 OpenAI에서 Claude로 교체했습니다.

![image](https://hackmd.io/_uploads/HyR9mHjBgg.png)

---

## 7. 왜 블록체인인가  
블록체인 기술은 AI 에이전트가 진정한 금융 자율성을 얻도록 합니다. 에이전트는 전통 중개 없이 암호화 월렛으로 가치를 보유·이전할 수 있고, 24시간·전 세계 거래가 가능합니다. 블록체인은 투명·검증 가능 환경을 제공하여 에이전트 행동에 신뢰를 부여합니다.

또한 단순 결제 이상으로 AI 에이전트는 대출, 탈중앙화 거래소 거래, 디지털 수집품 투자, 탈중앙화 거버넌스 참여 등 DeFi·dApp 생태계를 활용할 수 있습니다. 최신 L2 솔루션은 실시간·저비용 마이크로거래를 지원하여 에이전트가 데이터나 서비스를 즉시 결제할 수 있게 합니다.

---

## 8. 주요 인사이트 및 한계

### 주요 인사이트
* **강력한 시너지**: AI와 블록체인의 결합은 단독으로 불가능한 기능을 제공하여 차세대 참조 아키텍처를 제시합니다.  
* **미래 대비 설계**: 모델·프레임워크 불가지론적 모듈형 접근은 빠르게 변하는 기술 환경에 유연하게 대응합니다.  
* **마찰 없는 도입**: 가스 요금, 월렛 충전, 키 관리 등 복잡성을 추상화하여 개발자 진입 장벽을 낮춥니다.  
* **커뮤니티 주도 성장**: 오픈 소스와 커뮤니티 기여로 혁신이 가속화되어 다양한 도구와 유스케이스가 생겨났습니다.  
* **경제 주체로서 AI 검증**: 에이전트가 실제 경제 활동에 참여할 수 있음을 증명하여 블록체인을 결제 계층으로 활용합니다.

### 한계 및 미해결 질문
* **초기·실험 단계**: 아직 프로덕션 준비가 미흡해 프롬프트 인젝션 등 안전 가드레일이 부족합니다.  
* **보안 위험**: AI가 실수나 악의적 입력으로 자금을 잃을 수 있는 리스크가 큽니다.  
* **중앙화 의존**: 기본 인프라가 Coinbase의 중앙화 시스템에 의존해 자율성과 편의성 사이 트레이드오프가 발생합니다.  
* **규제 불확실성**: 자율 에이전트의 법적 책임·규제 준수 여부가 그레이 영역에 있습니다.  
* **확장성·복잡성**: 수백만 에이전트 지원과 복잡한 온체인 작업 처리 능력은 아직 검증되지 않았습니다.

---

## 9. 회고 및 토론

### 💡 개인적인 회고  
AgentKit을 공부하며 AI 에이전트를 블록체인의 “사용자”로 보는 시각이 크게 바뀌었습니다. 단순 결제를 넘어 AI 로직과 온체인 로직이 결합되어 에이전트가 자산을 독립 관리·운용할 수 있음을 체감했습니다. 초기에는 회의적이었지만, 추상화의 힘을 통해 복잡한 기술 간 간극을 효과적으로 메우는 설계에 감탄했습니다.

### ❓ 토론 질문
- **자율성 대 통제**: 실제 자금을 제어하는 AI 에이전트에 대해 지출 한도나 킬스위치 등의 안전장치를 어떻게 구현하면서도 자율성을 유지할 수 있을까요?  
- **경제적 영향**: AI 에이전트가 거래, 경매, 서비스 시장에서 인간과 경쟁할 때 발생할 위험과 기회는 무엇일까요?  
- **탈중앙화의 필요성**: 중앙화된 기업이 AgentKit과 유사한 기능을 제공할 수 있다면, 블록체인이 제공하는 핵심 가치는 무엇일까요?

---

## 10. 타인의 인사이트  
수업 발표 후 소규모 토론 그룹을 구성하여 섹션 9의 질문을 논의하고, 그룹에서 도출된 주요 포인트나 인사이트를 여기에 작성해주세요.

---

## 11. 참고 문헌  
* *Introducing AgentKit, a toolkit for building AI agents onchain*. (Coinbase Developer Platform). [https://www.coinbase.com/developer-platform/discover/launches/introducing-agentkit](https://www.coinbase.com/developer-platform/discover/launches/introducing-agentkit)  
* *AgentKit Documentation*. (Coinbase Developer Platform). [https://docs.cdp.coinbase.com/agent-kit/welcome](https://docs.cdp.coinbase.com/agent-kit/welcome)  
* *Build with Coinbase and OpenAI's new Agents SDK*. (Coinbase Developer Platform). [https://www.coinbase.com/developer-platform/discover/launches/openai-agents-sdk](https://www.coinbase.com/developer-platform/discover/launches/openai-agents-sdk)  
* *AgentKit Q1 2025 Update: Building agents with Solana, OpenAI, and more*. (Coinbase Developer Platform). [https://www.coinbase.com/developer-platform/discover/launches/agentkit-q1-update](https://www.coinbase.com/developer-platform/discover/launches/agentkit-q1-update)  
* *The rise of onchain AI agents, apps, and commerce*. (Coinbase Blog). [https://www.coinbase.com/en-gb/blog/the-rise-of-onchain-ai-agents-apps-and-commerce](https://www.coinbase.com/en-gb/blog/the-rise-of-onchain-ai-agents-apps-and-commerce)  
* *Coinbase Developer Platform AgentKit Quickstart Guide*. (Replit). [https://replit.com/guides/coinbase-developer-platform-agentkit-quickstart-guide](https://replit.com/guides/coinbase-developer-platform-agentkit-quickstart-guide)  
* *coinbase/agentkit GitHub Repository*. (GitHub). [https://github.com/coinbase/agentkit](https://github.com/coinbase/agentkit)  
