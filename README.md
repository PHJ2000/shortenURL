# ShortenURL

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

## 프로젝트 개요
ShortenURL은 **FastAPI를 활용한 URL 단축 서비스**입니다. 사용자가 긴 URL을 입력하면 짧은 URL로 변환하여 제공합니다. 단축된 URL을 통해 원본 URL로 리디렉션할 수 있습니다.

## 주요 기능
- **URL 단축**: 긴 URL을 입력하면 고유한 짧은 URL을 생성
- **URL 리디렉션**: 단축된 URL을 입력하면 원본 URL로 이동
- **FastAPI 기반 API 제공**: RESTful API 방식으로 URL을 관리
- **SQLite 또는 파일 기반 데이터 저장**

## 설치 방법
1. **프로젝트 클론**
    ```bash
    git clone https://github.com/brain-hack/shortenURL.git
    ```
2. **의존성 설치**
    ```bash
    pip install -r requirements.txt
    ```
3. **앱 실행**
    ```bash
    uvicorn main:app --reload
    ```

## API 사용 방법
### 1. URL 단축
- **엔드포인트**: `POST /shorten`
- **요청 예시**
    ```json
    {
        "url": "https://example.com/long-url"
    }
    ```
- **응답 예시**
    ```json
    {
        "short_url": "http://localhost:8000/abcd1234"
    }
    ```

### 2. 단축 URL 리디렉션
- **엔드포인트**: `GET /{short_url}`
- **설명**: 단축된 URL을 입력하면 원본 URL로 자동 이동합니다.

## 프로젝트 구조
```
shortenURL/
│── main.py  # FastAPI 메인 실행 파일
│── config.py  # 설정 파일
│── data.py  # 데이터 저장 및 로드 관련 코드
│── shorten.py  # URL 단축 기능 구현
│── randstr.py  # 랜덤 문자열 생성 모듈
│── requirements.txt  # 필요 라이브러리 목록
│── README.md  # 프로젝트 설명 파일
└── LICENCE  # 라이선스 정보
```

## 기여 방법
1. 본 레포지토리를 포크합니다.
2. 새로운 브랜치를 생성합니다.
3. 변경 사항을 커밋하고 푸시합니다.
4. Pull Request를 생성하여 기여합니다.

## 라이선스
이 프로젝트는 MIT 라이선스를 따릅니다.

