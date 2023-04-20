# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![aish django output (12)](https://user-images.githubusercontent.com/121166390/233250890-a89cfb37-4bcc-4773-80c9-6bedebd50a7d.jpg)

## DESIGN STEPS
### STEP 1:
An Django application is created inside dataproject folder.

### STEP 2:
A python program is written to create a table to store and retrieve data.

### STEP 3:
The table is created with 5 fields in which the username field is made as PrimaryKey.

### STEP 4:
Then the project files migrated. A superuser is also created.

### STEP 5:
Now the server side program is executed .

### STEP 6:
The admin page of our website is accessed using username and password.

### STEP 7:
Records are added and saved in the table inside the database.

## PROGRAM
```
Developed by : Thirukaalathessvarar S
Reg.no : 212222230161
```

### model.py
```
from django.db import models
from django.contrib import admin

class Student(models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    dept=models.CharField(max_length=5)


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','dept')
```

### admin.py
```
from django.contrib import admin
from .models import Student,StudentAdmin
admin.site.register(Student,StudentAdmin)
```

## OUTPUT

![aish django output (1)](https://user-images.githubusercontent.com/121166390/233250196-279a602e-47e5-4dbf-9799-801052751214.jpg)


## RESULT
A Django application has been created that can be used to store and retrieve data from the database using Object Relational Mapping(ORM).
