# Laravel User Management System

A robust user management system built with Laravel, featuring role-based authentication and a modern UI with Alpine.js.

## Features

- 🔐 User Authentication (Register, Login, Logout)
- 👥 Role-based Access Control (Admin & User roles)
- 📊 Admin Dashboard for User Management
- ✨ Modern UI with Bootstrap 5
- 🔄 Real-time Search with Alpine.js
- 📱 Responsive Design
- 🔒 Security Features (Password Hashing, CSRF Protection)

## Prerequisites

Before you begin, ensure you have the following installed:
- PHP >= 8.1
- Composer
- MySQL/PostgreSQL
- Node.js & NPM

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd user-management
```

2. Install PHP dependencies:
```bash
composer install
```

3. Install NPM dependencies:
```bash
npm install
```

4. Create a copy of the environment file:
```bash
cp .env.example .env
```

5. Generate application key:
```bash
php artisan key:generate
```

6. Configure your database in `.env`:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

7. Run database migrations and seeders:
```bash
php artisan migrate
php artisan db:seed --class=AdminSeeder
```

8. Start the development server:
```bash
php artisan serve
```

9. In a separate terminal, compile assets:
```bash
npm run dev
```

## Default Admin Credentials

- Email: admin@example.com
- Password: password

## Project Structure

```
├── app/
│   ├── Http/
│   │   ├── Controllers/
│   │   │   └── UserController.php
│   │   └── Middleware/
│   │       └── AdminMiddleware.php
│   └── Models/
│       └── User.php
├── database/
│   ├── migrations/
│   │   └── 2024_03_21_000000_add_role_to_users_table.php
│   └── seeders/
│       └── AdminSeeder.php
├── resources/
│   └── views/
│       ├── layouts/
│       │   └── app.blade.php
│       └── users/
│           ├── index.blade.php
│           ├── create.blade.php
│           └── edit.blade.php
└── routes/
    └── web.php
```

## Features in Detail

### User Authentication
- Secure registration and login system
- Password hashing and validation
- Remember me functionality
- Session management

### Role-based Access Control
- Admin and User roles
- Middleware protection for admin routes
- Role-based UI elements

### Admin Dashboard
- User listing with search functionality
- Create new users
- Edit existing users
- Delete users
- Role management

### UI/UX Features
- Responsive Bootstrap 5 design
- Real-time search with Alpine.js
- Form validation with error messages
- Success/error notifications
- Confirmation dialogs for destructive actions

## Security Features

- Password hashing using Laravel's built-in hashing
- CSRF protection
- Form validation
- SQL injection prevention
- XSS protection
- Role-based access control

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

If you encounter any issues or have questions, please open an issue in the repository.

## Acknowledgments

- Laravel Framework
- Bootstrap 5
- Alpine.js
- All contributors who have helped with the project 