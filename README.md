# django_models

This is an exercise to setup a django project, define and create models.

## Prerequisites

Python 3, pip, and venv(virtual environment) installed on your machine.

## Steps

1. Create a new GitHub repository with a README.md, and Python .gitignore file.

2. Clone it to your machine/computer, which will create a new folder on your computer with your repository’s content.

3. Create a new virtual environment in that folder named .env and install Django in it.
    ```
    pip install django
    ```

4. Create a new Django project.
    ```
    django-admin startproject <projectname>
    ```

5. Move into the django project directory and ensure you have the file manage.py inside the directory, then test/run your server.
    ```
    python manage.py runserver
    ```

    Open the url displayed on your terminal in your browser, if the page opens successfully you can stop the server with CTRL/CMD + C.

6. Create a new application using the Django startapp command. The app should be called blog.
    ```
    django-admin startapp <appname>
    ```

7. Add the blog app to the main_projects INSTALLED_APPS.

8. Create a new model in the blog app called Post. It should have the following fields:

    Post

    --------

    Title : A string of maxlength 200, use Django’s models.CharField  
    Text : Any amount of text, use Django’s TextField  
    Author : A Foreign Key to the current user model. Make use of Django’s get_user_model function.  
    Created_date : A date-time column, use Django’s models.DateTimeField.  
    Published_date : A date-time column, use Django’s models.DateTimeField.

9. Create migrations for your new model using the makemigrations Django command.
    ```
    python manage.py makemigrations
    ```

10. Run all migrations using the migrate Django command.
    ```
    python manage.py migrate
    ```

11. To test your model.
    - create a superuser 'python manage.py createsuperuser'.
    - Add/Register the model in the app file admin.py, import the model
    ```
    from .models import Post
    ```

    Register the model

    ```
    admin.site.register(Post)
    ```

    Save the file

    - To view, create and delete, run the server, add '/admin' to the base url and login with the the superuser credentials, once you are logged, use the admin panel to create and delete users.

12. Stage and Commit your Django project and push your changes to your GitHub repository.
