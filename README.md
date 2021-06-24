# django-rest-api
django rest api 

### Getting started with python django restful api
1. Make sure you have `python` and `pip` installed in your local machine
2. Create a directory `$mkdir demo`
3.To get started, run the following commands *(MacOs users)*
    - Create a virtual environment `python3 -m venv venv`
    - Start the virtual environment `source venv/bin/activate`
    - Install **Django** and **Django Rest Framwork** `pip3 install django` and `pip install djangorestframework`
    - Check installed packages `pip3 freeze`
    - Create a requirements text file `pip3 freeze > requirements.txt`
    - Setup a new project `django-admin startproject demo_api`
    - Within the newly created `demo_api` run `django-admin startapp api` or `python3 manage.py startup api`
      
4. We can set up our database by running our first migration
   - `python3 manage.py makemigrations`
   - `python3 manage.py migrate`
   
5. Finally, we’ll need to create our first user. Let’s call this user admin, and set the user’s password to password. From the terminal, run:
  - `python3 manage.py createsuperuser`

6. Installed Apps (settings.py)
   - Adding multiple apps in order to make use of them in our Django project
   - We'll have to add `api` and `rest_framework` in our `settings.py` file.
     ```python:
         INSTALLED_APPS = [
               ‘api’,
               ‘rest_framework’,
         ]
      ```

7. Build out our API
  - Now that our housekeeping is done, you can proceed onto writing some of your own code.

#### (a) Serializers (serializers.py)
#### (b) Views (views.py)
#### (c) URLs (urls.py)
#### (d) Pagination (settings.py)
   ```python:
         REST_FRAMEWORK = {
             'DEFAULT_PAGINATION_CLASS': 'rest_framework.pagination.PageNumberPagination',
             'PAGE_SIZE': 10
         }
   ```
