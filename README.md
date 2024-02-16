Step 1: Create a Django Project


django-admin startproject mansa_prj
cd mansa_prj/

Step 2: Create a Django App

python manage.py runserver

Step 3: Define a View

python manage.py startapp polls

Open polls/views.py and define a simple view that returns a JSON response

The sequel for the project 
more db.sqlite3

Running the migration


from django.http import httpResponse

def index(request):
    return HttpResponse('Hello World')

Step 4: Configure URL Routing

Open 'polls/urls.py' and configure URL routing for the 'index' view:

from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
]

Step 5: Include the polls  URLs in the Project
Open polls/urls.py and include the URLs from the index app:

from django.contrib import admin
from django.urls import include, path

urlpatterns = [
        path('polls/', include('polls.urls')),
        path('admin/', admin.site.urls),
]


Step 6: Run the Development Server

python manage.py runserver

Visit http://localhost:8000/admin/ in your browser, and you should see the JSON response: 
Message: 'Hello World'


Step 7: Create a README
Create a README.md file in the project's root directory with instructions on running the app.

# Hello World Django App

This Django app provides a simple Hello World JSON response.

## How to Run the App

1. Install Django:
   
   pip install Django

1. Apply migrations:
python manage.py migrate

2. Run the Django development server:
python manage.py runserver

3.Open your browser and go to http://localhost:8000/admin/.


Step 8: Commit and Push to GitHub

Initialize a git repository, commit your changes, and push to GitHub.

git status
git init
git add .
git commit -m "adding files to the github account"
git remote add origin https://github.com/raajayyappa98/Django.git
git push -u origin master








