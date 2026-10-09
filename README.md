# 🏥 Med-Plus — Online Pharmacy & Prescription Management System

**A Spring Boot-based web application for online medicine shopping, prescription management, and pharmacy operations.**

Med-Plus is a web-based pharmacy management system designed to simplify medicine browsing, online ordering, prescription submissions, and pharmacy inventory management. The application provides separate functionalities for Customers, Pharmacists, and Administrators through a user-friendly JSP-based interface.

## ✨ Key Features

### 👤 User Authentication & Management
- User registration and login.
- Role-based access for Customers, Pharmacists, and Administrators.
- Separate dashboards and functionalities based on user roles.

### 💊 Medicine Catalog
- Browse available medicines and categories.
- View medicine descriptions, prices, and stock availability.
- Manage medicine information and category details.

### 📋 Prescription Management
- Upload prescriptions for pharmacist review.
- Review submitted prescription requests.
- Process prescriptions and convert eligible requests into orders.

### 🛒 Shopping Cart & Checkout
- Add medicines to the shopping cart.
- Manage cart items before checkout.
- Select available delivery methods.
- Place and manage medicine orders.

### 📦 Pharmacy & Inventory Management
- Manage medicine stock and inventory.
- Monitor customer orders.
- Update order fulfillment statuses.
- Support pharmacy operations through dedicated dashboards.

### 🛡️ Admin Dashboard
- Manage user accounts.
- Monitor orders across the system.
- Oversee medicine catalog and pharmacy operations.

### 💬 Customer Support
- Contact page for customer inquiries.
- About page with information about the application.
- Message management functionality.

## 🛠️ Technology Stack

| Component | Technologies |
|---|---|
| Backend | Java, Spring Boot, Spring MVC |
| Frontend | JSP, HTML5, CSS3, JavaScript |
| Styling | Custom CSS (`style.css`) |
| Data Storage | JSON file-based persistence |
| Build Tool | Maven |
| Application Architecture | Controller, Model, Repository, Service layers |
| Version Control | Git and GitHub |

## 🏗️ Project Structure

```text
med-plus/
├── .github/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/medplus/
│       │       ├── controller/
│       │       ├── model/
│       │       ├── repository/
│       │       ├── service/
│       │       └── MedPlusApplication.java
│       ├── resources/
│       │   ├── application.properties
│       │   └── static/
│       │       └── css/
│       └── webapp/
│           └── WEB-INF/
│               └── jsp/
├── data/
│   ├── categories.json
│   ├── medicines.json
│   ├── users.json
│   ├── orders.json
│   ├── prescriptions.json
│   └── messages.json
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md
```

*Note: The structure above represents the main application components. Actual files and folders may vary.*

## ⚙️ Getting Started

Follow the instructions below to run Med-Plus on your local machine.

### Prerequisites

Make sure you have the following installed:

- **Java JDK 17 or higher**
- **Git**
- An IDE such as IntelliJ IDEA (recommended)
- Maven, or use the Maven Wrapper included in the project

### 1. Clone the Repository

```bash
git clone https://github.com/jalinawaruna/med-plus-web_site.git
```

### 2. Navigate to the Project Directory

```bash
cd med-plus-web_site
```

If the repository contains a nested application directory, navigate into the directory containing the `pom.xml` file.

### 3. Run the Application

**Windows — Command Prompt or PowerShell**

```bash
mvnw.cmd spring-boot:run
```

If the Maven Wrapper is not available or cannot run, use:

```bash
mvn spring-boot:run
```


Alternatively, open the project in IntelliJ IDEA, allow Maven dependencies to load, and run the `MedPlusApplication` main class.

### 4. Access the Application

Once the application starts successfully, open your browser and visit:

**http://localhost:8080**

If a different port is configured in `application.properties`, use that port instead.

## 👥 User Guide

### Customer
1. Register a new account or log in.
2. Browse medicine categories and available products.
3. Upload a prescription when required.
4. Add medicines to the shopping cart.
5. Select a delivery method and place an order.
6. Access the available customer support features.

### Pharmacist
1. Log in using a pharmacist account.
2. Review submitted prescription requests.
3. Manage medicine inventory and stock.
4. Process orders and update fulfillment statuses.

### Administrator
1. Log in using an administrator account.
2. Manage user accounts and medicine catalog information.
3. Monitor customer orders.
4. Oversee pharmacy management activities.

## 💾 Data Storage

Med-Plus uses JSON files for data persistence instead of a traditional relational database.

The application stores data in files such as:

- `categories.json` — Medicine categories.
- `medicines.json` — Medicine records.
- `users.json` — User information.
- `orders.json` — Order information.
- `prescriptions.json` — Prescription records.
- `messages.json` — Customer messages.

The application requires appropriate read and write permissions for the data directory. Keep sensitive user information and real prescription data out of public repositories.

## 🔐 Security Considerations

- Role-based access should be enforced on the server side.
- Passwords should be securely hashed rather than stored as plain text.
- Uploaded prescription files should be validated and protected from unauthorized access.
- Sensitive configuration and personal data should not be committed to GitHub.
- JSON file-based persistence is suitable for a learning project, but concurrent writes and data integrity should be considered before production use.

## 🚀 Future Enhancements

- Integration with a relational database such as MySQL or PostgreSQL.
- Online payment gateway integration.
- Email notifications for orders and prescriptions.
- Medicine expiry-date monitoring and low-stock alerts.
- Advanced medicine search and filtering.
- Improved reporting and analytics.
- Enhanced security and deployment support.

## 🎯 Project Objectives

- Simplify online medicine ordering.
- Improve prescription submission and review workflows.
- Organize pharmacy inventory and order management.
- Provide role-specific functionality for Customers, Pharmacists, and Administrators.
- Demonstrate practical web development using Java and Spring Boot.

## 🤝 Contributing

Contributions, bug reports, and feature suggestions are welcome. Feel free to open an issue or submit a pull request to help improve the project.

---

**Med-Plus — Making Online Pharmacy Management Simpler.** 💊
