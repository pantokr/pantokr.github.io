---
layout: post
title: unity-csharp-gyudoku
tags: [Unity, CSharp]
excerpt_separator: <!--more-->
---

# 규도쿠

<!--more-->

각종 스도쿠 공식을 통해 스도쿠 문제를 해결할 수 있는 Windows에서 실행 가능한 스도쿠 애플리케이션입니다.

---

## 🔗 Github

- **Github Repository**  
  [![Github](https://img.shields.io/badge/Github-Repository-black?logo=github)](https://github.com/pantokr/unity-csharp-gyudoku)

- **Git Clone**  
  ```bash
  git clone https://github.com/pantokr/unity-csharp-gyudoku.git
  ```

---

## 📌 주요 기능

### 1. 스도쿠 생성
- 랜덤하게 각 난이도에 알맞는 맵을 생성합니다.
- 커스텀으로 사용자가 원하는 스도쿠를 생성할 수 있습니다.
  
### 2. 메모
- 각 셀에 들어갈 수 있는 숫자를 메모할 수 있습니다.
- 자동으로 모든 셀에 들어갈 수 있는 수를 자동으로 메모하는 기능이 있습니다.

### 3. 힌트
- 고급 레벨 이상부터 현재 상황에서 사용할 수 있는 힌트를 제공합니다.
- 각 힌트는 커스텀 모드에서도 작동하며 힌트가 작동하는 원리도 제공합니다.
- **Auto Single 기능**으로 한 숫자만 들어갈 수 있는 셀을 자동으로 채워 줍니다.
- 
### 3. 기타
- 방금 행동을 되돌릴 수 있는 **되돌리기 기능**이 있습니다.
- 지금까지의 진행 상황을 저장하고 나중에 다시 시작할 수 있도록 **저장 기능**을 제공합니다.

---

## 📸 스크린샷

**1. 스도쿠 화면**

<img src="/assets/img/posts/2021-05-17-unity-csharp-gyudoku/sudoku-panel.png" alt="스도쿠 패널" style="width:50%;">

<br>

**2. 메모 화면**

<img src="/assets/img/posts/2021-05-17-unity-csharp-gyudoku/memo.png" alt="메모 화면" style="width:50%;">

<br>

**3. 힌트 화면**

<img src="/assets/img/posts/2021-05-17-unity-csharp-gyudoku/hint-title.png" alt="힌트 화면" style="width:50%;">
<img src="/assets/img/posts/2021-05-17-unity-csharp-gyudoku/hint-script1.png" alt="힌트 설명1 화면" style="width:50%;">
<img src="/assets/img/posts/2021-05-17-unity-csharp-gyudoku/hint-script2.png" alt="힌트 설명2 화면" style="width:50%;">
<img src="/assets/img/posts/2021-05-17-unity-csharp-gyudoku/hint-script3.png" alt="힌트 설명3 화면" style="width:50%;">

---

## 🛠️ 개발환경

- **IDE**: Unity3D, Visual Studio 
- **언어**: CSharp 
- **지원 OS**: Windows

---

## 📋 기타

- **output/**에 실행할 수 있는 **Sudoku.exe**이 존재합니다.
- **output/**의 모든 하위 파일이 포함되어 있을 때 **Sudoku.exe**가 정상 실행 됩니다.
- 사용된 BGM은 **Linda 행진곡 - 클라 인 러브**와 **천사소녀 네티 BGM**입니다.