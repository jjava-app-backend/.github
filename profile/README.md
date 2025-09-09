# OpenAI 기반 코드 리팩토링 기능을 갖춘 블록코딩 학습 앱 짜바(JJAVA)

<img width="390" height="374" alt="로~고" src="https://github.com/user-attachments/assets/dd02416a-9f26-42c6-a64f-ceffe4ca24d6" />


---



<img width="200" height="1275" alt="워크스페이스" src="https://github.com/user-attachments/assets/58b40fe4-2efe-4a8c-be78-06bbd8144678" />
<img width="200" height="1277" alt="문제풀기" src="https://github.com/user-attachments/assets/19f35d55-e0f5-451f-a56c-cd7f2f043bd0" />
<img width="200" height="1277" alt="ai 첨삭" src="https://github.com/user-attachments/assets/12f3eaf5-f196-4bb9-8243-f9f1fa18b8bf" />
<img width="200" height="1287" alt="지난학습" src="https://github.com/user-attachments/assets/1631f3b1-7da3-41c1-92ea-618ee37ab976" />


## 🎥 시연영상
### 워크 스페이스
<video src="https://github.com/user-attachments/assets/6a016756-c46d-4571-8ebc-2317beeb1a89" controls width="600"></video
### 문제 풀기
<video src="https://github.com/user-attachments/assets/7a7539e0-993a-4f1e-bb68-164185abacf5" controls width="600"></video>


## 목차
1. [🗓️ 개발 기간 및 참여 인원](#개발기간및참여인원)
2. [🔚 회고](#회고)
3. [💡 주요 기능](#주요기능)
4. [✍️ 개인 기여도 및 역할](#개인기여도및역할)
5. [👥 백엔드 팀원](#백엔드팀원)
6. [🛠️ 기술 스택](#기술스택)
7. [🧩 문제 해결 경험](#문제해결경험)
8. [🗂️ ERD](#erd)
9. [📄 API 문서](#api문서)
10. [🧠 프로젝트 소개](#프로젝트소개)


<a id="개발기간및참여인원"></a>
## 🗓️ 개발 기간 및 참여 인원
- 기간: 2025.06.16 ~ 2025.07.17
- 인원: 7인 팀 프로젝트



<a id="회고"></a>
## 🔚 회고

1️⃣ **샘플링의 중요성**

프로젝트 초기에 데이터를 충분히 샘플링해둔 덕분에 맡은 기능을 빠르게 개발할 수 있었고, 이를 통해 **초기 샘플링이 개발 효율성에 직결된다**는 점을 체감했습니다.

2️⃣ **비즈니스 이해**

프로젝트 초반에는 비즈니스 로직을 완전히 이해하지 못해 개발 중간에 팀장에게 질문을 자주 해야 했습니다. 이번 경험을 통해 **개발에 들어가기 전 비즈니스 도메인을 명확히 파악하는 것의 중요성**을 느꼈고, 앞으로는 설계 단계에서 이를 충분히 숙지해 개발에 집중할 수 있도록 노력해야겠다고 생각했습니다.

3️⃣ **프론트엔드 협업 경험**

개발을 빠르게 마무리하여 프론트엔드 통신 작업을 함께 도왔습니다. 이를 통해 **백엔드와 프론트엔드를 동시에 경험할 수 있었던 점이 큰 배움**이었습니다. 다음 프로젝트에서는 프론트엔드 파트도 직접 맡아보며 풀스택 관점에서 경험을 쌓아보고 싶다는 생각이 들었습니다.


<a id="주요기능"></a>
## 💡 주요 기능
### 1. 워크스페이스
- 블록코딩으로 코딩 연습 가능, 작성한 블록을 저장 및 불러오기 지원
- 저장된 워크스페이스를 불러와 이전 코드 복원 가능
- 행 시 정상 결과 출력, 오류 발생 시 한글 에러 메시지 제공

### 2. 학습 하기
- 원하는 문제 선택 후 실행 → 정답일 경우 AI 리팩토링 결과 제공
	- 오답일 경우 오류 메시지 출력
- 정답 문제에 대해 점수 반영 및 유저 스코어 업데이트
- 진행 중인 문제 자동 저장 및 학습 이력 관리

### 3. 지난 학습 리스트
- 완료한 문제 목록 확인 가능
- 선택 시 블록코딩 이력 및 AI 리팩토링 결과 함께 확인 가능

### 4. 리더보드
- 유저 스코어 기준 상위 10명 랭킹 표시 (매주 월요일 자정 업데이트)
- 상위 10명 누적 점수 공개

### 5. 마이페이지
- 개인별 랭킹 순위 및 누적 점수 확인 가능


<a id="개인기여도및역할"></a>
## ✍️ 개인 기여도 및 역할
### 개인
- 워크 스페이스 블록코딩 코드 컴파일 성공 & 실패 서비스 제작
    - 블록 코딩의 결과를 파싱하여 코드를 저장하고, 컴파일 성공 시 컴파일 결과를 반환하고 실패 시 한글 오류 메세지를 반환하는 로직 구현
- 학습 문제 블록코딩 정답 & 실패 서비스 제작
    - 블록 코딩을 통한 문제 정답 제출 시 문제에 저장되어 있던 더미 값을 추가로 컴파일 서버에 전송하여 컴파일 및 검산 후 성공 시 컴파일 및 AI 첨삭 결과 반환 로직 및 CRUD 작성
    - 블록 코딩의 결과를 파싱하여 코드를 저장하고, 컴파일 성공 후 AI 첨삭 요청 시 저장된 코드를 AI의 첨삭을 더하여 결과 반환 로직 구현
    - 블록 코딩을 통한 문제 정답 제출 시 문제에 저장되어 있던 더미 값을 추가로 컴파일 서버에 전송하여 컴파일 및 검산 중 컴파일 오류 또는 검산 실패 시 결과 반환 로직 및 CRUD 작성
- 학습 문제 리스트 & 상세보기 전달 기능 제작
    - 문제를 카테고리 별로 확인할 수 있는 문제 리스트 조회 로직과 문제의 상세 내용 조회 로직 구현
- Docker
    - 배포 전 로컬 환경 테스트를 위한 dockerfile 작성 및 환경 변수 설정 후 docker-compose를 통한 다중 컨테이너 환경 조성과 함께 Docker로 로컬 테스트 진행
- [Front] 문제 리스트 통신 구현
    - 전체 리스트 중 유저가 푼 문제의 경우 회색으로 표시


### 공통
- 주제 선정 및 리퍼런싱
    - 기초테이블, 행위테이블 설계
- 비즈니스 설계 및 보완
    - 주제를 프로젝트로 실현시키기 위한 비즈니스 설계 및 보완
- 테이블 설계
		- 저장이 필요한 엔티티 및 속성에 따른 데이터베이스 테이블 설계
- 컨벤션 토의
		- 협업, 필요한 규칙에 대한 컨벤션 토의


<a id="백엔드팀원"></a>
## 👥 백엔드 팀원
<table>
  <thead>
    <tr>
      <th>문정준</th>
      <th>김미숙</th>
      <th>손영민</th>
      <th>이민경</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://avatars.githubusercontent.com/u/106750460?v=4" alt="문정준" width="100" /></td>
      <td><img src="https://avatars.githubusercontent.com/u/203644415?v=4" alt="김미숙" width="100" /></td>
      <td><img src="https://avatars.githubusercontent.com/u/203730285?v=4" alt="손영민" width="100" /></td>
      <td><img src="https://avatars.githubusercontent.com/u/185046866?v=4" alt="이민경" width="100" /></td>
    </tr>
    <tr>
      <td>PL</td>
      <td>BE</td>
      <td>BE</td>
      <td>BE</td>
    </tr>
    <tr>
      <td><a href="https://github.com/Sxias">GitHub</a></td>
      <td><a href="https://github.com/parangdajavous">GitHub</a></td>
      <td><a href="https://github.com/son7571">GitHub</a></td>
      <td><a href="https://github.com/alsrud-602">GitHub</a></td>
    </tr>
  </tbody>
</table>


<a id="기술스택"></a>
## 🛠️ 기술 스택
| 구분 | 내용 |
|------|------|
| **Language & Framework** | ![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white) |
| **블록코딩 & 코드 실행** | ![GraalVM](https://img.shields.io/badge/GraalVM-007396?style=for-the-badge&logo=oracle&logoColor=white) |
| **인증/보안** | ![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white) ![OAuth2](https://img.shields.io/badge/OAuth2-3EAAAF?style=for-the-badge&logo=oauth&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white) |
| **외부 API 연동** | ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white) ![Resend](https://img.shields.io/badge/Resend-000000?style=for-the-badge&logo=minutemailer&logoColor=white) |
| **API 문서화** | ![REST Docs](https://img.shields.io/badge/Spring%20REST%20Docs-6DB33F?style=for-the-badge&logo=spring&logoColor=white) ![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black) |
| **테스트** | ![JUnit5](https://img.shields.io/badge/JUnit5-25A162?style=for-the-badge&logo=junit5&logoColor=white) |
| **에러 로깅** | ![Sentry](https://img.shields.io/badge/Sentry-362D59?style=for-the-badge&logo=sentry&logoColor=white) |
| **배포 및 환경** | ![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) <br>※ Docker는 로컬 테스트 용으로만 사용 |
| **Database** | ![H2 Database](https://img.shields.io/badge/H2-007396?style=for-the-badge&logo=java&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) (개발용) ![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white) (운영) |
| **협업 도구** | ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white) ![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white) |


<a id="문제해결경험"></a>
## 🧩 문제 해결 경험
### 🔔 문제1 : 메인서버가 컴파일 서버의 주소를 못 찾는 문제
<img width="1141" height="275" alt="image" src="https://github.com/user-attachments/assets/e13831f2-47dc-49d6-8585-004e4521b879" />

- ✅ **문제 상황**
    - http://localhost:8081/check로 연결을 시도했지만, 그 주소/포트에 서버가 떠 있지 않아서 연결 거부(Connection refused)가 났다.
    
<img width="512" height="264" alt="image1" src="https://github.com/user-attachments/assets/5c48a0ed-d3ae-45bf-bad6-52b340dfc0d7" />

- ⚠️ **원인**
    - localhost는 자기 컨테이너 자신을 가리킨다. 메인 서버 컨테이너에서 localhost:8081로 치면 메인 서버 컨테이너 내부 8081을 보게 되고, 컴파일 서버 컨테이너에는 못 간다.

- **🔧 해결 방법**:
    - 컴파일 서버의 서비스 이름을 호출한다.

- 💡 **느낀 점**
    - 이번 경험을 통해 컨테이너 환경에서의 localhost는 자기 자신만 가리킨다는 사실을 명확히 이해했다. 단순히 포트 문제로 접근하기보다, 컨테이너 네트워크 구조를 고려해야 한다는 점을 배웠다. 이를 통해 문제를 구조적으로 파악하고 서비스 이름 기반으로 통신하는 방식으로 해결하는 경험을 쌓을 수 있었다.


### 🔔 문제1-1 : 컴파일 서버 요청 거부
<img width="1215" height="394" alt="image2" src="https://github.com/user-attachments/assets/38930a9e-5a64-4f04-8c99-c09415cbc60d" />

- ✅ **문제 상황**
    - 컴파일 서버의 `docker-compose.yml` 작성 시 서비스 이름을 `jjava_compile`로 기재 후 메인 서버에서 `http://jjava_compile:8081` 로 요청을 했는데 400 에러가 떴다.
    
- ⚠️ **원인**
    - **Tomcat이 HTTP `Host` 헤더의 호스트명에 `_`(언더스코어)가 있으면 400으로 거부한다**.
    - 메인서버가 `http://jjava_compile:8081/check` 로 호출하면 `Host: jjava_compile:8081` 이 들어가고, 컴파일 서버의 Tomcat이 **RFC 규격 위반**으로 판단해 요청을 파싱 단계에서 튕긴다.
    - 핵심 오류 문구 : `The character [_] is never valid in a domain name.`

- **🔧 해결 방법**
    - 서비스명의 언더스코어( `_` )를 하이픈( `-` )으로 변경한다.


- 💡 **느낀 점**
    - 이번 경험을 통해 도커 서비스 네이밍과 실제 HTTP Host 헤더의 차이를 이해할 수 있었다. 특히 언더스코어(`_`)가 도메인 규격에 맞지 않아 Tomcat에서 요청을 거부한다는 점을 알게 되었고, 서비스 이름 하나도 RFC 규약을 고려해야 함을 깨달았다. 이를 통해 환경 설정 시 사소한 네이밍 규칙도 중요하다는 교훈을 얻었다



### 🔐 문제2 : 컨테이너 생성 중 오류
<img width="699" height="123" alt="image3" src="https://github.com/user-attachments/assets/0e30e7c6-ccbb-4367-82e7-ec49e86f4ea4" />

- **✅ 문제 상황**
    - 메인 서버 컨테이너 생성 시 네트워크가 연결되지 않는 오류가 발생했다.
    
- ⚠️ **원인**
    - external 네트워크 backend-net 이 아직 존재하지 않는데 참조했기 때문

- **🔧 해결 방법**
    - 둘 중 한 군데에 네트워크를 생성하고, 나머지 하나를 생성된 네트워크에 연결한다.
	    - 컴파일 서버에서 네트워크를 생성 후 컴파일 서버에서 생성된 네트워크를 메인서버에 연결.
        - 메인 서버에서 네트워크를 생성하고 컴파일 서버를 연결해도 된다.

    <table>
  <thead>
    <tr>
      <th>compile</th>
      <th>main</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/e0ad1975-7b91-4282-833d-a3fe4c4d80c0" alt="compile" width="200" /></td>
      <td><img src="https://github.com/user-attachments/assets/dd558f6a-606d-49f6-81ab-6e3db12ecfdf" alt="main" width="200" /></td>
  </tbody>
</table>

- `name: backend-net, driver: bridge` → "이 네트워크를 직접 만든다"
- `external: true` → "이미 만들어진 네트워크에 조인"
- 두 compose가 같은 네트워크 이름(`backend-net`)을 공유하므로 → 컨테이너 간 **DNS 기반 서비스명 통신**이 가능

<img width="514" height="356" alt="image6" src="https://github.com/user-attachments/assets/499fd2bd-352b-4627-8058-0b132bca22d6" />

- **backend-net (bridge network)**
    
    → 모든 컨테이너(DB, Redis, jjava-main, jjava-compile)가 같은 네트워크에 붙어 있음
    
- **DB, Redis**
    
    → **jjava-main** 만 직접 접근
    
- **jjava-main ↔ jjava-compile**
    
    → HTTP 요청/응답만 주고받음
    
    → **jjava-compile** 은 DB/Redis에 직접 연결하지 않음
    

즉, 구조는 **메인 서버(jjava-main)가 중심**이 되고,

- DB/Redis는 **메인 서버 전용 리소스**
- jjava-compile은 단순히 **보조 서비스(컴파일 전용)** 로, 메인 서버랑만 통신
- 모든 통신은 **backend-net** 안에서 서비스명(DNS)으로 연결됨


- **💡 느낀 점**
    - 이번 경험을 통해 도커 네트워크 설정의 개념과 external 네트워크 사용 방식을 명확히 이해할 수 있었다. 단순히 컨테이너 실행만으로는 서비스 간 통신이 되지 않고, 동일한 네트워크를 공유해야만 DNS 기반 이름 해석을 통해 연결된다는 점을 배웠다. 또한 external: true 선언은 이미 생성된 네트워크를 참조하는 용도이며, 직접 생성이 필요한 경우 driver: bridge로 별도로 정의해야 한다는 사실을 알게 되었다. 이를 통해 컨테이너 간 통신 구조를 설계할 때 네트워크 설정이 핵심적이라는 점을 깨닫게 되었다.

 

<a id="erd"></a>
## 🗂️ ERD
<img width="2110" height="1175" alt="erd" src="https://github.com/user-attachments/assets/8105bd48-76bd-4d09-bfcc-531051b74855" />


<a id="api문서"></a>
## 📄 API 문서
[api 문서](https://github.com/user-attachments/files/22226277/api.9.html)



<img width="726" height="916" alt="문서1" src="https://github.com/user-attachments/assets/84149901-d86d-4e08-8cf7-e7bdecd0b18c" />
<img width="669" height="590" alt="문서2" src="https://github.com/user-attachments/assets/7d0a7afe-e953-4d70-a74c-8b7bb95fd4e2" />
<img width="674" height="614" alt="문서3" src="https://github.com/user-attachments/assets/d5ceb5c5-5478-4a57-a3d5-d4b5233e3ec8" />
<img width="665" height="619" alt="문서4" src="https://github.com/user-attachments/assets/ddcaf440-b852-4592-80d6-ea8fb3befab1" />



<a id="프로젝트소개"></a>
## 🧠 프로젝트 소개
<img width="600" height="500" alt="프로젝트 소개" src="https://github.com/user-attachments/assets/1a80e0ef-cd4f-4079-9d7e-2841a1b28ad4" />

<img width="600" height="500" alt="프로젝트 소개2" src="https://github.com/user-attachments/assets/c3631b0e-ee37-410d-a554-dd2d83981850" />


### 🚀 새로 도입해본 기술
<img width="600" height="500" alt="기술1" src="https://github.com/user-attachments/assets/3e5e02b8-8ed1-44d1-9fcf-e31eb0cf3330" />
<img width="600" height="550" alt="기술4" src="https://github.com/user-attachments/assets/78a1dc96-62e4-4878-a081-e7ffab7a7c63" />
<img width="500" height="500" alt="기술5" src="https://github.com/user-attachments/assets/71292a4f-4521-4d0f-bbd3-08a698b1d57b" />
<img width="500" height="500" alt="기술6" src="https://github.com/user-attachments/assets/e8a53089-36ea-4713-8556-99bca2470342" />
<img width="600" height="550" alt="기술7" src="https://github.com/user-attachments/assets/77e486c3-7648-4ffc-ae0d-7434b094213c" />
<img width="600" height="500" alt="기술8" src="https://github.com/user-attachments/assets/4676fdaf-23b0-459f-b11c-8c64eb3755a6" />
<img width="400" height="300" alt="기술9" src="https://github.com/user-attachments/assets/c46a75e4-db19-4cdc-a9b9-1b5c1365c750" />
<img width="400" height="300" alt="기술10" src="https://github.com/user-attachments/assets/e83ed00a-b1b8-484a-acb5-a494b707d175" />
