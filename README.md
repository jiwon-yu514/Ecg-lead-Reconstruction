# 🫀 가변 리드 조합에서의 단일 딥러닝 모델을 활용한 12리드 심전도 재구성  
**12-lead Electrocardiogram Reconstruction Using a Single Deep Learning Model with Variable Lead Combinations**

## 📌 연구/프로젝트 개요

웨어러블 심전도 기기는 주로 **소수의 사지 유도(1–3리드)** 만 제공하는 반면, 실제 임상 진단은 여전히 **표준 12리드 ECG**에 의존함.  
본 프로젝트의 목표는 다음과 같음.

- ✅ **서로 다른 입력 리드 조합(C1–C6)** 에서 **하나의 딥러닝 모델**로 12리드 ECG를 재구성할 수 있는지 평가  
- ✅ **MIMIC-IV-ECG**로 학습하고, **PTB-XL**에서 외부 검증 수행  
- ✅ 리드 수/조합/해부학적 위치에 따른 **재구성 난이도 차이 정량·정성 분석**  
- ✅ 웨어러블/부분 리드 환경에서 사용할 수 있는 **범용(Universal) 12리드 재구성 모델**의 가능성 검토  

