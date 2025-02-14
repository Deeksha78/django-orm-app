# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![OUTPUT](./er.png)

## DESIGN STEPS

### STEP 1:
Clone the repository from github.

### STEP 2:
Create an admin interface for Django.

### STEP 3:
Create an app and edit settings.py

### STEP 4:
Makemigrations and migrate the changes.

### STEP 5:
Create admin user and write Python code for admin and models.

### STEP 6:
Make all the migrations to 'myapp'

### STEP 7:
Create an employee database with 10 fields using runserver command.

## PROGRAM

```
admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

models.py
from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

```

## OUTPUT

![OUTPUT](./out.png)

## RESULT
Program executed successfully