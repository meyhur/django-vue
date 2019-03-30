# Create Virtual Enviroment and Django Project
***

## Create Virtual Enviroment

```console
virtualenv venvdjangovue -p python3
cd venvdjangovue
source bin/activate
```

## Clone project

```console
git clone https://github.com/meyhur/django-vue.git
cd django-vue
pip install -r requirements.txt
```

## Migrate django

```console
python manage.py migrate
python manage.py createsuperuser

*Username (leave blank to use 'yourname'):*
*Email address:*
*Password:*
*Password (again):*
```

## Install npm dependencies

```console
cd frontend
npm install
```

# Running the Vue bundle in Django DevServer

## We need two terminals.

### First we run **frontend**

```console
cd frontend
npm run serve
```

### Than, in another terminal, this should have your virtual environment activated

```console
virtualenv django-vue -p python3
source bin/activate
python manage.py runserver
```

Now navigate to <http://127.0.0.1:8000>, and you should see the Vue App instead of django’s default page.