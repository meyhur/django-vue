h1 Create Virtual Enviroment and Django Project
***

h2 Create Virtual Enviroment

```console
virtualenv django-vue -p python3
cd django-vue
source bin/activate
```

h2 Clone project

```console
git clone ...
cd myproject
pip install -r requirements.txt
```

h2 Migrate django

```console
python manage.py migrate
python manage.py createsuperuser

*** Username (leave blank to use 'yourname'): ***
*** Email address: ***
*** Password: ***
*** Password (again): ***
```

h2 Install npm dependencies

```console
cd frontend
npm install
```

h1 Running the Vue bundle in Django DevServer

h2 We need two terminals.

h3 First we run **frontend**

```console
cd frontend
npm run serve
```

h3 Than, in another terminal, this should have your virtual environment activated

```console
virtualenv django-vue -p python3
source bin/activate
python manage.py runserver
```

Now navigate to <http://127.0.0.1:8000>, and you should see the Vue App instead of django’s default page.