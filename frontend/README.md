# Team Management Frontend

A React-based frontend application for managing students and teams.

## Features

- **Student Management**: Add, edit, delete, and view students
- **Team Management**: Create teams and add students as members
- Clean and responsive UI
- Real-time updates

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Backend API running on `http://localhost:5000`

## Installation

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application

1. Make sure the backend API is running on port 5000

2. Start the React development server:
   ```bash
   npm start
   ```

3. Open your browser and navigate to `http://localhost:3000`

## Available Scripts

- `npm start` - Runs the app in development mode
- `npm build` - Builds the app for production
- `npm test` - Runs the test suite
- `npm eject` - Ejects from Create React App (one-way operation)

## Project Structure

```
frontend/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── Students.js      # Student management component
│   │   └── Teams.js          # Team management component
│   ├── services/
│   │   └── api.js            # API service layer
│   ├── App.js                # Main app component
│   ├── App.css               # App styles
│   ├── index.js              # Entry point
│   └── index.css             # Global styles
└── package.json
```

## API Integration

The frontend communicates with the Flask backend API using the following endpoints:

### Students
- `GET /students` - Get all students
- `GET /students/:id` - Get student by ID
- `POST /students` - Create new student
- `PUT /students/:id` - Update student
- `DELETE /students/:id` - Delete student

### Teams
- `GET /teams` - Get all teams
- `POST /teams` - Create new team
- `POST /teams/:id/add_member` - Add member to team

## Usage

### Managing Students

1. Click on the "Students" tab
2. Fill in the form to add a new student (name is required)
3. Click "Add Student" to create
4. Use "Edit" button to modify existing students
5. Use "Delete" button to remove students

### Managing Teams

1. Click on the "Teams" tab
2. Enter a team name and click "Create Team"
3. Select a team and a student from the dropdowns
4. Click "Add Member" to add the student to the team
5. View team members in the team cards on the right

## Development Notes

- The app uses React Hooks for state management
- API proxy is configured in `package.json` to forward requests to `http://localhost:5000`
- Error handling is implemented for all API calls
- Form validation ensures required fields are filled
