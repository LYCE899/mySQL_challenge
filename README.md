# Todo API

## Overview
This is a **Todo API** built with **Django**. The API allows users to manage their tasks, including adding, updating, deleting, and listing tasks. It also utilizes Docker for containerization, GitHub Actions for CI/CD, and Ansible for deployment automation.

## Features
- **User Authentication**: Register and login users.
- **Task Management**: Users can create, read, update, and delete tasks.
- **Data Persistence**: Task data is stored in a **PostgreSQL** database.
- **Dockerized Environment**: The application is containerized using Docker and orchestrated with Docker Compose.
- **CI/CD with GitHub Actions**: Continuous integration and deployment pipeline for automatic testing and building.
- **Automated Deployment with Ansible**: Use Ansible playbooks to deploy the application to remote servers.

## Technologies Used
- **Django**: Backend framework.
- **PostgreSQL**: Database for storing task data.
- **Docker**: Containerization of the application.
- **GitHub Actions**: Continuous Integration and Continuous Deployment.
- **Ansible**: Automated deployment of the application.

## Installation

### Prerequisites
Before setting up the project, make sure you have the following installed:
- **Docker** and **Docker Compose**: [Docker Installation Guide](https://docs.docker.com/get-docker/)
- **Python 3.x**: [Python Installation Guide](https://www.python.org/downloads/)
- **Git**: [Git Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

### Setup

1. **Clone the repository**:
   
   git clone https://github.com/your-username/todo-api.git
   cd todo-api
### Create and activate a Python virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
#### Install project dependencies:
pip install -r requirements.txt

#### Set up the environment variables: Create a .env file with the following:

DB_NAME=todo_db
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=db  
DB_PORT=5432

#### Run migrations to set up the database:

python manage.py migrate

## Docker Setup
### Build the Docker containers:

docker-compose build

#### Run the Docker containers:

docker-compose up -d

This will start the following services:

-Django application on http://localhost:8000
-PostgreSQL database
-Nginx (optional for reverse proxy)
Access the API: You can now test the API endpoints using tools like Postman or curl.

Example requests:

POST /api/register/ to register a new user.
POST /api/login/ to log in and get a JWT token.
GET /api/tasks/ to get all tasks.
POST /api/tasks/ to create a new task.

## CI/CD with GitHub Actions
Whenever a change is pushed to the repository, the GitHub Actions workflow will trigger. It will:

-Run code quality checks.
-Build the Docker image.
-Run unit and integration tests.
-Push the image to Docker Hub.
You can view the status of the workflow under the Actions tab of the GitHub repository.

## Deployment with Ansible
Set up the remote server where you want to deploy the application.

Run the Ansible playbook to deploy the application:

ansible-playbook deploy.yml

This playbook will:

Pull the Docker images.
Set up necessary configurations.
Deploy the application on the remote server.

#### THANK YOU
