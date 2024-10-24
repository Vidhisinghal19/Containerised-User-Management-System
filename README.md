# Containerised-User-Management-System
This User Management System (UMS) is a role-based user access system built using Flask, MySQL, and Docker. The system provides role-based login functionality with dedicated portals for admins, managers, and regular employees. Each user type has specific operations and authorities based on their role, with CRUD (Create, Read, Update, Delete) capabilities and MySQL database management.

The project is containerized using Docker and managed through Docker Compose, making it easy to deploy and maintain.
KEY FEATURES:
   1.Role-based login: The system allows users to log in based on their roles (admin, manager, employee) and presents the corresponding operations for each role.
   2. CRUD Operations: Each role (Admin, Manager, Employee) has specific CRUD operations:
        Admin: Can manage all users, roles, and departments.
        Manager: Can manage users within their department.
        Employee: Can view and update their own profile.
   3.Database Management: The system connects to a MySQL database for persistent user and role data.
   4.Dynamic Role-Based Interface:
        Admin Portal: A centralized, grid-style interface resembling an Excel sheet where admins can manage users, update user details in bulk, delete users, and add new users.
        Manager Portal: A manager-specific interface to manage employees within their own department.
        Employee Portal: Allows regular employees to view and modify their own profile information.
   5.Dockerized: The project is containerized using Docker and managed through Docker Compose, ensuring seamless deployment across different environments.
   6.Non-Session Based Authentication: Simple login system with email and passcode validation without using session management.
   7.JSON API: Provides REST API-style outputs with JSON responses on localhost:5000, designed for simplicity and efficiency without complex HTML frontends.

PROJECT STRUCTURE:
/UMS/
  |--- dockerfile
  |--- docker-compose.yml
  |--- requirements.txt 
  |--- app/
        |--- __init__.py               # Flask app initialization
        |--- admin_operations.py       # Logic for user, role, and department management
        |--- manager_operations.py      # Logic for manager-specific operations
        |--- employee_operations.py     # Logic for employee-specific operations
        |--- main.py                   # Entry point to run the Flask app
        |--- models.py                 # Models and database logic
        |--- db.py                     # Database connection logic
        |--- utils.py                  # Utility functions (e.g., hashing passwords)
        |--- routes.py                 # Flask routes for handling API operations
        |--- admin_dashboard.py         # Admin dashboard routes and logic
        |--- manager_dashboard.py       # Manager dashboard routes and logic
        |--- employee_dashboard.py      # Employee dashboard routes and logic
        |--- templates/                 # HTML templates (if needed)
              |--- admin_portal.html     # Template for the admin portal
              |--- manager_portal.html   # Template for the manager portal
              |--- employee_portal.html  # Template for the employee portal
        |--- static/                   # Static files (CSS, JS, etc.)
              |--- css/
                    |--- admin_portal.css     # CSS for the admin portal
                    |--- manager_portal.css   # CSS for the manager portal
                    |--- employee_portal.css  # CSS for the employee portal

   
