# Authentication System - Frontend & Backend

A complete full-stack authentication system built with Node.js, Express, MongoDB for the backend, and React for the frontend. This project provides a secure and scalable authentication solution with features like user registration, login, email verification, and profile management.

## Features

### Backend
- User Registration with email verification
- Secure Login with JWT authentication
- Email verification system
- User Profile Management
- Role-based access control (Customer/Admin)
- Secure password hashing with bcrypt
- MongoDB database integration
- CORS enabled for frontend integration
- Environment variable configuration

### Frontend
- Modern and responsive UI with React
- Form validation and error handling
- Protected routes and authentication state management
- User profile management interface
- Email verification flow
- Loading states and error handling
- Responsive design for all devices

## Tech Stack

### Backend
- **Framework:** Node.js with Express
- **Database:** MongoDB with Mongoose ODM
- **Authentication:** JWT (JSON Web Tokens)
- **Password Hashing:** bcryptjs
- **Email Service:** Nodemailer
- **Environment Variables:** dotenv
- **CORS:** cors middleware

### Frontend
- **Framework:** React.js
- **State Management:** React Context API
- **Routing:** React Router
- **HTTP Client:** Axios
- **UI Components:** Tailwind CSS
- **Form Handling:** React Hook Form


## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm package manager
- Modern web browser

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd <project-directory>
```

2. Install backend dependencies:
```bash
cd backend
npm install
```

3. Install frontend dependencies:
```bash
cd ../frontend
npm install
```

4. Create a `.env` file in the backend directory:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/auth-app
JWT_SECRET=your_jwt_secret_key
EMAIL_USERNAME=your_email@gmail.com
EMAIL_PASSWORD=your_email_password
```

5. Create a `.env` file in the frontend directory:
```env
REACT_APP_API_URL=http://localhost:5000/api
```

6. Start the development servers:

Backend:
```bash
cd backend
npm run dev
```

Frontend:
```bash
cd frontend
npm start
```


## API Endpoints

### Authentication

- **Register User**
  - POST `/api/auth/register`
  - Request Body:
    ```json
    {
      "firstName": "John",
      "lastName": "Doe",
      "email": "john@example.com",
      "password": "password123",
      "role": "admin/customer"
    }
    ```

- **Login User**
  - POST `/api/auth/login`
  - Request Body:
    ```json
    {
      "email": "john@example.com",
      "password": "password123",
      "role": "admin/customer"
    }
    ```

- **Verify Email**
  - POST `/api/auth/verify`
  - Request Body:
    ```json
    {
      "email": "john@example.com",
      "code": "123456"
    }
    ```


