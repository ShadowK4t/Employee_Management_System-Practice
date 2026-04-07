## Employee Management System - Full Stack Application

A full-stack web application for managing employee records, built with React, Node.js, Express, MongoDB, and Docker.


## Tech Stack

### Frontend
- React.js
- React Router DOM
- React Bootstrap
- Axios
- Bootstrap 5

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- Bcrypt (password hashing)
- Multer (file uploads)
- Express Validator

### Deployment
- Docker
- Docker Compose

## Features

### User Management
- User signup with validation
- User login with authentication
- Session management using localStorage
- Logout functionality

### Employee Management
- View all employees in a table format
- Add new employee with profile picture upload
- View employee details
- Update employee information
- Delete employee records
- Search employees by department or position
- Form validation for all inputs

## Project Structure

```
├── docker-compose.yml
├── backend/
│   ├── config/
│   │   └── database.js
│   ├── controllers/
│   │   ├── userController.js
│   │   └── employeeController.js
│   ├── middleware/
│   │   └── upload.js
│   ├── models/
│   │   ├── User.js
│   │   └── Employee.js
│   ├── routes/
│   │   ├── userRoutes.js
│   │   └── employeeRoutes.js
│   ├── uploads/
│   ├── .env
│   ├── .env.example
│   ├── Dockerfile
│   ├── package.json
│   └── server.js
└── frontend/
    ├── public/
    ├── src/
    │   ├── components/
    │   │   ├── Login.js
    │   │   ├── Signup.js
    │   │   └── EmployeeList.js
    │   ├── contexts/
    │   │   └── AuthContext.js
    │   ├── services/
    │   │   └── api.js
    │   └── App.js
    ├── .env
    ├── .env.example
    ├── Dockerfile
    └── package.json
```

## Setup Instructions

### Prerequisites
- Node.js (v16 or higher)
- Docker Desktop
- Git

### Using Docker (Recommended)

1. **Clone the repository**
   ```bash
   git clone https://github.com/ShadowK4t/101512887_comp3123_assignment2_reactjs.git
   cd 
   ```

2. **Start all services with Docker Compose**
   ```bash
   docker-compose up --build
   ```

3. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:3001
   - MongoDB: localhost:27017

4. **Stop the services**
   ```bash
   docker-compose down
   ```

## API Endpoints

### User Endpoints
| Method | Endpoint | Description | Status |
|--------|----------|-------------|--------|
| POST | `/api/v1/user/signup` | Create a new user | 201 |
| POST | `/api/v1/user/login` | Login user | 200 |

### Employee Endpoints
| Method | Endpoint | Description | Status |
|--------|----------|-------------|--------|
| GET | `/api/v1/emp/employees` | Get all employees | 200 |
| POST | `/api/v1/emp/employees` | Create new employee | 201 |
| GET | `/api/v1/emp/employees/:id` | Get employee by ID | 200 |
| PUT | `/api/v1/emp/employees/:id` | Update employee | 200 |
| DELETE | `/api/v1/emp/employees?eid=xxx` | Delete employee | 204 |
| GET | `/api/v1/emp/employees/search` | Search employees | 200 |

## Sample Credentials for Testing

**User Account:**
- Username: `testuser`
- Email: `test@example.com`
- Password: `Test123!`

**Note:** You'll need to create this account using the signup page or via Postman.

## Testing with Postman

1. Import the Postman collection 
2. Test all endpoints
3. Ensure MongoDB is running
4. Check response status codes and data

## Screenshots

Screenshots are included in the `/screenshots` folder:
- Login screen
- Signup screen
- Employee list
- Add employee form
- Edit employee form
- Delete confirmation
- Search results
- MongoDB collections
- Postman tests

## Docker Information

### Services
- **MongoDB**: Database service running on port 27017
- **Backend**: Node.js/Express API running on port 3001
- **Frontend**: React application running on port 3000

### Docker Commands
```bash
# Build and start all services
docker-compose up --build

# Start services in detached mode
docker-compose up -d

# Stop all services
docker-compose down

# View logs
docker-compose logs -f

# Rebuild specific service
docker-compose up --build backend
```

## UI/UX Design

- Professional design using React Bootstrap
- Responsive layout for all screen sizes
- Clean and intuitive user interface
- Proper error handling and validation messages
- Loading states for better UX

## Validation

The application includes comprehensive validation for:
- Email format validation
- Password strength requirements
- Required field validation
- File type validation for image uploads
- Salary and date format validation

## Deployment

This application can be deployed using:
- Docker Compose (current setup)

---
**Last Updated:** April 2026
