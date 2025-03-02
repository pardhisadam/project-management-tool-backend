# Project Management Backend

A pure JavaScript project management tool backend with RESTful API endpoints for managing projects, tasks, and users.

## Features

- User authentication (register, login)
- Project management (create, read, update, delete)
- Task management (create, read, update, delete)
- User management
- Role-based access control

## API Endpoints

### Authentication

- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login and get token

### Projects

- GET /api/projects - Get all projects for the authenticated user
- GET /api/projects/:id - Get a specific project
- POST /api/projects - Create a new project
- PUT /api/projects/:id - Update a project
- DELETE /api/projects/:id - Delete a project
- POST /api/projects/:id/members - Add a member to a project
- DELETE /api/projects/:id/members/:userId - Remove a member from a project
- GET /api/projects/:id/tasks - Get all tasks for a project

### Tasks

- GET /api/tasks - Get all tasks assigned to the authenticated user
- GET /api/tasks/:id - Get a specific task
- POST /api/tasks - Create a new task
- PUT /api/tasks/:id - Update a task
- DELETE /api/tasks/:id - Delete a task

### Users

- GET /api/users - Get all users
- GET /api/users/me - Get the authenticated user
- GET /api/users/:id - Get a specific user
- PUT /api/users/me - Update the authenticated user

## Getting Started

1. Clone the repository
2. Install dependencies: npm install
3. Create a .env file with the following variables:
   
   PORT=3000
   JWT_SECRET=your_jwt_secret_key_change_this_in_production
   
4. Start the server: npm start
5. For development with auto-restart: npm run dev

## Data Storage

This backend uses file-based storage with JSON files in the data directory:
- users.json - User data
- projects.json - Project data
- tasks.json - Task data

## Authentication

The API uses JWT (JSON Web Token) for authentication. To access protected endpoints, include the token in the request header:


x-auth-token: your_jwt_token

