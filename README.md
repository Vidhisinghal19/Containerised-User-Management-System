# Containerised-User-Management-System
This User Management System (UMS) is a role-based user access system built using Flask, MySQL, and Docker. The system provides role-based login functionality with dedicated portals for admins, managers, and regular employees. Each user type has specific operations and authorities based on their role, with CRUD (Create, Read, Update, Delete) capabilities and MySQL database management.

The project is containerized using Docker and managed through Docker Compose, making it easy to deploy and maintain.
Key Features:
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
