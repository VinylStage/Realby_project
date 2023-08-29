# RealBy

[Frontend](https://github.com/vinylstage/Realby)

[Backend](https://github.com/hanilcome/Realby_project)


## Start Routine

### 가상환경 재구성

    poetry shell

#### window기준

    source .venv/scripts/activate

#### mac은 해당 path를 찾아주어 적용하면 됨

    poetry env info --path

### 종속패키지 설치

#### requirements사용시

    pip install -r requirements.txt

#### poetry 사용시

    poetry update package

    poetry install

#### requirements에서 poetry로 이동시

    cat requirements.txt | grep -E '^[^# ]' | cut -d= -f1 | xargs -n 1 poetry add

#### poetry에서 requirements로 이동시

    poetry export -f requirements.txt --output requirements.txt

### 시크릿키 발급

    py -c 'from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())'

https://djecrety.ir/

    touch secrets.json

    {
      "SECRET_KEY": "해당 키",
    }

#### db.sqlite3에 migrate

    py manage.py migrate

#### 이슈체크

    py manage.py check

#### 관리자 계정생성 및 서버테스트

    py manage.py createsuperuser

    py manage.py runserver

---

# Project Purpose

사용자가 자신의 관심사나 주제에 대해 다양한 토픽의 글을 작성 및 게시하고, 블로거와 유저 간 소통을 극대화한 범용적인 블로그 플랫폼.

## Usage Language & FrameWork

Backend - Python, Django Rest Framework

Frontend - next.js

## Usage Management Method

requirements.txt

poetry

json

## Usage Package

    python = "^3.11"
    django = "^4.2"
    djangorestframework = "^3.14.0"
    django-cors-headers = "^3.14.0"
    pillow = "^9.5.0"
    django-nextjs = "^2.2.2"
    djangorestframework-simplejwt = "^5.2.2"
