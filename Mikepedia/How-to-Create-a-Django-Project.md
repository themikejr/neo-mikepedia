---  
share: true  
---  
up :: [∴ Software Development](./%E2%88%B4-Software-Development.md)  
  
# Database  
  
## Postgres  
  
Start postgres:  
  
```sh  
sudo service postgresql start  
```  
  
Create a database:  
  
```sh  
sudo -u postgres createdb <project-name>  
```  
  
# Django  
  
Make a project dir:  
  
```sh  
mkdir <project-dir>  
cd <project-dir>  
```  
  
Init poetry:  
  
```sh  
poetry init  
```  
  
Follow the prompts. Add `Django` as a dependency and `black` as a development dependency.  
  
Poetry install:   
  
```sh  
poetry install  
```  
  
Create django project:  
  
```sh  
poetry run django-admin startproject <project-name> .  
```  
  
Create django app:  
  
```sh  
poetry run ./mange.py startapp <app-name>  
```  
  
Run initial migrations:  
  
```cli  
poetry run ./manage.py migrate  
```  
  
Start local server:   
  
```cli  
poetry run ./manage.py runserver  
```  
