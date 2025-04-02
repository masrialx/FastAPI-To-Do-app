# FastAPI To-Do App with Authentication

A simple To-Do application built with FastAPI, featuring user authentication and task management. This app allows users to sign up, log in, and securely manage their tasks, which are associated with their user accounts.

## Features
- **User Authentication**: Users can sign up, log in, and receive a token for authentication.
- **Task Management**: Users can create, read, update, and delete tasks.
- **Task Ownership**: Each task is tied to a specific user, ensuring that users can only manage their own tasks.
- **Task Details**: Each task includes a title and an optional description.

## Tech Stack
- **FastAPI**: A fast, modern web framework for building APIs.
- **Pydantic**: Used for data validation and serialization.
- **SQLite**: A lightweight database for storing user and task data.
- **JWT**: JSON Web Token is used for secure user authentication.
- **SQLAlchemy**: ORM for database interaction and management.
- **Passlib**: For securely hashing passwords.

## Database Models

### User Model
The `User` model represents users who can sign up and log in to the system. Each user has a unique email address and a hashed password stored for authentication.

### Todo Model
The `Todo` model represents the tasks that users can create, update, and delete. Each task has a title and an optional description, and is associated with a specific user.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/masrialx/FastAPI-To-Do-app
   ```

2. Navigate to the project directory:

   ```bash
   cd FastAPI-To-Do-app
   ```

3. Create a virtual environment:

   ```bash
   python3 -m venv venv
   ```

4. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Running the App

To run the app, use the following command:

```bash
uvicorn main:app --reload
```

The app will be available at `http://127.0.0.1:8000`.

## API Endpoints

### Authentication Endpoints
- **POST /signup**: Allows new users to create an account by providing an email and password.
- **POST /login**: Allows users to log in with their email and password to receive a JWT token for authentication.

### Task Management Endpoints
- **GET /tasks**: Lists all tasks belonging to the authenticated user.
- **POST /tasks**: Allows the authenticated user to create a new task with a title and an optional description.
- **PUT /tasks/{task_id}**: Allows the authenticated user to update an existing task (e.g., change the title or description).
- **DELETE /tasks/{task_id}**: Allows the authenticated user to delete a task.

## Example Usage

- **Sign Up**: Users can create an account by providing an email and password.
- **Log In**: After signing up, users can log in to receive a JWT token.
- **Create Task**: With the JWT token, users can create a new task.
- **List Tasks**: Users can view all tasks associated with their account.
- **Update Task**: Users can update task details, such as changing the description.
- **Delete Task**: Users can delete a task.

