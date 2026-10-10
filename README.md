# 🏖️ Aira — Short-Term Vacation Rental, Calendar Availability Booking & Host Payout API

![Architecture Banner](./assets/banner.svg)

<p align="center">
  <a href="https://www.postman.com/shahjalal-backend-9458759/shahjalal-api-portfolio" target="_blank">
    <img src="https://run.pstmn.io/button.svg" alt="View in Postman" />
  </a>
  <a href="https://www.postman.com/shahjalal-backend-9458759/shahjalal-api-portfolio" target="_blank">
    <img src="https://img.shields.io/badge/Postman-Instant_Live_API_Docs-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Live API Documentation" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express" />
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white" alt="Stripe" />
  <img src="https://img.shields.io/badge/Hospitality_API-14B8A6?style=for-the-badge&logo=home&logoColor=white" alt="Hospitality_API" />
  
</p>

---

## 📌 Executive Overview

**Aira Backend** (Short-Time Rental Service) is a hospitality and vacation property booking backend engineered with **Node.js, TypeScript, Express, and Prisma ORM**. The platform powers short-term accommodation booking operations: **vacation property listings with amenities and add-on services**, **dynamic calendar day pricing and blackout date availability**, guest reservation state machine, host withdrawal requests with payout tracking, guest reviews, and in-app guest-host messaging.

---

## 🚀 Key Architectural & Domain Capabilities

- **Dynamic Calendar Availability & Rates**: Granular date-by-date pricing (`CalendarDay`) allowing seasonal surcharges and custom booking rules.
- **Add-On Service Bookings**: Guests can reserve supplemental amenities (`AddOn`, `PropertyAddOn`) such as airport transfers and private chef services.
- **Host Withdrawal & Financial Balance**: Automated commission deduction, host payout ledger (`HostWithdrawal`), and payout approvals.
- **Guest-Host Real-Time Messaging**: Built-in communication channels (`Room`, `Message`) facilitating guest inquiries and check-in instructions.
- **Verified Guest Reviews & Favorites**: Post-stay rating submissions with host response management and guest property bookmarks.

---

## 📬 API Documentation & Interactive Postman Collection

The complete REST API specification is published in our public Postman showcase workspace:

* 🌐 **Instant Live API Documentation**: [Explore aira_backend in Postman (Instant Web View)](https://www.postman.com/shahjalal-backend-9458759/shahjalal-api-portfolio)

### Core Endpoint Modules

| Module | Base Route | Key Capabilities |
|---|---|---|
| **Authentication** | `/api/v1/auth` | Guest and host onboarding, JWT authentication, role guards |
| **Properties & Listings** | `/api/v1/property` | Manage vacation rental properties, photo galleries, amenity specs |
| **Calendar & Availability** | `/api/v1/calendarDay` | Day-by-day availability toggles, seasonal pricing adjustments |
| **Bookings & Add-Ons** | `/api/v1/booking` | Guest stay reservations, add-on service billing, check-in state machine |
| **Host Payouts** | `/api/v1/hostWithdrawal` | Host revenue ledger, withdrawal requests, payment settlement logs |
| **Messaging** | `/api/v1/room` | In-app communication channel between guests and property hosts |

---

## 📂 Project Architecture

```plaintext
aira_backend/
├── assets/
│   └── banner.svg               # Architectural visual banner
├── src/
│   ├── app/
│   │   ├── middlewares/         # Global error handlers, auth & validation guards
│   │   ├── modules/             # Domain feature modules (Property, Calendar, Booking)
│   │   └── routes/              # Centralized route registration
│   ├── config/                  # Environment & external service configurations
│   └── server.ts                # Application bootstrapper
├── prisma/
│   └── schema.prisma            # Prisma database schema definition
├── .env.example                 # Sanitized environment template
├── package.json
└── tsconfig.json
```

---

## 🛠️ Quickstart & Local Setup

### Prerequisites
* **Node.js**: `v20.x` or higher
* **Database**: PostgreSQL

### 1. Clone & Install Dependencies
```bash
git clone https://github.com/shahjalal-labs/aira_backend.git
cd aira_backend
npm install
```

### 2. Configure Environment Variables
```bash
cp .env.example .env
```

### 3. Generate Prisma Client
```bash
npx prisma generate
```

### 4. Run Development Server
```bash
npm run dev
```

---

## 👨‍💻 Engineering & Authorship

Developed and engineered by **Md. Shahjalal**.

* **GitHub**: [@shahjalal-labs](https://github.com/shahjalal-labs)
* **Email**: [muhommodshahjalal@gmail.com](mailto:muhommodshahjalal@gmail.com)

---

## 📄 License

This project is licensed under the [ISC License](LICENSE).
