---
layout: post
title: call-factory-frontend
tags: [React, Vite, TypeScript, Docker]
excerpt_separator: <!--more-->
---

# Call Factory Frontend

<!--more-->

`Call Factory` 프로젝트의 프론트엔드입니다.

---

## 🔗 Github

- **Github Repository**  
  [![Github](https://img.shields.io/badge/Github-Repository-black?logo=github)](https://github.com/pantokr/call-factory-frontend)

- **Git Clone**  
  ```bash
  git clone https://github.com/pantokr/call-factory-frontend.git
  ```

---

## 📌 주요 기능

### 1. 인증
- `EmpId`와 `Key`를 `GET`방식으로 받으면 한정된 시간에 인가된 사용자만 세션을 통해 메인 화면으로 이동하도록 하는 로그인 화면을 만들었습니다.

### 2. 음성 파일 열람
- 화면 좌측에는 `Call Factory`를 통해 생성된 음성 파일 리스트를 배치했습니다.
- 화면 우측에서는 좌측의 데이터 리스트 중 하나를 클릭 시 해당하는 음성 파일 정보를 확인할 수 있으며, 음성 파일 재생, `.csv`를 통해 얻을 수 있는 시간, 감정, STT을 할 수 있습니다.

---

## 📸 스크린샷

**1. 메인 화면**

<img src="/assets/img/posts/2025-10-31-call-factory-frontend/image.png" alt="메인 화면" style="width:50%;">
  
---

## 🛠️ 개발환경

- **기술 스택**: React, Vite, TypeScript, Docker
- **주요 라이브러리**: AGGrid, WaveSurfer, Axios
- **지원 OS**: Chrome

---

## 📋 기타

- **환경 변수:** `.env.*` 파일에 백엔드와 통신하기 위한 환경 변수가 담겨 있으며, 현재는 비공개 처리되었습니다.
* **향후 계획:** 이 파이프라인이 적용되는 **백엔드 프로젝트**도 GitHub에 등재할 예정입니다.