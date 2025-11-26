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
models.py
from django.db import models
from django.contrib import admin
class Website(models.Model):
    name = models.CharField(max_length=100)
    product_id = models.AutoField(primary_key=True)
    product_name = models.CharField(max_length=200)
    product_price = models.DecimalField(max_digits=10, decimal_places=2)
    product_description = models.TextField()
    product_seller = models.CharField(max_length=100)
class websiteadmin(admin.ModelAdmin):
    list_display=['product_id','product_name','product_price','product_description','product_seller']
```

```
admin.py
from django.contrib import admin
from .models import Website,websiteadmin
admin.site.register(Website,websiteadmin)
```





## OUTPUT

![WhatsApp Image 2025-11-27 at 00 00 23_4d3a4ea5](https://github.com/user-attachments/assets/954ce851-d2fa-4f0a-91a2-6523d04d862d)


## RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
