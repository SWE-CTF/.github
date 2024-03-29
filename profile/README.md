# CherryCode
<img width="1280" alt="KakaoTalk_20231201_175544671" src="https://github.com/SWE-CTF/.github/assets/123055298/6b803ab2-3d5b-416d-b7f5-b0435eda7aae">
<img width="1280" alt="KakaoTalk_20231201_175517814" src="https://github.com/SWE-CTF/.github/assets/123055298/e0169605-727e-4d00-841b-0a5e599160ec">

<p></p>
CherryCode는 누구나 자신의 코드를 테스트 할 수 있는 온라인 저지 사이트입니다.

<p></p>
<p></p>

[CherryCode](http://13.48.161.97:3000/) [배포 중단]

## Getting Started / 어떻게 시작하나요?

### 프론트 <https://github.com/SWE-CTF/front>

먼저, 해당 레포지토리에서 프로젝트를 받고 시작하세요.

1. master 브랜치에서 프로젝트를 받아오세요.
   ```
   git clone -b master --single-branch https://github.com/SWE-CTF/front.git
   ```
2. 코드가 있는 폴더로 이동을 합니다.
   ```
   cd /front/src/main/frontend
   ```
3. node_modules를 다운 받습니다.
   ```
   npm install
   ```
4. 설치가 완료되면 현재 위치에서 다음 코드를 실행하여 시작합니다.
   ```
   npm start
   ```
5. 웹 프론트 서버가 켜지고 다음 주소로 접속하면 됩니다.
   ```
   http://localhost:3000
   ```

### 백엔드 <https://github.com/SWE-CTF/backend>

먼저, 해당 레포지토리에서 프로젝트를 받고 시작하세요.

1. develop 브랜치에서 프로젝트를 받아오세요.
   ```
   git clone -b develop --single-branch https://github.com/SWE-CTF/backend.git
   ```
2. 다음 디렉토리로 이동합니다.
   ```
   cd /backend/src/main
   ```
3. 해당 위치에 resources 폴더를 생성합니다.
   ```
   mkdir resources
   ```
4. resources 폴더에 application.properties를 생성합니다.
5. 다음의 설정중 사용자의 편의에 맞게 수정해주세요.
   ```
   spring.datasource.driver-class-name = com.mysql.cj.jdbc.Driver
   spring.datasource.url = jdbc:mysql://데이터베이스IP주소/데이터베이스이름
   spring.datasource.username = 데이터베이스 접속 아이디
   spring.datasource.password = 데이터베이스 접속 비밀번호

   spring.jpa.hibernate.ddl-auto = (none, validate, update, create, create-drop)
   spring.jpa.generate.ddl = (true, false)
   spring.jpa.show-sql = (true, false)
   spring.jpa.properties.hibernate.show_sql = (true, false)
   spring.jpa.properties.hibernate.format_sql = (true, false)
   spring.mvc.pathmatch.matching-strategy = ant_path_matcher

   user.file.path = 사진 파일 저장 경로
   code.storage.path = 코드 파일 저장 경로

   jwt.secret.key = 256bit의 문자열
   ```
6. 설정이 완료되면 CtfApplication을 실행합니다.
7. 웹 백엔드 서버가 켜지고 프론트에서 접속한 사이트로 사용하면 됩니다.


### Prerequisites / 선행 조건

아래 사항들이 설치가 되어있어야합니다.

```
Node 18.17.1 이상, JDK 11 (temurin), mysql 8.0.35-0 이상
```


## Built With / 누구랑 만들었나요?

* [유재혁](https://github.com/Evon00) - 프로젝트 설계, 데이터베이스 설계, 웹 백엔드 제작
* [오주은](https://github.com/zoouniak) - 프로젝트 설계, 데이터베이스 설계, 웹 백엔드 제작
* [오상훈](https://github.com/OhSSangHoon) - 프로젝트 설계, 웹 프론트엔드 제작
* [김동현](https://github.com/1s0m0rph1sm) - 프로젝트 설계, 웹 프론트엔드 제작
* [박연기](https://github.com/yeongipark) - 프로젝트 설계, 웹 프론트엔드 제작

## Function / 기능
+ 로그인
+ 로그아웃
+ 회원가입
+ 랭킹 조회
+ 문제 출제
+ 문제 코드 제출
+ 개인 코드 이력 확인
+ 다른 사용자 코드 확인
+ 공지사항
+ 마이 페이지

## ERD diagram

![sw (1)](https://github.com/SWE-CTF/.github/assets/88364328/8750d9b0-0753-48dd-8043-98600c6a01ef)   

## Front-End Technology / 프론트 기술

+ NodeJS axios 통신
+ monaco editor를 사용한 코드에디터 구현

## Back-End Technology / 백엔드 기술
+ Spring boot 2.7.16 (SnapShot)
+ Spring Data JPA
+ Spring Security
+ JWT
+ SWAGGER
+ AWS EC2

## Caution / 주의사항
+ c 언어 코드 제출의 경우 로컬 환경이 linux여야 실행이 됩니다.
