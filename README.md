# Django-Note-Taking-API

This Django project provides a simple RESTful API for a note-taking application. Built with Django and Django REST Framework, it allows for creating, fetching, querying, and updating notes. This API is designed to be straightforward, focusing on the backend functionality without user management. Additionally, this project includes Swagger UI integration for easy testing and interaction with the API endpoints.

##Features
- Create Notes: Add new notes with titles and content.
- Retrieve Notes: Fetch a list of all notes or a specific note by ID.
- Update Notes: Modify the title or content of an existing note.
- Query Notes: Filter notes based on specific criteria (e.g., keywords in the title or content).
- Swagger UI: Test API endpoints directly through an auto-generated, interactive API documentation.

##Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

##Prerequisites
- Python 3.8 or higher
- Django 3.2 or higher
- Django REST Framework
- drf-yasg for Swagger UI

##Installation
- Clone the repository

    git clone https://github.com/yourusername/django-notes-api.git
    cd django-notes-api
- Set up a virtual environment

    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
- Install the dependencies
    pip install -r requirements.txt
- Run migrations to create the database schema
    python manage.py makemigrations
    python manage.py migrate
- Start the development server
    python manage.py runserver
  
The API should now be accessible at http://127.0.0.1:8000/api/, and the Swagger UI documentation at http://127.0.0.1:8000/swagger/.

## Usage
Here are some examples of how to interact with the API using curl. You can also use the Swagger UI for an interactive approach.

### Creating a note
  curl -X POST http://127.0.0.1:8000/api/notes/ -d "title=Sample Note&content=This is a sample note."

### Fetching all notes
  curl http://127.0.0.1:8000/api/notes/
### Updating a note
  Assuming the note ID is 1:
    curl -X PUT http://127.0.0.1:8000/api/notes/1/ -d "title=Updated Title&content=Updated content."
