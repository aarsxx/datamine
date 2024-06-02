# Datamine To Do list

This is a web-based task management application developed using Laravel, Livewire, and Tailwind CSS. The application allows users to create, manage, and organize their tasks into groups. It offers features such as task grouping, scheduling, and user authentication.
## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#uasage)

## Features

- User Authentication: Secure system for user login and data protection.
- Task Creation: Create tasks with name, description, due date, and priority.
- Task Groups: Organize tasks into categories (e.g., work, personal).
- Scheduled Tasks: Set tasks to repeat daily, weekly, or monthly.
- Task List: View and manage tasks in a list format.
- Task Status: Mark tasks as completed or pending.
- Responsive UI: Works on various devices and screen sizes.

## Prerequisites

Before you start, please install this:

- [PHP](https://www.php.net/) (>=8.3)
- [Laravel](https://laravel.com/) (>=8.8)
- [Composer](https://getcomposer.org/) (>=2.7.5)
- [Node.js](https://nodejs.org/) (>=16.0.0)
- [NPM](https://www.npmjs.com/)
- [Tailwind](https://tailwindcss.com/) (3.3.0)
- [PostgresSQL](https://www.postgresql.org/)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/andikaleonardo/datamine
   ```

2. Navigate to the project directory:

   ```bash
   cd datamine
   ```
3. Update PHP dependencies using Composer:

   ```bash
   composer update
   ```
4. Install PHP dependencies using Composer:

   ```bash
   composer install
   ```

4. Install JavaScript dependencies using NPM:

   ```bash
   npm install
   ```
5. Create a `.env` file by copying `.env.example` and update it with your database configuration:

   ```bash
   cp .env.example .env
   ```
6. Generate application key:

   ```bash
   php artisan key:generate
   ```

7. Make sure `APP_URL` & `ASSET_URL` in `.env` is defined because laravel pointed to those URL.
  
   ```bash
   APP_URL=https://datamine-13120b40742a.herokuapp.com
   ASSET_URL=https://datamine-13120b40742a.herokuapp.com
   ```

8. Migrate the database:

   ```bash
   php artisan migrate
   ```
9. Compile Assets:
 
   ```bash
   npm run dev
   ```

10. Start the Local development server:

   ```bash
   php artisan serve
   ```
11. Access the Application: Open your web browser and go to `http://localhost:8000`

## Usage

![Alt text](/images/example-image.svg)

## Documentation