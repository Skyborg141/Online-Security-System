# Online Security System

A PHP-based e-commerce web application for buying home and office security products. The platform allows customers to browse, search, and purchase security equipment such as CCTV cameras, digital lockers/vaults, and bundled packages — with a full admin panel for managing products and orders.

---

## Features

### Customer Side
- **Homepage** — image carousel, product category cards (CCTV, Digital Locker, Packages, Store locator), and a "Products You Might Like" section showing up to 8 items
- **Product listing & search** — browse products by category via `search.php`
- **Product detail page** — shows product image, title, description, price, brand, stock status, quantity selector, and delivery info (free delivery for orders ৳200+, otherwise ৳40)
- **Shopping cart** — add/remove items, view quantity and per-item price, clear cart, item stock status indicator
- **Checkout** — two payment options: standard checkout (`final.php`) and bKash mobile payment (`final1.php`)
- **User authentication** — sign up (`signUp.php`), login (`login.php`), and logout (`logout.php`) with PHP session management
- **Delivery address** — logged-in users see their saved address on the product detail page

### Admin Side
- Separate admin login panel (`admin/login.php`)
- Product and order management via the `admin/` module

### Pricing Model
- Prices are listed **per day** (rental/service model for security equipment)
- Package deals offer up to **70% discount**; admin refunds the discount amount manually

---

## Tech Stack

- **Backend** — PHP (server-side scripting, session handling, MySQL queries)
- **Database** — MySQL (schema in the `SQL/` folder)
- **Frontend** — HTML, CSS, Bootstrap 3, jQuery
- **Payment** — bKash integration (mobile payment, Bangladesh)
- **Server** — Apache via XAMPP / WAMP (local) or any PHP-compatible web host

---

## Project Structure

```
├── SQL/                  # Database schema and seed data
├── admin/                # Admin panel (login, product/order management)
├── images/               # Product and UI images
├── includes/             # Shared PHP partials
│   ├── head.php          # HTML head, CSS/JS includes
│   ├── header.php        # Navigation header
│   ├── footer.php        # Footer
│   └── functions.php     # Core functions (DB queries, cart, auth)
├── index.php             # Homepage
├── product.php           # Product detail page
├── search.php            # Product search/filter by category
├── cart.php              # Shopping cart
├── final.php             # Checkout / order placement
├── final1.php            # bKash payment page
├── login.php             # User login
├── logout.php            # Session logout
├── signUp.php            # User registration
├── index.css             # Homepage styles
├── style.css             # Global styles
└── README.md
```

---

## Getting Started

### Prerequisites

- PHP 7.4+
- MySQL 5.7+
- XAMPP, WAMP, or any Apache+PHP+MySQL stack

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Skyborg141/Online-Security-System.git
   ```

2. **Move to your server's web root**
   ```bash
   # For XAMPP on Windows
   move Online-Security-System C:\xampp\htdocs\

   # For Linux
   cp -r Online-Security-System /var/www/html/
   ```

3. **Import the database**
   - Open **phpMyAdmin** at `http://localhost/phpmyadmin`
   - Create a new database (e.g. `security_system`)
   - Import the SQL file from the `SQL/` folder

4. **Configure the database connection**
   - Open `includes/functions.php`
   - Update the DB credentials (`host`, `username`, `password`, `database name`) to match your local setup

5. **Run the app**
   - Start Apache and MySQL from XAMPP/WAMP Control Panel
   - Visit `http://localhost/Online-Security-System/`

---

## Default Access

| Role  | URL |
|-------|-----|
| Customer | `http://localhost/Online-Security-System/` |
| Admin | `http://localhost/Online-Security-System/admin/login.php` |

---

## License

This project does not currently include a license file.
