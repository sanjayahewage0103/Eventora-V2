# Eventora V2

Eventora is an event management platform built with **PHP (OOP, MVC)** and **HTML/CSS/JS**.  
It supports three roles:

- **Users (Attendees)** → register/login, search events, view details, buy tickets, manage profile, booking history.
- **Organizers** → create/manage events, schedule, ticket categories, track sales, validate tickets, view revenue.
- **Admins** → approve/promote events, manage users, view total/separate revenues, handle inquiries, oversee the platform.

---

## 🚀 Tech Stack

- **Backend**: PHP 8+ (MVC pattern, OOP, SOLID principles)
- **Frontend**: HTML5, CSS3, JavaScript
- **Database**: MySQL
- **Server**: Apache (WAMP/LAMP stack)

---

## 📂 Folder Structure

```
eventora/
├─ public/                  # Entry point (index.php), assets served here
├─ app/                     # MVC application code
│  ├─ Core/                 # Core classes (Router, Controller, View, etc.)
│  ├─ Controllers/          # Application controllers (Admin, Organizer, User)
│  ├─ Models/               # Database models (User, Event, Ticket, etc.)
│  ├─ Repositories/         # Data access layer
│  ├─ Services/             # Business services (Payment, Email, etc.)
│  ├─ Middlewares/          # Auth & role checks
│  └─ Views/                # Templates (auth, events, tickets, admin, organizer)
├─ config/                  # App & database configuration
├─ database/                # Migrations and seeds
├─ resources/               # Source CSS/JS/images
├─ storage/                 # Logs, cache, uploads
├─ tests/                   # PHPUnit tests
└─ vendor/                  # Composer dependencies
```

---

## ⚙️ Setup (Local WAMP/LAMP)

1. **Clone the repo:**
   ```bash
   git clone https://github.com/sanjayahewage0103/Eventora-V2.git
   cd Eventora-V2
   ```

2. **Install dependencies:**
   ```bash
   composer install
   ```

3. **Copy `.env.example` to `.env` and update DB credentials:**
   ```env
   DB_HOST=127.0.0.1
   DB_NAME=eventora
   DB_USER=root
   DB_PASS=
   ```

4. **Import migrations into MySQL:**
   ```bash
   mysql -u root -p eventora < database/migrations/your_migration.sql
   ```

5. **Start server:**
   - If using WAMP → put project in `www/` and visit `http://localhost/Eventora-V2/public`
   - If using PHP built-in server:
     ```bash
     php -S localhost:8000 -t public
     ```

---

## 🔧 Development

- **Framework**: Custom PHP MVC framework
- **Database**: MySQL with custom ORM-like repository pattern
- **Authentication**: Session-based with role management
- **Payment**: Integration ready for payment gateways
- **Testing**: PHPUnit for unit and integration tests

---

## 📝 Features

### For Users (Attendees)
- User registration and authentication
- Browse and search events
- Event details and ticket purchasing
- Profile management
- Booking history and ticket management

### For Organizers  
- Event creation and management
- Ticket categories and pricing
- Sales tracking and analytics
- Ticket validation system
- Revenue reporting

### For Admins
- Platform oversight and management
- Event approval and promotion
- User management
- Revenue analytics (total and per organizer)
- Inquiry and support management

---

## 🚀 Getting Started

1. Ensure you have PHP 8+, MySQL, and Apache running
2. Follow the setup instructions above
3. Access the application at your configured URL
4. Register as a user or use admin credentials to get started

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
