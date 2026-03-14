# Cosmetics Store

Full-stack cosmetics and skincare platform built with React, Node.js, Express, and MongoDB. The project supports three main user flows: customer, agent, and admin.

## Overview

This project combines an e-commerce flow with skincare consultation features.

- Customers can register, log in, browse products, place orders, track orders, submit skincare forms, and write reviews.
- Agents can log in, place customer orders, track referred orders, and monitor balances or commissions.
- Admins can manage users, products, orders, order tracking, and agent-related operations.

## Core Features

- Role-based authentication for user, agent, and admin
- Product listing and product management
- Order creation, order history, and tracking updates
- Coupon support and agent referral flow
- OTP-based password reset and login support
- Skincare consultation form with image uploads
- Review submission and review display
- Admin dashboard and agent dashboard

## Tech Stack

### Frontend

- React
- React Router
- Axios
- Bootstrap
- Framer Motion
- Styled Components

### Backend

- Node.js
- Express
- MongoDB
- Mongoose
- JWT
- bcryptjs
- multer
- nodemailer

## Repository Structure

liveServer/
|-- app.js
|-- package.json
|-- Cosmetics-store-Backend/
|   |-- controllers/
|   |-- middleware/
|   |-- models/
|   |-- routes/
|   |-- scripts/
|   `-- uploads/
`-- cosmetics-store-front/
    |-- public/
    |-- src/
    |   |-- assets/
    |   |-- component/
    |   |-- context/
    |   |-- pages/
    |   |-- routes/
    |   `-- utils/
    `-- package.json
```

## Frontend Structure

The frontend lives inside `cosmetics-store-front/`.

- `src/index.js` bootstraps the React application and wraps it with the auth provider.
- `src/App.js` defines the main route map.
- `src/pages/` contains route-level screens such as home, login, register, admin dashboard, and agent dashboard.
- `src/component/` contains reusable feature components such as order forms, review UI, skincare form, and dashboard widgets.
- `src/context/` contains auth state management for user, admin, and agent sessions.
- `src/utils/axios.js` contains shared Axios configuration for backend API access.
- `src/assets/` stores static images and media used in the UI.

## Backend Structure

The backend is split between `app.js` and `Cosmetics-store-Backend/`.

- `app.js` is the Express entry point. It loads middleware, connects to MongoDB, mounts routes, and starts the server.
- `routes/` defines API endpoints grouped by feature.
- `controllers/` contains business logic.
- `models/` contains Mongoose schemas.
- `middleware/` contains reusable logic such as JWT auth and file uploads.
- `scripts/` contains helper scripts such as admin creation.
- `uploads/` stores uploaded files from the skincare flow.

## Main API Modules

- `/api/auth` - user registration and login
- `/api/users` - user profile-related actions
- `/api/products` - product listing and product CRUD
- `/api/orders` - order creation, fetch, status update, and tracking
- `/api/admin` - admin-only management routes
- `/api/agents` - agent login, orders, balance, and commission routes
- `/api/reviews` - review creation and fetch
- `/api/skincare` - skincare form submission and fetch
- `/api/payments/phonepe` - payment initiation and callback flow
- `/api/otp` - OTP request, verify, and password reset
- `/api/admin/coupons` and `/api/orders/apply-coupon` - coupon management and application

## Running the Project Locally

### 1. Install backend dependencies

```bash
npm install
```

### 2. Install frontend dependencies

```bash
cd cosmetics-store-front
npm install
```

### 3. Create environment file

Copy `.env.example` to `.env` and update the values.

### 4. Start the backend

From the project root:

```bash
npm start
```

### 5. Start the frontend

In a second terminal:

```bash
cd cosmetics-store-front
npm start
```

Default local URLs:

- Frontend: `http://localhost:3000`
- Backend: `http://localhost:5000`

## Environment Variables

Create a `.env` file in the project root with values similar to the following:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_app_password
FRONTEND_URL=http://localhost:3000
```


## Resume-Friendly Summary

Developed a full-stack cosmetics store and skincare consultation platform with role-based access for customers, agents, and admins. Built a React frontend with protected routes and dashboard flows, and a Node.js/Express backend with MongoDB, JWT authentication, OTP support, coupon logic, order management, review handling, and image upload functionality. 

