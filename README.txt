commands
python3 -m venv env # create virtual env
source env/bin/activate # activate virtual env

export PG_HOME=/Library/PostgreSQL/17  # pg_config executable not found.
export PATH=$PATH:$PG_HOME/bin

 pip install -r requirements.txt


 django-admin startproject backend #make project

python manage.py startapp api

python manage.py makemigrations

python manage.py runserver

python manage.py migrate
settings

npm create vite@latest frontend -- --template react

cors
CORS_ALLOW_ALL_ORIGINS = True
CORS_ALLOWS_CREDENTIALS = True
ALLOWED_HOSTS = ['*']

JWT
REST_FRAMEWORK = {
    "DEFAULT_AUTHENTICATION_CLASSES": (
        "rest_framework_simplejwt.authentication.JWTAuthentication",
    ),
    "DEFAULT_PERMISSION_CLASSES": [
        "rest_framework.permissions.IsAuthenticated",
    ],
}

SIMPLE_JWT = {
    "ACCESS_TOKEN_LIFETIME": timedelta(minutes=30),
    "REFRESH_TOKEN_LIFETIME": timedelta(days=1),
}

backend/api -> create a file serializers.py
url.py => 

INSTALLED_APPS
with anything you add
    "api",
    "rest_framework",
    "corsheaders",

middleweare


    "corsheaders.middleware.CorsMiddleware",

Requirements

asgiref
Django
django-cors-headers # CORS issues
djangorestframework
djangorestframework-simplejwt # handling JWT auth
PyJWT 
pytz
sqlparse
psycopg2-binary #post greee
python-dotenv # loading env 