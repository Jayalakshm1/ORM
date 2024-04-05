# Ex02 Django ORM Web Application
## Date: 04/04/2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

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
models.py
```
from django.db import models

class Author(models.Model):
    name = models.CharField(max_length=100)
    nationality = models.CharField(max_length=100)
    birth_year = models.IntegerField()
    biography = models.TextField()

class Book(models.Model):
    title = models.CharField(max_length=200)
    author = models.ForeignKey(Author, on_delete=models.CASCADE)
    genre = models.CharField(max_length=100)
    publication_year = models.IntegerField()
    pages = models.IntegerField()
```
admin.py
```
from django.contrib import admin
from .models import Author, Book

admin.site.register(Author)
admin.site.register(Book)
```
## OUTPUT 
![alt text](<WhatsApp Image 2024-04-05 at 12.03.28 PM.jpeg>)
![alt text](<WhatsApp Image 2024-04-05 at 12.03.28 PM (1).jpeg>)
![alt text](<WhatsApp Image 2024-04-05 at 12.03.27 PM.jpeg>) 
![alt text](<WhatsApp Image 2024-04-05 at 12.03.27 PM (1).jpeg>)
## RESULT
Thus the program for creating a database using ORM hass been executed successfully
