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

## structure

```
.
├── Dockerfile
├── README.ko.md
├── README.md
├── app.py
├── common
│   ├── __init__.py
│   ├── errors
│   │   ├── __init__.py
│   │   └── exception.py
│   └── protocols
│       ├── __init__.py
│       ├── event.py
│       ├── model_mapper.py
│       ├── persistence_adapter.py
│       └── usecase.py
├── container.py
├── core
│   ├── __init__.py
│   ├── fastapi
│   │   ├── __init__.py
│   │   ├── error.py
│   │   ├── event
│   │   │   ├── __init__.py
│   │   │   ├── dispatcher.py
│   │   │   ├── exception.py
│   │   │   ├── handler.py
│   │   │   └── middleware.py
│   │   ├── responses.py
│   │   └── routes.py
│   ├── pydantic.py
│   └── snowflake.py
├── images
│   ├── cqrs.png
│   ├── ddd_db_schema.png
│   ├── normal_db_schema.png
│   └── python_event.png
├── modules
│   ├── __init__.py
│   ├── author
│   │   ├── __init__.py
│   │   ├── domain
│   │   │   ├── __init__.py
│   │   │   ├── aggregate
│   │   │   │   ├── __init__.py
│   │   │   │   ├── id.py
│   │   │   │   └── model.py
│   │   │   └── value_objects.py
│   │   ├── infrastructure
│   │   │   ├── __init__.py
│   │   │   ├── persistence
│   │   │   │   ├── __init__.py
│   │   │   │   ├── adapter.py
│   │   │   │   ├── mapper.py
│   │   │   │   └── uow.py
│   │   │   └── query
│   │   │       ├── __init__.py
│   │   │       ├── dto.py
│   │   │       ├── mapper.py
│   │   │       ├── repository
│   │   │       │   ├── __init__.py
│   │   │       │   ├── impl.py
│   │   │       │   └── protocol.py
│   │   │       └── uow.py
│   │   └── usecase
│   │       ├── __init__.py
│   │       ├── addBookToAuthor
│   │       │   ├── __init__.py
│   │       │   ├── command.py
│   │       │   ├── event_handler.py
│   │       │   └── impl.py
│   │       └── newAuthor
│   │           ├── __init__.py
│   │           ├── api.py
│   │           ├── command.py
│   │           └── impl.py
│   └── book
│       ├── __init__.py
│       ├── domain
│       │   ├── __init__.py
│       │   ├── aggregate
│       │   │   ├── __init__.py
│       │   │   ├── id.py
│       │   │   └── model.py
│       │   ├── event.py
│       │   └── value_objects.py
│       ├── infrastructure
│       │   ├── __init__.py
│       │   ├── persistence
│       │   │   ├── __init__.py
│       │   │   ├── adapter.py
│       │   │   ├── mapper.py
│       │   │   └── uow.py
│       │   └── query
│       │       ├── __init__.py
│       │       ├── dto.py
│       │       ├── mapper.py
│       │       ├── repository
│       │       │   ├── __init__.py
│       │       │   ├── impl.py
│       │       │   └── protocol.py
│       │       └── uow.py
│       └── usecase
│           ├── __init__.py
│           ├── addAuthor
│           │   ├── __init__.py
│           │   ├── api.py
│           │   ├── command.py
│           │   └── impl.py
│           ├── deleteBook
│           │   ├── __init__.py
│           │   ├── api.py
│           │   ├── command.py
│           │   └── impl.py
│           ├── findBookByTitle
│           │   ├── __init__.py
│           │   ├── api.py
│           │   └── impl.py
│           └── newBook
│               ├── __init__.py
│               ├── api.py
│               ├── command.py
│               └── impl.py
├── persistence
│   ├── __init__.py
│   ├── author
│   │   ├── __init__.py
│   │   ├── entity.py
│   │   └── repository.py
│   └── book
│       ├── __init__.py
│       ├── entity.py
│       └── repository.py
├── poetry.lock
└── pyproject.toml
```
