# Django Local Library

## Overview

This web application creates an online catalog for a small local library, where users can browse available books and manage their accounts.

The main features that have currently been implemented are:

* There are models for books, book copies, genre, language and authors.
* Users can view list and detail information for books and authors.
* Admin users can create and manage models. The admin has been optimised (the basic registration is present in admin.py, but commented out).
* Librarians can renew reserved books

## Quick Start

Make sure you're in the root directory where requirements.txt is located. 
   ```
   python3 -m venv anyenvname # any name your want, all lowercase, no spaces or special characters
   source anyenvname/bin/activate
   pip3 install -r requirements.txt
   python3 manage.py makemigrations
   python3 manage.py migrate
   python3 manage.py collectstatic
   python3 manage.py test # run the standard tests, all should pass
   python3 manage.py createsuperuser # create a superuser & password that you will use for Admin log in. 
   python3 manage.py runserver
   ```

Admin: `http://127.0.0.1:8000/admin/` - Log in and create new entries, after adding, make sure you see them on the main page: `http://127.0.0.1:8000`. 

## Deploy 

Follow insturctions for deploying Django apps on the hosting service ([Heroku's instructions](https://devcenter.heroku.com/articles/deploying-python)). 