# Install and Run First Django Project on Ubuntu 18.04


## First install and setup enviornment

### setting up enviornment 


`sudo apt-get update`

`sudo apt-get -y upgrade`

`python3 --version`

`sudo apt-get install -y python3-pip`

`sudo apt-get install build-essential libssl-dev libffi-dev python-dev`
 
`sudo apt-get install -y python3-venv`
 
`mkdir environments`

`cd environments`

`python3 -m venv project_env`

`source project_env/bin/activate`

#### final output

`(project_env) bobby@bobby:~/environments$`


## 2. Install Django 

`sudo nano requirements.txt`   Then add line ->   `Django~=2.0.6`  we can change the version according to our needs . But we need to create new env  Then `CTRL+O`,`CTRL+Q`

`pip install -r requirements.txt`

#### final output

`(project_env) bobby@bobby:~/environments$ pip install -r requirements.txt`

`Collecting Django~=2.0.6 (from -r requirements.txt (line 1))`

  `Downloading Django-2.0.6-py3-none-any.whl (7.1MB)`
  
`Installing collected packages: Django`

`Successfully installed Django-2.0.6`

