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

## Starting the front-end

From the leadmanager folder run:
`python manage.py startapp frontend` - create a new app called fronend \
`mkdir -p ./frontend/src/components/` - create folder for components \
`mkdir -p ./frontend/static/frontend` - contains compiled javascript\
`mkdir -p ./frontend/templates/frontend` - has main index.html \

cd to the root:
`npm init -y` \
`npm i -D webpack webpack-cli` \
`npm i -D @babel/core babel-loader @babel/preset-env @babel/preset-react babel-plugin-transform-class-properties` - transpiling javascript from ES2015 and beyond \
`npm i react react-dom prop-types`

create `.babelrc` file with preset configurations \
create `webpack.config.js` for webpack configuration

The whole application has to be rebuilt upon any changes,
otherwise the main.js will not change, and therefore changes will not be applied.

Adding `--watch` to the script in `package.json` allows for npm run dev to run, everytime a change in files has occured, therefore recompiling the application, therefore showing in the browser straight away.

## Redux

`npm i --save redux react-redux redux-thunk redux-devtools-extension`
`npm i --save axios`

## Alerts

`npm i --save react-alert react-alert-template-basic react-transition-group`
