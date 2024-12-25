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
###  four_leaf_clover PPT

[RePick.pdf](https://github.com/user-attachments/files/18246060/RePick.pdf)

