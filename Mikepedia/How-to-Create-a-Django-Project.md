---  
share: true  
title: "How to Create a Django Project"  
---  
up :: [∴ Software Development](./%E2%88%B4-Software-Development.md)  
  
# Database  
  
## Postgres  
  
Start postgres:  
  
```shell  
sudo service postgresql start  
```  
  
Create a database:  
  
```shell  
sudo -u postgres createdb <project-name>  
```  
  
# Django  
  
Make a project dir:  
  
```shell  
mkdir <project-dir>  
cd <project-dir>  
```  
  
Init poetry:  
  
```shell  
poetry init  
```  
  
Follow the prompts. Add `Django` as a dependency and `black` as a development dependency.  
  
Poetry install:   
  
```shell  
poetry install  
```  
  
Create django project:  
  
```shell  
poetry run django-admin startproject <project-name> .  
```  
  
Create django app:  
  
```shell  
poetry run ./mange.py startapp <app-name>  
```  
  
Run initial migrations:  
  
```shell  
poetry run ./manage.py migrate  
```  
  
Start local server:   
  
```shell  
poetry run ./manage.py runserver  
```  
