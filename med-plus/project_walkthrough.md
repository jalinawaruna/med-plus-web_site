# Med+ Project Walkthrough & Class Documentation

This document provides a detailed explanation of how the Med+ system works, broken down by its functional components and Java classes.

## 🚀 Core Application Flow

1.  **Startup**: The `MedPlusApplication.java` launches the Spring Boot context. It initializes all repositories, ensuring the `data/` folder and JSON files exist.
2.  **User Access**: `HomeController.java` serves the landing page. Users can browse medicines before logging in.
3.  **Authentication**: `AuthController.java` manages login/registration. Upon login, the user's role (Admin, Pharmacist, Customer) is stored in the session, determining which dashboard they see.
4.  **Shopping**: Customers add items to a session-based cart. If an item requires a prescription, the system prompts for an upload via `PrescriptionController.java`.
5.  **Order Processing**: `CheckoutController.java` converts the cart into an `Order` object, generates a tracking ID, and saves it via `OrderService.java`.
6.  **Staff Fulfillment**: Pharmacists use `PharmacistController.java` to approve prescriptions and update order statuses. Admins use `AdminController.java` for high-level inventory and user management.

---

## 📂 Layer-by-Layer Class Breakdown

### 1. Controllers (Web Layer)
*   **HomeController**: Manages the main shop view, search filters, and category navigation.
*   **AuthController**: Handles user sessions, password validation, and role assignment.
*   **AdminController**: Provides endpoints for the admin dashboard statistics and management tables.
*   **PharmacistController**: Manages the work queue for staff, including order status transitions.
*   **MedicineController**: Displays individual product details.
*   **Cart/CheckoutControllers**: Handle the logic for purchasing, including delivery method selection (Urgent vs. Normal).
*   **ContactController**: Manages the messaging system and "Coming Soon" doctor channeling portal.

### 2. Models (Data Layer)
*   **BaseModel**: The parent class for all entities, providing UUID generation and timestamps.
*   **User**: Stores credentials and role-based permissions.
*   **Medicine**: Contains product info, price, and prescription requirements.
*   **Order / OrderItem**: Represent a transaction. An Order contains a list of OrderItems.
*   **Prescription**: Holds the metadata and file path for customer-uploaded documents.
*   **ContactMessage**: Represents an inquiry sent via the contact form.

### 3. Repositories (Persistence Layer)
*   **BaseFileRepository**: An abstract generic class that uses Jackson (ObjectMapper) to read/write Java objects to JSON files. It handles the core "FindAll", "FindById", and "Save" operations.
*   **Specific Repositories**: (e.g., `UserRepository`, `MedicineRepository`) Inherit from the base repository and specify the target file (e.g., `data/users.json`).

### 4. Services (Business Logic Layer)
*   **MedicineService**: Handles stock updates and inventory filtering.
*   **OrderService**: Manages the order lifecycle and status workflows.
*   **UserService**: Encapsulates user retrieval and registration logic.
*   **PrescriptionService**: Manages the approval status and file references for prescriptions.

---

## 🛠️ Data Storage (JSON)
Unlike traditional databases, Med+ uses human-readable JSON files in the `/data` directory. This makes the project extremely portable—you can copy the folder to any machine with Java, and it will run without needing a SQL server setup.

*   `users.json`: Security and profile data.
*   `medicines.json`: The "database" of available products.
*   `orders.json`: The history of all customer purchases.
*   `messages.json`: Log of all customer contact inquiries.


---
**Contact:** SLIIT, Malabe, Sri Lanka | **Phone:** +94112000000 | **Email:** support@medplus.lk
