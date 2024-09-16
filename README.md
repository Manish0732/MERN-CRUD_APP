# CRUD Application with Authentication

This project is a CRUD (Create, Read, Update, Delete) application built using Node.js, Express, and MongoDB. It includes user authentication and authorization features using the Passport.js library. The application allows users to register, log in, log out, and reset their passwords. Additionally, it provides complex CRUD operations for managing users, products, states, and cities.

## Features

- **User Registration**: Users can register by providing their details and uploading a profile photo.
- **User Login**: Users can log in using their email and password.
- **User Logout**: Users can log out of their account.
- **Password Reset**: Users can reset their password by receiving an OTP via email.
- **User Management**: Admins can view, update, block, and unblock users.
- **Product Management**: Users can add, update, and delete products.
- **State Management**: Admins can add and delete states.
- **City Management**: Admins can add and delete cities.

## Technologies Used

- **Node.js**: JavaScript runtime environment.
- **Express**: Web framework for Node.js.
- **MongoDB**: NoSQL database.
- **Mongoose**: MongoDB object modeling tool.
- **Passport.js**: Authentication middleware for Node.js.
- **EJS**: Embedded JavaScript templating.
- **Formidable**: Node.js module for parsing form data, especially file uploads.
- **Bcrypt.js**: Library to hash passwords.
- **Nodemailer**: Module to send emails.
- **Country-State-City**: Library to get country, state, and city data.
- **Express-Session**: Middleware to manage sessions.
- **Express-Flash**: Middleware to display flash messages.
- **Morgan**: HTTP request logger middleware.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-repo/crud-auth-app.git
   cd crud-auth-app

   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:
   Create a '.env' file in the root directory and add the following:

   ```env
   EMAIL=your-email@example.com
   EMAIL_PASSWORD=your-email-password
   ```

4. Start the MongoDB server:

   ```bash
   mongod
   ```

5. Run the application:

   ```bash
   npm start
   ```

6. Open your browser and navigate to 'http://localhost:3005'

## Project Structure

- **models/**: Contains Mongoose schemas for User, Product, State, and City.
- **passportAuth/**: Contains Passport.js configuration.
- **resetPass/**: Contains email sending functionality for password reset.
- **templates/views/**: Contains EJS templates for rendering views.
- **public/**: Contains static files like CSS and JavaScript.

## Routes

### User Routes

- **GET /register**: Render the registration page.
- **POST /register**: Handle user registration.
- **GET /**: Render the login page.
- **POST /**: Handle user login.
- **GET /logout**: Handle user logout.
- **POST /updateMe**: Handle user profile update.
- **POST /updateU**: Render the user update page for admin.
- **POST /updateUser**: Handle user update by admin.
- **POST /block**: Handle user blocking by admin.
- **POST /unblock**: Handle user unblocking by admin.

### Product Routes

- **GET /products**: Render the products page.
- **POST /updateProduct**: Handle product update.
- **POST /deleteProduct**: Handle product deletion.
- **POST /addP**: Handle adding a new product.

### State Routes

- **GET /state**: Render the state page.
- **POST /state**: Handle adding a new state.
- **POST /deleteState**: Handle state deletion.

### City Routes

- **GET /city**: Render the city page.
- **GET /city/get-cities**: Get cities of a state dynamically.
- **POST /city**: Handle adding a new city.
- **POST /deleteCity**: Handle city deletion.

### Password Reset Routes

- **GET /forgot**: Render the forgot password page.
- **POST /forgot**: Handle sending OTP for password reset.
- **GET /reset**: Render the reset password page.
- **POST /reset**: Handle password reset.

### Author

- [Manish Joshi](https://github.com/manish0732/)
