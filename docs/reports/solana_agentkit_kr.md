# 📄 Solana Agent Kit  
- 👤 Author: [20220162 / 김주현] (www.linkedin.com/in/joohyeun-kim)
- 📆 Presentation Date: [2025-07-09]  

---

## 1. Overview

- **Project Name**: 솔라나 에이전트 키트 Solana Agent Kit
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
Solana Agent Kit는 AI 에이전트가 블록체인과 자연스럽게 상호작용할 수 있도록 도와주는 툴킷이다. 기존에는 AI가 온체인(블록체인 위에서 직접 일어나는 모든 활동으로 블록체인에 기록되고 검증되는 데이터나 거래를 뜻함.) 자산을 다루는 데 제약이 많았지만, 이 키트를 통해 토큰 스왑, 대출, NFT 민팅(디지털 자산을 블록체인에 등록해 소유권을 증명할 수 있게 만드는 과정) 등 60개 이상의 Solana 액션을 자유롭게 수행할 수 있다. 주요 특징은 플러그인 기반(시스템 외부에서 추가하는 기능 확장) 아키텍쳐, LangChain(LLM 조합 프레임워크) 및 Vercel AI SDK(프론트엔드에 AI 기능을 붙이는 툴킷) 연동, zk 기반의 airdrop 지원, 챗형/자율형 에이전트 모드 등을 포함한다. 

---

## 2. Background & Problem Statement

- 해결하려는 문제: AI 에이전트가 온체인 환경에 접근하지 못해 분산 생태계(중앙 서버나 기관 없이, 여러 참여자가 서로 연결되어 자율적으로 운영되는 시스템)에서 제 역할을 하지 못한다.  
- 기존 중앙화 방식의 한계: API는 폐쇄적이고, 접근에 제약이 있으며, 디파이나 NFT와 같은 Web3 프로토콜과 쉽게 통합되지 않는다.   
- AI와의 관련성: 자율 에이전트가 점점 늘어나는 추세에서, 블록체인 상 자산을 직접 조작할 수 있어야 자동화와 탈중앙 협력이 가능해진다. 

---

## 3. How It Works

### 🔍 3.1 Project Approach  
- 핵심 아이디어: AI가 Solana를 제어할 수 있도록 표준화된 플러그인 인터페이스를 제공  
- 차별점: 지갑 관리, RPC(Remote Procedure Call 다른 컴퓨터에 있는 함수를 마치 내 컴퓨터처럼 호출하는 기술) 호출, 프로토콜 별 로직을 추상화하여 개발자 부담 최소화

---

### 🏗️ 3.2 Architecture  
- AI 모델 (예: GPT-4o, Claude 등)
- 다양한 플러그인(Token, NFT, DeFi, Misc, Blinks 등)
- Solana RPC/지갑
- 온체인 프로토콜(Jupiter, Raydium, Metaplex)
- 사용자 입력 → AI 에이전트 → Solana Agent Kit → 플러그인 → Solana 프로토콜

![image](https://hackmd.io/_uploads/rJGQhK9Hxx.png)

---

### 🎯 3.3 Core Components  
- Token Plugin: SPL(Solana Program Library) 토큰 전송, 발행, 스왑
- NFT Plugin: 민팅, 판매, 메타데이터 관리
- DeFi Plugin: 대출, 스테이킹, 파생상품 연동
- Misc Plugin: 가격 조회, SNS 도메인, 에어드랍 등
- Blinks Plungin: 미니게임, JulSOL 참여 등

---

### 🔁 3.4 Workflow Overview  
AI 에이전트 온체인 작업 흐름:
1. 사용자 입력
   - 자연어 명령: `"1 SOL 스테이킹해줘"`
2. AI 명령 분석
   - 행동 파악: `스테이킹`
   - 자산 종류: `SOL`
   - 수량: `1`
   - 명령이 온체인 트랜잭션이라는 점 인식
3. Solana Agent Kit 호출
   - AI가 분석 결과를 Agent Kit으로 전달
   - 적절한 플러그인 결정
4. 스테이킹 플러그인 실행
   - 스테이킹 트랜잭션 생성
   - 사용자 지갑과 RPC 연결
   - Solana 블록체인으로 트랜잭션 전송
5. 트랜잭션 결과 반환
   - 성공 여부 확인
   - 트랜잭션 해시 반환
   - 사용자에게 피드백
6. 오류 처리 / 자율 재시도
   - 실패 시:
     - 재시도
     - 다른 프로토콜로 우회
     - 사용자에게 상황 안내


---

## 4. Token Economy

- 자체 토큰 없음
- 연동되는 토큰: $SEND (SendAI), $USDC, $JUP 등과 상호작용 가능
- 경제적 인센티브: Agent Kit 자체에는 없음, 연동된 프로토콜에서 토큰 경제 작동

---

## 5. Project Status & Plan

- 현황: 오픈소스로 릴리즈됨(v2 기준, 사용 가능)
- 커뮤니티: GitHub 기준 Star 1.4k+, Fork 700+
- 후원/참여: Solana Foundation 지원, AI 해커톤 소개
- Solana Agent Kit 비공식 로드맵

**Solana Agent Kit 비공식 로드맵**
| 단계 | 주요 내용 | 상태 |
|------|-----------|------|
| v2 릴리즈 | 플러그인 기반 구조, LangChain/Vercel AI SDK 통합, zk airdrop 지원 | 완료 |
| 에이전트 모드 고도화 | 자율형 에이전트 반복 실행, 오류 복구, 멀티 액션 처리 | 진행 중 |
| 모바일/React Native 지원 | 모바일 환경에서 에이전트 실행 가능 | 일부 구현됨 |
| 임베디드 지갑 통합 | Turnkey, Privy 등과 연동하여 보안 강화 | 지원 중 |
| LangChain 평가 시스템(Evals) | 프롬프트 성능 벤치마크 내장 | 적용됨 |
| MCP Adapter 개발 | Claude Desktop 등 외부 AI와의 연동 | 개발 중 |
| 더 많은 프로토콜 통합 | Drift, Meteora, Adrena 등 디파이/선물 확장 | 지속 중 |
| SendAI 생태계 통합 | SEND 토큰, JupSOL, Arcade 등과 연계 강화 | 확장 중 |
| 테스트넷/시뮬레이션 환경 | 개발자용 테스트 환경 제공 예정 | 계획 단계 |


---

## 6. User Experience & Hands-on Review *(if applicable)*


### Solana Agent 예제 코드 (Balance Check)

```ts
import { SolanaAgentKit, createSolanaTools } from "solana-agent-kit";
import { createReactAgent } from "@langchain/langgraph/prebuilt";
import { ChatOpenAI } from "@langchain/openai";
import { MemorySaver } from "@langchain/langgraph";
import * as dotenv from "dotenv";
dotenv.config();

// LLM 설정
const llm = new ChatOpenAI({
  modelName: process.env.SOLANA_AGENT_OPENAI_MODEL || "gpt-4",
  temperature: 0.7,
  apiKey: process.env.OPENAI_API_KEY,
});

// SolanaAgentKit 인스턴스 생성
const agentKit = new SolanaAgentKit(
  process.env.SOLANA_PRIVATE_KEY!,
  process.env.RPC_URL || "https://api.mainnet-beta.solana.com",
  process.env.OPENAI_API_KEY!
);

// Solana 툴셋 생성
const tools = createSolanaTools(agentKit);

// 메모리 저장소 생성
const memory = new MemorySaver();

// Agent 생성
const agent = await createReactAgent({
  llm,
  tools,
  checkpointSaver: memory,
});

// 지갑 주소 입력
const walletAddress = "Wallet Address"; // 예: "9LKK..."

async function main() {
  const prompt = "내 솔라나 지갑 잔액 얼마나 돼?";
  console.log(`사용자 입력: ${prompt}`);

  const res = await agent.invoke({
    input: prompt,
    config: {
      metadata: {
        userId: "test-user-001",
        wallets: [{ address: walletAddress, chain: "solana" }],
      },
    },
  });

  console.log("Agent 응답:\n", res.output);
}

main();
```

### 탐색한 기능
- `SolanaAgentKit`을 활용해 Solana 지갑과 연결된 AI 에이전트 구성
- 사용자 프롬프트로 지갑 잔액 조회
- 전체 구성 흐름:
  1. OpenAI API 기반 LLM 설정
  2. LangChain Graph 기반 에이전트 생성
  3. Solana 도구 세트 통합
  4. 사용자 지갑 주소 기반 요청 처리

---

### 단계별 구현 과정

1. GitHub에서 `solana-agent-kit` 클론  
2. `.env` 파일에 환경 변수 설정  
   - 예: `SOLANA_PRIVATE_KEY`, `RPC_URL`, `OPENAI_API_KEY`  
3. `index.ts` 작성 및 프로젝트 디렉토리 구성  
4. 외부 패키지 수동 설치  
   - `solana-agent-kit`, `@langchain/openai`, `@langchain/langgraph`, `bs58` 등  
5. TypeScript 모듈 경로 문제 해결  
   - `tsconfig.json`에 `paths` 설정 추가  
   - VS Code TS 서버 재시작  
6. 구식 API → 신버전 API 마이그레이션  
   - `createAgent` → `createReactAgent`  
   - `Solana` → `SolanaAgentKit`, `createOpenAITools`  
7. 최종 실행: 지갑 주소 기반으로 잔액 질의 및 응답 확인  

---

### 온보딩 경험

- **난이도:** 중간~어려움  
- **이유:**  
  - 구버전(v1)과 신버전(v2) API가 문서상 혼용되어 있어 혼란  
  - 에러 메시지와 문서 사이에 괴리가 있음  

---

### 기존 서비스와의 차별점

- 자연어로 블록체인 데이터(지갑 잔액 등)에 접근 가능한 새로운 사용자 경험  
- 전통적인 non-blockchain API 서비스에 비해:  
  - **더 많은 설정 필요**  
  - **분산된 데이터 구조와 상호작용**  

---

### 잘 된 점 & 부족한 점

| 잘 된 점 ✅ | 부족한 점 ❌ |
|------------|--------------|
| 자연어 기반 사용자 인터페이스 | 복잡한 초기 환경 설정 |
| 지갑 연결 및 실시간 응답 처리 | API 버전 혼용으로 인한 디버깅 비용 |
| Langchain과 Solana를 매끄럽게 연결 | 문서화 부족으로 인한 학습 곡선 |

![image](https://hackmd.io/_uploads/ByMGZwsrxe.png)
![image](https://hackmd.io/_uploads/r1397worgl.png)

---

## 7. Why Blockchain

- 필요성: AI가 한 결정을 투명하게 기록하고, 나중에 누구든 검증할 수 있다.
- 전통 기술로는 불가능한 점: 스마트 컨트랙트 기반 실행, 거버넌스 및 경제적 동기 부여, 무허가 탈중앙 네트워크 접근

---

## 8. Insights & Limitations

### ✅ Key Takeaways
- 플러그인 구조로 AI 개발자들이 쉽게 확장 가능 
- 다양한 Solana 프로토콜을 포괄

### ⚠ Limitations / Open Questions
- 자체 인센티브 토큰 부재
- 고급 기능에 대한 문서 부족

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- LangChain과 Solana 연계가 생각보다 매끄러워 놀랐다.
- 앞으로 Web3에서 자율 에이전트 인터페이스가 얼마나 중요한지 체감할 수 있었다. 

### ❓ Discussion Questions
- AI가 지갑을 자율적으로 운영해도 될까?
- AI의 실수나 사고에 대한 책임은 누가 질까?

---

## 10. Insight from others

After each presentation in class, we will form small groups for each case for discussion. At that time, please discuss with your group the questions posed in Section 9, and write any key points or insights from your discussion group here.

---

## 11. References

- [Solana Agent Kit MCP Server](https://github.com/sendaifun/solana-mcp)
- [Introduction to Solana Agent Kit v2](https://docs.sendai.fun/docs/v2/introduction)
- [솔라나 AI 에코 시스템 개요](https://solana.com/ko/ai?form=MG0AV3)
