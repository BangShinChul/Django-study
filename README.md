# Django-study
> Django Study 내용을 적어놓는 원격리포지토리 입니다.
<br>
<b>참고</b>  
 - https://docs.djangoproject.com/ko/2.1/intro/tutorial01/
 - https://tutorial.djangogirls.org/ko/django_start_project/

저는 Ubuntu16.04 LTS 에서 테스트했으므로 이 운영체제 기준으로 작성하겠습니다.
<br>
<br>
먼저 python 3.5 버젼을 설치한 후<br>
가상 환경(Virtual environment)을 설치한 뒤<br>
Django를 설치하였습니다.
<br>
***
### python 설치법
```
$ sudo apt-get install python3
$ python -V
Python 3.5.2
```
<br>
pip는 파이썬 라이브러리를 관리해주는 툴입니다.<br> 
python3.4 이후 버젼부터 포함되어있지만 그 이전버젼의 python은 pip가 포함되어있지 않으므로<br>
만약 python3.4 버젼보다 낮은 python을 설치하셨다면 pip를 직접 받아야 합니다.
```
$ sudo apt-get install pip
```
<br>
아래는 pip를 최신버젼으로 업데이트해주는 명령어입니다.
```
$ python -m pip install --update pip
```
<br>
### 가상환경 설치법
아래의 코드는 venv라는 가상환경을 만들어주는 python의 라이브러리를 사용하여 myvenv라는 가상환경을 생성해주는 명령어입니다.
```
$ python -m venv myvenv
```
<br>
에러가 날 시에는 아래의 명령어를 통해 가상환경 라이브러리를 설치해줍니다.
```
$ sudo apt install python3-venv
```
<br>
생성한 가상환경을 실행해주는 명령어는 아래와 같습니다.
```
$ source myvenv/bin/activate
```
<br>
### Django 설치법
아래의 명령어를 실행해줍니다.
```
$ pip install django
$ python -m django --version
2.1.2
```
django app을 시작하는 명령어는 아래와 같습니다.<br>
먼저 아래 명령어를 통해 myapp이라는 django 애플리케이션을 만들어보겠습니다.
```
$ django-admin startproject myapp
```
이제 ls -al 명령어를 통해 myapp이라는 디렉터리가 생긴 것을 확인해보실 수 있습니다.
myapp이라는 django 애플리케이션을 아래 명령어를 통해 실행할 수 있습니다.
```
$ cd myapp
$ python manage.py migrate
$ python manage.py runserver

Performing system checks...

System check identified no issues (0 silenced).
October 21, 2018 - 12:19:33
Django version 2.1.2, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```
아래의 명령어를 통해 원하는 port를 지정하여 애플리케이션을 실행시킬 수 있습니다.
아래의 명령어는 1234 port로 애플리케이션을 실행시키는 명령어 입니다.
```
$ python manage.py runserver 1234
```
