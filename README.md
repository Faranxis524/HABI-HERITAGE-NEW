# Habi Heritage

Habi Heritage is a full-stack web application built with Laravel (backend) and React (frontend) to showcase and manage cultural heritage content, including products, storytelling, gallery, fundraising, and donations.

## Features

- User registration and authentication
- Admin dashboard for managing content
- Product catalog
- Storytelling section
- Gallery
- Fundraising campaigns
- Donation system
- Checkout system

## Prerequisites

- PHP 8.1 or higher
- Composer
- Node.js and npm
- MySQL or another database supported by Laravel

## Installation

### Backend Setup

1. Navigate to the backend directory:

    ```bash
    cd backend-habiheritage
    ```

    [View backend code on GitHub](https://github.com/Faranxis524/Habi-Heritage/tree/main/backend-habiheritage)

2. Install PHP dependencies:

   ```bash
   composer install
   ```

3. Copy the environment file and configure it:

   ```bash
   cp .env.example .env
   ```

   Update the `.env` file with your database credentials and other settings.

4. Generate application key:

   ```bash
   php artisan key:generate
   ```

5. Run database migrations:

   ```bash
   php artisan migrate
   ```

6. (Optional) Seed the database:

   ```bash
   php artisan db:seed
   ```

7. Start the Laravel development server:

   ```bash
   php artisan serve
   ```

   The backend will be available at `http://localhost:8000`.

### Frontend Setup

1. Navigate to the frontend directory:

    ```bash
    cd frontend-habiheritage
    ```

    [View frontend code on GitHub](https://github.com/Faranxis524/Habi-Heritage/tree/main/frontend-habiheritage)

2. Install JavaScript dependencies:

   ```bash
   npm install
   ```

3. Start the React development server:

   ```bash
   npm start
   ```

   The frontend will be available at `http://localhost:3000`.

## Usage

- Access the application at `http://localhost:3000`.
- Register as a user or log in.
- Admins can access the dashboard to manage content.

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Commit and push.
5. Create a pull request.

## License

This project is licensed under the MIT License.