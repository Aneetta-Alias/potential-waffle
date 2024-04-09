
# Project Name Todo_list
Purpose
Display Todo List: The primary purpose of this template is to display a list of tasks (todos) that users can add, view, and delete.
User Interaction: It provides a form for adding new tasks and buttons for deleting existing tasks, enabling users to manage their todo list.


Main Features
Form for Adding Tasks:
Title Input: Users can enter a title for their task.
Description Textarea: Users can provide a detailed description of the task.
Category Selection: Users can select a category for the task from a dropdown list, which is populated dynamically from the categories context variable.
Submit Button: Users can submit the form to add a new task to the list.
Display of Existing Tasks:
Task List: The template iterates over the todos context variable to display each task.
Task Details: For each task, it displays the title, description, and category.
Delete Button: Each task has a delete button that, when clicked, submits a form to delete the task. A confirmation dialog is shown to prevent accidental deletions.
Security:
CSRF Token: The template includes a CSRF token ({% csrf_token %}) in both the add task form and the delete task form. This is a security measure to prevent cross-site request forgery attacks.
Styling and Layout:
Inline Styling: The delete task form is styled with display: inline; to allow the delete button to appear next to the task details.
Block Structure: The template uses Django's template language to define blocks ({% block content %}) and extends a base template, allowing for a consistent layout across different pages.
Additional Considerations
Dynamic Content: The template dynamically generates the category dropdown options and the list of existing tasks based on the context variables passed from the view (categories and todos).
User Experience: The use of a confirmation dialog for task deletion improves the user experience by preventing accidental deletions.
Accessibility: The template uses semantic HTML elements (e.g., <label>, <textarea>) and includes for attributes for form controls, which is good for accessibility.



## Team members
1. [Aksa-Boben](https://github.com/TH-Activities/saturday-hack-night-template)
3. [Ann-Maria-Benny](https://github.com/TH-Activities/saturday-hack-night-template)

## How it Works ?

Base Template: The base.html template acts as a layout template, defining the overall structure of the page, including the header, footer, and navigation. It also defines blocks where specific content can be inserted.
Child Template: The provided template extends base.html and fills in the content block with the specific content for the Todo List page. This includes a form for adding tasks, a list of existing tasks, and a form for deleting tasks.
Context Variables: The view passes context variables (categories, todos) to the template. These variables are used to dynamically generate the HTML for the category dropdown and the list of tasks.
Form Submission: When the user submits the form to add a new task or delete an existing task, the form data is sent to the server. The view handles these requests, updating the database as necessary and redirecting the user back to the Todo List page.

# Libraries used
Library Name - Django 5.0.2
## How to configure

1. Prepare Your Environment
Install Python: Ensure Python is installed on your system. Django requires Python 3.6 or higher.
Set Up a Virtual Environment: It's a good practice to create a virtual environment for your Django project to manage dependencies.
Install Django
Install Django: With your virtual environment activated, install Django using pip:

 Create a Django Project
Create a Django Project: Use the django-admin command to create a new Django project. Replace myproject with your desired project name
Create a Django App
Create a Django App: Inside your project directory, create a new Django app. Replace myapp with your desired app name:

Configure Your Project
Add Your App to INSTALLED_APPS: Open myproject/settings.py and add your app to the INSTALLED_APPS list:

Set Up Your Models
Define Your Models: In myapp/models.py, define your models. For the provided code, you might have models for Todo and Category.
 Create Migrations
Create Migrations: After defining your models, create migrations for your database schema

Apply Migrations
Apply Migrations: Apply the migrations to your database

Create Your Views
Create Views: In myapp/views.py, create the views to handle the logic for displaying and adding tasks.
Configure URLs
Configure URLs: In myapp/urls.py, define the URL patterns for your views. Then, include these URLs in your project's urls.py.
Create Your Templates
Create Templates: Based on the provided code, create your templates in myapp/templates/myapp/. Make sure to create a templates directory inside your app if it doesn't exist.
Run Your Server
Run Your Server: Finally, start your Django development server:
python manage.py runserver
This setup process involves creating a Django project, setting up a virtual environment, installing Django, creating an app, defining models, and setting up views and templates. It's a foundational setup for developing a Django web application, as described in the sources 123.







