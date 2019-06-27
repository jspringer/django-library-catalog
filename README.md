# Django Local Library

Mock online library catalog access platform that allows the end user to see books the library carries and their availability. The end user cannot check out books online. 

[Demo](http://jsnspr-django-library.herokuapp.com/)

A superuser/admin can access the [Admin platform](https://jsnspr-django-library.herokuapp.com/admin/) (/admin) to add new authors and books. Login: ``admin`` password: ``Qaz2Wsx#Edc``

The main features that have currently been implemented are:

* There are models for books, book copies, genre, language and authors.
* Users can view list and detail information for books and authors.
* Admin users can create and manage models. The admin has been optimised (the basic registration is present in admin.py, but commented out).
* Librarians can renew reserved books.

## Fixes/Features being worked on: 
1. Improve the UI for all devices. 
2. Fix 500 error when accessing "All Borrowed" (/catalog/borrowed/). Works locally but not on Heroku, related to static files, see [Heroku doc](https://devcenter.heroku.com/articles/django-assets).

## Quick Start

Make sure you're in the root directory where requirements.txt is located and set this up within a Python virtual environment. 
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