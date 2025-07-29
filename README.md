# LearnWise

LEARNWISE is a web application that allows users to create, manage, and track their personalized learning roadmaps. It provides a visual interface for learning paths, progress tracking, and resource management.

---

## Features

- **Custom Roadmaps**: Create personalized learning paths tailored to your goals and current knowledge level.
- **Progress Tracking**: Monitor your learning journey with visual progress indicators and milestone tracking.
- **Flexible Timeline**: Learn at your own pace with customizable timeframes for each skill path.
- **Node Management**: Mark nodes as completed, view descriptions, and access resources like YouTube videos and websites.
- **Completed Roadmaps**: View and celebrate your completed roadmaps.
- **Authentication**: Secure login and signup functionality.

---

## Tech Stack

### Frontend
- **React**: For building the user interface.
- **React Router**: For routing and navigation.
- **ReactFlow**: For visualizing roadmaps as flowcharts.
- **Zustand**: For state management.
- **Tailwind CSS**: For styling.
- **Axios**: For API requests.

### Backend
- **FastAPI**: For building the REST API.
- **SQLite**: For database storage.
- **SQLAlchemy**: For ORM and database interactions.
- **JWT**: For authentication and authorization.

---

## Installation

### Prerequisites
- Node.js and npm installed.
- Python 3.9+ installed.
  
### Get API Keys
You will need API keys for external services. Create accounts and generate keys from the following services:

- Google API Key
- Google Custom Search CX ID
- YouTube API Key
- GROQ API Key

Once obtained, create a .env file inside the backend/ directory with the following content:
```bash
GOOGLE_API_KEY=your_google_api_key
CX_ID=your_google_cx_id
YOUTUBE_API_KEY=your_youtube_api_key
GROQ_API_KEY=your_groq_api_key
```
## Run Backend
```bash
cd backend
python -m venv venv
```
Activate the virtual environment
- On Windows:
```bash
venv\Scripts\activate
```
- On macOS/Linux:
```bash
source venv/bin/activate
```

Install Python dependencies
```bash
pip install -r requirements.txt
```
Start the backend server
```bash
 uvicorn app.main:app --reload
```
## Run Frontend 
Open new terminal from base directory:
```bash
cd frontend
```
Install npm dependencies (run once):
```bash
npm install
```
Start the development server:
```bash
npm run dev
```
## Usage
- Sign up or log in to your account.
- Create a new roadmap by providing the skill, timeframe, and target level.
- Visualize your roadmap, mark nodes as completed, and track your progress.
- View completed roadmaps in the "Completed" section.
---
## API Endpoints
### Authentication
- POST /api/auth/signup: Sign up a new user.
- POST /api/auth/login: Log in an existing user.
- GET /api/auth/me: Get the current user's profile.
### Roadmaps
- POST /api/roadmap/create: Create a new roadmap.
- GET /api/roadmap/ongoing: Get all ongoing roadmaps.
- GET /api/roadmap/completed: Get all completed roadmaps.
- GET /api/roadmap/{roadmap_id}: Get details of a specific roadmap.
- PUT /api/roadmap/{roadmap_id}/progress: Update progress for a roadmap.

## Acknowledgments
- ReactFlow for the flowchart visualization.
- FastAPI for the backend framework.
- Tailwind CSS for styling.
- Lucide React for icons.

