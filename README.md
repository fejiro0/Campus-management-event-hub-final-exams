# Campus Event Management System

## Project Overview
The **Campus Event Management System** is a web application designed to facilitate the organization and management of campus events. The platform allows students and staff to view and register for events such as workshops, seminars, and club activities. Admins can create events with detailed information and manage event capacities. The system includes features like user registration, event preferences, RSVP functionality, and a calendar view for better event navigation.

## Tech Stack

- **Frontend**: React.js
- **Backend**: Node.js with Express.js
- **Database**: MongoDB
- **CSS Framework**: Tailwind CSS

## Installation Instructions

### Prerequisites

- **Node.js** and **npm** must be installed on your machine.
- **MongoDB** (local or cloud-based like MongoDB Atlas) for storing user data and events.
- **Git** for version control.


## Deployment Link
The application is deployed on Vercel:
[https://event-management-hub-fe-git-main-fejiros-projects-fd950239.vercel.app/](#)

## Login Details
For testing purposes, use the following credentials:

**User Account:**
- Username: famous@yahoo.com
- Password: newpassword

**Admin Account:**
- Username: famous@admin.com
- Password: newpassword@123

## Feature Checklist
### User Features
- [x] User Registration and Login
- [x] Event Preferences Selection
- [x] View Upcoming Events with Details (name, date, time, location, available seats)
- [x] RSVP for Events (updates available seats and stores in user profile)
- [x] Filter Events by Preferences
- [x] Calendar View for Event Navigation

### Admin Features
- [x] Create Events with Details (name, date, location, description, capacity)
- [x] Manage Event Capacity

## Installation Instructions
To run the project locally, follow these steps:

1. **Clone the repository**
   ```bash
   git clone https://github.com/fejiro0/Campus-management-event-hub-final-exams.git
   cd campus-event-management-system
   ```

2. **Install dependencies**
   Install dependencies for both the frontend and backend:
   ```bash
   # Frontend
   cd frontend
   npm install

   # Backend
   cd ../backend
   npm install
   ```

3. **Set up environment variables**
   Create a `.env` file in the `backend` directory with the following variables:
   ```env
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   ```

4. **Run the application**
   Start both the frontend and backend servers:
   ```bash
   # Frontend (from the `frontend` directory)
   npm run dev

   # Backend (from the `backend` directory)
   npm start
   ```

5. **Access the application**
   Open your browser and navigate to:
   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend API: [http://localhost:5000](http://localhost:5000)

## API Documentation
### API Endpoints
Below are the key API endpoints and their functionality:

1. **User Registration**
   - **POST** `/api/users/register`
   - Request Body:
     ```json
     {
       "name": "John Doe",
       "email": "john@example.com",
       "password": "password123",
       "preferences": ["Workshops", "Seminars"]
     }
     ```

2. **User Login**
   - **POST** `/api/users/login`
   - Request Body:
     ```json
     {
       "email": "john@example.com",
       "password": "password123"
     }
     ```

3. **Get Events**
   - **GET** `/api/events`

4. **RSVP for Event**
   - **POST** `/api/events/rsvp`
   - Request Body:
     ```json
     {
       "eventId": "12345"
     }
     ```

5. **Create Event (Admin Only)**
   - **POST** `/api/events/create`
   - Request Body:
     ```json
     {
       "name": "Coding Workshop",
       "date": "2024-01-15",
       "time": "10:00 AM",
       "location": "Room 101",
       "capacity": 50,
       "description": "Learn advanced coding techniques."
     }
     ```

### Postman API Test Screenshot
Below is a sample screenshot of Postman API tests for the key endpoints:
![Login](/public/Login.png)
![RSVP](/public/RSVP.png)
![User Registration](/public/Register.png)


