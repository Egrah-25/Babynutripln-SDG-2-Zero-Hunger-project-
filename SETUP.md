# BabyNutriPlan - Firebase Setup Instructions

Thank you for checking out our BabyNutriPlan project! This document provides instructions for setting up the Firebase backend for full functionality.

## Demo Mode

The application currently runs in demo mode with simulated authentication and data storage. No setup is required to use the demo version.

## Firebase Setup Instructions

To enable full functionality with Firebase authentication and database:

### 1. Create a Firebase Project

1. Go to the [Firebase Console](https://console.firebase.google.com/)
2. Click "Create a project" or "Add project"
3. Enter a project name (e.g., "BabyNutriPlan")
4. Follow the setup instructions

### 2. Enable Authentication

1. In your Firebase project, go to "Authentication" in the left sidebar
2. Click "Get started"
3. Go to the "Sign-in method" tab
4. Enable "Email/Password" provider

### 3. Set Up Firestore Database

1. In your Firebase project, go to "Firestore Database" in the left sidebar
2. Click "Create database"
3. Start in test mode (for demo purposes)
4. Select a location for your database

### 4. Get Your Configuration Details

1. Go to Project Settings (click the gear icon next to "Project Overview")
2. Scroll down to "Your apps"
3. Click the web icon (`</>`) to add a web app
4. Register your app with a nickname
5. Copy the configuration object that appears

### 5. Configure the Application

Replace the mock Firebase implementation in the script with real Firebase initialization:

```javascript
// Replace the MockFirebase code with this real implementation:

// Firebase configuration (replace with your actual config)
const firebaseConfig = {
  apiKey: "your-api-key",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project-id",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "123456789",
  appId: "your-app-id"
};

// Initialize Firebase
firebase.initializeApp(firebaseConfig);
const auth = firebase.auth();
const db = firebase.firestore();
