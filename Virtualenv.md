#VirtualEnv

##Installing Python3

http://blog.manbolo.com/2013/02/04/how-to-install-python-3-and-pydev-on-osx

http://hackercodex.com/guide/python-development-environment-on-mac-osx/

##Updating version 3.4.1 to 3.4.3

As of august 2015 Heroku supports 3.4.3 which is the lateste versión. 

Since I cheated forcing home brew to  install an older Python3 formula. I had to do a hard reset to eliminate the python3.rb formula.

``````bash
$ cd $( brew --prefix )

$ git reset –hard

$ brew upgrade

$ brew install python3

``````

![alt text](./images/image002.png "Git results")


##Installing versión Python 3.4.1

Current homebrew version installs Python 3.4.2 but Heroku currently supports python 3.4.1.
So we need to install 3.4.1. To do this  we need to install a specific commit

The commit we are looking for can be found at http://braumeister.org/formula/python3


![alt text](./images/image003.png "Python 3.4.1 formula")

![alt text](./images/image004.png "Python 3.4.1 commit")

You must unlink the current versión 3.4.2

``````
$ brew unlink python3
``````

![alt text](./images/image005.png "Python 3.4.1 unlink")


First, go to the homebrew base directory
``````
$ cd $( brew --prefix )
``````

Checkout some old formula
```````
$ git checkout 979810a69b2dd4e9e0e4374b9eb3f361dc6cd54a Library/Formula/python3.rb
$ brew install python3
``````
 
![alt text](./images/image006.png "Python 3.4.1 install")

![alt text](./images/image007.png "Python 3.4.1 version")

##Installing Virtualenv for Python3

``````
$ pip3 install virtualenv
``````

It gets installed /usr/local/lib/python3.4/site-packages/

##Creating a Virtual Environment on Windows 7

``````
$ cd c:\python_environments
$ c:\Python34\python.exe c:\Python34\Lib\site-packages\virtualenv.py --no-site-packages <virtual_environment_name>
``````
![alt text](./images/image008.png "Python 3.4.1 version windows")

##Creating a Virtual Environment on Mac

My path for virtual environments es ~/virtual_environments.

Replace <virtual_environment_name> with the name of your virtual environment.

``````
$ cd ~/virtual_environments
$ python3 /usr/local/lib/python3.4/site-packages/virtualenv.py --no-site-packages <virtual_environment_name>
``````
 ![alt text](./images/image009.png "Creating virtual environment")

If you have installed Anaconda. You will get an error (see Problem with Anaconda and VirtualEnv  on page 11). Use this command instead
``````
$ /usr/local/Cellar/python3/3.4.1_1/bin/python3 /usr/local/lib/python3.4/site-packages/virtualenv.py --no-site-packages <virtual_environment_name>
``````
``````
cd ~/virtual_environments
source ./<virtual_environment_name>/bin/actívate
``````

``````
python --version
``````
 
 ![alt text](./images/image010.png "Python version mac")
 
 
##Installing Django

To install Django in the new virtual environment, run the following command:

``````
$ pip install django 
``````

## Creating your Project

The proposed projec structure is based on the book Two Scoops of Icecream. The template is found here: https://github.com/twoscoops/django-twoscoops-project 
To create a new Django project called 'wildbills' using django-twoscoops-project, run the following command:
``````
$ cd ~/PycharmProjects
``````

I created a fork of the project with the two scoops template to add Heroku support.

This project has the Procfile, runtime.txt files that require Heroku. This project is configured for Python 3.4.1.
``````
$ django-admin.py startproject --template=https://github.com/luiscberrocal/django-twoscoops-project/archive/master.zip --extension=py,rst,html --name=Procfile wildbills_project
``````
The original I used was this one. Do not use this one, I’m showing it as reference to remember where I got the command from.

``````
$ django-admin.py startproject --template=https://github.com/twoscoops/django-twoscoops-project/archive/master.zip --extension=py,rst,html wildbills_project
``````

 ![alt text](./images/image011.png "List of project content")


 


 
 




