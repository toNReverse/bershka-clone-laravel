<p align="center">
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel">
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
</p>

# Bershka Clone – Laravel Version

*A full-featured e-commerce web application inspired by the Bershka website, built with Laravel, Blade, HTML, CSS, JavaScript, and MySQL.*

This project is a complete e-commerce web application inspired by the Bershka website. It is developed using **Laravel**, **Blade templates**, **HTML**, **CSS**, and **JavaScript**, following MVC architecture and using modern tooling for asset compilation and routing.

Originally created as part of a university exam, it has been refactored and enhanced for use as a professional portfolio project.

[![Bershka Clone Screenshot](https://camo.githubusercontent.com/5e3e86b62e1273df64148247f435ed97f36aa4c7bc33ed2db38aa0f81fb52810/68747470733a2f2f692e696d6775722e636f6d2f54576554714f512e6a706567)](https://camo.githubusercontent.com/5e3e86b62e1273df64148247f435ed97f36aa4c7bc33ed2db38aa0f81fb52810/68747470733a2f2f692e696d6775722e636f6d2f54576554714f512e6a706567)

---

## 🌟 Overview

The application replicates a modern fashion e-commerce experience with real-time product search, user authentication, cart and wishlist management, and checkout via Stripe.

It uses Laravel’s MVC structure, Blade templating engine, built-in routing, migration system, and leverages external APIs for translation, currency conversion, and product data retrieval.

---

## ✨ Features

### Frontend
* Fully responsive layout built with HTML5 and CSS3, using Laravel’s frontend tooling.
* Live product search integrated via JavaScript and external APIs.
* Wishlist and cart management through Laravel controllers, API endpoints, and AJAX/Fetch.
* Modal-based cart with dynamic updates.
* Login, registration, password reset via Laravel Auth.
* Layouts and components via Blade templates for reuse and clean UI.

### Backend
* Laravel controllers and routes to manage:
  * Wishlist and cart operations.
  * Product searches via external API.
  * Currency conversion and language translation.
  * Checkout session creation with Stripe.
* Eloquent ORM models and migrations for users, products, wishlist, cart, orders.
* Artisan commands and migration system for infrastructure management.
* Clear separation: `app/Http/Controllers`, `app/Models`, `resources/views`, `routes/web.php`.

---

## 🧱 Laravel Structure Overview

The project follows Laravel’s standard structure:

```text
bershka-laravel/
├── app/
│   ├── Http/
│   │   ├── Controllers/       # Main app logic (CartController, WishlistController, etc.)
│   │   └── Middleware/
│   ├── Models/                # Eloquent models (User, Product, Cart, Wishlist…)
│
├── resources/
│   ├── views/                 # Blade templates
│   │   ├── layouts/           # Main layout files (app.blade.php)
│   │   ├── auth/              # Login, Register, Password Reset
│   │   ├── pages/             # Home, Search, Checkout…
│   │   └── components/        # Reusable Blade components
│   ├── js/                    # JavaScript modules (cart.js, search.js, etc.)
│   └── css/                   # Stylesheets
│
├── routes/
│   ├── web.php                # Web routes (pages)
│   └── api.php                # API endpoints for fetch calls
│
├── database/
│   ├── migrations/            # Table creation scripts
│   └── seeders/               # Sample data
│
├── public/
│   ├── images/                # Product/media assets
│   ├── css/                   # Compiled styles
│   ├── js/                    # Compiled scripts
│   └── index.php
│
├── .env                       # Environment configuration (DB, API keys, etc.)
└── composer.json
```

---

## 🚀 Installation & Setup

Follow these steps to set up the project locally. Ensure you have PHP, Composer, Node.js, and a MySQL database server installed.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/toNReverse/bershka-clone-laravel.git](https://github.com/toNReverse/bershka-clone-laravel.git)
   cd bershka-clone-laravel
   ```

2. **Install PHP dependencies:**
   ```bash
   composer install
   ```

3. **Install NPM dependencies & compile assets:**
   ```bash
   npm install
   npm run build
   ```

4. **Environment Configuration:**
   Copy the example environment file and generate the application key:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Database Setup:**
   Configure your database credentials (e.g., `DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`) in the newly created `.env` file. Then, run the migrations to create the database tables:
   ```bash
   php artisan migrate
   ```
   *(If you have seeders available, you can run `php artisan migrate --seed` to populate the database with sample data).*

6. **Start the local development server:**
   ```bash
   php artisan serve
   ```
   The application will be accessible at `http://localhost:8000`.

---

## ⚙️ Configuration (API Keys)

Before using all features, you must configure the necessary API keys in your `.env` file. **Do not hardcode keys in your PHP or JavaScript files.**

Add the following variables to your `.env` file:

```env
SERPAPI_KEY=your_serpapi_key_here
MYMEMORY_KEY=your_mymemory_key_here
EXCHANGERATE_KEY=your_exchangerate_key_here
STRIPE_PUBLIC_KEY=your_stripe_public_key_here
STRIPE_SECRET_KEY=your_stripe_secret_key_here
```

### API Details

1. **SerpAPI:** Used for product search functionality. Register at [https://serpapi.com](https://serpapi.com).
2. **MyMemory Translation API:** Used to dynamically translate product names and descriptions. Register at [https://mymemory.translated.net/doc/spec.php](https://mymemory.translated.net/doc/spec.php).
3. **ExchangeRate API:** Used to convert product prices to the user’s selected currency. Obtain it from [https://www.exchangerate-api.com](https://www.exchangerate-api.com).
4. **Stripe:** Used to handle payment processing (in test mode). Available in your Stripe dashboard at [https://dashboard.stripe.com/apikeys](https://dashboard.stripe.com/apikeys).

---

## 📄 License

This project is released under the **MIT License**.

You are free to use, modify, and distribute the code for personal or commercial purposes, provided that proper credit is given to the original author.

> © 2025 Marco Sapienza
> 
> This project was originally developed as part of an academic coursework and later refined for portfolio presentation purposes.

For full license details, please refer to the `LICENSE` file included in this repository.
