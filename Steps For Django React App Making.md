# Steps For Creating DJANGO - REACT APP

### Setting Up DJANGO


- `mkdir django-react-app`
- create venv by add interpreter
- `pip install django`
- `djnago-admin startproject backend`
- `cd backend`
- `python manage.py startapp todo`
- `python manage.py migrate`
- `python manage.py runserver`
- register todo app in settings
- todo model
- `python manage.py makemigration todo`
- `python manage.py migrate todo`
- register model in admin.py
- `python manage.py createsuperuser`
- `python manage.py runserver`

### Setting Up Api DRF

- `pip install djangorestframework django-cors-headers`
- register it in installed app and middleware cors-header
- cors origin whitelist - localhost:3000
- creation serializers,viewsets and routers for it
- `python manage.py runserver`

### Setting Up Frontend
- install node
- `npx create-react-app frontend`
- cd frontend
- `npm start`
- `npm install bootstrap reactbootstrap`
- add css files to index.js
- create your ui and working things in app.js
- create modal with modal js in components
- install axios : `npm install axios`
- add proxy to package.json
  > proxy:"http://localhost:8000"
- without proxy
  > axios.get("http://localhost:8000/api/todos")
- with proxy relative path
  > axios.get("api/todos/")
- now you can make requests with axios for data operation

### Now DO Final Step:
- `python manage.py runserver`
- `npm start`

