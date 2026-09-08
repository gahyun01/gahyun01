<div align="center">

# 안녕하세요, AI와 백엔드를 함께 개발하는 정가현입니다 🙇‍♀️

**ML/DL · Backend Developer**

</div>

# 자기소개

저는 새로운 기술을 빠르게 익히고, 복잡한 문제를 실제로 사용할 수 있는 결과물로 만드는 개발자입니다.

백엔드 개발에서 시작해 AI·머신러닝으로 영역을 확장했으며, **데이터의 제약을 분석해 문제를 다시 정의하고 모델부터 서비스 구조까지 연결하는 일**에 관심이 있습니다. 조색 AI 프로젝트에서는 개별 조색제의 색상 정보가 없는 산업 데이터를 바탕으로 예측 구조를 설계했고, 기존에 약 1시간 30분에서 2시간이 걸리던 탐색 과정을 일반적인 시뮬레이션 기준 1분 이내로 단축했습니다.

익숙하지 않은 분야에서도 공식 문서와 코드를 통해 빠르게 학습하고, 끝까지 구현하며 문제를 해결하는 것이 강점입니다. AI 모델을 만드는 데서 멈추지 않고 API와 웹 서비스로 연결해 실제 업무의 시간과 반복 작업을 줄이는 개발자로 성장하고 있습니다.

---

# 주요 프로젝트

## 컴파이드 : Paint Color Formulation AI

조색제 개별 색상 정보가 없는 환경에서 목표 LAB 색상값으로부터 14개 조색제의 배합 비율을 예측하는 산업용 조색 AI 모델입니다.

<aside>

**기간**: 2026.03 - 2026.05  
**역할**: 데이터 분석, 문제 정의, 모델 설계·학습, 성능 분석 및 최적화  
**기술**: Python, PyTorch, NumPy, Pandas, SciPy, Scikit-learn  
**GitHub**: [Paint Color Formulation AI](https://github.com/gahyun01/paint-color-formulation-ai)

</aside>

- 조색 문제를 **LAB → 배합 비율 → LAB**의 inverse problem으로 재정의했습니다.
- 배합 비율로 LAB를 예측하는 forward model을 먼저 학습하고, 이를 고정된 simulator로 활용해 inverse model을 구성했습니다.
- 개별 색상 정보가 없는 14개 조색제의 잠재 LAB 표현을 데이터로부터 추정했습니다.
- Kubelka–Munk 기반 색 혼합 아이디어와 ΔE 기반 손실을 모델링에 반영했습니다.
- 신경망 예측과 gradient·global optimization을 결합해 기존 약 **1시간 30분~2시간의 탐색 과정을 일반적인 경우 1분 이내로 단축**했습니다.
- LAB 색공간의 데이터 불균형을 분석하고, 진한 파란색·보라색 등 희소 색상 영역에서 발생하는 성능 한계를 확인했습니다.

<br/>

## NASA Space Apps Challenge 2025 : ExoVision AI

Kepler, K2, TESS 관측 데이터를 통합해 외계행성 후보를 판별하는 계층형 머신러닝 프로젝트입니다.

<aside>

**기간**: 2025  
**역할**: 천문 데이터 통합·전처리, 특징 설계, 분류 모델 및 추론 파이프라인 구현  
**기술**: Python, Pandas, Scikit-learn, XGBoost, LightGBM, CatBoost  
**GitHub**: [ExoVision AI](https://github.com/gahyun01/ExoVision-AI)

</aside>

- 구조와 단위가 서로 다른 세 관측 데이터셋을 공통 스키마로 변환해 **21,271개 샘플**로 통합했습니다.
- 항성 질량과 궤도 반장축 등 주요 결측값을 물리 법칙과 회귀 모델을 이용해 보완했습니다.
- 관측 오차를 변수 특성에 맞게 정제하고, 행성과 항성의 물리 관계를 반영한 파생 특징을 설계했습니다.
- 단일 3-class 분류 대신 `CONFIRMED ↔ FALSE POSITIVE` 판별과 `CANDIDATE` 탐지를 결합한 **2-stage hierarchical classification** 구조를 구현했습니다.
- 여러 boosting 모델과 voting ensemble을 비교하고 confidence threshold 기반 최종 분류 흐름을 구성했습니다.

<br/>

## 졸업작품 : BabyStory

아기의 울음 원인을 분석하고 육아 기록과 커뮤니티 기능을 제공하는 AI 기반 육아 보조 서비스입니다.

<aside>

**기간/인원**: 2024 · 3명  
**역할**: 데이터베이스 설계, 백엔드 API 개발, 테스트 코드 구현, 화면 검수  
**기술**: Python, FastAPI, SQLAlchemy, MySQL, Pytest  
**GitHub**: [BabyStory Backend](https://github.com/BabyStory-App/BabyStory-Backend)

</aside>

- 서비스 요구사항을 바탕으로 사용자, 육아 기록, 커뮤니티 기능의 데이터 관계와 제약조건을 설계했습니다.
- AI 모델 및 모바일 앱과 연동되는 백엔드 API를 구현했습니다.
- API 명세를 기반으로 테스트 코드를 먼저 작성하는 TDD 흐름으로 개발했습니다.
- 팀 협업 과정에서 Trunk-based 방식으로 코드를 관리하고 기능 단위 테스트를 진행했습니다.
- AI 활용성과 서비스 완성도를 인정받아 **강남대학교 ICT공학부 졸업작품 우수상(2등)**을 수상했습니다.

<br/>

## Image Inpainting & Colorization

흑백 이미지의 손실·모자이크 영역을 복원하고 자연스러운 색을 입히는 이미지 복원 및 색상화 프로젝트입니다.

<aside>

**역할**: 데이터 전처리, 복원·색상화 파이프라인 구현 및 모델 실험  
**기술**: Python, PyTorch, YOLO, Simple LaMa, U-Net, OpenCV  
**GitHub**: [inpaint-color](https://github.com/gahyun01/inpaint-color)

</aside>

- YOLO로 손실 영역을 탐지하고 OpenCV로 복원 마스크를 생성했습니다.
- Simple LaMa 기반 인페인팅과 U-Net 기반 색상화를 하나의 처리 과정으로 연결했습니다.
- 멀티프로세싱을 적용해 이미지 전처리 작업을 구성했습니다.
- 종료된 DACON 대회 데이터를 활용한 별도 실험에서 SSIM `0.5025636871`, `0.5264520135`를 기록했습니다.

<br/>

---

# 경력 및 개발 경험

## 컴파이드 | AI 개발자 ( 인턴 )

**기간**: 2026.03 - 2026.05

- 페인트 회사 협업 과제의 조색 비율 예측 AI 모델을 설계하고 구현했습니다.
- 기존 홈페이지의 구조와 UI를 전반적으로 분석한 뒤 프론트엔드와 백엔드 코드를 대폭 리팩터링했습니다.
- React·TypeScript 기반 화면과 Django REST Framework 기반 API를 정비하고 Docker와 AWS를 이용해 배포했습니다.

## 가이온 | 솔루션개발팀 웹 개발자 ( 인턴 )

**기간**: 2024.07 - 2025.03

- Django 기반 사내 솔루션 개발에 참여하여 웹 기능 구현과 기존 기능 개선을 담당했습니다.
- React Flow를 활용해 사용자가 편집할 수 있는 플로우차트의 노드와 엣지를 개발했습니다.
- 엔트리와 로봇 디바이스를 연동하고, 사용자가 엔트리에서 블록 코딩으로 하드웨어를 제어할 수 있도록 전용 블록과 동작 로직을 구현했습니다.

<br/>

---

# 기타 프로젝트

## [Side Project] myT

Django 학습 내용을 서비스 형태로 확장한 여행 계획 및 후기 공유 웹 애플리케이션입니다.

- 회원 인증, 여행 일정, 후기와 다중 이미지, 해시태그, 좋아요, 스크랩, 댓글·대댓글을 구현했습니다.
- Django ORM으로 데이터 관계를 설계하고 기상청 API를 연동했습니다.
- **GitHub**: [myT](https://github.com/gahyun01/myT)

## [Learning Project] FastAPI Practice

졸업작품을 시작하기 전 FastAPI 기반 백엔드 구조를 익히기 위해 진행한 프로젝트입니다.

- REST API, SQLAlchemy 관계 설정, MySQL 연동, JWT 인증을 단계적으로 구현했습니다.
- **GitHub**: [FastAPI Practice](https://github.com/gahyun01/FastAPI)

## [Learning Project] Django Local Library

솔루션개발팀 이동을 준비하며 Django 공식 튜토리얼을 기반으로 구현한 도서 대출 관리 서비스입니다.

- Django ORM, 클래스형 View, 인증·권한, 관리자 페이지, Form과 테스트를 학습했습니다.
- **GitHub**: [Django Local Library](https://github.com/gahyun01/Django_locallibrary)

<br/>

---

# 학습 기록

- [Deep Learning](https://github.com/gahyun01/Deep-Learning) — NumPy로 자동 미분과 역전파를 구현하며 자체 딥러닝 프레임워크 학습
- [Network](https://github.com/gahyun01/Network) — C++·Winsock 기반 TCP/UDP, 멀티스레드, 비동기 소켓 프로그래밍
- [OOP](https://github.com/gahyun01/OOP) — C++ 객체지향 프로그래밍 주차별 학습 및 과제
- [Arduino](https://github.com/gahyun01/Arduino) — 센서·모터·통신 모듈을 활용한 임베디드 시스템 실습
- [Academy Cloud Java](https://github.com/gahyun01/Academy_CloudJava) — Java, JDBC, JSP 및 웹 개발 기초 학습
- [Information Processing Engineer](https://github.com/gahyun01/information-processing-engineer) — 정보처리기사 필기·실기 개념과 시험 직전 암기 노트 정리

<br/>

---

# 교육 및 학력

## [교육] 그린컴퓨터아카데미 역삼점

- 클라우드 활용 Java·Spring Framework 개발자 과정 수료
- Java 객체지향 프로그래밍, 데이터베이스, JDBC, JSP 및 웹 개발 학습

## [학력] 강남대학교

- 소프트웨어전공 학사 졸업 · 2025.02
- AI 기반 육아 보조 서비스로 ICT공학부 졸업작품 우수상(2등)

<br/>

---

# Tech Stack

**AI / Data**  
Python · PyTorch · TensorFlow · Pandas · NumPy · Scikit-learn · XGBoost · LightGBM · CatBoost · OpenCV

**Backend**  
FastAPI · Django · Django REST Framework · SQLAlchemy · MySQL · SQLite · REST API · JWT

**Frontend / DevOps**  
React · TypeScript · JavaScript · HTML · CSS · Docker · AWS · Git · GitHub

**Other**  
Java · C++ · Arduino · Winsock

<br/>

---

# Contact

- GitHub: [github.com/gahyun01](https://github.com/gahyun01)
- Mail: gahyun727301@gmail.com

<div align="center">

<a href="https://github.com/devxb/gitanimals">
  <img src="https://render.gitanimals.org/lines/gahyun01?pet-id=644068695498298728" width="600" height="120" />
</a>

</div>
