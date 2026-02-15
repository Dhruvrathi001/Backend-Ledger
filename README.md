```markdown
# 🏦 Backend Ledger – Banking Transaction Engine

A secure and scalable **Node.js + Express + MongoDB** backend designed to simulate real-world banking operations.  
This project implements core financial flows including **authentication**, **account management**, **double-entry ledger tracking**, and **idempotent transaction processing**.

Built using production-oriented principles such as **immutable ledger records**, **MongoDB ACID transactions**, **JWT security**, and **fraud-safe idempotency handling**.

---

## 🚀 Features

✔ User Registration & Login (JWT + Cookies)  
✔ Secure Authentication Middleware  
✔ Account Creation & Retrieval  
✔ Real-Time Balance Calculation  
✔ Double-Entry Ledger System (Credit / Debit)  
✔ Idempotent Transaction Processing  
✔ MongoDB ACID Transactions (Sessions)  
✔ Immutable Ledger Records  
✔ Token Blacklisting (Secure Logout)  
✔ Email Notifications (Nodemailer)

---

## 🧠 Core Concepts Implemented

### ✅ Double-Entry Accounting
Every transaction generates:

• DEBIT entry (sender)  
• CREDIT entry (receiver)

Ensures financial consistency.

---

### ✅ Idempotency Protection
Prevents duplicate transactions using:

```

idempotencyKey

```

Critical for banking systems.

---

### ✅ Immutable Ledger
Ledger entries **cannot be modified or deleted**, ensuring audit safety.

---

### ✅ ACID Transactions
MongoDB sessions guarantee:

✔ Atomicity  
✔ Consistency  
✔ Isolation  
✔ Durability

---

## 🛠 Tech Stack

• Node.js  
• Express.js  
• MongoDB  
• Mongoose  
• JSON Web Token (JWT)  
• bcryptjs  
• Nodemailer  

---

## 📁 Project Structure

```

src/
│
├── config/        # DB Connection
├── controllers/   # Business Logic
├── middleware/    # Auth / Security
├── models/        # Database Schemas
├── routes/        # API Endpoints
├── services/      # Email Service
└── app.js

```

---

## 🔐 Environment Variables

Create `.env` file:

```

MONGO_URI=
JWT_SECRET=

EMAIL_USER=
CLIENT_ID=
CLIENT_SECRET=
REFRESH_TOKEN=

````

---

## ⚙️ Installation

```bash
npm install
````

---

## ▶ Running Server

```bash
nodemon server.js
```

Expected Output:

```
Server is running on port 3000
server is connected to DB
Email server is ready to send messages
```

---

## 🌐 API Endpoints

---

### ✅ Authentication

**Register User**

```
POST /api/auth/register
```

**Login User**

```
POST /api/auth/login
```

**Logout User**

```
POST /api/auth/logout
```

---

### ✅ Accounts

**Create Account**

```
POST /api/accounts/
```

**Get User Accounts**

```
GET /api/accounts/
```

**Get Account Balance**

```
GET /api/accounts/balance/:accountId
```

---

### ✅ Transactions

**Create Transaction**

```
POST /api/transactions/
```

**Initial Funds (System User)**

```
POST /api/transactions/system/initial-funds
```

---

## 🔁 Transaction Flow (Simplified)

1️⃣ Validate request
2️⃣ Validate idempotency key
3️⃣ Check account status
4️⃣ Derive balance from ledger
5️⃣ Create transaction (PENDING)
6️⃣ Create DEBIT ledger entry
7️⃣ Create CREDIT ledger entry
8️⃣ Mark transaction COMPLETED
9️⃣ Commit MongoDB session
🔟 Send email notification

---

## 🛡 Security Measures

✔ JWT Authentication
✔ Cookie-Based Sessions
✔ Token Blacklisting
✔ Immutable Ledger Records
✔ Idempotent Transactions
✔ MongoDB ACID Transactions

---

## 📈 Future Improvements

• Transaction History API
• Bank Statement Generation
• OTP / Email Verification
• Rate Limiting
• Fraud Detection Logic
• Admin Dashboard
• Audit Logging

---

## ☁ Deployment

Backend can be deployed using:

✔ Render
✔ Railway
✔ Cyclic

---

## 📜 License

For educational & portfolio purposes.

---

## 👨‍💻 Author

Backend Ledger – Banking Simulation Engine

```
