Geo-Referenced Map Interface using Open Source Technologies

A full-stack web application that provides an interactive geo-referenced map interface for exploring locations, managing user accounts, and accessing location-based information through an intuitive web platform.

This project is built using HTML, CSS, JavaScript, Tailwind CSS, PHP, and MySQL, combining a responsive frontend with a secure backend and database-driven functionality.

Features
User Features
User registration and login system
Secure authentication with session management
Password hashing and validation
Forgot password functionality
Responsive UI with Tailwind CSS
Interactive geo-referenced map interface
Location-based search and navigation
User-friendly dashboard and navigation
Logout functionality
System Features
Frontend and backend form validation
Secure user authentication
MySQL database integration
Session and cookie handling
Organized modular file structure
Scalable backend architecture
Tech Stack
Frontend
HTML5
CSS3
Tailwind CSS
JavaScript
Backend
PHP
MySQL
Tools & Environment
XAMPP / WAMP / LAMP
phpMyAdmin
Apache Server
Project Structure
geo_map/
│
├── assets/                  # Images, icons, static resources
├── css/                     # Custom stylesheets
├── js/                      # Frontend scripts
├── includes/                # Reusable PHP components
├── config/                  # Database connection files
├── pages/                   # Internal pages
├── auth/                    # Login, signup, forgot password logic
│
├── index.html               # Landing page
├── login.html               # Login page
├── signup.html              # Signup page
├── forgot.html              # Forgot password page
├── dashboard.php            # User dashboard
├── map.php                  # Interactive geo-referenced map page
└── README.md
Installation & Setup
1. Clone or Download the Project
git clone https://github.com/your-username/geo-map-interface.git

Or place the project folder inside your local server directory:

XAMPP: htdocs/
WAMP: www/

Example:

C:/xampp/htdocs/geo_map/
Database Setup
1. Open phpMyAdmin

Visit:

http://localhost/phpmyadmin
2. Create Database

Create a new database:

CREATE DATABASE geo_map;
3. Import SQL File

Import the provided SQL file (if available) into the geo_map database.

If no SQL file is included, create a users table manually:

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    fullname VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
Configuration
Configure Database Connection

Update your database connection file (example: config/db.php):

<?php
$conn = mysqli_connect("localhost", "root", "", "geo_map");

if (!$conn) {
    die("Database connection failed: " . mysqli_connect_error());
}
?>
Running the Project
Start Apache and MySQL

Open XAMPP Control Panel and start:

Apache
MySQL
Open in Browser

Visit:

http://localhost/geo_map/
Authentication Flow
User signs up with name, email, and password
Password is validated and securely hashed
User logs in with credentials
Session is created after successful login
User accesses dashboard and map interface
User can log out securely
Core Pages
index.html – Landing page
signup.html – User registration
login.html – User login
forgot.html – Password recovery
dashboard.php – User dashboard
map.php – Interactive map interface
Security Features
Password hashing using PHP
Input sanitization
Form validation
Session-based authentication
Protected routes
Secure logout handling
Future Improvements
Real-time geolocation tracking
Route planning and navigation
Nearby place suggestions
Admin dashboard for location management
User profile management
Email verification
Password reset via email
Map marker customization
Integration with OpenStreetMap / Leaflet API


Contributors
Ananya Kumari


License

This project is licensed under the MIT License.

Acknowledgements

This project was developed as part of an academic project to demonstrate the implementation of a geo-referenced map interface using open source web technologies, secure authentication, and database integration.
