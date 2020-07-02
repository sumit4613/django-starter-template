# DjangoStarterTemplate

A template for launching new Django Rest Framework projects quickly. Comes with a custom user model, login/logout/register/login_with_otp via [drf_user](https://github.com/101Loop/drf-user) and more.

## Features

- Django 2.0(LTS), Django REST Framework 3.11
- Custom user model via [drf_user](https://github.com/101Loop/drf-user)
- JWT Token-based auth
- Signup/login/logout
- Requirements.txt for managing dependencies
- Env based settings, just copy .env.example file to .env and add your variables
- [Swagger](https://github.com/axnsan12/drf-yasg) for API documentation

## First-time setup

-  Make sure Python 3.x is already installed. [See here for help](https://www.python.org/downloads/).
-  Clone the repo and configure the virtual environment:
-  To know about virtualenv use this link [VirtualEnv](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)
```
$ git clone https://github.com/sumit4613/django-starter-template.git
$ cd django-starter-template
$ source .venv/bin/activate # activate virtual environment (.venv is the name, use any name as you like)
$ pip install -r requirements.txt
```

-  Set up the initial migration for our custom user models in users and build the database.

```
(.venv) $ python manage.py migrate
(.venv) $ python manage.py createsuperuser
(.venv) $ python manage.py runserver
```

-  Endpoints

Login with your superuser account. Then navigate to [Swagger Url](http://127.0.0.1:8000/swagger) to view all the endpoints.

- account - http://127.0.0.1:8000/api/v1/user/account/
- isunique - http://127.0.0.1:8000/api/v1/user/isunique/
- login - http://127.0.0.1:8000/api/v1/user/login/
- otp - http://127.0.0.1:8000/api/v1/user/otp/
- otpreglogin - http://127.0.0.1:8000/api/v1/user/otpreglogin/
- register - http://127.0.0.1:8000/api/v1/user/register/

---
