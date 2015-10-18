##Creating a Virtual Environment on OSx

My path for virtual environments is ~/virtual_environments.

Replace <virtual_environment_name> with the name of your virtual environment.

``````
$ cd ~/virtual_environments

$ python3 /usr/local/lib/python3.4/site-packages/virtualenv.py --no-site-packages <virtual_environment_name>
``````
 ![alt text](../images/image009.png "Creating virtual environment")

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
 
 ![alt text](../images/image010.png "Python version mac")
