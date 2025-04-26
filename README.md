# Assignment
# Task Tracker Application

A full-stack task management application built with React, Express, and MongoDB that allows users to organize and track their projects and tasks.

## Features

- User authentication with JWT
- Up to 4 projects per user
- Task management with status tracking
- Project details and task lists
- User profile management
- Responsive design for all devices

## Tech Stack

### Frontend
- React
- TypeScript
- React Router for navigation
- Tailwind CSS for styling
- Axios for API requests
- Lucide React for icons
- Context API for state management

### Backend
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- BCrypt for password hashing
- CORS enabled

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- MongoDB installed locally or a MongoDB Atlas account

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd task-tracker
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory:
```
MONGO_URI=mongodb://localhost:27017/tasktracker
JWT_SECRET=your-secret-token-here
PORT=5000
```

4. Start the development server:
```bash
# Run frontend and backend concurrently
npm run dev:full

# Or run them separately
npm run server  # Backend
npm run dev     # Frontend
```

5. Open [http://localhost:5173](http://localhost:5173) in your browser

## Project Structure

```
task-tracker/
├── server/                # Backend code
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/          # Mongoose models
│   ├── routes/          # API routes
│   └── server.js        # Server entry point
├── src/                  # Frontend code
│   ├── components/      # React components
│   ├── context/         # React Context providers
│   ├── pages/           # Page components
│   └── types/           # TypeScript types
└── package.json         # Project dependencies
```

## API Endpoints

### Authentication
- `POST /api/users` - Register new user
- `POST /api/users/login` - User login
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile

### Projects
- `GET /api/projects` - Get all user projects
- `POST /api/projects` - Create new project
- `GET /api/projects/:id` - Get project by ID
- `PUT /api/projects/:id` - Update project
- `DELETE /api/projects/:id` - Delete project

### Tasks
- `GET /api/tasks/project/:projectId` - Get tasks by project
- `POST /api/tasks` - Create new task
- `GET /api/tasks/:id` - Get task by ID
- `PUT /api/tasks/:id` - Update task
- `DELETE /api/tasks/:id` - Delete task

## Features

### User Management
- User registration with email validation
- Secure password hashing
- JWT-based authentication
- Profile management

### Project Management
- Create up to 4 projects
- Project details with title and description
- Project listing and individual view
- Project editing and deletion

### Task Management
- Create tasks within projects
- Task status tracking (To Do, In Progress, Completed)
- Task creation and completion dates
- Task filtering by status
- Task editing and deletion

### Dashboard
- Overview of all projects
- Task statistics
- Recent project activity
- Quick access to projects

## Security Features

- Password hashing with BCrypt
- JWT token authentication
- Protected API routes
- Input validation
- Error handling
- CORS protection

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
