# FintechFlow — Personal Finance & Loan Manager

## Project Description
FintechFlow is a comprehensive personal finance management application designed to help users track their digital wallet, manage micro-loans, and monitor transaction histories. Built with a React frontend and a Node.js/Express backend, it features a sophisticated "Natural Tones" aesthetic for a premium fintech experience.

### Key Features
- **Wallet Management**: Deposit and withdraw funds with real-time balance updates.
- **Transaction History**: Comprehensive log of all credits and debits with filtering capabilities.
- **Micro-Loan System**: Multi-step application process with purpose tracking and automated status updates.
- **EMI Calculator**: Built-in tool to calculate monthly installments and interest for planned loans.
- **Responsive Design**: Fully mobile-friendly layout with smooth animations and transitions.

---

## Student Information
**Name:** Yumna  
**Roll No:** 23i4518

---

## How to Run Locally

### Prerequisites
- [Node.js](https://nodejs.org/) (Compatible with v18+)
- npm (comes with Node.js)

### Installation & Setup
1. **Clone/Download**: Extract the project files to your local machine.
2. **Open Terminal**: Navigate to the project root directory.
3. **Install Dependencies**:
   ```bash
   npm install --legacy-peer-deps
   ```
4. **Environment Configuration**:
   - Create a `.env` file in the root directory (copy from `.env.example`).
   - Note: Since this app uses in-memory storage, no database setup is required.

### Running the App
- **Option 1: Using VS Code (Recommended)**
  - Open the project in VS Code.
  - Go to the **Run and Debug** tab (`Ctrl+Shift+D`).
  - Select **"Launch FintechFlow"** and press **F5**.

- **Option 2: Using Terminal**
  ```bash
  npm run dev
  ```
- The application will be accessible at: [http://localhost:3000](http://localhost:3000)

---

## API Documentation

The backend exposes the following RESTful endpoints:

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| **GET** | `/api/wallet` | Fetch current wallet balance and owner details. |
| **POST** | `/api/wallet/deposit` | Add funds to the wallet. (Body: `{amount}`) |
| **POST** | `/api/wallet/withdraw` | Withdraw funds from the wallet. (Body: `{amount}`) |
| **GET** | `/api/transactions` | Retrieve all transactions. Supports `?type=credit/debit` filtering. |
| **GET** | `/api/loans` | Get a list of all loan applications. |
| **POST** | `/api/loans/apply` | Submit a new loan application. |
| **PATCH** | `/api/loans/:id/status` | Update loan status (approved/rejected). |
| **GET** | `/api/emi-calculator` | Calculate EMI values. (Params: `principal`, `annualRate`, `months`) |

---

## Deployment
This app is ready for deployment to Cloud Run. Ensure `NODE_ENV` is set to `production` to serve optimized static files.
