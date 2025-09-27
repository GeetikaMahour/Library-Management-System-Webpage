📚 React + Firebase Library Management System
This project is a single-file, responsive web application built with React and Tailwind CSS for managing a small personal or departmental library inventory and transaction log. It uses Google Firestore for real-time data persistence and Firebase Authentication for secure user isolation.

This application was developed as a submission for a collaborative coding environment, demonstrating best practices for single-file component architecture and integrating modern cloud services.

✨ Features
Real-Time Data Sync: Uses Firestore's onSnapshot to ensure the dashboard and inventory views update instantly across all connected devices.

Book Management:

Add new books with title, author, ISBN, and total copies.

Edit existing book details.

Delete books (with validation to prevent deletion if copies are currently issued).

Inventory Tracking: Displays available copies vs. total copies for each book.

User Isolation: Data is securely stored under a unique user ID (userId) derived from Firebase Authentication, ensuring private data access.

🛠️ Technology Stack
Frontend: React (Functional Components and Hooks)

Styling: Tailwind CSS (for responsive, utility-first design)

Database: Google Firestore (Real-time NoSQL)

Authentication: Firebase Authentication (Handles user sessions and isolation)

🚀 Setup & Installation (Standard React Project)
This project requires a standard Node.js environment.

1. Clone the repository
git clone <your-repo-link>
cd library-management-system

2. Install dependencies
npm install

(This installs react, react-dom, and firebase as defined in package.json)

3. Firebase Configuration
Since this application relies on environment variables (__app_id, __firebase_config, __initial_auth_token), you will need to replace the placeholders in the src/App.jsx file with your own local Firebase project configuration for it to run outside of the specific development environment it was built for.

In src/App.jsx, replace the initial configuration block with your actual values:

// Example of what to replace:
// const firebaseConfig = typeof __firebase_config !== 'undefined' ? JSON.parse(__firebase_config) : {};
// const initialAuthToken = typeof __initial_auth_token !== 'undefined' ? __initial_auth_token : null;
// const appId = typeof __app_id !== 'undefined' ? __app_id : 'default-app-id';

// Replace with your actual Firebase config:
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    // ... other config values
};
// You will also need to manually handle authentication for a standard setup.

4. Run the application
npm start

The application will open in your browser, typically at http://localhost:3000.# Library-Management-System-Webpage
