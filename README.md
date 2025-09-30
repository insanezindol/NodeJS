# Node.js 학습 프로젝트

Node.js의 기본 개념과 기능들을 학습하기 위한 예제 프로젝트입니다.

## 프로젝트 개요

이 프로젝트는 Node.js의 다양한 기능들을 실습하고 학습하기 위한 예제 코드들을 포함하고 있습니다.

## 파일 구조

-   `hello-world-server.js` - 간단한 "Hello World" HTTP 서버
-   `server.js` - 정적 파일을 제공하는 HTTP 서버
-   `blocking.js` - 동기(블로킹) 파일 읽기 예제
-   `nonblocking.js` - 비동기(논블로킹) 파일 읽기 예제
-   `events.js` - EventEmitter를 사용한 이벤트 처리 예제
-   `client.js` - HTTP 클라이언트 예제
-   `index.html` - 정적 웹 페이지
-   `input.txt` - 파일 읽기 예제를 위한 텍스트 파일

## 예제 설명

### 1. Hello World 서버 (`hello-world-server.js`)

가장 기본적인 HTTP 서버를 생성하는 예제입니다.

-   포트 8081에서 실행
-   모든 요청에 "Hello World" 응답

### 2. 정적 파일 서버 (`server.js`)

요청된 URL에 따라 적절한 파일을 제공하는 웹 서버입니다.

-   URL 파싱을 통한 파일 경로 추출
-   파일 존재 여부 확인 및 적절한 HTTP 상태 코드 반환
-   기본 페이지로 index.html 제공

### 3. 블로킹 vs 논블로킹 I/O

-   `blocking.js`: 동기적으로 파일을 읽어 프로그램이 대기
-   `nonblocking.js`: 비동기적으로 파일을 읽어 프로그램이 계속 진행

### 4. 이벤트 처리 (`events.js`)

Node.js의 EventEmitter를 사용한 이벤트 기반 프로그래밍 예제입니다.

-   이벤트 핸들러 등록
-   이벤트 발생 및 처리
-   이벤트 체인 구현

### 5. HTTP 클라이언트 (`client.js`)

HTTP 요청을 보내고 응답을 처리하는 클라이언트 예제입니다.

-   HTTP 요청 옵션 설정
-   응답 데이터 수신 및 처리

## 실행 방법

### 1. Hello World 서버 실행

```bash
node hello-world-server.js
```

브라우저에서 http://127.0.0.1:8081 접속

### 2. 정적 파일 서버 실행

```bash
node server.js
```

브라우저에서 http://127.0.0.1:8081 접속하여 index.html 확인

### 3. 파일 I/O 예제 실행

```bash
# 동기 파일 읽기
node blocking.js

# 비동기 파일 읽기
node nonblocking.js
```

### 4. 이벤트 예제 실행

```bash
node events.js
```

### 5. HTTP 클라이언트 실행

먼저 서버를 실행한 후:

```bash
node client.js
```

## 학습 목표

이 프로젝트를 통해 다음 개념들을 학습할 수 있습니다:

1. **HTTP 서버 생성**: Node.js의 http 모듈 사용법
2. **파일 시스템**: fs 모듈을 통한 파일 읽기/쓰기
3. **동기 vs 비동기**: 블로킹과 논블로킹 I/O의 차이점
4. **이벤트 기반 프로그래밍**: EventEmitter 사용법
5. **HTTP 클라이언트**: HTTP 요청 생성 및 응답 처리
6. **URL 파싱**: url 모듈을 통한 요청 URL 분석

## 요구사항

-   Node.js (버전 0.1.0 이상)
