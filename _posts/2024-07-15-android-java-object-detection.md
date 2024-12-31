---
layout: post
title: android-java-object-detection
tags: [Android, Java, TensorFlow]
excerpt_separator: <!--more-->
---

# EfficientDet을 활용한 객체 인식 

<!--more-->

EfficientDet.tflite을 이용해 Android에서 객체 인식을 하는 기본 코드입니다. 

---

## 🔗 Github

- **Github Repository**  
  [![Github](https://img.shields.io/badge/Github-Repository-black?logo=github)](https://github.com/pantokr/android-java-object-detection)

- **Git Clone**  
  ```bash
  git clone https://github.com/pantokr/android-java-object-detection.git
  ```

---

## 📌 주요 기능

### 1. 객체 인식
- 실생활에서의 물체를 인식합니다.
- COCO 데이터셋의 객체 클래스(총 80가지)를 인식할 수 있습니다.

---

## 📸 스크린샷

**1. 객체 인식 화면**

<img src="/assets/img/posts/2024-07-15-android-java-object-detection/object.png" alt="객체 인식" style="width:50%;">

<br>

---

## 🛠️ 개발환경

- **IDE**: Android Studio
- **언어**: Java
- **주요 라이브러리**: CameraX, TensorFlow
- **지원 OS**: Android 11 (API 레벨 30) 이상
---

## 📋 기타

- **EfficientDet.tflite** 버전에 따라 다르게 적용할 수 있습니다.
- **EfficientDet.tflite** 파일은 **assets/**에 있으며 숫자가 높을수록 입력 크기가 커지며 시간이 오래 걸릴 수 있습니다.
- 여러 객체를 인식할 수 있으나 하나만 인식하도록 현재 설정되어 있습니다.