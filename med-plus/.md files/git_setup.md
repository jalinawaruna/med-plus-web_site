# GitHub Setup Guide for Med+ Team

Follow these steps to initialize your repository and set up the working branches for your 6-person team.

## 1. Initial Setup (For the Lead)

Open your terminal in the `med-plus` folder and run:

```bash
# Initialize git
git init

# Add all files (respects the .gitignore we created)
git add .

# Initial commit
git commit -m "Initial commit: Med+ Project Baseline"

# Add your GitHub repository link (Replace the URL with your actual repo link)
git remote add origin https://github.com/YOUR_USERNAME/med-plus.git

# Push the main branch
git branch -M main
git push -u origin main
```

## 2. Creating Team Branches

Run these commands to create and push dedicated branches for each team member. This allows everyone to work independently:

```bash
# Member 1: Authentication & Users
git checkout -b feature/auth-management
git push -u origin feature/auth-management

# Member 2: Medicine & Inventory
git checkout -b feature/medicine-inventory
git push -u origin feature/medicine-inventory

# Member 3: Orders & Checkout
git checkout -b feature/order-management
git push -u origin feature/order-management

# Member 4: Prescription System
git checkout -b feature/prescription-system
git push -u origin feature/prescription-system

# Member 5: Admin Dashboard
git checkout -b feature/admin-dashboard
git push -u origin feature/admin-dashboard

# Member 6: Pharmacist Panel
git checkout -b feature/pharmacist-panel
git push -u origin feature/pharmacist-panel

# Return to main branch
git checkout main
```

## 3. Workflow for Team Members

Each member should follow this process to get their work into the project:

1.  **Clone the repo**: `git clone https://github.com/YOUR_USERNAME/med-plus.git`
2.  **Switch to their branch**: `git checkout feature/your-assigned-branch`
3.  **Work and Commit**:
    *   `git add .`
    *   `git commit -m "Added login validation logic"`
4.  **Push to GitHub**: `git push origin feature/your-assigned-branch`
5.  **Merge to Main**: When a feature is ready, create a **Pull Request (PR)** on GitHub from your branch to `main`.

## ⚠️ Important Tips
*   **Never push directly to `main`** after the initial setup.
*   **Pull before you push**: Always run `git pull origin main` into your branch to stay updated with other members' work.


---
**Contact:** SLIIT, Malabe, Sri Lanka | **Phone:** +94112000000 | **Email:** support@medplus.lk
