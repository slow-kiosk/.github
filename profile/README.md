# "천천히 말씀하셔도 괜찮아요, 느린 키오스크"
<img width="519" height="398" alt="2025_AI 라이프 솔루션 챌린지" src="https://github.com/user-attachments/assets/0a3ce870-f939-414a-99ea-ad71da084120" />
<br>

## 📝 프로젝트 소개


**느린 키오스크**는 디지털 기기 사용에 익숙하지 않은 고령층과 디지털 소외 계층을 위해 설계된 **AI 음성 대화형 키오스크 서비스**입니다.<br>
복잡한 화면 터치 대신, 사람에게 말하듯 자연스러운 대화로 주문을 완료할 수 있는 환경을 제공합니다.

### 기획 배경
 **디지털 격차 심화**: 식당, 카페 등의 키오스크 도입이 늘어나면서, 기기 사용법을 모르는 고령층의 불편함이 가중되고 있습니다.<br>
 **심리적 부담감**: "사용법을 몰라 헤매는 동안 뒷사람의 눈치가 보인다"는 이유로 키오스크 사용 자체를 포기하는 사례가 많습니다.<br>
 **복잡한 UI와 시각적 혼잡(Visual Crowding)**: 작은 글씨, 복잡한 선택 옵션,<br>
 매장마다 제각각인 UI는 노안이나 인지 기능이 약화된 사용자에게 큰 진입 장벽입니다.<br>

### 솔루션

- **대화형 주문 (Voice First)**
  - “따뜻한 아메리카노 한 잔 줘”처럼 평소 식당에서 주문하듯 말하면, AI가 의도를 파악해 메뉴를 인식하고 장바구니를 구성합니다.
- **직관적인 화면 구성**
  - 큰 글씨, 명확한 색 대비, 단순화된 레이아웃으로 시각적 혼잡을 줄이고 필요한 정보만 단계별로 보여줍니다.
- **실시간 시각 피드백**
  - 사용자가 메뉴나 재료를 말하면 화면에 해당 메뉴/옵션이 장바구니에 쌓이는 모습을 시각적으로 보여줘, 주문 상태를 쉽게 확인할 수 있습니다.
- **표준화된 경험 제공**
  - 어느 매장을 가더라도 “말로 주문하는” 동일한 경험을 제공하여, 새로운 매장에서도 추가 학습 없이 사용할 수 있습니다.
<br>

## 🔗 배포 및 테스트 정보

 **프로젝트 기간** :2025.11.12 ~ 2025.12.02

* **배포 URL** : [https://slow-kiosk-frontend.vercel.app/](https://slow-kiosk-frontend.vercel.app/)

* ### 테스트 환경 가이드

- **마이크 및 카메라 권한 허용**
  - 브라우저 최초 진입 시 마이크·카메라 권한을 허용해야 음성 주문 및 바코드 스캔 기능이 정상 작동합니다.
- **해상도**
  - FHD 세로형 키오스크(1080 x 1920)에 최적화되어 있습니다.
  - 브라우저 개발자 도구의 Device Toolbar를 활용해 1080 x 1920 해상도로 테스트하는 것을 권장합니다.

<br>

## 👨‍👩‍👧 팀원 구성

|                                   백민근                                   |                                   이서현                                   |                                   정용진                                   |
| :------------------------------------------------------------------------: | :------------------------------------------------------------------------: | :------------------------------------------------------------------------: |
| <img src="https://via.placeholder.com/150" width="100px" alt="profile1" /> | <img src="https://via.placeholder.com/150" width="100px" alt="profile2" /> | <img src="https://via.placeholder.com/150" width="100px" alt="profile3" /> |
|                      [@GithubID](https://github.com/)                      |                      [@GithubID](https://github.com/)                      |                      [@GithubID](https://github.com/)                      |
|                            **Back-end & Infra**                            |                           **Front-end & Back-end**                            |                               **AI & Data**                                |



  
<br>


## 🛠️ 개발 환경

| 분류 | 기술 스택 |
| :-- | :-- |
| **Front-end** | <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=black"/> <img src="https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white"/> |
| **Back-end** | <img src="https://img.shields.io/badge/Spring_Boot_3.x-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/H2-1f425f?style=flat-square"/> <img src="https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white"/>|
| **AI** | <img src="https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white"/> |

### 🖥️ Front-end
* **Framework**: React
* **Communication**: Axios (REST API), WebSocket (실시간 음성/데이터 스트리밍)
* **Key Features**: 
    * 사용자 음성 녹음 및 서버 전송
    * 서버로부터 수신한 오디오(TTS) 재생
    * 음성 인식 결과에 따른 장바구니 실시간 UI 업데이트

### ⚙️ Back-end
* **Framework**: Spring Boot 3.x
* **Architecture**:
    * **Spring Web (MVC)**: 메뉴 조회 및 최종 주문 처리, 전반적인 비즈니스 로직 수행
    * **Spring WebSocket (STOMP)**: 프론트엔드와 JSON 데이터 및 상태 실시간 양방향 통신
    * **Spring WebFlux (WebClient)**: STT/LLM/TTS 등 외부 AI API의 비동기/병렬 호출 처리
* **Data Access**: Spring Data JPA, MySQL (메뉴 데이터 및 주문 이력 관리)
* **Validation**: Spring Validation (주문 데이터 무결성 검증)
* **Utils**: Lombok, Jackson

### 🤖 AI Service Pipeline
- **입력**
  - 사용자 음성 → 텍스트(STT)
  - 현재 화면 상태(scene), 장바구니(cart), 메뉴 정보(menu[])
- **처리**
  - LLM 기반 자연어 이해: 메뉴/옵션/수량 인식, 질문 의도 파악
  - 메뉴 CSV/DB에서 내려온 **재료(ingredients)**, **커스터마이즈 옵션(customizable)**,  
    **영양 정보(kcal, 단백질/지방/당/나트륨 등)**, **알레르기 정보(밀/대두/우유/계란/소고기/돼지고기/새우 등)** 를 함께 참조
- **출력 예시**
  - “이 메뉴는 칼로리가 어느 정도인지”, “우유 알레르기가 있으면 괜찮은지” 등의 질문에 대한 설명
  - 현재 상황에 맞는 **메뉴 추천, 성분/영양 설명, 알레르기 주의 안내, 야채/소스 커스터마이즈 제안**
  - 다음 단계로 이동할지 여부 및 화면 전환 안내

<br>


## 📲 페이지별 기능

### 1. 메인 키오스크 화면 (`KioskView`)

| 키오스크 모드 선택 | 메인 화면 |
| :---: | :---: |
| <img width="170" alt="키오스크 모드 선택" src="https://github.com/user-attachments/assets/dbe5d594-9153-435e-b3ef-dffef6473119" /> | <img width="170" alt="느린 키오스크 메인 화면" src="https://github.com/user-attachments/assets/802b8faf-6825-4045-b726-7b62ba9ab193"> |



**메인 화면 (`/`, `/kiosk`)**<br>
  - 새 사용자가 진입하면 기존 주문/대화 데이터를 초기화하고 환영 메시지를 표시합니다.
  - **느린 키오스크 모드 / 일반 키오스크 모드** 선택이 가능하며, “주문 시작하기” 버튼으로 주문 플로우를 시작합니다.
  - “사용자 맞춤” 버튼을 통해 접근성 설정 화면으로 이동할 수 있습니다.

| 사용자 맞춤 | (고대비 모드) | (글자 크기 조절) | (색약 모드) |
| :---: | :---: | :---: | :---: |
| <img width="170" alt="사용자 맞춤 설정" src="https://github.com/user-attachments/assets/4633fd8b-8614-44e7-81ce-e9a507f20ca0"> | <img width="170" alt="사용자 맞춤 설정 - 고대비 모드" src="https://github.com/user-attachments/assets/c555932c-0d52-46e4-881c-013ee9895d34"> | <img width="170" alt="사용자 맞춤 설정 - 글자 크기 조절" src="https://github.com/user-attachments/assets/cf2e8ecf-8524-4793-98d4-6c7340e213eb"> | <img width="170" alt="사용자 맞춤 설정 - 색약 모드" src="https://github.com/user-attachments/assets/511329f1-6785-4108-a9b9-90e0debb4340"> 

**사용자 맞춤 설정 (`/global`)**<br>
  - **고대비 모드, 글자 크기(1x / 1.5x), 색약 모드** 등을 토글로 설정할 수 있습니다.
  - 설정 값은 전역 상태로 관리되어 이후 모든 화면에 동일하게 적용되어, 한 번만 설정하면 계속 유지됩니다.

<br/>

### 2.  이용 방식 및 결제 방식 선택 (`PaymentView`)

|                                       이용/결제 방식 선택                                       |
| :---------------------------------------------------------------------------------------------: |
| <img width="170" alt="결제 선택 - 기프티콘" src="https://github.com/user-attachments/assets/2c63f6bf-f4fa-468b-9e64-4b322cba9208" /> |

**경로**: `/payment`<br>
**주요 기능**<br>
  - **서비스 타입 선택**: 포장(`takeout`) / 매장 식사(`dineIn`)를 버튼 또는 음성으로 선택
  - **결제 수단 선택**: 카드 / 모바일 / 기프티콘
    - “카드”, “모바일”, “기프티콘” 등 직관적인 음성 명령을 인식
  - **기프티콘 바코드 스캔**
    - 카메라 권한 요청 후, 바코드 캡처 → 인식 → 해당 기프티콘 메뉴를 자동으로 장바구니에 추가
  - 선택 결과에 따라 **바로 결제 화면(CheckoutView)** 또는 **주문 화면(OrderingView)** 으로 이동

<br/>

### 3. 음성 주문 & AI 대화형 주문 화면 (`OrderingView`)

|  음성 주문 & AI 대화   | (글자 1.5배 + 노년층 주문) | (아이를 위한 메뉴 추천) | (다이어트 및 알레르기 주문) |
| :---: | :---: | :---: | :---: |
| <img width="170" alt="메뉴 주문" src="https://github.com/user-attachments/assets/4d755038-d691-4d78-acae-94c9cdf7ceea" /> | <video src="https://github.com/user-attachments/assets/5e9f4bc8-9305-42e4-9e2e-54801e5eeed1" width="170" alt="글자 1.5배 + 노년층 주문" controls /> |
| <video src="https://github.com/user-attachments/assets/6bef175c-adfa-4b9f-b811-9fb8332822bb" width="170" alt="아이를 위한 메뉴 추천" controls /> |
| <video src="https://github.com/user-attachments/assets/06a3446c-a272-40ab-b30c-9bea38cf3c31" width="170" alt="다이어트 및 알레르기 주문" controls> |

**경로**: `/ordering`<br>
**주요 기능**<br>
  - **음성 주문**
    - “따뜻한 아메리카노 두 잔”, “얼음은 조금만” 등 자연어 명령을 Web Speech API로 인식 후,  
      WebSocket을 통해 서버로 전송하고 AI가 메뉴를 인식해 장바구니를 구성합니다.
  - **메뉴 카드 선택**
    - 음성이 어려운 사용자도 화면의 메뉴 카드를 눌러 장바구니에 담을 수 있습니다.
  - **AI 챗봇 대화**
    - 우측 채팅 영역에서 주문 상태, 추천, 영양/알레르기 안내 등 AI의 안내를 문장과 음성으로 함께 제공합니다.
  - **화면 전환**
    - “주문 내역”, “주문 완료” 등의 음성 명령 또는 버튼으로 주문 내역/결제 화면으로 이동합니다.
    - AI 응답에서 주문 완료 상태가 되면 일정 시간 후 자동으로 결제 화면으로 전환됩니다.

<br/>

### 4. 주문 내역 확인 (`OrderListView`)

|                                        주문 내역 확인                                        |
| :------------------------------------------------------------------------------------------: |
| <img width="170" alt="주문 내역 - 키프티콘" src="https://github.com/user-attachments/assets/278efb0b-d242-4c01-9e48-28b8eaee0090" />

**경로**: `/order-list`<br>
**주요 기능**<br>
  - 장바구니에 담긴 메뉴, 수량, 할인을 포함한 **주문 요약 정보**를 한 화면에 크게 표시합니다.
  - “주문 계속하기” 버튼 또는 음성 명령으로 다시 `OrderingView`로 돌아가 메뉴를 추가할 수 있습니다.

<br/>

### 5. 결제 확인 & 완료 (`CheckoutView`)

| 최종 결제 (기프티콘) | 최종 결제 (카드) | 최종 결제 (모바일) | 메뉴 준비 안내 |
| :---: | :---: | :---: | :---: |
| <img width="170" alt="최종 결제 - 기프티콘" src="https://github.com/user-attachments/assets/e57d8d17-1836-4a46-b786-64184b945d34" /> | <img width="170" alt="최종 결제 - 카드" src="https://github.com/user-attachments/assets/821a2aaa-d781-44c7-a783-9c40387ae834" /> | <img width="170" alt="최종 결제 - 모바일" src="https://github.com/user-attachments/assets/a1fd4ef0-f17c-412d-8b68-c2dff752da9f" /> | <img width="170" alt="메뉴 준비 중" src="https://github.com/user-attachments/assets/df603fde-1981-4c52-8730-a897830f453f" /> |


**경로**: `/checkout`<br>
**주요 기능**<br>
  - 최종 주문 금액, 할인 내역, 결제 수단 정보를 한 번 더 확인할 수 있습니다.
  - “결제하기” 버튼을 누르면 결제 수단에 따라  
    “모바일 페이를 인식해주세요.” 등 단계별 진행 상황을 안내하는 애니메이션과 음성 안내**가 재생됩니다.
  - 결제 완료 후 **번호표 발급 → 메뉴 준비 안내 → 일정 시간 후 메인 화면으로 자동 복귀**까지 흐름이 자동으로 진행됩니다.

<br/>




