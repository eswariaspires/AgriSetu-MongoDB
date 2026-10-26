# AgriSetu — Farmer–Buyer Direct Connection Platform

AgriSetu is a full-stack web application designed to connect farmers directly with buyers. Farmers can publish agricultural produce listings, while buyers can explore available produce and connect with farmers. The platform aims to simplify agricultural trade by providing a common digital space for farmers and buyers.

This version uses **MongoDB** as its database.

## Features

- User registration and login
- Role-based access for farmers and buyers
- Farmer produce management
- Add, view, edit, and delete produce listings
- Browse available agricultural products
- Buyer–farmer connection requests
- Accept or manage connection requests
- Notifications for relevant activities
- Reviews and ratings
- JWT-based authentication
- Password hashing for improved security

## Technology Stack

### Frontend
- React
- Vite
- JavaScript
- CSS

### Backend
- Node.js
- Express.js
- Mongoose
- JSON Web Tokens (JWT)
- bcryptjs

### Database
- MongoDB
- MongoDB Atlas or a local MongoDB server

## Prerequisites

Install the following before running the application:

- Node.js
- npm
- A MongoDB database
- Git (optional)

## Project Structure

```text
agrisetu/
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── server.js
│   ├── package.json
│   └── .env.example
├── src/
├── public/
├── package.json
├── .gitignore
└── README.md
```

The exact folder structure may vary depending on the current implementation.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/eswariaspires/AgriSetu-MongoDB.git
cd AgriSetu-MongoDB
```

### 2. Install Frontend Dependencies

From the project root:

```bash
npm install
```

### 3. Install Backend Dependencies

```bash
cd backend
npm install
```

### 4. Configure Environment Variables

Create a `.env` file inside the `backend` directory using `.env.example` as a template.

Example configuration:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secure_jwt_secret
```

Replace the placeholder values with your own configuration.

**Never commit your actual `.env` file, database credentials, or JWT secret to GitHub.**

### 5. Start the Backend

From the `backend` directory:

```bash
npm run dev
```

The backend should run at:

```text
http://localhost:5000
```

### 6. Start the Frontend

Open another terminal in the project root:

```bash
npm run dev
```

Vite will display the local frontend address. Open that address in your browser.

## Database Configuration

AgriSetu uses MongoDB to store application data, including:

- User accounts
- Produce listings
- Farmer–buyer connections
- Reviews
- Notifications

Mongoose is used to define data models and interact with the MongoDB database.

For MongoDB Atlas, configure the connection string in `backend/.env`. Ensure that your database user has the required permissions and that your network access settings allow the application to connect.

## Authentication and Security

- User passwords are hashed before storage.
- JWTs are used for authentication.
- Role-based access distinguishes farmers and buyers.
- Database credentials are stored in environment variables.
- Protected backend routes should validate authentication and authorization.

## Future Enhancements

- Advanced produce search and filtering
- Improved mobile responsiveness
- Price comparison and market insights
- Better farmer and buyer dashboards
- Deployment to a production hosting platform
- Enhanced analytics and reporting

## Project Objective

AgriSetu demonstrates how a full-stack web application can support direct communication between farmers and buyers using a modern frontend, REST APIs, authentication, and a NoSQL database.

## Author

**Eeswari**  
GitHub: [eswariaspires](https://github.com/eswariaspires)
