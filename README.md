# Lead Manger Application

## Starting the project

`pip3 install pipenv` \
`pipenv shell` - creates a virtual environment and creates a Pipfile \
`pipenv install django djangorestframework django-rest-knox` - django-rest-knox for token authentication \
`django-admin startproject leadmanager` - start a new project \
`cd leadmanager` \
`python manage.py startapp leads` - creates a new app called leads

In settings add `'leads', 'rest_framework'` in INSTALLED_APPS.

Create migration: `python manage.py makemigrations leads` \
Put table and columns into database: `python manage.py migrate`

## Running the project

Run the server:`python manage.py runserver`
