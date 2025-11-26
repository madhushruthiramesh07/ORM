# Ex01 Django ORM Web Application
## Date: 

## AIM
To develop a Django Application to store and retrieve data from a E-Commerce Website Database for Amazon or Flipkart using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
```
admin.py
from django.contrib import admin
from .models import Car, CarAdmin

admin.site.register(Car, CarAdmin)
```

```
models.py
from django.db import models
from django.contrib import admin

class Car(models.Model):
    car_id = models.AutoField(primary_key=True)   # Primary key
    model_name = models.CharField(max_length=100)
    manufacturer = models.CharField(max_length=100)
    year_of_make = models.IntegerField()
    price = models.FloatField()
    fuel_type = models.CharField(max_length=20)
    mileage = models.FloatField()

    def __str__(self):
        return f"{self.model_name} ({self.manufacturer})"


class CarAdmin(admin.ModelAdmin):
    list_display = ["car_id", "model_name", "manufacturer", "year_of_make", "fuel_type"]
```


## OUTPUT

<img width="1920" height="1020" alt="Screenshot 2025-11-25 235544" src="https://github.com/user-attachments/assets/80ac8acf-f2f3-449a-b6ad-ecf28b5e9941" />


## RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
