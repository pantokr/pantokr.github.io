---
layout: post
title: python-call-factory
tags: [Python, Torch, TensorFlow, Docker]
excerpt_separator: <!--more-->
---

# 음성 파일을 넣으면 화자 분리 및 STT 적용하여 .csv로 반환

<!--more-->

통화음이 포함된 .WAV 파일을 화자 분리 및 STT 적용하여 .csv로 반환하는 Python 프로젝트입니다.

## 🔗 Github

- **Github Repository**  
  [![Github](https://img.shields.io/badge/Github-Repository-black?logo=github)](https://github.com/pantokr/call-factory)

- **Git Clone**
  ```bash
  git clone https://github.com/pantokr/call-factory.git
  ```

---
## 📌 주요 기능 & 파이프라인

다양한 오픈소스 인공지능 모델을 순차적으로 처리하는 **파이프라인**을 구성하여, 각 단계를 거치며 파일이 생성되고 다음 모델의 입력으로 사용됩니다.

### 1. ⚙️ 전처리 (Preprocessing)

* **표준화:** 코덱 없이 재생 불가능한 `.wav` 파일을 **16000Hz 샘플링**, **Mono**, **16 Width**로 통일합니다.

### 2. 📞 비연결/연결 통화 분류

* **모델:** 이전 프로젝트 **`python-missed-call-filter`**에서 생성된 모델 사용
* **목적:** 통화음 지속, 바로 끊음 등 **비연결 통화**와 **실제 연결 통화**를 분류합니다.

### 3. 🔊 대화 음성 추출 (VAD)

* **모델:** **Yamnet TensorFlow Lite (CPU)** 모델 사용
* **목적:** 정적, 컬러링 등 **잡음을 제거**하고 **실제 대화 음성**만 추출합니다.

### 4. 🧑‍🤝‍🧑 화자 분리 (Speaker Diarization)

* **라이브러리/모델:** **`Pyannote.audio`** 라이브러리의 **Speaker Diarization 3.1**
* **목적:** STT 텍스트가 길어지는 것을 방지하고, 발화 시작/종료 시간을 통해 WAV 파일을 파싱해 여러 파일로 저장합니다.
* **결과:** 각 파일의 **파일명** 및 **시간 정보**를 담은 **`.csv` 파일 생성**

### 5. 📝 STT (Speech-to-Text)

* **모델:** **Whisper Large V3** (한국어 특화)
* **적용:** 이전 단계에서 생성된 **`.csv`** 파일의 각 데이터(분리된 음성 파일)에 **STT를 적용**합니다.

### 6. 😮‍💨 음성 감정 인식 (Emotion Recognition)

* **모델:** **Emotion2Vec Plus Large**
* **적용:** STT와 마찬가지로 **`.csv`** 파일의 각 데이터에 **음성 감정 인식**을 적용합니다.

---

## 📅 제작 정보 및 환경

### 💻 개발 환경 (Development Environment)

| 구분 | 상세 내용 | 비고 |
| :--- | :--- | :--- |
| **기술 스택** | Python (v3.12.10, virtual environment), Docker | |
| **주요 라이브러리** | **Torch**, **TensorFlow**, PyTorch, SoundFile, Pyannote, Whisper | 딥러닝 프레임워크 및 음성 처리 |
| **필요 도구** | Pydub 사용을 위한 **`.ffmpeg`**, **`.ffprobe`** | |

### 🗓️ 제작 기간

* **기간:** 2025년 9월 1일 ~ 2025년 10월 31일 (미래신용정보 프로젝트)
* **결과:** 1차 결과물 산출

---

## 💡 사용 및 설정 가이드

### 📁 디렉터리 구조

* **`files/in_files/`**: **입력 `.WAV` 파일**을 배치하는 곳 (대소문자 일치)
* **`files/out_files/`**: 각 작업 단계를 거친 파일 및 최종 결과물이 생성/이동되는 곳

### 🤖 AI 모델 설정

오픈소스 AI 모델은 **Hugging Face**에서 다운로드하여 로컬 환경에 설치해야 합니다.

* **모델 배치 위치:** **`models/`** 디렉터리
* **경량 모델:** `python-missed-call-filter`, `Yamnet` 모델은 **가중치 파일만** `models/`에 배치합니다.
* **대용량 모델:** `Whisper Large V3`, `Pyannote/~ v3.1`, `Emotion2Vec Plus Large`는 **`model_loader.py`를 참고**하여 별도의 디렉터리를 만들고 그 안에 배치해야 합니다.

### 🔒 기타 (DB 및 파이프라인)

* **환경 변수:** `.env.*` 파일에 **DB 삽입**을 위한 환경 변수가 담겨 있으며, 현재는 비공개 처리되었습니다.
* **처리 완료:** 모든 작업이 완전히 끝난 후에만 파일들이 `out_files`로 이동됩니다.
* **향후 계획:** 이 파이프라인이 적용되는 **프론트엔드/백엔드 프로젝트**도 GitHub에 등재할 예정입니다.