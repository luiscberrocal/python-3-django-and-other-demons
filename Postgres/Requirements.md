##Requirements

###Postgres.app

Download from http://postgresapp.com/ 

What's In The Box?
Postgres.app contains a full-featured PostgreSQL installation in a single package:

PostgreSQL 9.3.5
PostGIS 2.1.3
Procedural languages: PL/pgSQL, PL/Perl, PL/Python, and PLV8 (Javascript)
Popular extensions, including hstore and uuid-ossp, and more
A number of command-line utilities for managing PostgreSQL and working with GIS data

####Installing Postgres.app
To install Postgres.app, just drag it to your Applications folder and double click.

On first launch, Postgres will initialise a new database cluster and create a database for your username. A few moments after launching, you should be able to click on "Open psql" to connect to the database.

If you'd like to use the command line tools delivered with Postgres.app, see the section on Command Line Tools.


![Installing Postgres.app 1](./images/image057.png "Installing Postgres.app 1")

![Installing Postgres.app 2](./images/image058.png "Installing Postgres.app 2")

###PGAdmin3 1.18.1

It seems the postgress.app installation does not creat a postgress role by default. It created a username luiscberrocal. I could only connect to the database with that user.


Download from http://www.postgresql.org/ftp/pgadmin3/release/v1.18.1/osx/


![PGAdmin3 1.18.1 1](./images/image059.png "PGAdmin3 1.18.1 1")

![PGAdmin3 1.18.1 2](./images/image060.png "PGAdmin3 1.18.1 2")
