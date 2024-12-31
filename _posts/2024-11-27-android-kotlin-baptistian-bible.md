---
layout: post
title: android-kotlin-baptistian-bible
tags: [Android, Kotlin]
excerpt_separator: <!--more-->
---

# 침례표기성경

<!--more-->

세례를 침례로 표기한 안드로이드 성경 애플리케이션입니다.

---

## 🔗 Github

- **Github Repository**  
  [![Github](https://img.shields.io/badge/Github-Repository-black?logo=github)](https://github.com/pantokr/android-kotlin-baptistian-bible)

- **Git Clone**  
  ```bash
  git clone https://github.com/pantokr/android-kotlin-baptistian-bible.git
  ```

---

## 📌 주요 기능

### 1. 검색
- 직관적인 성경 검색 기능을 제공합니다.
- 검색하려는 문구가 완전 일치하지 않아도 부분적으로 일치한다면 검색할 수 있습니다.
- 검색 시 검색 기록이 남아 검색 페이지 하단의 기록 버튼을 누르면 확인할 수 있습니다.

### 2. 번역본 선택
- 개역한글, 개역개정, KJV, NIV가 기본적으로 제공됩니다.
- 대역 선택 시 두 번역본을 한 눈에 볼 수 있습니다.

### 3. 말씀 선택
- 말씀 구절을 길게 누르면 선택 모드에 진입합니다.
- 선택 모드에서는 선택된 말씀 복사, 저장, 하이라이트를 할 수 있습니다.

### 4. 개인 설정
- 글자 크기, 문단 간격, 테마 모드를 설정할 수 있습니다.

### 5. 찬송가 
- 찬송가 목록을 새찬송가, 통일찬송가로 검색할 수 있습니다.
- 악보를 확인할 수 있습니다. 

### 6. 사전 
- NAVER 지식백과 API를 이용해 성경 관련 용어를 검색할 수 있습니다.

---

## 📸 스크린샷

**1. 메인 화면**

<img src="/assets/img/posts/2024-11-27-android-kotlin-baptistian-bible/main.jpg" alt="메인 화면" style="width:50%;">
  
<br>

**2. 검색 화면**

<img src="/assets/img/posts/2024-11-27-android-kotlin-baptistian-bible/search.jpg" alt="검색 화면" style="width:50%;">

<br>

**3. 대역 화면**

<img src="/assets/img/posts/2024-11-27-android-kotlin-baptistian-bible/translated.jpg" alt="대역 화면" style="width:50%;">

<br>

**4. 찬송가 화면**

<img src="/assets/img/posts/2024-11-27-android-kotlin-baptistian-bible/hymn.jpg" alt="찬송가 화면" style="width:50%;">

---

## 🛠️ 개발환경

- **기술 스택**: Android, Kotlin  
- **빌드 도구**: Gradle (Kotlin DSL)  
- **주요 라이브러리**: Jetpack Compose, Room  
- **지원 OS**: Android 13 (API 레벨 33) 이상

---

## 📋 기타

- 네이버 지식백과 API 사용
- Python을 이용해 대한성서공회 웹사이트에서 성경 데이터 크롤링
- 새찬송가 버전 찬송가 이미지 출처: [nybethel.org](https://nybethel.org/240/11)