# "천천히 말씀하셔도 괜찮아요, 느린 키오스크"
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
**대화형 주문 (Voice First)**: "따뜻한 아메리카노 한 잔 줘"와 같이 평소 식당에서 주문하듯 말하면, AI가 의도를 파악하여 주문을 처리합니다.<br>
**직관적인 화면 구성**: 시각적 혼잡을 줄이기 위해 큰 글씨와 단순화된 이미지를 사용하며, 복잡한 메뉴 선택 과정을 최소화했습니다.<br>
**실시간 시각 피드백**: 사용자가 메뉴나 재료를 말하면 화면에 해당 재료가 쌓이는 모습을 보여주어,<br>주문이 제대로 되고 있는지 직관적으로 확인시켜 줍니다.<br>
**표준화된 경험 제공**: 어느 매장을 가더라도 '말'로 주문하는 통일된 경험을 제공하여 학습 비용을 낮춥니다.<br>

<br>

## 🔗 배포 및 테스트 정보

* **배포 URL** : 

<br>

## 👨‍👩‍👧 팀원 구성

| [팀원 1 이름] | [팀원 2 이름] | [팀원 3 이름] |
| :---: | :---: | :---: |
| <img src="https://via.placeholder.com/150" width="100px" alt="profile1" /> | <img src="https://via.placeholder.com/150" width="100px" alt="profile2" /> | <img src="https://via.placeholder.com/150" width="100px" alt="profile3" /> |
| [@GithubID](https://github.com/) | [@GithubID](https://github.com/) | [@GithubID](https://github.com/) |
| **Role & Part** | **Role & Part** | **Role & Part** |

<br>


##  📅 개발 기간 및 작업 관리

### 개발 기간
* **전체 기간** : 

### 작업 관리
* 
* 

<br>


## 🛠️ 개발 환경

| 분류 | 기술 스택 |
| :-- | :-- |
| **Front-end** | <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=black"/> <img src="https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white"/>  |
| **Back-end** | <img src="https://img.shields.io/badge/Spring_Boot_3.x-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white"/> <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/> <img src="https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white"/>|
| **AI** | <img src="https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white"/> |

### 🖥️ Front-end
* **Framework**: React
* **UI/UX**: Tailwind CSS (접근성을 고려한 직관적 UI 및 큰 폰트 구성)
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
사용자의 음성 데이터를 텍스트로 변환하고, 의도를 파악하여 응답을 생성한 뒤, 다시 음성으로 들려주는 핵심 로직입니다.
1.  **STT (Speech-to-Text)**: OpenAI Whisper API (사용자 음성 → 텍스트 변환)
2.  **LLM (Large Language Model)**: OpenAI GPT-5o (텍스트 의도 파악, 메뉴 매칭, JSON 응답 생성)
3.  **TTS (Text-to-Speech)**: OpenAI TTS (응답 텍스트 → 음성 합성)

### 🗄️ Infrastructure & Database
* **Database**: MySQL (관계형 데이터베이스, 추후 확장 가능성 고려)
* **Collaboration**: Discord, Notion, Github

<br>

## 📂 프로젝트 구조

```bash
├── public
│    └── index.html
└── src
     ├── api           # API 통신 모듈
     ├── asset         # 
     ├── routes        # 라우팅 설정 (PrivateRoutes)
     └── styles        # 전역 스타일
```




## 📲 페이지별 기능

### [페이지 명]
| 상세 페이지1 | 상세 페이지2 | 상세 페이지3 |
| :---: | :---: | :---: |
| <img src="https://via.placeholder.com/200x400?text=Splash" alt="초기화면" width="200" /> | <img src="https://via.placeholder.com/200x400?text=Join" alt="회원가입" width="200" /> | <img src="https://via.placeholder.com/200x400?text=Login" alt="로그인" width="200" /> |

* **상세 페이지1**: 설명
* **상세 페이지2**: 설명

### [페이지 명]
| 상세 페이지1 | 상세 페이지2 |
| :---: | :---: |
| <img src="https://via.placeholder.com/200x400?text=Home" alt="홈 피드" width="200" /> | <img src="https://via.placeholder.com/200x400?text=Search" alt="검색" width="200" /> |

* **상세 페이지1**: 설명
* **상세 페이지2**: 설명
<br>

## 💣 트러블 슈팅

<details>
<summary><b>1. </b></summary>
<div markdown="1">

* **문제 상황** : (여기에 문제 내용을 작성하세요)
* **원인** :
* **해결** :

</div>
</details>


<br>

## 🚀 개선 목표 및 성과

### 개선 목표
- [ ]
- [ ]
### 
* **이미지 최적화**
    * 


<br>

## 10. 💬 프로젝트 후기

* **[팀원 1 이름]**
    * 
* **[팀원 2 이름]**
    * 
* **[팀원 3 이름]**
    * 




