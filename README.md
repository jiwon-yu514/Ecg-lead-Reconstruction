# Ecg-lead-Reconstruction

# 🫀 ECG Lead Reconstruction from Limited Leads

> Reconstructing standard 12-lead ECG from a small subset of leads using a Multi-Channel Masked Autoencoder (MCMA)–style model.

---

## 📌 Overview

Wearable or reduced-lead ECG devices often record only 1–3 leads, which limits their diagnostic utility compared to standard 12-lead ECG.  
This project aims to **reconstruct full 12-lead ECG waveforms from a small subset of input leads**, using a deep learning model inspired by **masked autoencoders** and recent **ECG lead reconstruction** studies.

주요 목표:

- ✅ 적은 리드(예: 1~7리드)로부터 **표준 12리드 파형 재구성**
- ✅ **MIMIC-IV-ECG, PTB-XL** 등 공개 데이터셋 기반 실험
- ✅ 리드 조합별 성능 비교 및 임상적 의미 분석

---

## 🗂 Project Structure

```bash
ecg-lead-reconstruction/
├─ data/                # 원본/전처리 데이터 (gitignore 권장)
├─ configs/             # 실험 설정 (리드 조합, 하이퍼파라미터 등)
├─ src/
│  ├─ preprocess/       # WFDB → NPY/NPZ, 리샘플링, 필터링, 윈도 나누기
│  ├─ models/           # MCMA / UNet / Transformer 등 모델 정의
│  ├─ training/         # 학습 루프, 콜백, 로그 저장
│  ├─ evaluation/       # MSE, PCC, SSIM, FID, CID 등 평가 스크립트
│  └─ visualization/    # 리드별 파형 비교, 히트맵, 결과 그림 저장
├─ notebooks/           # 실험용 Jupyter 노트북
├─ scripts/             # 쉘/파이썬 실행 스크립트 (전처리, 학습, 평가)
├─ figs/                # 논문/발표용 그림
├─ requirements.txt     # 파이썬 의존성
└─ README.md
