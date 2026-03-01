# CipherSQLStudio
🚀CipherSQLStudio, SQL Learning Platform

A Full-Stack SQL Practice & AI-Assisted Learning Platform built with React, Node.js, MongoDB, and OpenAI.

🌐 Live Overview

The SQL Learning Platform is an interactive web application that allows users to:

Write and execute SQL queries

Practice structured assignments

Receive AI-powered hints (without revealing full solutions)

View results in a structured format

Learn SQL in a real IDE-like environment

This project simulates a modern SQL learning tool similar to LeetCode / HackerRank.

🧩 Architecture Overview
User → React Frontend → Express Backend → MongoDB
                               ↓
                           OpenAI API

React handles UI and SQL editor

Express manages API routing and validation

MongoDB stores assignments and schema

OpenAI generates contextual SQL hints

🛠 Tech Stack
Frontend

React.js

Axios

Monaco Editor (VS Code-like SQL Editor)

CSS

Backend

Node.js

Express.js

MongoDB

Mongoose

OpenAI API

📁 Folder Structure
sql-learning-platform/

✨ Key Features
🧠 AI-Powered Hint System

Integrates OpenAI API

Provides contextual guidance

Avoids revealing full solutions

💻 Professional SQL Editor

Monaco Editor (VS Code engine)

Syntax highlighting

Auto-completion

Formatting support

Responsive design

🔄 Real-Time Query Execution

Structured API response

Proper HTTP status codes

Error handling middleware

🛡 Robust Error Handling

400 Validation errors

500 Internal server handling

Axios error management

Graceful UI feedback

🗃 Assignment-Based Practice

MongoDB-based schema storage

Seeded sample data

Dynamic assignment loading

⚙️ Installation Guide
1️⃣ Clone Repository
git clone https://github.com/riteshmaurya089/CipherSchools
cd sql-learning-platform
2️⃣ Backend Setup
cd backend
npm install

Create .env file:

PORT=5000
MONGO_URI=your_mongodb_connection_string
OPENAI_API_KEY=your_openai_api_key

Run server:

npm run dev

Server runs at:

http://localhost:5000
3️⃣ Frontend Setup
cd frontend
npm install
npm start

App runs at:5173

http://localhost:
📡 API Endpoints
🔹 Execute SQL Query
POST (http://localhost:5000/api/queries/execute)

Request Body:

{
  "assignmentId": "123",
  "query": "SELECT * FROM employees"
}
🔹 Generate AI Hint
POST /api/hint

Request Body:

{
  "assignmentId": "123",
  "query": "SELECT name FROM employees"
}
📊 Data Flow Diagram

The system follows this data flow:

User writes SQL query

React sends API request

Express validates input

MongoDB provides schema/sample data

OpenAI generates hint (if requested)

Backend sends response to frontend

Results displayed in table format

(Hand-drawn DFD included in submission)

⚠️ Technical Challenges & Solutions
🔹 API Route Mismatch (400 / 404 Errors)

Solved by standardizing route naming and validating request body.

🔹 Axios Network Errors

Implemented loading states and disabled rapid multi-click.

🔹 Environment Variable Misconfiguration

Resolved by centralizing env config and verifying API keys.

🔹 LLM API Integration

Handled authentication errors and added fallback responses.

🔹 UI Responsiveness

Improved Monaco editor height and layout using viewport-based sizing.

🧠 Learning Outcomes

REST API Architecture

Frontend–Backend Integration

MongoDB Data Modeling

Error Handling Patterns

Environment Configuration

Git Version Control Best Practices

LLM API Integration

Debugging Network Issues

📈 Future Improvements

User authentication system

SQL execution sandbox engine

Query performance analyzer

Leaderboard system

Deployment on AWS / Render / Vercel

👨‍💻 Author

Your Name
GitHub: 
📄 License

This project is built for educational purposes.
