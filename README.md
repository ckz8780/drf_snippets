# Welcome

This little app allows the submission and syntax highlighting of code snippets. It is backed by the Django REST Framework and uses Python's [Pygments](http://pygments.org/) package for syntax highlighting.

## Requirements:

- Django 2.0.6+
- Python 3.6.5+
- Everything in requirements.txt

## Usage: 

1. `git clone` or download/extract this repo.
2. Create a [virtual environment](https://virtualenv.pypa.io/en/stable/userguide/#usage) (`virtualenv env_name`)
3. cd into and activate your venv (`source bin/activate` or `path\to\env\Scripts\activate`)
4. `sudo pip install -r requirements.txt`
5. Make/run migrations: `python manage.py makemigrations`, `python manage.py migrate`
6. Create a superuser `python manage.py createsuperuser`
7. Run the dev server: `python manage.py runserver`
8. Navigate to http://127.0.0.1:8000

## Available Endpoints: 

- /users/ - List/detail users
- /snippets/ - List/detail/create/delete/update snippets
- /schema/ - Display the schema

## CoreAPI:

You can use [coreapi-cli](http://www.coreapi.org/) to navigate around and manipulate this API. Try creating some snippets and then displaying/modifying them from the command line. 

## Notes:

This is not meant to be a production app. If you decide to extend it to make it do something where security matters, do not use the existing `SECRET_KEY` in production! Replace it and put it in an environment variable before going live. 