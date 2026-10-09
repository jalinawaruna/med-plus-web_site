# Future Improvements & Missing Features

While the current version of Med+ is functional, here are some key areas that can be improved or added to make it a production-ready application.

## 1. Security Enhancements
*   **Password Hashing**: Currently, passwords are stored in plain text. Implementing **BCrypt** hashing is critical for user data protection.
*   **Session Security**: Adding a `LoginInterceptor` or using **Spring Security** to prevent unauthorized URL access (e.g., stopping a customer from manually typing `/admin/dashboard`).

## 2. Order & Checkout Logic
*   **Stock Reservation**: Automatically reducing the `stock` count in `medicines.json` as soon as an order is placed.
*   **Dynamic WhatsApp Link**: Enhancing the "Urgent Delivery" button to automatically generate a WhatsApp message containing the real Tracking ID and Order Total.
*   **Payment Integration**: Adding a placeholder or real payment gateway (like Stripe or PayHere) for online transactions.

## 3. Advanced Pharmacist Features
*   **Prescription Rejection Reason**: When a pharmacist rejects a prescription, allow them to provide a reason (e.g., "Illegible handwriting" or "Expired date") which the customer can see.
*   **Digital Signature**: Allowing pharmacists to "sign" an approved order digitally.

## 4. Search & Filtering
*   **Price Filters**: Allowing users to filter medicines by a price range (e.g., Rs. 100 - Rs. 500).
*   **Sorting**: Adding "Sort by Price" or "Sort by Name" options to the home page.
*   **Low Stock Alerts**: Highlighting medicines in the Admin dashboard that have less than 5 units left.

## 5. System Robustness
*   **Concurrency Handling**: Adding `synchronized` blocks to the `BaseFileRepository` to prevent data loss if two users try to save data at the exact same millisecond.
*   **Input Validation**: Adding more strict server-side validation to ensure email formats are correct and prices aren't negative.

## 6. User Experience (UX)
*   **Toast Notifications**: Replacing full-page reloads with "Toast" messages (pop-ups) for actions like "Added to Cart".
*   **Image Uploads**: Allowing admins to upload real images for medicines instead of using icons.
*   **Order Tracking Page**: A dedicated public page where a customer can enter their Tracking ID to see the current status without logging in.


---
**Contact:** SLIIT, Malabe, Sri Lanka | **Phone:** +94112000000 | **Email:** support@medplus.lk
