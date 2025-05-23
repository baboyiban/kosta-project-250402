# Arduino_Project
아두이노 세미 프로젝트

---

### 📁 Git 커밋 전략
- 프로젝트 경로 내 `GitGuide.md` 파일 참고

## 📌 프로젝트 개요

본 프로젝트는 아두이노 기반의 실제 자동차와 유사한 조향 원리를 적용한 자율주행 RC카 구현을 목표로 합니다. 이를 통해 단순한 RC카 조작을 넘어, **실제 차량 제어 원리 학습과 응용 능력 향상**을 도모할 수 있습니다.

### 인원

| 이름 | 역할 |
| --- | --- |
| 장현민 | 팀장 |
| 최다루한 | 팀원 |
| 유명현 | 팀원 |

### 🎯목표
- 서보 모터(조향 장치)를 통한 앞바퀴 방향 제어
    - 조향 장치를 사용하는 이유 : 본 프로젝트의 가장 큰 특징은 **서보모터를 활용한 조향 제어 방식**입니다. 일반적인 RC카가 좌우 바퀴 속도 차이를 이용한 '탱크식 회전'을 구현하는 것과 달리, 본 RC카는 **서보모터를 통해 전륜 방향을 제어**하여 실제 차량처럼 자연스럽고 정확한 회전을 수행합니다. 이 방식은 실제 자율주행차의 조향 메커니즘과 유사하여 **실제 차량 제어 원리를 학습**하는 데 큰 도움이 됩니다.
- 블루투스 통신을 통한 RC카 주행 시스템
- 초음파 센서를 통한 충돌 방지 시스템
- 스마트 주차장 시스템

### 🔧 담당 파트

| 이름 | 담당 파트 |
| --- | --- |
| 장현민 | 프로젝트 관리, RC카 기능 개발, 자율 주행 시스템 구현, 스마트 주차장 코드 개선, 코드 병합 |
| 최다루한 | APP 인벤터 개발, 스마트 주차장 구현, 자율 주행 시스템 초기 함수 제작 |
| 유명현 | RC카 조향 장치 및 기능 구현, 하드웨어 제작, RC카 코드 최적화, 자율 주행 시스템 구현 |

### 📅 기간

> 2025-04-04 ~ 2025-04-11
> 
> 2025-04-14 : 추가 기능 구현
>  * 각 방향의 장애물 거리를 출력해주는 OLED 추가
>  * 회전 방향으로 LED 출력하는 기능 추가

## 폴더 구조

```
Arduino_Team_Project/ 
├── App/ # 앱인벤터 .aia 파일 │
├── Arduino/ 
│ ├── Parking.ino # 스마트 주차장 코드 
│ ├── RC_Car.ino # 자동차 제어 코드
| └── README.md # 코드 설명
├── library/
| └── PCF8574-master/ # PCF8574 라이브러리
```
※ PCF8574 라이브러리 출처: [GitHub 링크](https://github.com/xreef/PCF8574_library)

---

## ✅ 주요 기능 및 일정

**주요 코드에 대한 설명은 Arduino/README.md 경로에 작성하였습니다.**

### 계획서

| 기능명 | 날짜 | 비고 | 담당 | 설명 |
| --- | --- | --- | --- | --- |
| 앞바퀴 방향 제어 및 DC 모터 제어 | 2025년 4월 7일 -> 2025년 4월 7일 | O | 장현민, 유명현 |  |
| 좌우전후진 앱 개발(앱인벤터) | 2025년 4월 7일 -> 2025년 4월 7일 | 4월 8일 완료 | 유명현, 최다루한 | flutter 어플 개발 계획으로 인한 일정 조정 |
| flutter 어플 개발 (기능 구현, 테스트) (실패) | 2025년 4월 7일 -> 2025년 4월 10일 | x | 최다루한 | HC-06 모델은 클래식 블루투스 모델이라 라이브러리가 지원중단된 상태여서 환경 구성과 빌드에 실패함 |
| 연동 코드 작성 | 2025년 4월 7일 -> 2025년 4월 7일 | O | 장현민, 유명현 |  |
| 전체적인 부품 테스트 진행, 부품 스펙 조사 | 2025년 4월 7일 -> 2025년 4월 7일 | O | 장현민 |  |
| 회로도 도면 그리기 | 2025년 4월 7일 -> 2025년 4월 7일 | O | 장현민, 최다루한 |  |
| 조향 장치 제작 및 초기 하드웨어 제작 | 2025년 4월 8일 -> 2025년 4월 9일 | 4월 10일 완료 | 유명현 | 조향 장치 부품 문제로 인한 딜레이 |
| 블루투스 통신을 통한 주행 시스템 구현 | 2025년 4월 8일 -> 2025년 4월 8일 | 4월 10일 완료 | 장현민, 유명현 | 조향 장치 부품 문제로 인한 하드웨어 제작에 딜레이 |
| 조향 장치(서보 모터)를 활용한 방향 제어 기능 구현 | 2025년 4월 8일 -> 2025년 4월 8일 | O | 유명현 | 코드 구현 성공 -> 하드웨어 미구현 |
| 초음파 센서를 활용한 충돌 방지 시스템 구현 및 테스트 | 2025년 4월 8일 -> 2025년 4월 9일 | 4월 11일 완료 | 장현민, 최다루한 | 하드웨어 제작이 미뤄짐, 초기에 작성한 코드 수정 필요 |
| 테스트 환경 구성 | 2025년 4월 9일 -> 2025년 4월 9일 | 4월 11일 완료 | 장현민, 유명현 | 하드웨어 제작이 미뤄짐 |
| 전수 테스트 | 2025년 4월 9일 -> 2025년 4월 9일 | 기능 구현 및 테스트 완료 | 장현민, 유명현, 최다루한 |  |
| 스마트 주차장 시스템 구현 | 2025년 4월 10일 -> 2025년 4월 11일 | 4월 14일 완료 | 장현민, 유명현, 최다루한 | 스마트 주차장 코드 및 하드웨어에 문제 발생으로 인한 딜레이 |
| 기능 보완 | 2025년 4월 10일 -> 2025년 4월 11일 | 4월 14일 완료 | 장현민, 유명현, 최다루한 | 하드웨어 제작 딜레이로 인한 전체적인 일정 딜레이 |
| 발표 준비 | 2025년 4월 11일 -> 2025년 4월 14일 | 발표자 : 장현민 | 장현민, 유명현, 최다루한 | |

---

### 🛠 기술 스택

| 분류 | 도구/언어 | 설명 | 비고 |
| --- | --- | --- | --- |
| 개발 도구 | Arduino IDE | 아두이노 개발 환경 |  |
| 개발 도구 | C/C++ | 프로그래밍 언어 |  |
| 버전 관리 | GitHub | 코드 및 프로젝트 관리 | https://github.com/Hyunmin5928/Arduino_Project |
| 문서 관리 | Notion | 프로젝트 문서화 및 정리 | https://www.notion.so/1c4509b5e5858017aadeedd52537e593?v=1c4509b5e5858047ac4d000ca580f60f&pvs=4 |
| CAD 도구 |  | 회로 설계 및 시뮬레이션 | https://www.tinkercad.com/dashboard |
| 하드웨어 | Arduino UNO | 센서 및 모듈 제어용 MCU 보드 | UNO R3 |

---

## ⚙️ 부품 구성 및 회로도

### RC카 부품 구성

| 항목 | 수량 | 스펙(데이터 시트 참고) | 용도(중요) | 모델명 |
| --- | --- | --- | --- | --- |
| 아두이노 우노 | 1 | ATmega328P 마이크로 컨트롤러<br>입력 전압(권장) : 7~ 12V<br>디지털 I/O핀 : 14개(PWM 6개)<br>아날로그 입력 핀 : 6개 <br>DC 전류 : 40mA(핀당) | 메인 보드 | UNO R3 |
| 브레드 보드 | 1 |  | 회로 구성 | 400핀 |
| DC 모터 | 1 | 정격 전압 : 4.5V<br>작동 전압 : 3V ~ 6V<br>3V → 약 90RPM<br>6V → 약 200RPM | 동력원 | RF-310 |
| DC 모터 바퀴 | 4 | 듀얼 H-브리지<br> 작동 전압 : 5V ~ 35V<br> 출력 전류 : 최대 2A(모터당)<br> 논리 전압 : 5V | 자동차 바퀴 |  |
| L298N 모터 드라이버 | 1 | 듀얼 H-브리지<br>작동 전압 : 5V ~ 35V<br>출력 전류 : 최대 2A(모터당)<br>논리 전압 : 5V | DC 모터 제어용 |  |
| 서보 모터 | 1 | 작동 전압 : 4.8V \~ 6V <br>회전 각도 : 0° \~ 180° <br>제어 방식 : PWM <br>토크 : 약 1.8kg·cm (4.8V 기준) | 방향 전환용 | SG90 |
| 초음파 센서 | 3 | 측정 거리 : 2cm ~ 400cm <br>측정 정확도 : ±3mm <br>작동 전압 : 5V <br>제어 방식 : 트리거/에코 핀 | 자율 주행 모드를 위한 센서 |  |
| PCF8584 멀티플렉서 | 1 | 8-bit I/O 확장기 (I²C 인터페이스) <br>작동 전압: 2.5V ~ 6V <br>I²C 주소 지정 가능 (최대 8개 사용) <br>핀당 25mA 출력 | 우노 보드 디지털핀 확장용 |  |
| Bluetooth 또는 WI-FI 모듈 | 1 | 작동 전압 : 3.3V ~ 5V <br>통신 방식 : UART(TX/RX) <br>통신 속도 : 9600bps(기본) <br>작동 범위 : 약 10m | 스마트폰과 우노 보드 통신 |  |
| 18650 배터리 | 2 | 보호 회로 <br>정격 전압 : 3.7V <br>7.4V(2개 직렬 연결) <br>용량 : 3000mAh | 메인 전원 |  |
| 18650 배터리 2구 소켓 | 1 |  | 메인 전원과 우노 보드 연결용 |  |
| 18650 배터리 충전기 | 1 |  | 배터리 충전용 |  |
| AA 배터리 | 4 | 정격 전압 : 1.5V <br>6V(4개 직렬 연결) | DC 모터 전원 |  |
| 점퍼 케이블 수-수 | 30 |  | 회로 연결용 |  |
| 점퍼 케이블 암-수 | 30 |  | 회로 연결용 |  |

---

### 스마트 주차장 부품 구성

| 항목 | 수량 | 스펙(데이터 시트 참고) | 용도(중요) | 모델명 |
| --- | --- | --- | --- | --- |
| 아두이노 우노 보드 | 1 |  | 메인 보드 | UNO R3 |
| 브레드 보드 | 1 |  | 회로 구성 | 400핀 |
| DC 모터 | 1 | 정격 전압 : 4.5V<br>전압 : 3V ~ 6V<br>3V → 약 90RPM<br>6V → 약 200RPM | 환풍기 모터 | RF-310 |
| 다이오드 | 1 |  | DC 모터 제어용 | 1N4001 |
| 트랜지스터 | 1 |  | DC 모터 제어용 | 2N2222A |
| 9V 배터리 | 1 |  | DC 모터 전원 |  |
| 점퍼 케이블 수-수 | 20 |  | 회로 연결용 |  |
| 점퍼 케이블 암-수 | 50 |  | 회로 연결용 |  |
| 가스 센서 | 1 |  | 환풍기 제어용 | MQ-5 |
| 초음파 센서 | 2 |  | 입구 출입 감지용 | HC-SR04 |
| 피에조 스피커 | 1 |  | 출입 감지 시 경보 출력 |  |

---

### 🔌 회로 구성

### RC카 회로도
  
![Image](https://github.com/user-attachments/assets/4b728efe-6e84-4840-b1e6-1d8cee7b7480)

| 핀 번호 | 기능 설명                                  |
|--------|---------------------------------------------|
| D2, D3 | 블루투스 TXD, RXD                          |
| D6, D11| DC 모터 PWM 제어                           |
| D4, D7 | 1번 DC 모터 제어핀 (IN1, IN2)              |
| D8, D12| 2번 DC 모터 제어핀 (IN3, IN4)              |
| D9     | 서보 모터 제어                             |
| D5, D10, D13 | LED 제어 핀                          |
| A4, A5 | I2C 통신 (OLED, PCF8574 병렬 연결)         |
| P0~P5  | 초음파 센서 TRIG/ECHO 핀 (PCF8574 확장 사용) |

* I2C 모듈 OLED와 PCF8574를 병렬 연결하여 사용하였습니다.
* P# 핀은 PCF8574 확장 모듈에 존재하는 핀으로 초음파 센서에서 사용하도록 설계하였습니다.
* TinkerCad에 없는 모듈
  * HC06 블루투스 모듈은 회로도 상단에 와이파이 모듈로 대체하였습니다.
  * 모터 드라이버 L298N이 없어 유사한 기능을 가진 L293D로 대체하였습니다.

---

### 스마트 주차장 회로도
![image](https://github.com/user-attachments/assets/6999d75c-9beb-43dd-b531-7f49d0aec0fe)

---

## 하드웨어 제작 과정

### 조향 장치 + DC 모터 테스트 하드웨어
![image](https://github.com/user-attachments/assets/7a0fff87-f8f0-459d-bcd5-76317b816fbd)

### 초기 하드웨어 모습
![image](https://github.com/user-attachments/assets/5bcdc910-64c0-4cc8-a624-a5d235062a00)

### RC카 외관 디자인(초음파 센서 부착 전)
![image](https://github.com/user-attachments/assets/0f820660-5e47-4e75-926c-2c5af4a184be)

### RC카 초음파 센서 위치 조절
![image](https://github.com/user-attachments/assets/eab32af1-53b1-43a6-8491-0db21d8aa95b)

### RC카 완성 모습(외관)
![image](https://github.com/user-attachments/assets/67c2ebff-b444-40d8-8a54-48f6f20235e8)

### RC카 완성 모습(위)
![image](https://github.com/user-attachments/assets/70595a18-78f7-471b-9f46-cac58d497bd2)

### RC카 완성 내부 모습(앞)
![image](https://github.com/user-attachments/assets/62fc5a14-1db4-4045-94e7-08a435c1d3bf)

### RC카 완성 내부 모습(뒤)
![image](https://github.com/user-attachments/assets/14a31d78-de4d-468f-8cea-58e24872f170)

### 조향 장치 돌아가는 모습

https://github.com/user-attachments/assets/bf03cc3f-9413-47f2-8c14-719593ad8bbd
