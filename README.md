# Contributing to Laravel Project

Thank you for considering contributing to our Laravel application! Before getting started, please review the following guidelines and instructions to set up the project and work efficiently.

---

## Project Overview

This is a Laravel 11 application using the following stack and tools:
- **Backend**: PHP 8.2 with Laravel v11.37.0
- **Frontend**: JavaScript (TailwindCSS, Alpine.js, Vite)
- **Database**: SQLite
- **Queue Connections**: Database Queue
- **Package Manager**: Composer (backend) and npm (frontend)

---

## Getting Started

### Pre-requisites

Please ensure the following tools are installed on your system:

1. **PHP (v8.2 or higher)**: Ensure both PHP CLI and extensions required by Laravel are properly installed.
2. **Composer**: For managing PHP packages ([Get Composer](https://getcomposer.org)).
3. **Node.js (v18 or higher)**: Used for managing frontend dependencies ([Download Node.js](https://nodejs.org)).
4. **NPM**: Comes with Node.js installation.
5. **SQLite**: To work with the development database.
6. **Git**: For version control.

---

## Setting Up the Development Environment

1. **Fork and Clone the Repository**

   Fork the repository to your GitHub account and clone it locally.

   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository
   ```

2. **Install PHP Dependencies**

   Run the following command to install the backend dependencies.

   ```bash
   composer install
   ```

3. **Install Node.js Dependencies**

   Use npm to install front-end packages:

   ```bash
   npm install
   ```

4. **Set Up the Environment File**

   Copy the `.env.example` file as `.env` and adjust the necessary configuration.

   ```bash
   cp .env.example .env
   ```

   Key configuration to modify:
    - **Database**: Ensure the `DB_CONNECTION` is set to `sqlite` and set the path to your SQLite database file.
    - **Queue**: Make sure `QUEUE_CONNECTION=database` is enabled in `.env`.

5. **Generate Application Key**

   Generate the Laravel application key:

   ```bash
   php artisan key:generate
   ```

6. **Run Database Migrations**

   Run the migrations to set up database schema:

   ```bash
   php artisan migrate
   ```

7. **Run the Development Server**

   To serve the application locally:

   ```bash
   php artisan serve
   ```

   The application will be served at `http://127.0.0.1:8000`.

8. **Frontend Build and Watch**

   Run the following command for development to build and watch frontend changes:

   ```bash
   npm run dev
   ```

---

## Code Style and Standards

### PHP
Use [Laravel Pint](https://laravel.com/docs/11.x/pint) to ensure the code adheres to Laravel's coding standards. Run the following to check and fix code style:

```bash
./vendor/bin/pint
```

### JavaScript & CSS
Follow the implemented `eslint` and `stylelint` rules (if any). Ensure your JavaScript code and CSS adhere to TailwindCSS and project specifications.

---

## Testing

1. **Backend Tests**

   Be sure all existing tests pass before submitting your changes. Use PHPUnit for testing:

   ```bash
   php artisan test
   ```

2. **Frontend Tests**

   There are no predefined frontend tests, but contributors may choose to add them using preferred testing tools.

---

## Committing and Pushing Changes

1. **Follow Commit Standards**

   Use clear and concise commit messages. For example:
    - `fix: Resolve database migration issue`
    - `feat: Add user profile page`
    - `docs: Update Contributing guidelines`

2. **Pull Requests**

   Once your feature or fix branch is pushed, create a pull request to the repository's main branch with the following:
    - A clear summary of what the PR does.
    - Mention any issues fixed by your PR (e.g., Closes #123).

---

## Need Help?

If you're stuck or have any questions, feel free to reach out via:
- The issues section on GitHub.
- Contacting maintainers directly.

Thank you again for taking the time to contribute! 🎉
