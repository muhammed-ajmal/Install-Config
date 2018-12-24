# First Project

## small blog

`django-admin startproject mysite . `    `Don't forget to add the period (or dot) . at the end!`

### 1. settings.py 

1. `change your timezone and languages in settings.py`  [time zones](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) [languages](https://docs.djangoproject.com/en/2.0/ref/settings/#language-code)

2. We'll also need to add a path for static files.  

add this line `STATIC_ROOT = os.path.join(BASE_DIR, 'static')` below `STATIC_URL = '/static/'`

3. `ALLOWED_HOSTS = ['127.0.0.1', '.pythonanywhere.com']` change `ALLOWED_HOSTS = []`  NB:we are goig to deploy it at pythonanywhere

4. Data base setup using default sqlite3  which is already deifined

`DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}`


 To create a database for our blog, let's run the following in the console: `python manage.py migrate`
 
 ### Run the server
 
 `python manage.py runserver`
 
 ### create app for blog from the directory that contains manage.py
 
 `python manage.py startapp blog`
 
 ### 2.settings.py
 
 After creating an application, we also need to tell Django that it should use it. We do that in the file `mysite/settings.py` open it in your code editor. We need to find `INSTALLED_APPS` and add a line containing `'blog',` just above ]. So the final product should look like this:

` INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'blog',
]`
