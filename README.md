# ðŸ…¿ï¸ PARKLINK â€“ Smart Parking Marketplace for Transport Vehicles

> A complete full-stack web application connecting transport vehicle operators (trucks, trailers, buses, EV delivery fleets) with landowners offering secure vacant land.

---

## ðŸŒŸ Key Features

- ðŸšš **Vehicle & EV Selection**: Choose from 10 commercial vehicle types with specialized EV options (AC, 120kW DC Fast Charging, Battery Swapping).
- ðŸ—ºï¸ **Interactive OpenStreetMap**: Real-time Leaflet map visualization with live parking coordinates, markers, and price popups.
- âš¡ **Filter Engine**: Instant search by city, vehicle clearance, price slider, armed guard presence, CCTV, and covered parking.
- ðŸ“… **Conflict-Free Booking Engine**: Automatic duration-based fare calculator and database-level double-booking prevention.
- ðŸ” **Multi-Role Portals (RBAC)**:
  - **Vehicle Owner / Driver**: Book spaces, view active passes, manage vehicle fleet, track confirmations.
  - **Landowner**: List plots with image uploads, approve/reject driver booking requests, monitor revenue and bank payouts.
  - **Super Admin**: Platform statistics, user moderation (block/unblock), parking listing moderation.
- ðŸ›¡ï¸ **Enterprise Security**: Bcrypt password hashing, JWT authorization, prepared SQL queries, and role verification.
- ðŸ”„ **Dual-Mode Architecture**: Works seamlessly with full Node.js + MySQL backend, while also providing built-in fallback data for instant browser/Live Server evaluation.

---

## ðŸ› ï¸ Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend** | HTML5, Modern CSS3 (Variables, Grid, Flexbox), Vanilla JavaScript |
| **Maps** | Leaflet.js, OpenStreetMap (OSM) Tiles |
| **Backend** | Node.js, Express.js, Multer (File Uploads), CORS, Dotenv |
| **Database** | MySQL (`parklink_db`), `mysql2/promise` Connection Pool |
| **Security** | Bcrypt.js, JSON Web Tokens (JWT) |

---

## ðŸš€ Quick Start Guide

### 1. Import Database (MySQL)
Open phpMyAdmin or MySQL Workbench and import `database/parklink.sql`:
```bash
mysql -u root -p < database/parklink.sql
```

### 2. Start Backend Server
```bash
cd backend
npm install
npm start
```
The server will run at `http://localhost:5000`.

### 3. Open the Frontend
- Open `http://localhost:5000/index.html` in your browser.
- Or open `frontend/index.html` using the **VS Code Live Server** extension.

---

## ðŸ” Accounts

The database script creates the schema without preconfigured users or demo credentials. Register an account through the application to get started. Configure administrative accounts securely for your own environment.

---

## ðŸ“‚ Project Structure

```
parklink/
â”œâ”€â”€ backend/
â”‚   â”œâ”€â”€ config/db.js              # MySQL connection pool
â”‚   â”œâ”€â”€ controllers/              # Auth, Parking, Booking, User, Admin logic
â”‚   â”œâ”€â”€ middleware/               # JWT verification & Multer upload handling
â”‚   â”œâ”€â”€ routes/                   # Express API routes
â”‚   â”œâ”€â”€ uploads/                  # Uploaded parking photos
â”‚   â”œâ”€â”€ server.js                 # Express server entry point
â”‚   â”œâ”€â”€ package.json
â”‚   â””â”€â”€ .env
â”œâ”€â”€ database/
â”‚   â””â”€â”€ parklink.sql              # Database schema (10 tables)
â”œâ”€â”€ frontend/
â”‚   â”œâ”€â”€ css/style.css             # Unified modern theme
â”‚   â”œâ”€â”€ js/                       # API wrapper, auth, maps, booking, dashboard
â”‚   â”œâ”€â”€ index.html                # Modern Home page
â”‚   â”œâ”€â”€ vehicle.html              # Vehicle & EV selection
â”‚   â”œâ”€â”€ parking.html              # Parking search & Leaflet map
â”‚   â”œâ”€â”€ parking-details.html      # Parking details & reviews
â”‚   â”œâ”€â”€ booking.html              # Reservation & price breakdown
â”‚   â”œâ”€â”€ dashboard.html            # Multi-role dashboard
â”‚   â”œâ”€â”€ login.html & register.html
â”‚   â”œâ”€â”€ about.html, services.html, how-it-works.html, contact.html
â”œâ”€â”€ docs/
â”‚   â”œâ”€â”€ SETUP_GUIDE.md            # Step-by-step setup in VS Code & MySQL
â”‚   â”œâ”€â”€ API_DOCUMENTATION.md      # Full REST API specification
â”‚   â””â”€â”€ PROJECT_REPORT_VIVA.md    # College project synopsis & Top 20 Viva Q&A
â””â”€â”€ README.md
```

---

## ðŸ“„ Documentation & Evaluation Materials

- ðŸ“˜ [Setup & Installation Guide](docs/SETUP_GUIDE.MD)
- ðŸ“‘ [REST API Reference](docs/API_DOCUMENTATION.MD)
- ðŸŽ“ [College Project Report & Viva Voce Q&A](docs/PROJECT_REPORT_VIVA.MD)

