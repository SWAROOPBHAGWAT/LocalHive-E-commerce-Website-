# 🛒 E-Commerce Platform with RBAC

This is a full-stack e-commerce platform built with the MERN stack (MongoDB, Express.js, React, Node.js). The application incorporates robust **Authentication**, **Authorization**, and **Role-Based Access Control (RBAC)** mechanisms to ensure secure and efficient management of user interactions. Designed with security and scalability in mind, the platform adheres to industry-standard best practices for a seamless and secure user experience.

---

## 🔑 Key Features

### **Authentication**
- **User Registration**: Secure user signup with passwords hashed using **bcrypt**.
- **User Login**: Authenticated users receive **JWT tokens** for secure session management.
- **Forgot Password**: Enables users to securely reset passwords via email-based token validation.
- **Session Management**: Tokens are securely stored and validated on every request to protected routes.
- **Protected Routes**: Users must log in to access sensitive pages like dashboards, profiles, and orders.

### **Authorization**
- **Role-Based Permissions**:
  - **Admin**: Full control over the platform, including managing products, categories, users, and all orders.
  - **User**: Limited access to their dashboard, orders, and profile functionalities.
- **Dynamic Permissions**: Each role is dynamically checked during every API request to ensure only authorized users can access resources.

### **Role-Based Access Control (RBAC)**
- **Defined Roles**:
  - **Admin**:
    - Full access to product and user management routes.
    - Permissions to create, update, and delete categories and products.
    - Can view and manage all orders and registered users.
  - **User**:
    - Access to personalized dashboards and order histories.
    - Limited access to admin-protected functionality.
- **Dynamic Role Checks**: Backend middleware ensures every API request is validated for role-specific access.

### **E-Commerce Features**
- **Product Listings**: Users can browse categories and products with filters and pagination for better performance.
- **Shopping Cart**: Add, update, and remove items in the cart with a real-time total calculation.
- **Secure Payments**: Integrated payment gateway for seamless transactions.
- **Order Management**:
  - Users: Place and track orders in real-time.
  - Admins: View and update the status of all orders.

---

## 🛡️ Security Measures
- **Password Hashing**: User passwords are hashed using **bcrypt** to prevent plaintext password storage.
- **JWT Authentication**: Secure token-based authentication ensures session security.
- **Token Expiry**: JWT tokens have a defined expiry time, reducing the risk of misuse.
- **Input Sanitization**: Prevents SQL injection and XSS attacks by sanitizing all inputs.
- **HTTP Headers**: Security headers like **helmet** and **CORS** ensure data integrity.
- **Environment Variables**: Sensitive data such as API keys and database URIs are securely stored in environment variables.

---

## 🛠️ Implemented Functionality

### **User Features**
- **Dashboard**: A personalized space displaying user-specific information such as order history and account details.
- **Orders**: Allows users to view their order history, track delivery status, and interact with past purchases.
- **Profile Management**: Users can securely update their personal details such as email, password, and delivery address.

### **Admin Features**
- **Create Category**: Admins can create and manage product categories, organizing products into appropriate sections.
- **Create Product**: Admins can add and manage product details, including price, description, images, and stock count.
- **Manage Users**: Admins can view, edit, and delete registered user accounts to maintain the platform’s user base.
- **Manage Orders**: Admins can view and update the status of all customer orders, such as pending, shipped, or completed.
- **Update Products**: Admins can dynamically edit and update product information, including price adjustments or stock changes.

### **Error Handling**
- Non-existent routes are redirected to a **404 Page Not Found** component for a better user experience.
- **Custom Error Pages** for different error scenarios such as failed authentication or access-denied for unauthorized users.

### **Enhanced User Experience**
- **Responsive UI**: The platform is designed with a responsive UI, ensuring a smooth experience on both desktop and mobile devices.
- **Custom Modal Windows**: Used for adding, editing, and confirming product or user-related actions in an intuitive, user-friendly manner.
- **Notifications**: Instant notifications for users when their orders are updated or when they have a new message from the admin.

---

## ⚙️ Technology Stack
- **Frontend**: React.js, React Router DOM, CSS
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Security Libraries**: bcrypt, helmet, CORS

---

## 💡 Best Practices Implemented
- **Folder Structure**: Organized folder structure for separating concerns (e.g., routes, controllers, models) in both frontend and backend.
- **Scalable Design**: Components and APIs are designed to handle future scalability, supporting the addition of more features without major rework.
- **Pagination and Filtering**: Implemented on product listings to improve performance when dealing with large amounts of data.
- **Custom Hooks**: Utilized custom React hooks to simplify state management and improve code readability.
- **Error Handling**: Error handling mechanisms in place to ensure graceful degradation of features and clear user feedback.
- **Deployment**: Platform deployed to production server with optimized build and secure configurations.

---


