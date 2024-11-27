# E-Commerce MERN Project

## Overview
This is a full-stack e-commerce platform built with the MERN stack (MongoDB, Express.js, React, Node.js). The application incorporates robust **Authentication**, **Authorization**, and **Role-Based Access Control (RBAC)** mechanisms to ensure secure and efficient management of user interactions.

---

## Key Features

### **Authentication**
- **User Registration**: Allows new users to create accounts securely with hashed passwords.
- **User Login**: Authenticated users receive a JWT token for secure session management.
- **Forgot Password**: Enables users to reset passwords via a secure email-based link.
- **Protected Routes**: Only logged-in users can access certain pages like the user dashboard, profile, and orders.

### **Authorization**
- **Role-Based Permissions**:  
  Access to specific routes is restricted based on user roles stored in the database:
  - **Admin**: Can manage categories, products, users, and view all orders.
  - **User**: Can view and manage their profile and orders.
- **Token Validation**: Backend middleware validates JWT tokens to authorize requests.

### **Role-Based Access Control (RBAC)**
- **Defined Roles**: Roles like **Admin**, **User**, and potentially **Moderator** are assigned to users and stored in the database.
- **Route Protection**:  
  - Admin-specific routes (e.g., `/dashboard/admin`) are accessible only to users with the Admin role.
  - User-specific routes (e.g., `/dashboard/user`) are restricted to authenticated users.
- **Dynamic Role Checks**: The backend dynamically verifies roles during requests to grant or deny access.

---

## Implemented Functionality
- **User Pages**:  
  - **Dashboard**: A personalized space for authenticated users.  
  - **Orders**: Allows users to view their orders.  
  - **Profile**: Lets users manage their account details.

- **Admin Pages**:  
  - **Create Category**: Admins can create product categories.  
  - **Create Product**: Admins can add new products.  
  - **Manage Users**: View and manage registered users.  
  - **Manage Orders**: View and manage all customer orders.  
  - **Update Product**: Edit product details dynamically.

- **Error Handling**: Non-existent routes are redirected to a `404 Page Not Found` component.

---

## Technology Stack
- **Frontend**: React.js, React Router DOM
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Styling**: CSS

---


