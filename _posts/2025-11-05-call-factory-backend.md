---
layout: post
title: call-factory-backend
tags: [Node.js, TypeScript, Docker]
excerpt_separator: <!--more-->
---

# Call Factory Backend

<!--more-->

`Call Factory` 프로젝트의 백엔드입니다.

---

## 🔗 Github

- **Github Repository**  
  [![Github](https://img.shields.io/badge/Github-Repository-black?logo=github)](https://github.com/pantokr/call-factory-backend)

- **Git Clone**  
  ```bash
  git clone https://github.com/pantokr/call-factory-backend.git
  ```

---

## 📌 주요 기능

### 1. 세션
 - 20분여 길이의 Secret 을 적용한 세션을 생성합니다.
 - 인증 관련 요청 이외의 데이터 요청에는 기본적으로 `checkSession()`을 통해 브라우저의 세션이 유효한지 검증합니다.

### 2. CORS
 - CORS를 적용했습니다.

### 3. 인증
 - 프론트에서 받아온 파라미터(ID, KEY)로 DB의 데이터와 대조해서 유효하고 인가된 요청인지 확안합니다.
 - 일반적인 ID, PW의 로그인 방식이 아닙니다.
  
---

## 🛠️ 개발환경

- **기술 스택**: Node.js, TypeScript, Docker
- **주요 라이브러리**: Express, CORS

---

## 📋 기타

- **환경 변수:** `.env.*` 파일에 프론트엔드 및 DB와 통신하기 위한 환경 변수가 담겨 있으며, 현재는 비공개 처리되었습니다.
