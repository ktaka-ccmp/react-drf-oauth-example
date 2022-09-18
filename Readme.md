# React.js + Django Rest Framework + Google OAuth2

## Prep

### Django

python3 -m venv .venv\
source .venv/bin/activate
pip install django djangorestframework django-cors-headers 
pip install coreapi
django-admin startproject backend
cd backend/
django-admin startapp restapi
python manage.py createsuperuser --email admin@example.com --username admin

pip install model_bakery
vi backend/restapi/models.py
./manage.py  migrate
vi backend/restapi/test-models.py
./manage.py test restapi

backend/backend/settings.py
backend/backend/urls.py

backend/restapi/serializers.py
backend/restapi/views.py
backend/restapi/urls.py

curl -H 'Accept: application/json' http://localhost:8000/api/customer/|jq .

pip install python-decouple

### React.js

For react.js, frontend/.env:
REACT_APP_API_SERVER=http://v147.h.ccmp.jp:8000

For django, backend/backend/.env:
ORIGIN_SERVER=http://v147.h.ccmp.jp:3000

