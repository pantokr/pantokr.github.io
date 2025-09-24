---
layout: post
title: python-missed-call-filter
tags: [Python, Torch]
excerpt_separator: <!--more-->
---

# 연결/비연결 통화 분류 모델

<!--more-->

통화 음성 파일(.wav)를 이용해 연결 및 비연결(연결음, 컬러링, 바로 끊음 등) 통화 여부를 판단해 분류하는 모델과 관련 코드입니다.

## 🔗 Github

- **Github Repository**  
  [![Github](https://img.shields.io/badge/Github-Repository-black?logo=github)](https://github.com/pantokr/python-missed-call-filter)

- **Git Clone**
  ```bash
  git clone https://github.com/pantokr/python-missed-call-filter.git
  ```

---

## 📌 주요 기능

### 1. 연결/비연결 통화 분류

- 보유하고 있는 통화 데이터는 미연결 통화도 녹음되어 있어 이를 제거하는 작업이 필요했습니다.
- 미연결 통화는 연결음, ARS, 컬러링 등으로 구성된 통화, 거의 받자마자 끊어진 의미 없는 대화의 통화를 의미합니다.
- 이러한 통화를 0: 미연결, 1: 연결로 분류합니다.

---

## 📆 제작 과정

- 각 통화 후반부를 가지고 통화 분류에 사용하는 방법을 선택했습니다.
  - 후반부가 자연어 대화인지 다른 음성인지 판가름하는 요소라고 생각했습니다.
- MFCC (음성 특징 벡터화) + CNN을 사용했습니다.
- 약 1,600개의 통화 데이터를 직접 청취하고 라벨링 작업을 진행했습니다. _(음성 파일은 제공되지 않습니다.)_
- `train.py`로 모델을 생성하고, `example.py`로 `test.wav`를 분류할 수 있습니다.

---

## 🛠️ 개발환경

- **기술 스택**: Python(Colab)
- **주요 라이브러리**: Torch, Pandas, Librosa

---

## 📋 기타

- `example.py`에서 **Pydub** 라이브러리를 사용하므로 `.ffmpeg`, `.ffprobe`가 필요할 수 있습니다.
