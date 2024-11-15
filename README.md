# Django To-Do API Project
This project is a simple To-Do application built with Django, designed to practice modern DevOps techniques like containerization, automated testing, and deployment.

## Project Overview
This Django-based project is a basic To-Do list application that includes:

User Authentication: Secure login and registration for users.
Task Management: Add, update, delete, and list tasks through a REST API.
Database: Uses MySQL to store user and task data.
Email Notifications: Sends email notifications when tasks are created or updated.
## Technology Stack
Backend: Django (Python) for the web server.
Database: MySQL for storing data.
Containerization: Docker for packaging the application.
CI/CD: GitHub Actions for automated testing and deployments.
Deployment: Ansible for deploying the application to a server.
## Setup Instructions
Clone the Project:

git clone https://github.com/yourusername/todo_api_project.git
cd todo_api_project
### Run with Docker:

Build and start all services:

docker-compose up --build
Visit the app at http://localhost:8001.

### Run Locally Without Docker:

Create a virtual environment and install dependencies:

python -m venv venv
source venv/bin/activate  
pip install -r requirements.txt

### Set up MySQL database and run the server:

python manage.py migrate
python manage.py runserver
Access the app at http://127.0.0.1:8000.

## Key Features
Docker Setup: The project is containerized using Docker with separate containers for Django, MySQL, and Nginx.
CI/CD: GitHub Actions automate code testing, Docker builds, and deployment.
Ansible Deployment: Ansible playbook to automate deploying the app on a remote server.

## How to Use the API
Here are some basic endpoints:

Register: POST /api/register/
Login: POST /api/login/
Get To-Do List: GET /api/tasks/
Create To-Do Item: POST /api/tasks/
Update/Delete To-Do Item: PUT/DELETE /api/tasks/{id}/

## conclusion
This project successfully combines Django web development with essential DevOps practices, including Docker containerization, CI/CD with GitHub Actions, and automated deployment using Ansible. It provides a practical introduction to building, managing, and deploying web applications in a streamlined and efficient way, laying a strong foundation for modern web development and deployment workflows.