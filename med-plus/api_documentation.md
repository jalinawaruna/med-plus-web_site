# Med+ API Documentation

This document lists the primary URL mappings and endpoints for the Med+ Online Medical Store.

## 🏠 Public Endpoints

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/` | GET | Home page / Medicine catalog (supports `search` & `category` params) |
| `/about` | GET | About Us page |
| `/contact` | GET | Contact page & Doctor Channeling info |
| `/contact/send` | POST | Send a message (Saves to `messages.json`) |
| `/medicine/{id}`| GET | View detailed information for a specific medicine |

## 🔐 Authentication Endpoints

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/auth` | GET | Login and Registration page |
| `/login` | POST | Process user login |
| `/register` | POST | Register a new customer |
| `/logout` | GET | End user session |
| `/profile` | GET | View and edit user profile |

## 🛒 Shopping & Orders

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/cart` | GET | View current shopping cart |
| `/cart/add` | POST | Add medicine to cart (`medicineId`, `quantity`) |
| `/cart/remove` | POST | Remove item from cart |
| `/checkout` | GET | Proceed to checkout |
| `/checkout/place`| POST | Place order (Generates Tracking ID) |

## 📋 Prescription Management

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/prescription/upload` | GET/POST | Upload a digital prescription |
| `/prescription/history`| GET | View own prescription history |

## ⚙️ Admin Endpoints (Admin Role Only)

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/admin/dashboard` | GET | Admin overview and statistics |
| `/admin/medicines` | GET | Manage medicine inventory |
| `/admin/medicines/add`| POST | Add a new medicine |
| `/admin/users` | GET | Manage system users |
| `/admin/orders` | GET | View and manage all system orders |

## 👨‍⚕️ Pharmacist Endpoints (Pharmacist Role Only)

| Endpoint | Method | Description |
| :--- | :--- | :--- |
| `/pharmacist/dashboard` | GET | Pharmacist work queue (Orders/Prescriptions) |
| `/pharmacist/order/status`| POST | Update status of an order |
| `/pharmacist/prescription/review`| POST | Approve/Reject a prescription |

---
## 📄 Data Models (JSON)
*   `users.json`: Stores credentials and user profiles.
*   `medicines.json`: Stores the product catalog.
*   `orders.json`: Stores customer transactions.
*   `prescriptions.json`: Stores uploaded prescription metadata.
*   `messages.json`: Stores contact form submissions.


---
**Contact:** SLIIT, Malabe, Sri Lanka | **Phone:** +94112000000 | **Email:** support@medplus.lk
