# 🏠 Smart Home CCTV + AI System

> Raspberry Pi + LNN + Flask + MariaDB 하이브리드 스마트 홈 보안 시스템

## 프로젝트 개요
Raspberry Pi에서 실시간 카메라 영상을 수집하고 LNN(액체 신경망)으로 이상 상황을 감지하는 시스템입니다.  
감지된 이벤트는 PC의 Flask 서버 + MariaDB에 저장되며, 웹 대시보드에서 확인할 수 있습니다.

## 아키텍처
[Raspberry Pi - Edge]      [PC - Server]
│                              │
Camera → LNN 추론 ───────────▶ Flask API
│                              │
└────── 이벤트 데이터 ───────▶ MariaDB
text- **Edge (Pi)**: 영상 수집 + LNN 실시간 추론
- **Server (PC)**: Flask 웹 서비스 + MariaDB 데이터 관리

## 주요 기능
- 실시간 카메라 스트리밍
- LNN 기반 이벤트 감지 (이상 행동/소음)
- 웹 대시보드 (이벤트 목록, 영상 재생)
- MariaDB를 통한 이벤트 영구 저장

## 기술 스택
- **Raspberry Pi**: Python, OpenCV, LNN, Camera Module
- **Server**: Flask, MariaDB, SQLAlchemy
- **기타**: Git, Linux

## 실행 방법

### Raspberry Pi (Edge)
```bash
cd pi_edge
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python main.py
PC 서버
Bashcd server
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python main.py
GitHub 저장소

Smart_Home_CCTV

현재 진행 상황

 코드 구조를 Pi Edge / PC Server로 분리
 MariaDB 도입
 LNN 모델 최적화
 웹 대시보드 고도화
 실시간 알림 기능 추가


작성자: 이승민
마지막 업데이트: 2026년 6월