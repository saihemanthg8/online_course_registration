# Online Course Registration System

A comprehensive web-based application for managing course registrations in educational institutions. This system allows students to register, enroll in courses, and view their enrollment history, while administrators can manage courses, departments, students, and more.

## Project Overview

This Online Course Registration System is designed to streamline the course registration process for educational institutions. It provides separate interfaces for students and administrators, allowing for efficient management of course enrollments, student records, and academic information.

The system automates the traditional manual course registration process, making it more accessible, efficient, and error-free. Students can browse available courses, enroll in them based on their academic requirements, and track their enrollment history. Administrators can manage the entire system, including adding new courses, departments, semesters, and managing student registrations.

## System Requirements

- **PHP**: Version 7.4 or higher
- **MySQL**: Version 5.7 or higher
- **Web Server**: Apache 2.4 or higher
- **Web Browser**: Modern browsers like Chrome, Firefox, Safari, or Edge
- **Additional PHP Extensions**: 
  - mysqli
  - session
  - gd (for image processing)
  - mbstring

## Installation Instructions

Follow these steps to set up the Online Course Registration System:

1. **Clone or Download the Repository**
   ```
   git clone <repository-url>
   ```
   or download and extract the ZIP file to your web server's document root.

2. **Set Up the Database**
   - Create a new MySQL database named `onlinecourse`
   - Import the SQL file located at `SQL File/onlinecourse.sql` using phpMyAdmin or MySQL command line

3. **Configure Database Connection**
   - Open `includes/config.php` and update the database connection parameters if needed:
     ```php
     define('DB_SERVER','localhost');
     define('DB_USER','root');
     define('DB_PASS','');
     define('DB_NAME','onlinecourse');
     ```

4. **Set Proper Permissions**
   - Ensure the web server has read/write permissions to the project directory
   - Make sure the `studentphoto` directory is writable for student profile images

5. **Access the Application**
   - Navigate to the project URL in your web browser (e.g., `http://localhost/onlinecourse/`)

## Database Setup

The database structure is already defined in the SQL file provided with the project. Here's a brief overview of the main tables:

- `admin`: Stores administrator credentials
- `students`: Contains student information and login details
- `course`: Stores course information
- `department`: Lists academic departments
- `semester`: Contains semester information
- `session`: Academic sessions
- `courseenrolls`: Records of student course enrollments
- `userlog`: Logs of student logins
- `news`: News/announcements for the dashboard

## Running the Application

1. Start your Apache and MySQL services (using XAMPP, WAMP, MAMP, or similar)
2. Open your web browser and navigate to the project URL
3. You'll see the home page with login options for students and administrators

## Login Credentials

### Admin Login
- **Username**: admin
- **Password**: Test@123

### Student Login
- **Registration Number**: 10806121
- **Password**: Test@123

*Note: You can create new student accounts through the admin panel or use the default account for testing.*

## Features and Functionality

### Student Features
- **Account Management**:
  - Login with registration number and password
  - Change password
  - Update profile information
  - View personal details

- **Course Management**:
  - Enroll in available courses
  - View enrollment history
  - Check course details

- **General Features**:
  - View news and announcements
  - Access course information

### Administrator Features
- **Student Management**:
  - Register new students
  - Manage student information
  - Reset student passwords
  - View and delete student records

- **Course Management**:
  - Add new courses
  - Edit course details
  - Delete courses
  - Set seat limits for courses

- **Academic Structure Management**:
  - Manage departments
  - Configure semesters
  - Set up academic sessions
  - Define course levels

- **Enrollment Management**:
  - View enrollment history
  - Track student enrollments
  - Generate reports

- **System Management**:
  - Post news and announcements
  - View student login logs
  - Change admin password

## Project Structure

```
Online course registration Using PHP/
├── admin/                  # Administrator interface
│   ├── course.php          # Course management
│   ├── department.php      # Department management
│   ├── includes/           # Admin includes (header, footer, etc.)
│   ├── manage-students.php # Student management
│   ├── semester.php        # Semester management
│   └── ...
├── assets/                 # CSS, JS, and image files
│   ├── css/
│   ├── img/
│   └── js/
├── includes/               # Common include files
│   ├── config.php          # Database configuration
│   ├── footer.php          # Footer template
│   ├── header.php          # Header template
│   └── menubar.php         # Navigation menu
├── SQL File/               # Database SQL file
│   └── onlinecourse.sql    # Database structure and initial data
├── studentphoto/           # Student profile images
├── change-password.php     # Password change functionality
├── enroll.php              # Course enrollment page
├── enroll-history.php      # Enrollment history page
├── index.php               # Main entry point/login page
└── ...
```

## Troubleshooting Common Issues

### Database Connection Issues
- Verify that MySQL service is running
- Check database credentials in `includes/config.php`
- Ensure the `onlinecourse` database exists and has been properly imported

### Login Problems
- Make sure you're using the correct credentials
- For student login, use registration number, not username
- If password is forgotten, an administrator can reset it

### Enrollment Errors
- Verify that the course has available seats
- Check if you're already enrolled in the course
- Ensure your pincode is valid

### Image Upload Issues
- Check that the `studentphoto` directory has write permissions
- Verify that the uploaded image format is supported (JPG, PNG, GIF)
- Ensure the image size is within acceptable limits

## Credits and Acknowledgments

This Online Course Registration System was developed as an educational project to demonstrate PHP and MySQL web application development. Special thanks to:

- Bootstrap for the responsive frontend framework
- jQuery for JavaScript functionality
- Font Awesome for icons
- All contributors who helped test and improve the system

## License

This project is available for educational purposes.

---

For additional support or questions, please contact the system administrator.
