Step 1: Create a Django Project


django-admin star HelloWorld
cd HelloWorld

Step 2: Create a Django App

python manage.py runserver

Step 3: Define a View
Open polls/views.py and define a simple view that returns a JSON response

from django.http import httpResponse

def helloworld(request):
    return HttpResponse('Hello World')

Step 4: Configure URL Routing

from django.urls import path
from .views import helloworld

urlpatterns = [
    path('', helloworld, name='helloworld'),
]

Step 5: Include the polls  URLs in the Project




