# 📄 Grass  
### 👤 Author: [Jason Han](https://www.linkedin.com/in/jaesunhan/)  
### 📆 Presentation Date: [2025-07-02]  

---

## 1. Overview

- **Project Name**: Grass  
- **Category**: Decentralized AI Infrastructure
- **Key Technologies / Platforms**: ZK proof, Sovereign Rollup, Reputation Scoring, Solana  
- **Official Links**:
  - Website: https://www.grass.io/
  - Foundation: https://www.grassfoundation.io/
  - Contract Address:  [Grass7B4RdKfBCjTKgSqnXkqjwiGvQyFbuSCUJr3XXjs](https://solscan.io/token/Grass7B4RdKfBCjTKgSqnXkqjwiGvQyFbuSCUJr3XXjs) (Solana)
  - Whitepaper: N/A
  - Docs: https://grass-foundation.gitbook.io/grass-docs 
  - GitHub: N/A
  - X: https://x.com/grass

### 📌 Summary  
Briefly describe what problem this project is solving and how it is using blockchain to solve the problem. Then summarize the project's achievements and key takeaways.

---

## 2. Background & Problem Statement

### AI 모델 개발과 데이터 수집
LLM과 같은 AI 모델을 개발하기 위해서는 엄청난 규모의 데이터가 필요하다. 이러한 데이터를 수집하고 정제하고 학습을 위해 토큰화하는 과정에 많은 시간이 소요된다. 트랜스포머의 등장으로 라벨링 데이터가 필요없는 비지도 학습이 가능해 졌다고 하지만, 최신의 정보를 기반으로 학습과 추론하기 위해서는 실시간 웹 크롤링이 여전이 중요한 과제다.

### 웹 크롤링 현황
2025년 웹 크롤링 시장 규모는 10억3천만 달러이며, 연 평균 14% 성장이 예상되는 만큼 활발하다. 아래는 [웹 크롤링 시장 리포트](https://thunderbit.com/blog/web-crawling-stats-and-industry-benchmarks)에서 정리한 지표들이다.
- 전 세계 기업 65%가 웹 크롤링 또는 데이터 추출 기술을 도입
- 이커머스 분야가 가장 적극적이며 웹 스크래핑 사용자의 48%가 이커머스 분야
- 65% 조직이 크롤링된 데이터를 AI 학습과 분석에 활용
- 웹의 약 80-90%가 비정형 데이터
- 웹 트래픽의 약 절반(49.6%)은 봇에 의한 것
- 전체 웹사이트의 약 43%가 CAPTCHA나 Cloudflare와 같은 봇 방어 기술을 적용 중

### 웹 크롤링 방지 기술의 확대
앞의 보고서에서도 언급되었지만, 43% 사이트가 봇 방어 기술을 적용하고 있다. Cloudflare, CAPTCHA, IP 제한, JavaScript 기반 렌더링 등 다층적인 접근 제어가 일반화되고 있어 일반적인 크롤링 툴(예: Python의 requests, scrapy)은 다수의 사이트에서 차단되고 있다. 특히, 데이터센터 IP 주소의 경우 웹사이트들로 부터 차단되는 경우가 많다.

### 웹 크롤링 기업 현황
| 기업명                                     | 본사    | 특징 / 주요 서비스                            |
| --------------------------------------- | ----- | -------------------------------------- |
| **Bright Data** (구 Luminati)            | 이스라엘  | 최대 규모. **프록시+크롤링 API**. 수많은 타겟 웹사이트 지원 |
| **ScrapingBee**                         | 프랑스   | 헤드리스 브라우저 기반 크롤링 API. JS 렌더링 가능        |
| **Zyte** (구 Scrapy Cloud / Scrapinghub) | 아일랜드  | Scrapy 오픈소스 기반. 크롤링-as-a-service       |
| **Oxylabs**                             | 리투아니아 | 대규모 프록시 네트워크 + 기업용 데이터 수집 솔루션          |
| **SerpApi**                             | 미국    | Google 검색 결과 크롤링 특화. Captcha 우회 내장     |
| **Diffbot**                             | 미국    | AI 기반 웹 구조 분석 → JSON 데이터 추출            |
| **Webz.io**                             | 이스라엘  | 다크웹·오픈웹 모니터링 등 특수 목적 크롤링               |

이들이 데이터를 크롤링 하는 방식은 다음과 같다. 대부분 중앙화된 방식으로 웹 크롤링 방지 기술을 우회하는 방법을 사용하고 있다. 
| 방법               | 설명                                  |
| ---------------- | ----------------------------------- |
| **프록시 네트워크 사용**  | IP 차단 회피를 위해 수백만 개의 프록시 IP 활용       |
| **헤드리스 브라우저**    | Puppeteer, Playwright 등으로 JS 렌더링 대응 |
| **Captcha 우회**   | 자동화된 Captcha 해결 또는 인간 입력 서비스 연동     |
| **AI 기반 파싱**     | DOM 구조가 바뀌어도 AI가 주요 콘텐츠 자동 추출       |
| **API Wrapping** | 검색결과/뉴스/쇼핑 페이지 등을 REST API처럼 가공 제공  |


---

## 3. How It Works

### 🔍 3.1 Project Approach  
Grass는 탈중앙화된 웹 크롤링 네트워크를 구축한다. 일반 사용자들의 컴퓨터나 휴대폰에 웹 크롤링 노드를 설치해 크롤링하는 것이다. 참여자들은 유휴 인터넷 대역폭을 제공하고 Grass는 보상으로서 토큰을 제공한다. 이때 참여자 노드는 Residential IP이기 때문에 일반 사용자로 인식하여 IP 차단이 되지 않고 크롤링할 수 있는 것이다. 전 세계 노드를 통해 수집된 비정형 데이터는 AI 학습에 적합한 구조화된 데이터셋으로 변환해서 제공된다. 

[2025년 1월 기사](https://beincrypto.com/grass-unveils-2025-roadmap-what-you-need-to-know/)에 따르면 Grass는 1년만에 빠른 성장을 한 것을 알 수 있다.
| 항목           | 수치/설명                      |
| ------------ | -------------------------- |
| 사용자 수 (2024) | 20만 → 300만 (15× 증가)        |
| 비디오 인덱싱 규모   | 1000× 증가                   |
| 분배된 토큰 총량    | \$196M / 220만 명 이상         |
| 네트워크 효율 개선   | Sion Phase 1을 통해 60× 개선    |
| 토큰 가격        | 발표 직후 약 2.5% 상승, \$2.82 수준 |



---

### 🏗️ 3.2 Architecture  

![Architecture](https://grass-foundation.gitbook.io/grass-docs/~gitbook/image?url=https%3A%2F%2F4200124-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FVuFE5nRztwdZPBWH5NLC%252Fuploads%252F2QOjUX7BmbhyGAU1u6vK%252FGrass%2520Graphic%2520flow%2520%282%29.png%3Falt%3Dmedia%26token%3D93571a11-10f9-470f-af0e-4e298f00793e&width=768&dpr=4&quality=100&sign=d858da95&sv=2)

Grass 아키텍처는 크게 Validator, Router, Grass Node, Zk Processor, Data Ledger, Edge Embedding Models의 계층 구조로 이루어져 있다. 이 중 Validator, Router, Grass Node가 크롤링에 참여하고, 나머지는 데이터 증명과 전처리 작업을 한다. 

- **Validator**
  - 웹 요청을 시작하고, 노드의 트랜잭션을 검증해 ZK 증명을 생성
  - 초기에는 단일 구조지만, 향후 탈중앙화된 위원회로 전환 예정
- **Router**
  - Grass Node와 Validator 사이에서 요청을 중계하고 대역폭을 관리
  - 처리량 기준으로 보상 받음
- **Grass Node**
  - 사용자 기기에서 실행되며 웹 데이터를 수집
  - 암호화 요청을 처리하고, 트래픽을 라우터로 반환하며 평판 점수 기반으로 보상 받음 
- **Zk Processor**
  - 모든 세션의 **유효성 증명(ZK proof)**을 작성해 Layer‑1 블록체인(Solana)에 제출
  - 웹 크롤링 내역이 불변 증명으로 기록 
- **Grass Data Ledger**
  - 처리된 데이터와 on‑chain 증명을 연결한 불변 데이터 저장소 
- **Edge Embedding Models**
  - 수집된 비정형 웹 데이터를 전처리하여, AI 학습에 적합한 형식으로 정제

---

### 🎯 3.3 Core Components  

#### Validator
- 네트워크의 핵심 역할 중 하나로, 웹 요청을 시작하고 트랜잭션을 검증하는 두 가지 주요 역할을 수행
- TLS 연결을 위해 자체 키를 사용하여 다양한 암호화 알고리즘(AEAD, RSA, ChaCha20 등) 중 하나를 선택해 사용
- 세션 기반으로 pre-master, master, session 키를 안전하게 관리하며, 이를 통해 노드 트래픽 품질을 평가
- 검증이 완료된 세션 데이터는 ZK Processor로 전달되어 증명 생성 및 온체인 기록을 위한 배치 처리
- 현재는 단일 주체인데, 장기적으로는 경제적 담보를 지닌 여러 검증자가 참여하는 구조로 전환 예정

#### Router
- 지리적으로 분산된 허브(hub)로, Grass Node와 Validator 간의 연결을 중계하는 역할
- 네트워크 전체의 연결 상태를 유지하면서, 모든 입·출력 웹 요청을 Validator로 전달 및 관리
- 각 요청/응답의 바이트 수(size), 노드 및 Validator와의 지연 시간(latency), 연결 상태(connection health) 등의 메트릭을 Validator에 보고
- 스테이킹된 토큰 양에 비례하여 보상 받음
- 네트워크에 연결된 노드의 신뢰성 검증 및 상태 유지 책임있음
- 75% 이상 연결 유지 요구 조건을 충족하지 못하면, 스테이킹 자산 일부가 벌금(slashing)으로 차감될 수 있음

#### Grass Node
- 노드 운영자는 자신의 유휴 인터넷 대역폭을 제공하며, 이를 통해 발생한 트래픽에 대해 토큰으로 보상을 받음
- 공개 웹사이트에서 받은 응답을 암호화해 Router로 다시 전달함
- 설치가 간단하며, 설치 후 연결이 완료되면 자동으로 네트워크에 등록되며, 24시간 가동
- 노드는 사용자의 개인 활동에는 접근하지 않음
- 오직 공개 웹사이트 트래픽만 중계하며, 개인 데이터는 처리하지 않음
- 네트워크에서 토큰 보상을 받기 위해서는 Reputation Score가 중요함

| 평가 항목            | 설명                   |
| ---------------- | -------------------- |
| **Completeness** | 데이터가 얼마나 완전한지 평가     |
| **Consistency**  | 시간 및 요청 간 데이터 일관성 여부 |
| **Timeliness**   | 최신성이 유지되는지 여부        |
| **Availability** | 응답의 지속 가능성 평가        |


---

### 🔁 3.4 Workflow Overview  
![seq_diagram](https://hackmd.io/_uploads/rkCl2d-Sxg.png)


1️⃣ **클라이언트의 크롤링 요청을 Grass Node까지 전달**
1. 클라이언트가 크롤링 요청을 암호화하여 Validator에 전달
1. Validator는 요청을 검증한 뒤 적절한 Router에게 전달
1. Router는 요청을 적절한 Grass Node로 라우팅

2️⃣ **Grass Node에 의한 웹 요청 및 응답 수집**
1. Node는 받은 암호화된 요청을 탈암호화하여 웹사이트에 실제 접속
1. 웹사이트로부터 응답(데이터/HTML)을 수신
1. Node는 받은 응답을 암호화하여 Router를 통해 Validator로 전달

3️⃣ **ZK Processor → Layer‑1 블록체인**
1. 일정 수 이상의 웹 세션이 모이면 ZK Processor가 세션 데이터를 취합
1. ZK 기술을 이용해 Zero-Knowledge 증명(ZK proof)을 생성
1. 생성된 증명은 Layer‑1 블록체인(예: Solana)에 제출되어 세션 무결성이 입증

4️⃣ **데이터 전처리 및 저장**
1. 웹 콘텐츠와 증명은 Grass Data Ledger에 연결되어 불변 구조로 저장
1. Edge Embedding Models가 데이터를 정형화 + 정제하여 AI 학습용 형식으로 변환

---

## 4. Token Economy *(if applicable)*

### [Funding & TGE(Token Generation Event)](https://icodrops.com/grass/)
23년 12월 Seed Round 투자로 $3.5M을 받았고, 24년 9월 Series A 투자를 받은 후 10월에 TGE를 단행했다. Listing price는 $0.87이었고, 현재 $0.97이다. 투자자는 아래와 같다. 

![Investors](https://hackmd.io/_uploads/HJ33j4-Sxg.png)

### [Grass Token Status](https://coinmarketcap.com/currencies/grass/)
아래는 Coinmarketcap의 GRASS 토큰 현황입니다. 토큰 총 발행량은 10억개가 될 것이며, 현재 유통량(발행량)은 2.4억개이다. 토큰 하나의 가격은 $0.97이며 시가총액은 $237M이며, 현재 Coinmarketcap 순위는 165위이다. (시가총액기준) 만약 전체 토큰이 발행된다면(10억개) 시가총액은 $972M이 될 것이다. (FDV, Fully-Diluted Value)
![GRASS](https://hackmd.io/_uploads/S1cF34ZBlg.png =50%x)



### [GRASS Token Supply](https://grass-foundation.gitbook.io/grass-docs/introduction/grass/grass-tokenomics)
10억개 토큰에 대한 분배 계획은 아래 다이어그램과 같다. 
![Token Allocation](https://grass-foundation.gitbook.io/grass-docs/~gitbook/image?url=https%3A%2F%2F4200124-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FVuFE5nRztwdZPBWH5NLC%252Fuploads%252FzkFX1OTX1H6tiP0KPRBM%252Fimage%2520%2831%29.png%3Falt%3Dmedia%26token%3D1afd78d4-6025-45e6-9410-36ac71c6fc02&width=768&dpr=4&quality=100&sign=29125241&sv=2)

현재 2.4억개가 발행되었는데, 앞으로 순차적으로 공급되고 분배되어 총 10억개까지 공급될 예정이다. 공급/유통 스케쥴은 다음과 같다. 
![Circulating Schedule](https://grass-foundation.gitbook.io/grass-docs/~gitbook/image?url=https%3A%2F%2F4200124-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FVuFE5nRztwdZPBWH5NLC%252Fuploads%252FWPzZrO7szpF9s41IK3aL%252Fb4rveds54gref.png%3Falt%3Dmedia%26token%3D6f4d53c2-1bed-469e-af3b-19f7b0505c16&width=768&dpr=2&quality=100&sign=3d5e0c4&sv=2)

### [Grass Airdrop One](https://grass-foundation.gitbook.io/grass-docs/introduction/grass/grass-airdrop-one)
서비스 초기 사용자 유치를 위해 토큰 에어드롭 이벤트를 한다. Grass의 경우 1억개(총 발행량의 10%)를 초기 기여자들에게 에어드롭했다. 에어드롭 기간을 9개의 Epoch로 나누고 각 Epoch마다 획득한 Grass Points에 따라 Tier를 나누고 각 Tier별로 다르게 분배했다. 

![Epoch allocation](https://grass-foundation.gitbook.io/grass-docs/~gitbook/image?url=https%3A%2F%2F4200124-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FVuFE5nRztwdZPBWH5NLC%252Fuploads%252Fsd6YM3WefanJLN3gImae%252FFrame%25201597883803.png%3Falt%3Dmedia%26token%3D5019490a-964c-45f4-9c2e-08fc2cfbef9f&width=768&dpr=2&quality=100&sign=ff9978ec&sv=2 =50%x)

![Tier allocation](https://grass-foundation.gitbook.io/grass-docs/~gitbook/image?url=https%3A%2F%2F4200124-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FVuFE5nRztwdZPBWH5NLC%252Fuploads%252FFa6wSdRRXMpFruOdu914%252FFrame%25201597883805.png%3Falt%3Dmedia%26token%3D49702008-7f97-4f38-9285-2330f5142082&width=768&dpr=2&quality=100&sign=9b848bd9&sv=2)

### [Grass Points](https://grass-foundation.gitbook.io/grass-docs/how-to-guide/grass-points)
인터넷 bandwidth를 제공한다고 바로 Grass 토큰을 받는게 아니다. Grass 포인트를 받는다. 그리고 Epoch이 끝나면 쌓은 포인트에 따라 토큰이 분배되는 방식이다. Epoch의 기간은 정해져 있지만, Epoch에 얼마의 토큰이 분배되는지는 정해져 있지 않다. 

포인트를 받는 방법은 1) 인터넷 bandwidth를 제공하거나, 2) 다른 사람을 초대하는 것이다. 여기서 다른 사람을 초대하는 경우 첫 번째 초대자(Primary Referrals)가 받은 포인트의 20%를 받게 되고, 그 초대자가 다른 사람을 다시 초대하는 경우(Secondary Referrals) 새로운 초대자가 받은 포인트의 10%를 받게 된다. 이후 3차 수준 초대자 포인트의 5%를 받게 된다. 이런 Referral 포인트는 초대자가 서비스를 유지하는 동안 계속 받게 된다. 

그리고 Referral 수나 누적 포인트에 따라 Iron부터 Titan까지 10개 Tier 중 하나에 속하며 그에 따라 보너스 포인트를 받게 된다.  

### [Grass Staking](https://grass-foundation.gitbook.io/grass-docs/introduction/grass/grass-staking)

받은 Grass 토큰은 Router에 스테이킹해서 이자를 받을 수 있다. 아래 그림은 스테이킹 화면인데, 연이율(APR, Annual Percentage Rate) 35%의 보상이 주어지는 것을 볼 수 있다. 이것은 다른 스테이킹 서비스에 비해 매우 높은 수준인데, 이것이 어떻게 가능할지 살펴봐야 한다. Grass 토큰으로 보상이 주어지는데 이 토큰은 어디서 오는걸까? 토큰 이코노미에 인플레이션이 없었기 때문에 총 발행할 물량의 일부가 보상으로 지급되는게 아닐까 추측해 볼 수 있다. 서비스 초기이기 때문에 높은 APR로 Grass 토큰을 스테이킹하도록 유인해서 유통량을 줄이고 가격을 방어하기 위한 전략으로 보인다. 하지만, 충분한 토큰이 스테이킹되면 보상을 낮출 것으로 예상된다. 

![Grass Staking](https://hackmd.io/_uploads/ByQZDr-Heg.png)


---

## 5. Project Status & Impact

### [Grass Dashboard](https://www.grassfoundation.io/network/stats)

Grass 네트워크 현황을 볼 수 있는 대시보드를 제공한다. 하루 800 TB 이상의 데이터가 수집되고 있다.
![image](https://hackmd.io/_uploads/SyUdsBWHeg.png)
![image](https://hackmd.io/_uploads/rkDAiS-rgl.png)
![image](https://hackmd.io/_uploads/ByxoFLZrgl.png)

### [Sion Upgrade](https://x.com/grass/status/1886541454664974807)
25년 2월 Sion 2단계 업그레이드를 통해 컴퓨팅 자원을 수평적으로 확장하며, 네트워크 처리량을 10배 향상시키고, 페타바이트 규모에서 실시간 멀티모달 데이터 스크래핑(예: 4K 비디오 데이터 등)을 지원한다. 기술적인 핵심은 스크래핑 알고리즘을 최적화하고 워크로드를 여러 노드로 분산해 병렬 처리함으로써 처리량을 늘리고 스크랩핑 속도를 빠르게 한 것이다. 이로써 대용량 처리가 필요한 멀티모달 데이터를 수집하고 처리할 수 있게 되었고, 멀티모달 AI 개발에 데이터를 공급할 수 있게 되었다.

![Q1 Performance](https://pbs.twimg.com/media/GnibPjhbMAA2Ui2?format=jpg&name=large)

---

## 6. User Experience & Hands-on Review *(if applicable)*

### Grass Node 사용자 인터페이스
설치 후 Node 프로그램 UI는 아래와 같이 심플하다. 네트워크와 연결하는 버튼과 획득한 포인트를 보여준다.
![image](https://hackmd.io/_uploads/SksVxK-rxx.png =50%x)

대신 자세한 내용은 웹사이트 대시보드를 보면 확인할 수 있다. 일간 수익 통계, 접속한 네트워크 이력, 추천 프로그램 현황과 Tier, 리워드 현황을 확인할 수 있다.
![image](https://hackmd.io/_uploads/BJNxzK-Bee.png)
![image](https://hackmd.io/_uploads/SkvHfF-Slx.png)
![image](https://hackmd.io/_uploads/BkqtfF-Bee.png)

### 지갑과 이메일 인증 과정
3단계로 인증 과정이 일어난다.
1. 이메일 인증
1. 지갑 인증 (Solana 지갑)
1. 이메일에서 지갑 인증 (주소가 누구랑 연결된건지 확인)

![스크린샷 2025-07-01 오후 4.14.15](https://hackmd.io/_uploads/rJmu7tWrle.png =60%x)
![스크린샷 2025-07-01 오후 4.13.42](https://hackmd.io/_uploads/ry3YXKZBxg.png =60%x)

### 사용 후기
- 설치와 실행이 매우 쉬움
- 대시보드 역시 어렵지 않고 직관적임
- 특히, 레퍼럴 프로그램에 신경 많이 쓰고 집중하는 느낌
- 인증 과정도 수월하게 진행



---

## 7. Why Blockchain

[The official documentation](https://grass-foundation.gitbook.io/grass-docs/introduction/grass) describes the need for blockchain as follows.
[공식문서](https://grass-foundation.gitbook.io/grass-docs/introduction/grass)는 블록체인의 필요성을 다음과 같이 설명한다.

- **Transactional Efficiency**: Global settlement in over 190 countries is both easier and better on-chain than it is off-chain.
> With participants scattered across the globe and small amounts to be paid to them, using traditional money transfer systems is not only inefficient, it's impossible.
> 참여자들이 전 세계에 흩어져 있고, 그들에게 지불해야 하는 금액이 소액이라 전통적인 송금 시스템을 이용하는 것은 비효율적일 뿐만 아니라 불가능하다. 

- **Transparency**: Proofs of each transaction being posted on-chain provides empirical evidence that rewards are being equitably distributed. It also provides transparency with respect to the verification of data provenance.
> On-chain is the best way to ensure that everyone can verify that the distribution of tokens based on contributions is fair. And to verify the source and path of data, it should be transparently recorded on-chain.
> 기여에 따른 토큰의 분배가 공정히 되었는지를 모두가 확인하려면 on-chain이 가장 적합하다. 그리고 데이터의 출처와 경로를 검증하기 위해서는 on-chain에 투명하게 기록해야 한다. 

- **User Ownership**: Users should own their contributions to the internet, otherwise they will continue to be exploited by large tech companies.
> In a typical big tech company, users don't know about their contributions, can't claim them, and can't be compensated for them. However, your contributions should belong to you. This requires a blockchain-based way to record and control contributions.
> 일반적인 빅테크 기업에서 사용자는 자신의 기여를 알수도 없고 주장하거나 보상 받을 수 없다. 하지만, 사용자의 기여는 사용자의 소유가 되어야 한다. 그러기 위해서는 블록체인 기반으로 기여를 기록하고 사용자가 통제할 수 있어야 한다. 

---

## 8. Insights & Limitations

### ✅ Key Takeaways
- What did this project do right?  
- What important lessons or patterns can we learn from this project?

### ⚠ Limitations / Open Questions
- Validator와 Router가 아직 분산되어 운영된다는 언급이나 증거가 없다. 사람들의 유휴 네트워크 자원을 이용한다는 측면에서 탈중앙화가 이뤄지긴 하지만, 운영 시스템(Validator와 Router)은 아직 중앙화된 구조인 것 같다. 
- Validator를 탈중앙화하는 이유는 중앙의 운영주체를 없애기 위함인 것 같은데, 
- 보상을 극대화 하기 위해 Node를 악의적으로 운영할 수 있기 때문에 Node Reputation Scoring이 중요한 요소이다. 하지만, 문서에서는 어떤 정책으로 노드의 평판을 평가하겠다는 정책만 있고 측정하는 방법은 제시되어 있지 않다. 예를 들어 응답 데이터의 Completeness를 어떻게 측정할 것인지가 불분명하다. 크라우드소싱 방식으로 데이터 수집할 때 가장 어려운 부분이다. 악의적인 노드가 데이터를 변조하거나 가짜 데이터를 응답한다면 이를 검증하는 부분이 필요하다.  

---

## 9. Reflections & Discussion

### 💡 Personal Reflections
- What did you find most interesting or surprising?  
- How has your understanding of AI/blockchain changed after studying this?

### ❓ Discussion Questions
- [Thought-provoking question to ask during class]  
- [Optional: comparison to other projects in this space]

---

## 10. References

- [4pillars Grass Report (KR)](https://4pillars.io/ko/articles/ais-biggest-grassroots-moment)
- [4pillars Grass Report (EN)](https://4pillars.io/en/articles/ais-biggest-grassroots-moment)
- 
