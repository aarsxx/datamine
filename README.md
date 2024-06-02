<p align="center">
  <img src="public/tello.svg" alt="Just Do It" width="150">
</p>

<p align="center">
<a href="https://github.com/andikaleonardo/datamine/issues"><img src="https://img.shields.io/github/issues/andikaleonardo/datamine.svg" alt=""></a>
<a href="https://github.com/andikaleonardo/datamine/stargazers"><img src="https://img.shields.io/github/stars/andikaleonardo/datamine.svg" alt=""></a>
<a href="https://github.com/andikaleonardo/datamine/network"><img src="https://img.shields.io/github/forks/andikaleonardo/datamine.svg" alt=""></a>
<a href="https://status.heroku.com"><img src="https://img.shields.io/badge/heroku-status-brightgreen" alt="Heroku Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

<p align="center">
This is a web-based to do list application developed using Laravel, Livewire, and Tailwind CSS. The application allows users to create, manage, and organize their tasks into groups. It offers features such as task grouping, scheduling, and user authentication.
</p>

## Main Features

- User Authentication: Secure system for user login and data protection.
- Task Creation: Create tasks with name, description, due date, and priority.
- Task Groups: Organize tasks into categories (e.g., work, personal).
- Scheduled Tasks: Set tasks to repeat daily, weekly, or monthly.
- Task List: View and manage tasks in a list format.
- Task Status: Mark tasks as completed or pending.
- Responsive UI: Works on various devices and screen sizes.

## Diagram

<p align="center">
  <img src="public/flowchart.svg" alt="flowchart" width="700" height="700">
</p>

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


## Deploying to Heroku
1. Log in to Heroku:
   ```bash
   heroku login
   ```
2. Create a new Heroku application:
   ```bash
   heroku create your-app-name
   ```
3. Add the Heroku Postgres add-on:
   ```bash
   heroku addons:create heroku-postgresql:hobby-dev
   ```
4. Set environment variables in Heroku:
    ```bash
   heroku config:set APP_KEY=$(php artisan key:generate --show)
   heroku config:set APP_ENV=production
   heroku config:set APP_DEBUG=false
   heroku config:set APP_URL=https://your-app-name.herokuapp.com
   heroku config:set ASSET_URL=https://your-app-name.herokuapp.com
   ```
   
5. Add a Procfile to the root of your project to instruct Heroku how to run your app. Create a Procfile file with the following content:
   ```Procfile
   web: vendor/bin/heroku-php-apache2 public/
   ```

6. Commit your changes to git:
   ```bash
   git add .
   git commit -m "Prepare for Heroku deployment"
   ```
   
7. Deploy your application to Heroku:
   ```bash
   git push heroku main
   ```
8. Run database migrations on Heroku:
   ```bash
   heroku run php artisan migrate
   ```
9. Access your application on Heroku:
Open your web browser and go to https://your-app-name.herokuapp.com