# Bangazon Django REST API

## Steps to get the Bangazon API started

1. Create a new directory in your terminal. Clone down this repository by clicking the "Clone or Download" button above, copying the SSH key, and running the following command in your terminal `git clone sshKeyGoesHere`
1. `cd bangazon-api-imagination-station-api`
1. Create your OSX virtual environment in Terminal:
- `python -m venv bangazonenv`
- `source ./bangazonenv/bin/activate`
- Or create your Windows virtual environment in Command Line:
    - `python -m venv bangazonenv`
    - `source ./bangazonenv/Scripts/activate`
1. Install the app's dependencies:
- `pip install -r requirements.txt`
1. Build your database from the existing models:
- `python manage.py makemigrations bangazonapi`
- `python manage.py migrate`
1. Create a superuser for your local version of the app:
- `python manage.py createsuperuser`
1. Populate your database with initial data from fixtures files: (NOTE: every time you run this it will remove existing data and repopulate the tables)
- `python manage.py loaddata */fixtures/*.json`
1. Fire up your dev server and have some fun!
- `python manage.py runserver`

## Front-End Client
- This API is dependent on the front-end client. You can find it here: https://github.com/nss-cohort-40/bangazon-ecommerce-client-dead-parrots-frontend

## Fetch calls

Should you choose leverage this API for your own front-end application, please reference the example fetch calls to the endpoints below to see some of the capability of this API. Please note that you will need to pass the Token in the headers for most requests.

## Orders

- Get all orders in the database:
    - http://localhost:8000/orders

## Products

- Get all products in the database:
    - http://localhost:8000/products

## Erd

* (https://i.imgur.com/EntdGBz.png)