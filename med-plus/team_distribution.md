# Team Work Distribution - Med+ Project

This document outlines the division of tasks for a 6-person development team based on the 6 Core Components of the Med+ project requirements. Each component strictly contains all files (UIs and Java) related to its specific domain, ensuring no overlapping of domain logic.

---

## 👥 1. User Management Component (Member 1)
*   **Focus**: User accounts, profiles, authentication, and user administration.
*   **OOP Concepts Applied**: **Encapsulation** (User data protection), **Interface Implementation** (`UserService`).
*   **UIs Assigned (3)**: 
    *   `auth.jsp` (Login/Register)
    *   `profile.jsp` (User Profile)
    *   `admin_users.jsp` (Admin User List)
*   **Java Files Assigned**:
    *   `User.java`, `Role.java`
    *   `UserRepository.java`
    *   `UserService.java`, `UserServiceImpl.java`
    *   `AuthController.java`, `ProfileController.java`
*   **CRUD Operations (3)**:
    1.  **Create**: Register new customer/staff accounts.
    2.  **Read**: View own profile data & read all users (Admin).
    3.  **Update/Delete**: Update personal profile / Delete users from the system.

---

## 💊 2. Medicine Management Component (Member 2)
*   **Focus**: Medicine catalog, detailed views, and medicine administration.
*   **OOP Concepts Applied**: **Inheritance** (`BaseFileRepository`), **Encapsulation** (`Medicine`).
*   **UIs Assigned (3)**: 
    *   `index.jsp` (Home / Medicine List)
    *   `medicine_details.jsp` (Single Product View)
    *   `admin_medicines.jsp` (Add/Edit Medicine Forms)
*   **Java Files Assigned**:
    *   `Medicine.java`
    *   `MedicineRepository.java`
    *   `MedicineService.java`, `MedicineServiceImpl.java`
    *   `HomeController.java`, `MedicineController.java`
*   **CRUD Operations (3)**:
    1.  **Create**: Admin adds new medicine entries.
    2.  **Read**: Customer browses and searches the medicine catalog.
    3.  **Update/Delete**: Admin edits medicine details/pricing or deletes items.

---

## 🛒 3. Order Management Component (Member 3)
*   **Focus**: All order-related logic, including shopping cart, checkout, and global order views across all roles.
*   **OOP Concepts Applied**: **Composition** (`Order` contains `OrderItem`s), **Polymorphism/Strategy** (`DeliveryMethod.getFee()`).
*   **UIs Assigned (5)**: 
    *   `cart.jsp` (Shopping Cart)
    *   `checkout.jsp` (Checkout Process)
    *   `order_success.jsp` (Order Confirmation)
    *   `admin_orders.jsp` (Global Admin Orders)
    *   `pharmacist_orders.jsp` (Pharmacist Pending Orders)
*   **Java Files Assigned**:
    *   `Order.java`, `OrderItem.java`, `DeliveryMethod.java`
    *   `OrderRepository.java`
    *   `OrderService.java`, `OrderServiceImpl.java`
    *   `CartController.java`, `CheckoutController.java` (And order-related methods in other controllers)
*   **CRUD Operations (3)**:
    1.  **Create**: Add items to cart & Place final order.
    2.  **Read**: View order history (Customer) and view all orders (Admin/Pharmacist).
    3.  **Update**: Pharmacist updates order status (Pending -> Approved/Completed).

---

## 📄 4. Prescription Management Component (Member 4)
*   **Focus**: Secure prescription uploads, customer history, and pharmacist verification.
*   **OOP Concepts Applied**: **Interface Segregation** (`PrescriptionService` handles file I/O operations).
*   **UIs Assigned (3)**: 
    *   `prescription_upload.jsp` (Upload Form)
    *   `prescription_history.jsp` (Customer History)
    *   `prescription_review.jsp` (Pharmacist Verification Panel)
*   **Java Files Assigned**:
    *   `Prescription.java`, `PrescriptionStatus.java`
    *   `PrescriptionRepository.java`
    *   `PrescriptionService.java`, `PrescriptionServiceImpl.java`
    *   `PrescriptionController.java`
*   **CRUD Operations (3)**:
    1.  **Create**: Upload digital prescription files.
    2.  **Read**: View list of uploaded prescriptions.
    3.  **Update**: Pharmacist updates prescription status (Approved/Rejected).

---

## 📊 5. Admin Dashboard & Config Component (Member 5)
*   **Focus**: Main admin dashboard layout, system configurations, and categories.
*   **OOP Concepts Applied**: **Dependency Inversion** (Injecting services via Constructor).
*   **UIs Assigned (3)**: 
    *   `dashboard_admin.jsp` (Main Admin Stats Panel)
    *   `category_management.jsp` (Medicine Categories)
    *   `about.jsp` (System Information)
*   **Java Files Assigned**:
    *   `Category.java`
    *   `CategoryRepository.java`, `BaseFileRepository.java`
    *   `AdminController.java`, `CategoryController.java`, `AboutController.java`
*   **CRUD Operations (3)**:
    1.  **Create**: Add new medicine categories.
    2.  **Read**: View global dashboard statistics.
    3.  **Delete**: Remove categories.

---

## 👨‍⚕️ 6. Pharmacist Panel & Communications Component (Member 6)
*   **Focus**: Pharmacist home layout, quick stock updates, and customer communications.
*   **OOP Concepts Applied**: **Abstraction** (Interacting with complex states through simplified methods).
*   **UIs Assigned (3)**: 
    *   `dashboard_pharmacist.jsp` (Pharmacist Home)
    *   `pharmacist_stock.jsp` (Quick Stock Update View)
    *   `contact.jsp` (Customer Messaging)
*   **Java Files Assigned**:
    *   `OrderStatus.java`, `ContactMessage.java`
    *   `ContactMessageRepository.java`
    *   `PharmacistController.java`, `ContactController.java`
*   **CRUD Operations (3)**:
    1.  **Create**: Customers submit contact messages (Support inquiries).
    2.  **Read**: Pharmacist reads low-stock alerts and messages.
    3.  **Update**: Pharmacist manually updates stock levels from the stock panel.

---
**Contact:** SLIIT, Malabe, Sri Lanka | **Phone:** +94112000000 | **Email:** support@medplus.lk
