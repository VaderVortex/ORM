# Ex02 Django ORM Web Application
# Date:
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py


## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
admin.py
from django.contrib import admin
from .models import Movie  # Import your model

class MovieAdmin(admin.ModelAdmin):
    list_display = ('id', 'title', 'director', 'release_year', 'genre')  # Customize fields
    list_filter = ('genre', 'release_year')  # Optional: Add filtering options
    search_fields = ('title', 'director')  # Optional: Add a search bar

admin.site.register(Movie, MovieAdmin)  

models.py
from django.db import models

class Movie(models.Model):
    id = models.AutoField(primary_key=True)  # Primary key
    title = models.CharField(max_length=255)
    director = models.CharField(max_length=255)
    release_year = models.IntegerField()
    genre = models.CharField(max_length=100)
    rating = models.FloatField()

    def __str__(self):
        return self.title
# OUTPUT
Include the screenshot of your admin page.
![image](https://github.com/user-attachments/assets/cd67ba2e-e2d8-4c05-9e5d-88b66e60af2f)


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
