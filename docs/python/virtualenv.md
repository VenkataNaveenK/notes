# Virtual environment
## Using Virtualenv
Creating virtual environment using the below commands

1. Installing 'virtualenv' module
```py 
pip install virtualenv
```
2. Creating virtual environment
```
virtualenv venv
```
This command creates a ```venv``` folder in the current working directory.
3. Activating created virtual environment
```
venv\Scripts\activate
```
## Running application with .bat
1. Create a ```env_setup.bat``` file with the below commands
```
pip install virtualenv
virtualenv venv
pip install -r requirements.txt
```
2. Create a ```run.bat``` file with the below commands
```
call venv\Scripts\activate
<application start command>
```
## Using Anaconda
Create a virtual environment using a .yaml/.yml file
``` py
conda env create -f <filename.yml>
```
Sample environment.yml file:



