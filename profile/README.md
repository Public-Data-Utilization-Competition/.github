# SportsPath


### Overview
2024년 국민체육진흥공단 공공데이터 활용 경진대회

<img src = "https://github.com/user-attachments/assets/64837c55-74fc-48ef-bb75-86d8814cbea9" width="400" height="400"/>


## 📋 목차

1. [Overview](#overview)  
2. [Development Period](#development-period)  
3. [Introduction](#introduction)  
4. [Team Members](#team-members)  
5. [기술 스택](#-기술-스택)  
6. [기능](#-기능)
7. [UI](#-UI)
8. [프로젝트 구조](#-프로젝트-구조)  
    - [FrontEnd 구조](#frontend-구조)  
    - [BackEnd 구조](#backend-구조)  
9. [BackEnd 세부 기술 스택](#backend-세부-기술-스택)  
10. [API 문서](#-api-문서)  
11. [설치 및 실행 방법](#-설치-및-실행-방법)  
12. [Contributing](#-contributing)  
13. [License](#-license) 

### Development Period
2024.11.19 ~ 2024.12.08

### Introduction
`SportsPath`는 주변 공공 체육 시설에서 지원하는 다양한 스포츠 프로그램을 쉽고 빠르게 확인할 수 있도록
돕는 웹 페이지 입니다. 현재 많은 프로그램들이 각기 다른 플랫폼이나 사이트에 분산되어 있어 필요한 정보를 찾는데
어려움을 겪는 사용자들을 위해 모든 데이터를 한 곳에 모아 효율적으로 제공하는 것을 목표로 하고 있습니다.

## Team Member
| **박동규<br/>Park DongKyu** | **조완기<br/>Cho Wangi** | **박찬주<br/>Park Chanjoo** | **백태균<br/>Beak TeaKyun** |
| :------: | :------: | :------:  | :------: |
| [<img src="https://avatars.githubusercontent.com/u/86235780?v=4" height=100 width=100> <br/> @dong99u](https://github.com/dong99u) | [<img src="https://avatars.githubusercontent.com/u/70210457?v=4" height=100 width=100> <br/> @Anas-wg](https://github.com/Anas-wg) | [<img src="https://avatars.githubusercontent.com/u/95401144?v=4" height=100 width=100> <br/> @ElvaCJ](https://github.com/ElvaCJ) | [<img src="https://avatars.githubusercontent.com/u/147308244?v=4" height=100 width=100> <br/> @TaegyunB](https://github.com/TaegyunB) |
| Back-end | Front-end | Front-end / UI | Back-end |

## 🛠 기술 스택

### ✔️Frond-end
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=Flutter&logoColor=white"> <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=Figma&logoColor=white"> <img src="https://img.shields.io/badge/styledcomponents-DB7093?style=for-the-badge&logo=styled-components&logoColor=white">

### ✔️Back-end
<img src="https://img.shields.io/badge/Django-009688?style=for-the-badge&logo=Django&logoColor=white"> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=GoogleCloud&logoColor=white">

## 🚀 기능

- **검색 기능**:  
  - 스포츠 강좌를 **이름, 종목명, 지역**으로 검색할 수 있습니다.  

- **필터링 기능**:  
  - **지역, 가격, 날짜**를 기준으로 강좌를 필터링할 수 있습니다.  

- **정렬 기능**:  
  - **가격순** 및 **모집 인원순**으로 정렬이 가능합니다.  

- **페이지네이션**:  
  - 페이지별로 **10개의 강좌**를 표시하며 페이지 이동이 가능합니다.  

- **지역별 체육시설 정보 제공**:  
  - 사용자의 지역에 맞는 체육시설 정보를 한눈에 확인할 수 있습니다.  

- **종목별 프로그램 분류**:  
  - 다양한 스포츠 종목별로 강좌를 쉽게 탐색할 수 있습니다.  

- **실시간 프로그램 정보 업데이트**:  
  - 최신 프로그램 정보를 실시간으로 반영하여 정확한 정보를 제공합니다.  

## 💻 UI

## 📂 프로젝트 구조

### FrontEnd 구조
```
📦src
 ┣ 📂assets
 ┃ ┗ 📜react.svg
 ┣ 📂components
 ┃ ┣ 📂filter
 ┃ ┃ ┣ 📜DatePick.jsx
 ┃ ┃ ┣ 📜Region.jsx
 ┃ ┃ ┗ 📜Slider.jsx
 ┃ ┣ 📜Card.jsx
 ┃ ┣ 📜Filter.jsx
 ┃ ┣ 📜Label.jsx
 ┃ ┣ 📜LinkButton.jsx
 ┃ ┣ 📜Modal.jsx
 ┃ ┣ 📜Pagination.jsx
 ┃ ┣ 📜SearchBar.jsx
 ┃ ┗ 📜TopButton.jsx
 ┣ 📂images
 ┃ ┣ 📜avatar.png
 ┃ ┣ 📜filter_button.png
 ┃ ┣ 📜filter_reset.png
 ┃ ┗ 📜main_logo.png
 ┣ 📜.DS_Store
 ┣ 📜App.jsx
 ┣ 📜GlobalStyle.js
 ┗ 📜main.jsx
```

## BackEnd 구조

```
sportify/
├── config/                 # 프로젝트 설정
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── common/                 # 공통 기능
│   └── models.py
├── regions/               # 지역 관련 앱
│   ├── models.py         # Sido, Facility 모델
│   ├── serializers.py
│   └── views.py
├── categories/           # 카테고리 관련 앱
│   ├── models.py        # Category 모델
│   ├── serializers.py
│   └── views.py
├── programs/            # 프로그램 관련 앱
│   ├── models.py       # Program 모델
│   ├── serializers.py
│   ├── filters.py      # 필터링 설정
│   └── views.py
├── media/              # 미디어 파일 저장소
│   └── sido_images/    # 시도 이미지
├── staticfiles/        # 정적 파일
├── requirements.txt    # 의존성 목록
├── docker-compose.yml  # Docker 구성
├── Dockerfile         # Docker 빌드 설정
└── .env              # 환경 변수
```



### BackEnd 세부 기술 스택

#### Backend
- Python 3.11
- Django
- Django REST Framework
- MySQL (AWS RDS)

#### Deployment
- Docker
- Nginx
- AWS EC2



### 📝 API 문서

#### Programs API

##### 1. 프로그램 목록 조회
```http
GET /api/programs/
```

**Query Parameters:**
- `page`: 페이지 번호 (기본값: 1)
- `size`: 페이지 크기 (기본값: 10)
- `sido`: 시/도 이름으로 필터링
- `min_price`: 최소 가격
- `max_price`: 최대 가격
- `days`: 요일 필터링 (MON, TUE, WED, THU, FRI, SAT, SUN)
- `start_time`: 시작 시간으로 필터링 (HH:MM:SS)
- `end_time`: 종료 시간으로 필터링 (HH:MM:SS)
- `ordering`: 정렬 기준 (start_time, -start_time, progrm_prc, -progrm_prc)
- `search`: 프로그램명, 시설명 검색

**응답 예시:**
```json
{
    "count": 91,
    "next": "https://dev.hufsthon.site/api/programs/?page=2",
    "previous": null,
    "results": [
        {
            "id": 1,
            "progrm_nm": "수영 초급반",
            "category_name": "수영",
            "facility_name": "종로스포츠센터",
            "facility_address": "서울시 종로구",
            "region": "서울특별시",
            "region_image": "https://dev.hufsthon.site/media/sido_images/seoul.png",
            "progrm_days": ["MON", "WED", "FRI"],
            "days_display": "월, 수, 금",
            "start_time": "09:00:00",
            "end_time": "10:00:00",
            "time_range": "09:00 ~ 10:00",
            "progrm_begin_de": "2024-10-01",
            "progrm_end_de": "2024-10-31",
            "progrm_prc": 50000,
            "progrm_rcrit_nmpr_co": 20,
            "progrm_trget_nm": "성인",
            "hmpg_url": "https://example.com"
        }
    ]
}
```

#### Categories API

##### 1. 카테고리 목록 조회
```http
GET /api/categories/
```

**Query Parameters:**
- `parent`: 상위 카테고리 ID로 필터링
- `search`: 카테고리명 검색

#### Regions API

##### 1. 시도 목록 조회
```http
GET /api/regions/sidos/
```

##### 2. 시설 목록 조회
```http
GET /api/regions/facilities/
```

**Query Parameters:**
- `sido`: 시도 ID로 필터링
- `search`: 시설명 또는 주소 검색

### 🚀 설치 및 실행 방법

1. 저장소 클론
```bash
git clone https://github.com/your-username/sportify.git
cd sportify
```

2. 환경 변수 설정 (.env 파일 생성)
```
DEBUG=True
SECRET_KEY=your-secret-key
RDS_DB_NAME=your-db-name
RDS_USERNAME=your-username
RDS_PASSWORD=your-password
RDS_HOSTNAME=your-db-host
RDS_PORT=3306
```

3. Docker 실행
```bash
docker-compose up --build
```

### 🤝 Contributing

버그 리포트나 새로운 기능 제안은 언제나 환영합니다. 이슈를 생성하거나 풀 리퀘스트를 보내주세요.

### 📜 License

This project is licensed under the MIT License - see the LICENSE.md file for details.
