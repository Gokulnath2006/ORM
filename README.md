# Ex02 Django ORM Web Application
## Date: 
17-04-2025
## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![alt text](<Screenshot 2025-04-17 010143.png>)

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
admin.py

from django.contrib import admin
from .models import Movie

class MovieAdmin(admin.ModelAdmin):
    list_display = ('movie_id', 'title', 'genre', 'release_year', 'director', 'rating')

admin.site.register(Movie, MovieAdmin)

models.py

from django.db import models

class Movie(models.Model):
    movie_id = models.AutoField(primary_key=True)
    title = models.CharField(max_length=100)
    genre = models.CharField(max_length=50)
    release_year = models.IntegerField()
    director = models.CharField(max_length=100)
    rating = models.FloatField()

    def __str__(self):
        return self.title
```

## OUTPUT

![alt text](<Screenshot 2025-04-17 004801.png>)


## RESULT
Thus the program for creating movies database using ORM hass been executed successfully
