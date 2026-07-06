<div align="center">
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel">
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind">
  <img src="https://img.shields.io/badge/Alpine.js-8BC0D0?style=for-the-badge&logo=alpinedotjs&logoColor=white" alt="Alpine">

  <h1>🚀 SwiftShip Platform</h1>
  <p><strong>A Modern Logistics & Delivery Tracking CRM</strong></p>
</div>

<hr>

> **SwiftShip** is a Laravel 11 MVC CRM-style portal designed for managing shipments end-to-end. It features MongoDB-backed Eloquent models, dynamic Chart.js dashboards, live Leaflet tracking maps, real-time broadcast events, and role-based policies.

<br>

## ✨ Key Features

| Feature | Description |
| --- | --- |
| 📊 **Dashboards** | Interactive KPIs, volume/status charts, and live activity feeds. |
| 📦 **Shipment CRM** | Advanced search, filtering, bulk updates, and CSV exports. |
| 🗺️ **Live Tracking** | Leaflet-powered map with real-time auto-refreshing markers and tracking timeline. |
| 👥 **Customer CRM** | Profiles, shipment histories, performance stats, and secure role-based access. |
| 🔔 **Alerts System** | Real-time web-sockets, database notifications, and delayed shipment alerts. |

<br>

## 🛠️ Setup Instructions

To get the project running locally, execute the following commands in your terminal:

```bash
# 1. Install PHP dependencies
composer install

# 2. Setup your environment
cp .env.example .env
php artisan key:generate

# 3. Install NPM dependencies & compile assets
npm install
npm run dev

# 4. Seed the database with sample data
php artisan db:seed

# 5. Start the local server
php artisan serve
```

---

## 🔑 Demo Credentials

Once the server is running, navigate to `http://127.0.0.1:8000` and sign in with the default admin account:

> **Email:** `admin@logistics.test` <br>
> **Password:** `password`

### 🎭 Pre-configured Roles
*All seeded users share the same password: `password`*

- 👑 **Admin**: `admin@logistics.test`
- 💼 **Managers**: `riya.manager@logistics.test`, `arjun.manager@logistics.test`
- 👁️ **Viewers**: `meera.viewer@logistics.test`, `kabir.viewer@logistics.test`

<br>

## ⚡ Realtime & Queues

SwiftShip leverages **Laravel Reverb** for powerful local WebSockets. Run these commands in separate terminal tabs to enable real-time features:

```bash
# Start the WebSocket server
php artisan reverb:start

# Process background jobs
php artisan queue:work

# Run scheduled tasks
php artisan schedule:work
```
*(The scheduler dispatches location updates every minute. Status changes trigger broadcast events, updating the UI instantly!)*

<br>

## 🧩 Optional: Laravel Breeze

This repository includes a minimal Breeze-compatible session controller to run the seeded demo immediately. If you wish to replace it with the full Laravel Breeze authentication scaffolding:

```bash
composer require laravel/breeze --dev
php artisan breeze:install blade
npm install
npm run dev
```

<div align="center">
  <br>
  <sub>Built with ❤️ for modern logistics networks.</sub>
</div>
