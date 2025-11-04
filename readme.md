# 📝 Full-Stack Todo Application

A modern, full-stack todo application built with React, Spring Boot, and MongoDB. This project demonstrates a complete CRUD application with a RESTful API backend and a responsive React frontend.

![Todo App Screenshot](https://img.shields.io/badge/Status-Live-success)
![React](https://img.shields.io/badge/React-18.2-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2-green)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-brightgreen)

## 🌐 Live Demo

- **Frontend**: [https://todo-frontend-roan-kappa.vercel.app](https://todo-frontend-roan-kappa.vercel.app)
- **Backend API**: [https://todo-backend-30nv.onrender.com/api/todos](https://todo-backend-30nv.onrender.com/api/todos)

## ✨ Features

- ✅ Create, Read, Update, and Delete todos
- ✅ Mark todos as complete/incomplete
- ✅ Add optional descriptions to todos
- ✅ Filter todos (All, Active, Completed)
- ✅ Responsive design for mobile and desktop
- ✅ Real-time data persistence with MongoDB
- ✅ RESTful API architecture
- ✅ Modern UI with smooth animations

## 🛠️ Technology Stack

### Frontend
- **React 18.2** - UI library
- **Vite** - Build tool and development server
- **Axios** - HTTP client for API requests
- **CSS3** - Styling with modern features

### Backend
- **Spring Boot 3.2** - Java framework
- **Spring Data MongoDB** - Database integration
- **Maven** - Dependency management
- **Lombok** - Boilerplate code reduction

### Database
- **MongoDB Atlas** - Cloud-hosted NoSQL database

### Deployment
- **Vercel** - Frontend hosting
- **Render** - Backend hosting

## 📁 Project Structure

```
todo_using_react_springboot_mongodb/
│
├── todo-frontend/                 # React frontend application
│   ├── src/
│   │   ├── services/
│   │   │   └── api.js            # API service layer
│   │   ├── App.jsx               # Main application component
│   │   ├── App.css               # Application styles
│   │   └── main.jsx              # Entry point
│   ├── package.json
│   └── vite.config.js
│
└── todo-backend/                  # Spring Boot backend application
    ├── src/
    │   └── main/
    │       └── java/com/todo/todo_backend/
    │           ├── config/
    │           │   └── CorsConfig.java       # CORS configuration
    │           ├── controller/
    │           │   └── TodoController.java   # REST API endpoints
    │           ├── model/
    │           │   └── Todo.java             # Todo entity
    │           ├── repository/
    │           │   └── TodoRepository.java   # Database operations
    │           └── service/
    │               └── TodoService.java      # Business logic
    ├── pom.xml
    └── Dockerfile
```

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **Java JDK** (17 or higher)
- **Maven** (3.6 or higher)
- **MongoDB Atlas Account** (free tier)
- **Git**

### 1. Clone the Repositories

```bash
# Clone frontend
git clone https://github.com/YOUR_USERNAME/todo-frontend.git
cd todo-frontend

# Clone backend
git clone https://github.com/YOUR_USERNAME/todo-backend.git
cd todo-backend
```

### 2. Setup MongoDB Atlas

1. Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a free cluster
3. Create database user with username and password
4. Whitelist your IP address (0.0.0.0/0 for development)
5. Get your connection string

### 3. Backend Setup

```bash
cd todo-backend

# Update application.properties with your MongoDB URI
# src/main/resources/application.properties

# Install dependencies and run
mvn clean install
mvn spring-boot:run
```

Backend will start at `http://localhost:8080`

### 4. Frontend Setup

```bash
cd todo-frontend

# Install dependencies
npm install

# Update API URL in src/services/api.js if needed

# Run development server
npm run dev
```

Frontend will start at `http://localhost:5173`

## 📡 API Endpoints

Base URL: `http://localhost:8080/api/todos`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/todos` | Get all todos |
| GET | `/api/todos/{id}` | Get todo by ID |
| POST | `/api/todos` | Create new todo |
| PUT | `/api/todos/{id}` | Update todo |
| DELETE | `/api/todos/{id}` | Delete todo |
| GET | `/api/todos/completed` | Get completed todos |
| GET | `/api/todos/incomplete` | Get incomplete todos |

### Example Request/Response

**Create Todo (POST /api/todos)**

Request Body:
```json
{
  "title": "Learn Spring Boot",
  "description": "Complete the tutorial"
}
```

Response:
```json
{
  "id": "507f1f77bcf86cd799439011",
  "title": "Learn Spring Boot",
  "description": "Complete the tutorial",
  "completed": false,
  "createdAt": "2024-11-04T10:30:00",
  "updatedAt": "2024-11-04T10:30:00"
}
```



## 🔧 Configuration

### Backend Configuration

**application.properties:**
```properties
spring.application.name=todo-backend
server.port=8080

# MongoDB
spring.data.mongodb.uri=mongodb+srv://username:password@cluster.mongodb.net/tododb

# CORS
spring.web.cors.allowed-origins=http://localhost:5173,https://your-frontend-url.vercel.app
```

### Frontend Configuration

**api.js:**
```javascript
const API_BASE_URL = 'http://localhost:8080/api/todos';
// Change to production URL when deploying
```

## 🚢 Deployment

### Deploy Backend to Render

1. Create `Dockerfile` in backend root
2. Push to GitHub
3. Create new Web Service on Render
4. Connect GitHub repository
5. Add environment variables
6. Deploy

### Deploy Frontend to Vercel

1. Push frontend to GitHub
2. Import project to Vercel
3. Configure build settings (Vite)
4. Deploy automatically

**Note:** Update CORS settings and API URLs after deployment!

## 🧪 Testing

### Backend Testing
```bash
# Run backend
mvn spring-boot:run

# Test API endpoints
curl http://localhost:8080/api/todos
```

### Frontend Testing
```bash
# Run frontend
npm run dev

# Build for production
npm run build
```

## 📚 What I Learned

- Building RESTful APIs with Spring Boot
- React hooks (useState, useEffect) for state management
- MongoDB database integration and CRUD operations
- Axios for API communication
- Responsive CSS design
- CORS configuration for cross-origin requests
- Deploying full-stack applications to cloud platforms
- Git version control and collaboration

## 🙏 Acknowledgments

- Spring Boot Documentation
- React Documentation
- MongoDB Atlas
- Vercel & Render for free hosting
- Stack Overflow community


⭐ **If you found this project helpful, please give it a star!** ⭐

Made with ❤️ and ☕
