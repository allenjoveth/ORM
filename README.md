# Ex02 Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a student database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![erdiagram](erdiagram.png)


## DESIGN STEPS
STEP 1:
clone the repository inside the folder ex02 by the command 'git clone https://github.com/<>/django-orm-app'

STEP 2:
After cloning the folder with the repository name django-orm-app will be created

STEP 3:
Now move into the django-orm-appfolder by using the command 'cd django-orm-app'

STEP 4:
Now give the command python3 manage.py startapp myapp to create myapp

STEP 5:
In settings.py add 'import os' in line 14,add '*'in line 28 inside the bracket and type 'myapp' in the line 40 and add 'STATICFILES_DIRS=[os.path.join(BASE_DIR,'static')]

STEP 6:
In the myproj give the command 'python3 manage.py makemigrations'

STEP 7:
Give the command 'python3 manage.py migrate'

STEP 8:
Now give the command 'python3 manage.py createsuperuser'

STEP 9:
NOW give the command 'python3 manage.py runserver 0:8000'

STEP 10:
Now open django webserver crete users and students

STEP 11:
Now take the screenshot and upload it in django-orm-app

STEP 12:
Now command the git that you want to include updates by the command 'git add -A'

STEP 13:
Configure the username by the command "git config user.name 'username'"

STEP 14:
Configure the github email by the command git cofig user.email 'user@gmail.com'

STEP 15:
Commit all the updates git commit -m 'success'

STEP 16:
Change the url of the github remote repository by the command git remote set-url origin https://user:TOKEN@github.com/user/repo

STEP 17:
Push the changes in the branch github repository by the command git push origin main

## PROGRAM

```
admin.py

from django.contrib import admin
from .models import Student,StudentAdmin
admin.site.register(Student,StudentAdmin)

models.py

from django.db import models
from django.contrib import admin

class Student (models.Model):

    referencenumber=models.CharField(max_length=20,help_text="reference number")

    name=models.CharField(max_length=100)

    age=models.IntegerField()

    email=models.EmailField()

    salary=models.IntegerField()


class StudentAdmin(admin.ModelAdmin):

    list_display=('referencenumber','name','age','email','salary')


```

## OUTPUT
![output](out.png)


## RESULT
The program for creating an student database using ORM is executed successfully.