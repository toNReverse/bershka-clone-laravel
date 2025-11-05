<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

# Bershka Clone – Laravel Version

*A full-featured e-commerce web application inspired by the Bershka website, built with Laravel, Blade, HTML, CSS, JavaScript and MySQL.*

This project is a complete e-commerce web application inspired by the Bershka website.  
It is developed using **Laravel**, **Blade templates**, **HTML**, **CSS**, and **JavaScript**, following MVC architecture and using modern tooling for asset compilation and routing.  
Originally created as part of a university exam, it has been refactored and enhanced for use as a professional portfolio project.

![Bershka Clone Screenshot](https://i.imgur.com/TWeTqOQ.jpeg)

---

## Overview

The application replicates a modern fashion e-commerce experience with real-time product search, user authentication, cart and wishlist management, and checkout via Stripe.  
It uses Laravel’s MVC structure, Blade templating engine, built-in routing, migration system, and leverages external APIs for translation, currency conversion, and product data retrieval.

---

## Features

### Frontend
- Fully responsive layout built with HTML5 and CSS3, using Laravel’s frontend tooling.  
- Live product search integrated via JavaScript and external APIs.  
- Wishlist and cart management through Laravel controllers, API endpoints and AJAX/Fetch.  
- Modal-based cart with dynamic updates.  
- Login, registration, password reset via Laravel Auth.  
- Layouts and components via Blade templates for reuse and clean UI.

### Backend
- Laravel controllers and routes to manage:
  - Wishlist and cart operations.  
  - Product searches via external API.  
  - Currency conversion and language translation.  
  - Checkout session creation with Stripe.  
- Eloquent ORM models and migrations for users, products, wishlist, cart, orders.  
- Artisan commands and migration system for infrastructure management.  
- Clear separation: `app/Http/Controllers`, `app/Models`, `resources/views`, `routes/web.php`.
---

## 🧱 Laravel Structure Overview

The project follows Laravel’s standard structure:


```bash
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

# Configuration

Before running the project, make sure to properly configure the API keys and parameters required for external features to work.

### API Keys

The project uses several external APIs for product search, automatic translation, currency conversion, and payment processing.  
All keys must be manually set within the corresponding PHP or JavaScript files, as indicated in the code.

#### 1. SerpAPI
- Used for product search functionality.  
- Requires a variable named SERPAPI_KEY containing your private API key.  
- You can obtain it by registering at [https://serpapi.com](https://serpapi.com).

#### 2. MyMemory Translation API
- Used to dynamically translate product names and descriptions.  
- Requires a variable MYMEMORY_KEY (optional, but recommended to avoid request limits).  
- Register at [https://mymemory.translated.net/doc/spec.php](https://mymemory.translated.net/doc/spec.php) to obtain your key.

#### 3. ExchangeRate API
- Used to convert product prices to the user’s selected currency.  
- Set the variable EXCHANGERATE_KEY with your personal API key.  
- You can obtain it from [https://www.exchangerate-api.com](https://www.exchangerate-api.com).

#### 4. Stripe
- Used to handle payment processing (in test mode).  
- Requires two keys:
  - STRIPE_SECRET_KEY
  - STRIPE_PUBLIC_KEY  
- Both are available in your Stripe dashboard at [https://dashboard.stripe.com/apikeys](https://dashboard.stripe.com/apikeys).

---
## License

This project is released under the **MIT License**.  
You are free to use, modify, and distribute the code for personal or commercial purposes, provided that proper credit is given to the original author.

> © 2025 Marco Sapienza  
> This project was originally developed as part of an academic coursework and later refined for portfolio presentation purposes.

For full license details, please refer to the [LICENSE](LICENSE) file included in this repository.
