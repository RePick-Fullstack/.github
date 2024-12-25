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
- **기술 스택:** React, Tailwind, CSS

#### 2. **Backend 서비스** (마이크로서비스)
- **User Service**: 사용자 인증 및 프로필 관리  
- **Payments Service**: Toss Payments 및 PlantiPay API를 통한 결제 처리  
- **RealTimeChat Service**: 실시간 채팅 기능 제공  
- **Community Service**: 유저 커뮤니티 게시판 관리
- **comment Service**: 유저 커뮤니티 댓글 관리  
- **News Service**: 최신 금융 뉴스 데이터 제공  
- **Report Service**: 금융 리포트 데이터 관리 및 제공  
- **ChatBotAPI Service**: GPT-4 mini 기반의 자연어 처리 챗봇  
- **기술 스택:** Spring, Kafka, MySQL, Kubernetes

#### 3. **DevOps 및 배포**
- Kubernetes 및 Helm을 활용한 애플리케이션 배포 자동화
- GitHub Actions를 통한 CI/CD 파이프라인 구축
- Docker로 마이크로서비스 컨테이너화

#### 4. **외부 결제 연동**
- Toss Payments 및 PlantiPay API를 활용하여 유료 리포트 구매 지원

---
### 🌵 PPT

![0-0](https://github.com/user-attachments/assets/cdc4f678-e56f-4eef-9e55-8f7084bb7650)
![0-1](https://github.com/user-attachments/assets/dbe83f39-b7cd-41b1-bb9a-d0e1fae61b31)
![0-2](https://github.com/user-attachments/assets/3baabee0-e3c7-4b28-9312-92d0fe3dc2b6)
![1-0](https://github.com/user-attachments/assets/3b976ddc-0ea2-459f-ba9c-fd86e318a375)
![1-1](https://github.com/user-attachments/assets/0f1f2cfa-cdcf-4f12-b1b5-0b25b94ba227)
![1-2](https://github.com/user-attachments/assets/3a4c3430-d2fd-4500-b6a1-6fa412974aa3)
![1-3](https://github.com/user-attachments/assets/68aeebea-dc8a-4c46-8a75-c9d3f82d1d3a)
![1-4](https://github.com/user-attachments/assets/034c645e-3546-4056-a6ae-c4266d33f873)
![1-5](https://github.com/user-attachments/assets/c173ac90-8ddc-4680-be52-a74b8a53683c)
![2-0](https://github.com/user-attachments/assets/fc318e81-4336-4c93-bfeb-9c1debe4c894)
![2-1](https://github.com/user-attachments/assets/226f2263-cd93-441d-8f65-83bcfb774782)
![3-0](https://github.com/user-attachments/assets/22d23fd9-d8d8-4111-9ac9-9c1500ef3000)
![3-1](https://github.com/user-attachments/assets/aaa290d5-a609-4517-9537-fb1ca48fc5f2)
![3-2](https://github.com/user-attachments/assets/7cc27ecb-950d-4fad-9fe3-230284ebaaf3)
![3-3](https://github.com/user-attachments/assets/26e7de27-47b2-4608-b965-7ea334740510)
![3-5](https://github.com/user-attachments/assets/1ee7597f-3300-4805-a38e-c897f1646c45)
![3-5-1](https://github.com/user-attachments/assets/7cceb030-5b9f-49d1-9751-00d7d20669ad)
![3-6](https://github.com/user-attachments/assets/8f22f2fb-31c7-4179-83e9-ba1358bedb00)
![3-7](https://github.com/user-attachments/assets/1c9101d0-805e-4b53-b628-3d988614819b)
![3-8](https://github.com/user-attachments/assets/1349a5f8-4c99-41ac-9f4f-b7ec79591655)
![3-9](https://github.com/user-attachments/assets/0885839d-627b-4f75-9913-eb4ea586f3e2)
![3-10](https://github.com/user-attachments/assets/6603f538-20ab-40dd-84b8-16a742379833)
![3-11](https://github.com/user-attachments/assets/a35d6844-2121-4fb3-b6ef-f326ea269ffa)
![3-12](https://github.com/user-attachments/assets/1ab055c4-f481-4835-9246-2710121c32dd)
![3-13](https://github.com/user-attachments/assets/591c79ec-6ca1-4e8a-8c9c-4131dba9fa46)
![4-0](https://github.com/user-attachments/assets/3f77f7bb-1c06-4788-a52f-a9932a6e5188)
![4-1](https://github.com/user-attachments/assets/13659e4d-a16a-48a9-84fc-fc2b302e685d)
![4-2](https://github.com/user-attachments/assets/f1bdd7bf-a4f7-4627-8b6f-b84df47ed9d2)
![4-4](https://github.com/user-attachments/assets/1425cbd7-dce9-4491-9383-f08774c1eacf)
![4-3](https://github.com/user-attachments/assets/76ab4adf-4426-4540-b8fa-d7511a1958be)
![5-0](https://github.com/user-attachments/assets/5e45c870-4bd1-43aa-bae2-00f1281ea367)
![5-1](https://github.com/user-attachments/assets/b7f5e890-53d9-407b-8710-cb29fd163a53)
![5-2](https://github.com/user-attachments/assets/4ad51f5e-9056-4165-b298-61433c22c876)
![5-3](https://github.com/user-attachments/assets/a35f248b-e59f-465b-a7f4-b514079cc8df)
![5-4](https://github.com/user-attachments/assets/34722fc8-bc8d-41d9-80ad-3e951bd76936)
![5-5](https://github.com/user-attachments/assets/668434b1-c876-4e35-b64c-3956d5ddd4f3)
