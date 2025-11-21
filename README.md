VoiceBridge

VoiceBridge is a full-stack web application that converts text to speech (TTS), provides weather, date & time, dictionary lookup, jokes, and more. It is built using React, TailwindCSS, Node.js, Express, MongoDB, Socket.io, and Python Flask.

Features

Text-to-Speech (TTS): Converts typed text into audio

Speech-to-Text (STT): Converts voice input into text

Weather: Displays current weather for any city

Date & Time: Shows real-time date and time

Dictionary Lookup: Fetches word meanings via API

Jokes / Fun Facts: Provides random jokes

Real-time Communication: Uses Socket.io for live updates

Responsive UI built with TailwindCSS

Project Structure
VoiceBridge/
│
├─ client/           # React + Tailwind frontend
│   ├─ src/
│   ├─ public/
│   ├─ package.json
│   └─ ...
│
├─ server/           # Node + Express + MongoDB backend
│   ├─ models/
│   ├─ server.js
│   ├─ package.json
│   └─ .env
│
├─ flask/            # Python Flask microservice (TTS, STT, Dictionary, Jokes)
│   ├─ app.py
│   ├─ venv/
│   └─ requirements.txt
│
└─ README.md

Technologies Used

Frontend: React.js, TailwindCSS, JSX, HTML, CSS

Backend: Node.js, Express.js, MongoDB, Mongoose, Socket.io, CORS

Microservice: Python Flask, gTTS, SpeechRecognition, pyttsx3

Deployment: Vercel (frontend), MongoDB Atlas (database)

Installation & Setup
1. Clone the repository
git clone <your-repo-url>
cd VoiceBridge

2. Frontend Setup (React)
cd client
npm install
npm run dev      # Start development server (http://localhost:5173)


To build for production:

npm run build

3. Backend Setup (Node + Express)
cd server
npm install


Create .env:

MONGO_URI=your_mongodb_connection_string
PORT=5000


Start the server:

npx nodemon server.js

4. Flask Microservice Setup (TTS, STT, Dictionary, Jokes)
cd flask
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python app.py


Flask server runs at http://localhost:8000/

Usage

Open the frontend: http://localhost:5173/

Use the UI to:

Convert text to speech

Fetch jokes

Check dictionary

View weather and time

All API requests are routed to Flask (microservice) or Node backend.

Deployment

Frontend: Vercel

Build: npm run build

Deploy: vercel

Backend (Node): Can be deployed to Heroku, Render, or AWS

Flask Microservice: Can be deployed to Render, Railway, or any Python host

Environment Variables

.env in server/:

MONGO_URI=your_mongodb_connection_string
PORT=5000


.env (optional) for frontend API endpoints:

REACT_APP_NODE_URL=http://localhost:5000
REACT_APP_FLASK_URL=http://localhost:8000

Contributing

Fork the repository

Create a branch: git checkout -b feature/feature-name

Commit your changes: git commit -m "Add new feature"

Push to branch: git push origin feature/feature-name

Create a pull request

License

This project is open-source and available under the MIT License.
