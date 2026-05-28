## 이용수 (Yong-Su Lee)

**AI Researcher in Audio Deepfake Detection**  
오디오 딥페이크 탐지 · 음원 분리 · 설명 가능한 AI

---

### 🔬 Research

현재 **복합 오디오 위변조 탐지** 연구를 진행 중입니다.  
기존 모델이 "진짜/가짜" 이진 판별에 그치는 것과 달리, 음성과 환경음을 분리하여 **"어느 채널이 가짜인가"** 를 5개 클래스로 설명하는 프레임워크를 제안합니다.

**관심 연구 분야**
- 오디오 딥페이크 탐지 (Audio Anti-Spoofing)
- 음원 분리 (Blind Source Separation)
- 설명 가능한 AI (Explainable AI, XAI)
- 음성/오디오 신호 처리

---

### 🚀 Featured Research Project

#### [S-CAD: Spatial-Consistency-Aware Audio Detection](https://github.com/leeytkfng/S-CAD)

> 음원 분리 + 물리 음향 피처 기반 5-class 복합 오디오 위변조 탐지 시스템

| 항목 | 내용 |
|------|------|
| 데이터셋 | CompSpoofV2 (24,864 samples, 5-class) |
| 핵심 모델 | Conv-TasNet (음원 분리) + LightGBM (19-dim 물리 피처) |
| Accuracy | 69.8% · Macro-F1 0.6564 |
| FAKE Recall | 56.4% (SuDORM-RF 대비 +41%p 개선) |
| 논문 | 정보처리학회 논문 작성 중 (2026) |

**핵심 기여**
- 사전학습 없이 물리 음향 지표(RT60, Noise Floor, MSC, XCorr)만으로 경쟁력 있는 탐지 성능 달성
- SI-SNR ↔ FAKE recall 비선형 상관관계 정량 실증
- LightGBM Feature Importance를 통한 판정 근거 시각화

```
[입력 오디오]
     │
[LCNN-SE Gatekeeper]  →  REAL 조기 판정
     │
[Conv-TasNet 음원 분리]
     ├── 🗣️ Speech Stream → WavLM 위조 점수
     └── 🌿 Env Stream   → LCNN-SE 위조 점수
     │
[물리 음향 분석: RT60 · Noise Floor · MSC · XCorr]
     │
[LightGBM 5-class] → REAL / GENUINE / SPOOF_SPEECH / SPOOF_ENV / FAKE
```

---

### 🛠 Tech Stack

**AI / ML**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-2E8B57?style=flat&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)

**Audio / Signal Processing**  
![librosa](https://img.shields.io/badge/librosa-4B8BBE?style=flat&logoColor=white)
![torchaudio](https://img.shields.io/badge/torchaudio-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![SpeechBrain](https://img.shields.io/badge/SpeechBrain-5C4EE5?style=flat&logoColor=white)

**Backend (기존 경험)**  
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

### 📄 Publication

| 상태 | 제목 | 학술대회 |
|------|------|---------|
| 작성 중 | S-CAD: 음원 분리 기반 복합 오디오 위변조 5-class 탐지 | 정보처리학회 2026 |

---

### 📫 Contact

- Email: whgdkgo614@gmail.com
- Blog: [velog.io/@dydtn61498](https://velog.io/@dydtn61498/posts)

---

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=leeytkfng&layout=compact&langs_count=8&hide=html,css)

[![GitHub Streak](https://streak-stats.demolab.com?user=leeytkfng&theme=default)](https://git.io/streak-stats)
