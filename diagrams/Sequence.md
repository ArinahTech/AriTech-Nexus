# AriTech NEXUS Sequence Diagrams

## Overview

This document contains the primary sequence diagrams that describe the interaction between users, the frontend, backend services, database, and external systems during common business processes.

---

# 1. User Login

```mermaid
sequenceDiagram

actor User
participant Frontend
participant Backend
participant Database

User->>Frontend: Enter username & password
Frontend->>Backend: POST /auth/login
Backend->>Database: Validate credentials
Database-->>Backend: User record
Backend-->>Frontend: JWT Token
Frontend-->>User: Dashboard
```

---

# Description

The user authenticates with the system. After successful credential validation, the backend issues a JWT access token which is used for subsequent authenticated requests.

---

# 2. Customer Registration

```mermaid
sequenceDiagram

actor Administrator
participant Frontend
participant Backend
participant Database

Administrator->>Frontend: Enter customer details
Frontend->>Backend: POST /customers
Backend->>Database: Save customer
Database-->>Backend: Customer ID
Backend-->>Frontend: Customer created
Frontend-->>Administrator: Success message
```

---

# Description

An administrator registers a new customer. The backend validates the data and stores the customer record in the database.

---

# 3. Invoice Generation

```mermaid
sequenceDiagram

actor Finance
participant Frontend
participant Backend
participant Database

Finance->>Frontend: Generate invoice
Frontend->>Backend: POST /invoices
Backend->>Database: Create invoice
Database-->>Backend: Invoice created
Backend-->>Frontend: Invoice details
Frontend-->>Finance: Display invoice
```

---

# Description

The finance officer generates an invoice for a customer subscription. The invoice is stored in the database and returned to the frontend.

---

# 4. Payment Processing

```mermaid
sequenceDiagram

actor Finance
participant Frontend
participant Backend
participant Database

Finance->>Frontend: Record payment
Frontend->>Backend: POST /payments
Backend->>Database: Save payment
Backend->>Database: Update invoice status
Database-->>Backend: Payment successful
Backend-->>Frontend: Receipt generated
Frontend-->>Finance: Display confirmation
```

---

# Description

After a payment is received, the backend records the transaction, updates the invoice status, and generates a receipt.

---

# 5. Hotspot Voucher Generation

```mermaid
sequenceDiagram

actor Agent
participant Frontend
participant Backend
participant Database

Agent->>Frontend: Generate voucher
Frontend->>Backend: POST /vouchers
Backend->>Database: Create voucher
Database-->>Backend: Voucher code
Backend-->>Frontend: Voucher details
Frontend-->>Agent: Print voucher
```

---

# Description

A sales agent generates a hotspot voucher. The backend creates a unique voucher code and stores it in the database before returning it to the frontend.

---

# 6. MikroTik Customer Provisioning

```mermaid
sequenceDiagram

actor Administrator
participant Frontend
participant Backend
participant MikroTik
participant Database

Administrator->>Frontend: Activate subscription
Frontend->>Backend: POST /subscriptions/activate
Backend->>MikroTik: Create PPPoE/Hotspot user
MikroTik-->>Backend: Success
Backend->>Database: Update subscription status
Database-->>Backend: Saved
Backend-->>Frontend: Activation complete
Frontend-->>Administrator: Success message
```

---

# Description

When a customer's subscription is activated, the backend provisions the customer on the MikroTik router through the RouterOS API and updates the database.

---

# Summary

These sequence diagrams describe the most important operational workflows within AriTech NEXUS. They illustrate how users interact with the frontend, how requests are processed by the backend, how data is persisted in PostgreSQL, and how external systems such as MikroTik RouterOS participate in business operations.

Additional sequence diagrams may be added in future releases for:

- Password Reset
- Inventory Assignment
- Site Survey Workflow
- Support Ticket Resolution
- Router Monitoring
- Alert Notifications
- Report Generation
- Backup and Restore