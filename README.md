# poetry-demo

Poetry를 사용하여 설정한 FastAPI 프로젝트의 기본 데모입니다.

## Description

- **FastAPI:** Python 3.12 및 type hints로 API를 구축하기 위한 최신 고성능 웹 프레임워크
- **Uvicorn:** FastAPI 애플리케이션을 실행하기 위한 ASGI 서버
- **Poetry:** Python 종속성 및 패키징을 관리하기 위한 도구

## Getting Started

1. **설치**

```shell
git clone <원격저장소 URL>
cd poetry-demo
poetry install
```

2. **서버 실행**

```shell
poetry run uvicorn main:app --reload
```
