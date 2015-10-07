##Connecting and Configuring Django to Database

###Database configuration

This should have been installed with the local requirements. So DO NOT run it. 

```
$ pip install psycopg2
```

Edit settings/local.py and replace database configuration for this:

```python

########## DATABASE CONFIGURATION
# See: https://docs.djangoproject.com/en/dev/ref/settings/#databases
DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.postgresql_psycopg2",
        "NAME": "wildbills",
        "USER": "",
        "PASSWORD": "",
        "HOST": "localhost",
        "PORT": "",
    },
}
########## END DATABASE CONFIGURATION
```
