# Task Management Application

This is a simple CRUD application for managing tasks in a project management tool. The application consists of a Laravel backend for the RESTful API and a Vue.js frontend for the user interface.

## Backend (Laravel)

### Dependencies
- PHP >= 7.4
- Composer
- MySQL or SQLite (for database)

### Setup
1. Clone the repository: git clone https://github.com/ashu1409/project-management-tool
2. Navigate to the backend directory: cd backend
3. Install PHP dependencies: composer install
4. Rename the `.env.example` file to `.env` and update the database configuration:
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_database_username
DB_PASSWORD=your_database_password

5. Generate application key: php artisan key:generate
6. Migrate the database: php artisan migrate
7. Serve the application: php artisan serve


The backend API should now be running on http://localhost:8000.

## Frontend (Vue.js)

### Dependencies
- Node.js
- npm or yarn

### Setup
1. Navigate to the frontend directory: cd frontend
2. Install Node.js dependencies: npm install
3. Serve the application: npm run serve


The Vue.js frontend should now be running on http://localhost:8080.

## Usage

1. Access the application in your web browser using the provided URLs for the backend and frontend.
2. You can view, add, edit, and delete tasks using the interface provided.



## Support

If you encounter any issues or have any questions, please feel free to contact ajha1593@gmail.com.






