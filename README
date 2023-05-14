## このリポジトリについて

Djangoの勉強の一環として、下記ページを参照しながら作成したリポジトリです。

https://learn.microsoft.com/ja-jp/training/modules/django-get-started/

## 環境構築

### 1. 仮想環境作成

```bash
# Windows
python -m venv venv
.\\venv\\Scripts\\Activate

# macOS or Linux
python3 -m venv venv
source ./venv/bin/activate

## macOS + fish
python3 -m venv venv
set VIRTUAL_ENV "/path/to/hello_django/venv"
source ./venv/bin/activate.fish
```

### 2. Djangoインストール

```bash
pip install -r requirements.txt
```

### 3. プロジェクト作成

```bash
django-admin startproject helloproject .
```

### 4. アプリ作成

```bash
python manage.py startapp hello_world
```

### 5. プロジェクトにアプリを登録

`settings.py`

```python
INSTALLED_APPS = [
    :
    'hello_world.apps.HelloWorldConfig',
    ]
```

### 6. ビューを作る

`hello_world/views.py`

```python
from django.shortcuts import render
from django.http import HttpResponse


def index(request):
    return HttpResponse("Hello, world. You're at the polls index.")
```

### 7. URLconfをプロジェクトに登録する

`helloproject/urls.py`

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path("", include("hello_world.urls")),
    path("admin/", admin.site.urls),
]
```

### 8. サーバー起動

```bash
python manage.py runserver
```

### 9. ブラウザでURLを開く

http://127.0.0.1:8000/

`Hello, World!` が表示されていれば成功。
