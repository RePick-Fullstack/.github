# RePick (Research Pick)

**금융 리포트 요약 및 개인화 챗봇 서비스**  
RePick은 금융권 애널리스트 리포트를 데이터베이스로 활용하여 유저들에게 효율적인 정보 제공과 개인화된 추천을 제공하는 스마트 챗봇 서비스입니다.

---

## 🛠️ 시스템 아키텍처

RePick의 시스템 아키텍처는 금융 리포트 제공과 개인화된 추천 기능을 중심으로 설계되었습니다. MSA(Micro Service Architecture)를 기반으로 하며 확장성과 안정성을 목표로 설계되었습니다.

---

### 📊 아키텍처 다이어그램

![Fullstack_RePick_아키텍처](https://github.com/user-attachments/assets/eb055bc8-712f-41ca-875d-90c810c4f4bd)


---

### 🔧 구성 요소 설명

#### 1. **Frontend 서비스**
- 사용자와 상호작용하는 웹 애플리케이션
- 주요 기능: 질문 입력, 결과 시각화, 리포트 다운로드
- **기술 스택:** React, Tailwind CSS

#### 2. **Backend 서비스** (마이크로서비스)
- **User Service**: 사용자 인증 및 프로필 관리  
- **Payments Service**: Toss Payments 및 PlantiPay API를 통한 결제 처리  
- **RealTimeChat Service**: 실시간 채팅 기능 제공  
- **Community Service**: 유저 커뮤니티 게시판 관리  
- **News Service**: 최신 금융 뉴스 데이터 제공  
- **Report Service**: 금융 리포트 데이터 관리 및 제공  
- **ChatBotAPI Service**: GPT-4 기반의 자연어 처리 챗봇 응답 생성  
- **기술 스택:** Spring, Kafka, MySQL, Kubernetes

#### 3. **DevOps 및 배포**
- Kubernetes 및 Helm을 활용한 애플리케이션 배포 자동화
- GitHub Actions를 통한 CI/CD 파이프라인 구축
- Docker로 마이크로서비스 컨테이너화

#### 4. **외부 결제 연동**
- Toss Payments 및 PlantiPay API를 활용하여 유료 리포트 구매 지원

---

### 📘 주요 흐름

#### 1. **사용자 요청 처리**
- 사용자가 질문을 입력하면 ChatBotAPI 서비스가 의도를 분석하고 적합한 답변을 생성합니다.
- 답변과 관련된 데이터는 Report Service와 News Service를 통해 제공됩니다.

#### 2. **데이터 스트리밍**
- Kafka를 활용하여 실시간 데이터 스트리밍 및 서비스 간 이벤트 동기화를 처리합니다.

#### 3. **개인화된 추천**
- User Service의 프로필 데이터를 기반으로 유저의 관심사에 맞는 금융 리포트를 추천합니다.

#### 4. **결제 및 커뮤니티**
- Toss Payments API를 통해 프리미엄 리포트 구매를 지원하며, Community Service를 통해 유저 간 정보 공유를 활성화합니다.

---

### 🖼️ 프론트엔드 화면

RePick의 사용자 인터페이스(UI)는 간단하고 직관적으로 설계되어 있습니다.

#### 1. **메인 화면**
사용자가 금융 리포트를 검색하고, 추천받는 화면입니다.  

<img width="1440" alt="RePick_main" src="https://github.com/user-attachments/assets/52f0dc51-33d8-465f-9dac-2aaf70d0c9f4" />


#### 2. **질문 입력 화면**
질문을 입력하고, GPT-4 기반의 답변을 받을 수 있는 화면입니다.  

<img width="1440" alt="RePick_chatbot_1" src="https://github.com/user-attachments/assets/5b91ee77-f49b-4511-88cf-4f94308de2f0" />
<img width="1440" alt="RePick_chatot_2" src="https://github.com/user-attachments/assets/d6c862a4-164e-416d-b419-416d5a6694a9" />


#### 3. **추천 리포트 화면**
개인화된 금융 리포트를 추천받는 화면입니다.  
<img width="1440" alt="RePick_recommend_main" src="https://github.com/user-attachments/assets/c98cb72f-0814-47d0-aed0-2d0dfa64928a" />



#### 4. **커뮤니티 화면**
사용자끼리 정보 공유하는 화면입니다.  

<img width="1440" alt="RePick_community" src="https://github.com/user-attachments/assets/84605fed-800c-4fca-a31a-5448eaa398eb" />



#### 4. **관리자 페이지**
서비스 운영자들이 데이터를 관리하고 통계를 볼 수 있는 화면입니다.  
<img width="1440" alt="RePick_admin_ ermission_management" src="https://github.com/user-attachments/assets/3a61aa16-a107-430f-b0d2-a18822f2dd5e" />
<img width="1440" alt="RePick_admin_MAU" src="https://github.com/user-attachments/assets/79cfc5f1-5576-42f7-b66b-0c5fc1835ede" />
<img width="1440" alt="RePick_admin_users" src="https://github.com/user-attachments/assets/4e0c3cda-52f2-408a-b2a0-da1cf8829031" />


---

### 💡 특징

- **확장성:** MSA 구조를 통해 독립적으로 확장 가능한 모듈 설계  
- **신뢰성:** Kafka로 안정적인 데이터 동기화 구현  
- **개인화:** 유저별 맞춤 리포트 추천 기능  
- **실시간성:** 실시간 채팅 및 최신 금융 정보 제공  

---

이 시스템 아키텍처는 **유저 경험 최적화**와 **서비스 품질 향상**을 목표로 설계되었으며, 지속적으로 업데이트 및 개선되고 있습니다.
