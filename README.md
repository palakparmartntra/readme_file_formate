## Sunrise Diamond Project ( Backend Part )
> Outline a brief description of your project.project description of sunrise diamond which is en erp platform that we build in ddd architecture.

## Table of contents
* [Technologies](#technologies)
* [Folder structure](#folder-structure)
* [Folder description](#folder-description)
* [Project setup guide](#project-setup-guide)
* [Dependencies](#Dependencies)

## Technologies

* django rest framework
* ddd architecture 
* postgres

Folder structure
------------

    ├── README.md         
    ├── adapters
    │   ├── celery_adapters 
    │   ├── db_adapters  
    │   └── __init__.py  
    │
    ├── infrastructure            
    │   │── djangoapp
    │   │── __init__.py
    │   └──requirements.txt
    │
    ├── modules     
    │   │── common_utilities
    │   │── module_1
    │   │   └── README.md 
    │   │── module_2
    │   │   └── README.md 
    │   └── __init__.py
    │
    ├── tests        
    │   │── adapters
    │   │── infrasturcture
    │   └── modules
    │
    ├── .gitignore           
    │
    ├── requirements.txt   
    │
    └── setup.py        

--------


## Folder description


### Adapters

    Adapter is for any third party service like db message broker , apis ,generators etc.

### Infrastructure

    This part of project is for framework or web service you want to user to deploy your business app and also in shared folder you need to configure dependencies injector for using our modules in web service

### Modules

    It is used to write client specific modules.Some configuration and plugins I used, to make the application itself cleaner.
    each module have readme file for understand that module.
    for understand the module you have visit their readme file

### Tests

    This folder will be used to run testcases for adapters, infrastructure and modules to test every folder,

### Requirements.txt

    This files contains over all application requirement lib.

### Setup.py

    It will install all requirements of this project.

## Project setup guide

#### 1. Clone  the repo

    git clone https://github.com/rajatmishraintntra/djangpocimpro.git

#### 2. Install project as site-package

    cd djangpocimpro and run pip install -e .

#### 3. Install dependencies

    pip install -r requirements.txt

#### Set the Environment variables

| Variable name | Optional | Default Value |
|---------------|----------|---------------|
| db_name       | No       |               |
 | db_host       | No       |               |
 | db_user       | No       |               |
 | db_password   | No       |               |
 | db_driver     | No       | postgresql    |

#### 5. Run migrations and start the server

    python ./infrastructure/djangopoc/manage.py makemigrations && python ./infrastructure/djangopoc/manage.py migrate && python ./infrastructure/djangopoc/manage.py runserver



## Dependencies

- [Injector](https://github.com/alecthomas/injector)
- [pypika](https://pypika.readthedocs.io/en/latest/)
- [SQLAlchemy](https://www.sqlalchemy.org/)

 
