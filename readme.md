# Please read this file !

this file will store all the commands for this projects

# use to create a virutal enviroment
python -m venv env

# to check the python version
python -V

# activate virtual env
bin/Script/activate

# install package/library
pip install Django
pip install mssql-django

# create a new blog file and create a application file(article)
django-admin startproject blog
cd blog
python manage.py startapp article
python manage.py runserver


# change setting file
DATABASES = {
    'default': {
        'ENGINE': 'mssql',
        'NAME': 'Blog',
        'host': '(LocalDb)\MSSQLLocalDB',
        'user':'',
        'password':'',
        'options':{
            'driver': "ODBC Driver 17 for SQL Server",
        }
    }
}

# go sql server tools, create a new database

# create all models migration/update database
python manage.py makemigrations
python manage.py migrate

# create a super user account/admin
python manage.py createsuperuser