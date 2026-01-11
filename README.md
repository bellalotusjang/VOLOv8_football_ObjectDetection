![Python](https://img.shields.io/badge/Python-3.10-blue)
![YOLOv8](https://img.shields.io/badge/Model-YOLOv8n-green)
![YOLOv8](https://img.shields.io/badge/Model-YOLOv8s-yellow)
![GPU](https://img.shields.io/badge/Environment-T4_GPU-orange)

# ⚽ YOLO 축구 선수 및 공 탐지 프로젝트

YOLOv8을 활용하여 축구 경기 영상에서 선수와 공을 탐지하는 딥러닝 프로젝트입니다.

## 📊 주요 성과
- **Player 탐지 정확도**: 97.6% (mAP50)
- **전체 mAP50**: 53.5%
- **학습 시간**: 약 2시간 (YOLOv8s, 30 epochs)

## 🛠️ 기술 스택
- Python 3.12
- YOLOv8 (Ultralytics)
- PyTorch 2.9.0
- Google Colab (Tesla T4 GPU)

## 📂 프로젝트 구조
```
├── Football.ipynb          # 메인 노트북
├── dataset/
│   ├── train/             # 학습 데이터 (2,676장)
│   └── valid/             # 검증 데이터 (669장)
└── runs/
    └── detect/
        ├── soccer_n_model/ # YOLOv8n 결과
        └── soccer_s_model/ # YOLOv8s 결과
```

## 🚀 실행 방법
1. Google Colab에서 `Football.ipynb` 열기
2. GPU 런타임 설정
3. 순서대로 셀 실행

## 📈 학습 결과

### YOLOv8s (Best Model)
| 클래스 | Precision | Recall | mAP50 | mAP50-95 |
|--------|-----------|--------|-------|----------|
| Player | 95.7% | 94.5% | 97.6% | 68.2% |
| Ball   | 46.5% | 5.6%  | 8.6%  | 2.7%  |

<img width="969" height="546" alt="스크린샷 2026-01-11 오후 11 53 45" src="https://github.com/user-attachments/assets/21a351fd-0221-49fc-9dd3-6555556a1749" />

## 💡 주요 특징
- 데이터 샘플링으로 학습 시간 단축 (30% 사용)
- Labelme 형식 → YOLO 형식 자동 변환
- 두 가지 모델(Nano, Small) 비교 실험

## 🔧 개선 방향
- Ball 탐지 성능 향상 (데이터 증강)
- 전체 데이터셋 활용
- Focal Loss 적용 (클래스 불균형 해결)

## 📝 라이센스
교육용 프로젝트

---
**마지막 업데이트**: 2026년 1월
