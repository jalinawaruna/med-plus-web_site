**Project name** \- Online Medical Store (Med+ / Med Plus)

**User types**

* Admin  
* Customers  
* Pharmacists

**Components** 

1. User management  
2. Medicine management  
3. Order management  
4. Prescription management  
5. Admin dashboard  
6. Pharmacist panel  
   

**1\. User Management**

* UIs  
  * Login/ Register Page  
  * User Profile Page  
  * User List Page (admin only)  
* CRUD  
  * Customer  
    * Create account  
    * Read own profile  
    * Update own profile  
  * Admin  
    * Read all users  
    * Update users (optional)  
    * Delete users (optional)

**2\. Medicine Management**

* UIs  
  * Medicine List Page  
  * Medicine Details Page  
  * Add Medicine Form  
  * Edit Medicine Form  
* CRUD  
  * Admin  
    * Create medicine  
    * Read medicines  
    * Update medicine  
    * Delete medicine  
  * Customer  
    * Read medicines only

**3\. Order Management**

* UIs  
  * Cart Page  
  * Checkout Page  
  * My Orders Page  
  * Order Details Page  
* CRUD  
  * Customer  
    * Add to cart  
    * Place order  
    * View orders  
  * Pharmacist  
    * Update order status (PENDING / APPROVED / REJECTED / COMPLETED)

**4\. Prescription Management**

* UIs  
  * Upload Prescription Page  
  * Prescription Review Page  
  * Prescription Details Page  
* CRUD  
  * Customer  
    * Upload prescription  
    * View own prescriptions  
  * Pharmacist  
    * Read prescriptions  
    * Approve / Reject prescription

**5\. Admin Dashboard**

* UI Sections  
  * Statistics cards  
    * total users  
    * total medicines  
    * total orders  
  * User Management Table  
  * Medicine Management Table  
  * Pharmacist Management Table  
* CRUD  
  * Add pharmacist  
  * View everything  
  * Manage inventory

**6\. Pharmacist Panel**

* UI Sections  
  * Pending prescriptions table  
  * Pending orders table  
  * Medicine stock view  
* CRUD  
  * Approve prescriptions  
  * Reject prescriptions  
  * Update order status  
  * View medicines

**Extra Features**

* Logout  
* Search medicines  
* Medicine categories  
* Prescription-required medicines  
* Stock tracking  
* Order status workflow  
* Expiry dates (optional)  
* Low stock warning (optional)

**Rules**

* Prescription-required medicines need pharmacist approval   
* Customer cannot place order if stock unavailable   
* Expired medicines cannot be ordered   
* Only admins can add medicines  
* Only pharmacists can approve prescriptions  
* All the users share the same login and signup page  
  * After login,  
    * Admin → Admin dashboard  
    * Pharmacist → Pharmacist panel  
    * Customer → Home page	  
* First page is the home page not the login or signup page  
* User can select either urgent or normal delivery method before placing order  
  * Urgent → has to pay more  
    * Direct to whatsapp for faster communication and also provide orderID  
  * Normal only delivery fee  
* Users must log in before placing orders, uploading prescriptions, or accessing dashboards.  
* Each order is assigned a unique tracking ID  
* Customers can select medicine quantity before adding to cart


  

**Sample workflow**  
→ Customer visits home page  
→ Browse/search medicines  
→ Add medicines to cart  
→ If prescription-required medicine exists:  
      upload prescription  
→ Select delivery method  
      \- Normal  
      \- Urgent  
→ Place order  
→ Pharmacist reviews prescription/order  
→ Approve/reject  
→ Customer views status using tracking ID  
→ Urgent orders redirect to WhatsApp for faster communication

**Technologies**

* Java, Spring Boot ← Back end  
* JSP/CSS, JavaScript (for UI enhancements) ← Front end  
* File handling (text files) ← Data storage  
* Maven ← Build tool

**Colors and fonts**

* Primary Blue: \#2D9CDB  
* Success Green: \#27AE60  
* Background: \#F8FAFC  
* Text Dark: \#1F2937


| Element | Color |
| :---- | :---- |
| Navbar | Medical blue |
| Buttons | Green/Blue |
| Success | Green |
| Warning | Orange |
| Error | Red |
| Background | Very light gray/white |
| Cards | White |

* font-family: 'Poppins', sans-serif;

| Element | Size |
| ----- | ----- |
| Main heading | 32px |
| Section title | 24px |
| Card title | 18px |
| Normal text | 14–16px |
| Small labels | 12px |

