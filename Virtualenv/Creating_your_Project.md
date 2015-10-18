## Creating your Project

The proposed projec structure is based on the book Two Scoops of Icecream. The template is found here: https://github.com/twoscoops/django-twoscoops-project 
To create a new Django project called 'wildbills' using django-twoscoops-project, run the following command:
``````
$ cd ~/PycharmProjects
``````

I created a fork of the project with the two scoops template to add Heroku support.

This project has the Procfile, runtime.txt files that require Heroku. This project is configured for Python 3.4.1.

On mac run:

``````
$ django-admin.py startproject --template=https://github.com/luiscberrocal/django-twoscoops-project/archive/master.zip --extension=py,rst,html --name=Procfile wildbills_project
``````
On Windows run
``````
> django-admin startproject --template=https://github.com/luiscberrocal/django-twoscoops-project/archive/master.zip --extension=py,rst,html --name=Procfile wildbills_project
``````
The original I used was this one. Do not use this one, I’m showing it as reference to remember where I got the command from.

``````
$ django-admin.py startproject --template=https://github.com/twoscoops/django-twoscoops-project/archive/master.zip --extension=py,rst,html wildbills_project
``````

 ![alt text](../images/image011.png "List of project content")
