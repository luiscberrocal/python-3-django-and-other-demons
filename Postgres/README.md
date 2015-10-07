#Postgres

{% include Requirements.md %}

###PGAdmin3 1.18.1

It seems the postgress.app installation does not creat a postgress role by default. It created a username luiscberrocal. I could only connect to the database with that user.


Download from http://www.postgresql.org/ftp/pgadmin3/release/v1.18.1/osx/


![PGAdmin3 1.18.1 1](./images/image059.png "PGAdmin3 1.18.1 1")

![PGAdmin3 1.18.1 2](./images/image060.png "PGAdmin3 1.18.1 2")


##Starting Postgres

![Starting Postgres 1](./images/image061.png "Starting Postgres 1")

![Starting Postgres 2](./images/image062.png "Starting Postgres 2")


##Creating Database

![Creating Database 1](./images/image063.png "Creating Database 1")

![Creating Database 2](./images/image064.png "Creating Database 2")

![Creating Database 3](./images/image065.png "Creating Database 3")

![Creating Database 4](./images/image066.png "Creating Database 4")

![Creating Database 5](./images/image067.png "Creating Database 5")

![Creating Database 6](./images/image068.png "Creating Database 6")

![Creating Database 7](./images/image069.png "Creating Database 7")

![Creating Database 8](./images/image070.png "Creating Database 8")

![Creating Database 9](./images/image071.png "Creating Database 9")

![Creating Database 10](./images/image072.png "Creating Database 10")


##Exporting the Postgres path

If you get an error Reading:

Error: pg_config executable not found.

You need to include in the PATH variable the postgres path
```
PATH=$PATH:/Applications/Postgres.app/Contents/Versions/9.3/bin/
```

##Connecting Django to Database

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


##Run syncdb (Django 1.6 or less)

```
$ python manage.py syncdb --settings=timesheet_project.settings.local

```

![Run syncdb 1](./images/image073.png "Run syncdb 1")

![Run syncdb 2](./images/image074.png "Run syncdb 2")




##Run syncdb (Django 1.7.x)

```
$ python manage.py syncdb --settings=timesheet_project.settings.local
```

![Run syncdb 1.7](./images/image075.png "Run syncdb 1.7")

##Problem connecting to Postgres from Windows

I encountered this error when I tried to connect with pgAdmin running on Windows 7 to a Postgres instance running on an Ubuntu 14.04 LTS.

![Postgres error 1](./images/image076.png "Postgres error 1")

It seems my ip address was not cleared to connect to the server. I had to edit on the ubunte server the `/etc/postgresql/9.1/main/pg_hba.conf` file.

Run

```
$ sudo nano /etc/postgresql/9.1/main/pg_hba.conf
```

Add your ip address range.

![Postgres error 2](./images/image077.png "Postgres error 2")

```
$ service postgresql restart
```

