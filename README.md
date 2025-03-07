# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Entity Relationship Diagram](./er.png)

## DESIGN STEPS

### STEP 1:
Clone the problem from github

### STEP 2:
create a new app

### STEP 3:
Enter the code for admin.py and model.py

### STEP 4:
Execute Django admin and create 10 employees

## PROGRAM


Models.py

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

Admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)


## OUTPUT

![OUTPUT](./Out.png)
![out](https://user-images.githubusercontent.com/119393675/212843029-593f3147-e89c-4330-a5cd-0f341f26ac36.png)

## RESULT

Program executed successfully
