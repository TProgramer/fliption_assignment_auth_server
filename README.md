## 플립션 소프트웨어 엔지니어 과제 문제 3 - Nest.js 인증 서버 구현 과제

[![Open in Dev Containers](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/TProgramer/fliption_assignment_auth_server.git)

### ℹ️ Project Summary

- JWT 기반으로 동작하는 인증 서버
- OpenAPI 3.0 기반의 Swagger API Docs 제공
- DB는 stable하며 최신의 MySQL 8.4.0 LTS 연동
- 개발환경을 컨테이너 내애 구축 ([devcontainer란?](https://curvy-larkspur-75d.notion.site/DevContainers-Docker-IDE-3463ca8e634340858c4abfe948b6d329?pvs=4))
- 단위/통합/인수 테스트 기반의 TDD

### 🎯 MVP Features

- [x] 회원가입
- [x] 로그인
- [x] 로그아웃
- [x] 사용자 정보 조회

### 📔 작업 내역

> 로컬 개발환경을 위한 세팅을 컨테이너 상에서 구축하기 (devcontainer)

**BackEnd**

- node:18.18.2 이미지
- 편의를 위한 VSCode extension 세팅 ( Github PR, Nest.js Snippets, ESLint)
- 서버 시간 설정 (Asia/Seoul)
- DB 컨테이너 설정

**Database**

- mysql:8.4.0 이미지
- fliption_auth database 생성
- 사용자 계정 생성 (fliption)
- 서버 시간 설정 (Asia/Seoul)
- utf8mb4 인코딩 설정

> 도메인 정의하기

- user: MVP Features인 회원가입, 로그인, 로그아웃, 회원 탈퇴, 회원 정보를 담당
- auth: 인증과 인가를 담당
- crypto: 정보의 암호화/복호화 담당
- common: config나 decorator, filter의 집합

> 로컬 개발환경에서 DB(MySQL)에 연동 및 DB 모델링 작업하기

mysql:8.4.0 컨테이너에 typeorm을 사용하여 연결 설정

이 후, 총 3개의 엔티티를 DB에 생성

- 사용자 정보를 관리할 `user`
- JWT 정보를 관리할 `token`
- 만료된 JWT를 관리할 `expiry`

Coworker Test223

Merge Test 1
Merge Test 2
Merge Test 3
Merge Test 4
Merge Test 5

test 1
test 2
test 3