# Front-end and Back-end connection project

A simple full-stack web application demonstrating how to connect a React frontend with an Express.js backend. This project was built as a learning exercise to understand the fundamentals of full-stack development.

## Project Overview

This application consists of:
- A **backend** API server built with Express.js that serves a collection of jokes
- A **frontend** React application that fetches and displays jokes from the backend API

## Technologies Used

### Backend
- **Express.js**: A minimal and flexible Node.js web application framework
- **Node.js**: JavaScript runtime built on Chrome's V8 JavaScript engine
- **CORS**: Middleware for enabling Cross-Origin Resource Sharing

### Frontend
- **React**: A JavaScript library for building user interfaces
- **Vite**: A fast build tool and development server
- **Axios**: Promise-based HTTP client for the browser and Node.js

## Project Structure

```
Full-stack-basics/
├── backend/
│   ├── package.json      # Backend dependencies and scripts
│   └── server.js         # Express server and API endpoints
└── frontend/
    ├── package.json      # Frontend dependencies and scripts
    ├── vite.config.js    # Vite configuration with proxy settings
    └── src/
        ├── App.jsx       # Main React component
        └── main.jsx      # React application entry point
```

## How It Works

1. The backend server runs on port 3000 and serves a static API endpoint `/api/jokes`
2. The frontend runs on a development server (typically port 5173)
3. Vite's proxy configuration forwards API requests from the frontend to the backend
4. The React component fetches jokes using Axios and displays them in the UI

## Getting Started

### Prerequisites
- Node.js and npm installed on your machine

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Full-stack-basics
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

### Running the Application

1. Start the backend server:
   ```bash
   cd backend
   npm start
   ```
   The backend will be running at http://localhost:3000

2. Start the frontend development server (in a new terminal):
   ```bash
   cd frontend
   npm run dev
   ```
   The frontend will be running at http://localhost:5173 (or another available port)

## API Endpoints

### GET /api/jokes
Returns an array of joke objects with the following structure:
```json
[
  {
    "id": 1,
    "title": "A joke",
    "content": "This is a joke"
  },
  // ... more jokes
]
```

## Key Learning Points

This project demonstrates several important full-stack concepts:

1. **Separation of Concerns**: The frontend and backend are separate applications that communicate via HTTP requests
2. **API Design**: Simple RESTful API endpoint for data retrieval
3. **Proxy Configuration**: Using Vite's proxy to forward API requests during development
4. **State Management**: Using React hooks (useState, useEffect) to manage application state
5. **Data Fetching**: Using Axios to make HTTP requests to the backend API

## Future Improvements

Potential enhancements to this project:
- Add more API endpoints for creating, updating, and deleting jokes
- Implement error handling and loading states in the frontend
- Add authentication and authorization
- Connect to a database instead of using hardcoded data
- Add styling with CSS frameworks like Tailwind CSS or styled-components
- Implement form validation
- Add unit and integration tests

## Contributing

This project was created as a learning exercise. Feel free to fork it and experiment with different approaches or technologies.
