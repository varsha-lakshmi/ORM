# Ex01 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to manage an online food delivery platform like Zomato/Swiggy using Object Relational Mapping (ORM).

## ENTITY RELATIONSHIP DIAGRAM



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```
model.py
from django.db import models

class OrderDatabase(models.Model):
    OrderID = models.AutoField(primary_key=True)
    UserID = models.IntegerField()
    OrderDate = models.DateField()
    ItemName = models.CharField(max_length=100)
    OrderQty = models.IntegerField()
    UnitPrice = models.FloatField()
    TotalAmount = models.FloatField()
    DeliveryAddress = models.CharField(max_length=200)

    def __str__(self):
        return self.ItemName
    admin.py
        from django.contrib import admin

from .models import OrderDatabase

@admin.register(OrderDatabase)
class OrderAdmin(admin.ModelAdmin):
    list_display = (
        'OrderID',
        'UserID',
        'OrderDate',
        'ItemName',
        'OrderQty',
        'UnitPrice',
        'TotalAmount',
        'DeliveryAddress'
    )
```
## OUTPUT


![alt text](<Screenshot 2026-05-12 100944.png>)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
