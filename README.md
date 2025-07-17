# MONGODB-FIREBASE

# MongoDB + Firebase Full Guide for Beginners to Advanced (with MERN Stack)

# Introduction

What is MongoDB?

- MongoDB is a NoSQL database that stores data in a flexible, JSON-like format called BSON. Unlike traditional relational databases, MongoDB does not require predefined schemas and is highly scalable, making it perfect for modern web applications.

What is Firebase?

- Firebase is a Backend-as-a-Service (BaaS) platform developed by Google that offers tools such as real-time database, Firestore, authentication, hosting, cloud functions, and more.

Why Use MongoDB?

  - Schema-less structure (flexible)

  - High performance and scalability

  - Easy to integrate with JavaScript and Node.js

  - Great community and documentation

  - Powerful query language

Why Use Firebase?

  - Real-time database and Firestore

  - Built-in authentication (email/password, Google, GitHub, etc.)

  - Free hosting with SSL

  - Cloud functions and serverless

  - Google Analytics and Performance Monitoring


Comparison with SQL Databases

   | Feature           | SQL (MySQL, PostgreSQL)     | MongoDB (NoSQL)              | Firebase (NoSQL, Realtime)     |
|-------------------|-----------------------------|------------------------------|--------------------------------|
| **Schema** | Fixed (tables)              | Flexible (documents)         | Flexible                       |
| **Relationships** | JOINs                       | Embedded / Referenced        | Limited (No JOIN)              |
| **Query Language**| SQL                         | JSON-like syntax             | Limited Query Language         |
| **Scalability** | Vertical                    | Horizontal                   | Auto-scaled                    |
| **Ideal Use Case**| Structured data             | Dynamic / unstructured       | Realtime Apps, MVPs            |


# Installing MongoDB

For Windows
  1. Go to https://www.mongodb.com/try/download/community
  2. Select Windows > MSI Installer
  3. Install and check MongoDB Compass option
  4. Add MongoDB to environment variables
  5. Open CMD and run:

         mongo --version

For macOS

    brew tap mongodb/brew
    brew install mongodb-community@7.0
    brew services start mongodb/brew/mongodb-community

For Linux (Ubuntu)
      
    sudo apt update
    sudo apt install -y mongodb
    sudo systemctl start mongodb
    sudo systemctl enable mongodb

Using MongoDB Atlas (Cloud)
  1. Visit: https://cloud.mongodb.com
  2. Create a free cluster
  3. Create database user with password
  4. Whitelist your IP address
  5. Connect using connection string in Node.js or Mongo shell

# Installing Firebase
Prerequisites
  - Node.js installed
  - Google account

# Setup Firebase CLI

    npm install -g firebase-tools
    firebase login
    firebase init

Choose features like:
  - Firestore
  - Authentication
  - Hosting
  - Functions (Cloud Functions)

Firebase Console:
  1. Go to https://console.firebase.google.com
  2. Create a new project
  3. Get credentials from Project Settings > General > Web App
  4. Copy config and use in your app

# Setting Up MongoDB
 - Starting the MongoDB Service

           # Windows
        net start MongoDB
        
        # macOS/Linux
        brew services start mongodb/brew/mongodb-community

- Connecting using MongoDB Shell

      mongo

Using Compass GUI

  1. Open Compass

  2. Paste connection string (for Atlas or local mongodb://localhost:27017)

  3. Explore databases and collections visually
