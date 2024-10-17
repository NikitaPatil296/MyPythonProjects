# Hello World Django Web Application  

This is a simple Django project that displays "Hello World" on a webpage. The purpose of this project is to demonstrate a basic Django setup and web application. <br>

## Requirements 
Python 3.x	<br> 	
pip (Python package installer)<br> 
Virtualenv or venv (optional, but recommended)<br> 
Django (you can install the latest version) <br>

## Run the Django Development Server 
```
python manage.py runserver
```

## View the Application
http://127.0.0.1:8000/  
You should see the Hello World message displayed on the page.
<br>

## Project Explanation
<b>1. Views</b>  
In views.py, the hello_world view function is defined to return an HTTP response with "Hello World".
```python
from django.http import HttpResponse

def hello_world(request):
    return HttpResponse("Hello World")
```
<br> 
  
<b>2. URLs of App</b>  
In urls.py, we define a URL pattern to map the root URL to the hello_world view.
```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.hello_world, name='hello_world'),
]
```
<br> 
  
<b>3. URLs of Main Project</b>
```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('', include('HelloWorldApp.urls')),
    path('admin/', admin.site.urls),
]
```

## Acknowledgments  
This project was created as a simple demonstration of a Django web application.
