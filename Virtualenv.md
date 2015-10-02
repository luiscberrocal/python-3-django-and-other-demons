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
