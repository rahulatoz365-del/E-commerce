# Full-Stack E-Commerce Platform

## 1. Overview

This project is an end-to-end e-commerce web application built using React, Express.js, and MongoDB. It provides a complete shopping experience for customers and a dedicated administrative interface for managing products and orders.

The application includes:

- A React single-page application (SPA) frontend, bundled with Vite for fast development and Hot Module Replacement (HMR).
- A Node.js/Express.js backend exposing RESTful APIs.
- A MongoDB database for persistence of users, products, orders, and reviews.
- PayPal integration for secure payment processing.

---

## 2. Architecture and Technology Stack

### 2.1 High-Level Architecture

- **Frontend:** React + Vite
- **Backend:** Node.js + Express.js
- **Database:** MongoDB
- **Payments:** PayPal API / PayPal Developer SDK

### 2.2 Technology Stack Details

| Layer       | Technology            | Purpose                                                  |
|------------|------------------------|----------------------------------------------------------|
| Frontend   | React                  | Component-based user interface                           |
| Build Tool | Vite                   | Fast development server and optimized production builds  |
| Backend    | Express.js             | Web framework for routing and API endpoints              |
| Database   | MongoDB                | NoSQL database for flexible schema and high scalability  |
| Payments   | PayPal API / SDK       | Secure, external payment processing                      |

---

## 3. Features

### 3.1 Customer-Facing Functionality

**User Authentication**

- User registration, login, and logout.
- Secure session handling for authenticated access to protected routes.

**Product Browsing and Shopping**

- Browse a catalog of products with:
  - Name
  - Description
  - Price
  - Stock availability
  - Product images
- Add products to a shopping cart for later checkout.

**Checkout and Payments**

- Streamlined checkout workflow for authenticated users.
- Integration with PayPal via the PayPal Developer SDK for secure transactions.

**Ratings and Reviews**

- Customers can submit product ratings and text reviews.
- Reviews are restricted to users who have purchased the corresponding product.

**Dynamic Home Page Hero Section**

- Hero section on the home page with an automated image slideshow.
- Configurable set of images for promotional or branding content.

---

### 3.2 Administration Dashboard

Access to the admin dashboard is restricted to authorized administrative users.

**Product Management**

- Create new product listings.
- Update existing products, including:
  - Name
  - Description
  - Price
  - Stock quantity
  - Images
- Delete products from the catalog.

**Order Management**

- View a list of all customer orders with relevant details.
- Update order status, including:
  - Shipping status
  - Delivery status

---

## 4. Frontend Development with React and Vite

The frontend is scaffolded using Vite for a modern, efficient development experience with HMR and optimized builds.

This setup uses one of Vite’s official React plugins for Fast Refresh:

- `@vitejs/plugin-react`  
  Uses [Babel](https://babeljs.io/) for enabling React Fast Refresh.

- `@vitejs/plugin-react-swc`  
  Uses [SWC](https://swc.rs/) (a Rust-based compiler) for faster builds and Fast Refresh.

Both plugins provide equivalent functionality for development; the choice between them depends on performance and tooling preferences.

---

## 5. Getting Started

### 5.1 Prerequisites

- Node.js (version 14 or later recommended)
- npm or yarn
- MongoDB instance (local or hosted, e.g., MongoDB Atlas)
- PayPal Developer account and Client ID

### 5.2 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-organization/your-repo.git
   cd your-repo
   
2. **Install frontend dependencies**

   ```bash
   cd frontend
   npm install
   # or
   # yarn install
   ```

3. **Install backend dependencies**

   ```bash
   cd ../backend
   npm install
   # or
   # yarn install
   ```

### 5.3 Environment Configuration

Create an `.env` file in the backend directory with at least the following variables:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PAYPAL_CLIENT_ID=your_paypal_client_id
```

Adjust names and values as required by your internal standards and deployment environment.

### 5.4 Running the Application

Run the backend and frontend in separate terminals.

**Backend (Express.js)**

```bash
cd backend
npm run server
# or
# yarn server
```

**Frontend (React + Vite)**

```bash
cd frontend
npm run dev
# or
# yarn dev
```

By default, Vite will start the frontend development server on a port such as `http://localhost:5173`, and the backend will run on the configured `PORT` (e.g., `http://localhost:5000`).
