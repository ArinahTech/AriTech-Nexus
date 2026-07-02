# AriTech NEXUS Entity Relationship Diagram (ERD)

## Overview

The Entity Relationship Diagram (ERD) defines the logical structure of the AriTech NEXUS database. It illustrates the entities, their attributes, and the relationships required to support ISP management, hotspot services, billing, inventory, monitoring, and customer support.

---

# Entity Relationship Diagram

```mermaid
erDiagram

    ROLE ||--o{ USER : assigns

    USER ||--o{ CUSTOMER : registers

    CUSTOMER ||--o{ SUBSCRIPTION : owns

    PLAN ||--o{ SUBSCRIPTION : includes

    CUSTOMER ||--o{ INVOICE : receives

    INVOICE ||--o{ PAYMENT : paid_by

    CUSTOMER ||--o{ VOUCHER : purchases

    AGENT ||--o{ VOUCHER : generates

    ROUTER ||--o{ MONITORING_LOG : records

    SITE ||--o{ ROUTER : contains

    CUSTOMER ||--o{ SUPPORT_TICKET : creates

    USER ||--o{ SUPPORT_TICKET : assigned

    EQUIPMENT ||--o{ STOCK_MOVEMENT : tracked

    SUPPLIER ||--o{ EQUIPMENT : supplies

    WAREHOUSE ||--o{ EQUIPMENT : stores

    USER ||--o{ AUDIT_LOG : creates

    ROLE {
        int id PK
        string name
        string description
    }

    USER {
        int id PK
        string firstName
        string lastName
        string email
        string password
        string phone
        boolean active
        int roleId FK
    }

    CUSTOMER {
        int id PK
        string accountNumber
        string fullName
        string phone
        string email
        string address
        string status
        int createdBy FK
    }

    PLAN {
        int id PK
        string name
        decimal price
        string speed
    }

    SUBSCRIPTION {
        int id PK
        int customerId FK
        int planId FK
        date startDate
        date endDate
        string status
    }

    INVOICE {
        int id PK
        int customerId FK
        decimal amount
        date dueDate
        string status
    }

    PAYMENT {
        int id PK
        int invoiceId FK
        decimal amount
        string method
        datetime paidAt
    }

    AGENT {
        int id PK
        string name
        string phone
        decimal commission
    }

    VOUCHER {
        int id PK
        string code
        string profile
        decimal price
        string status
        int agentId FK
    }

    SITE {
        int id PK
        string name
        string location
    }

    ROUTER {
        int id PK
        string hostname
        string ipAddress
        string model
        int siteId FK
    }

    MONITORING_LOG {
        int id PK
        int routerId FK
        float cpuUsage
        float memoryUsage
        datetime recordedAt
    }

    SUPPORT_TICKET {
        int id PK
        string subject
        string priority
        string status
        int customerId FK
        int assignedTo FK
    }

    SUPPLIER {
        int id PK
        string name
        string phone
    }

    WAREHOUSE {
        int id PK
        string name
        string location
    }

    EQUIPMENT {
        int id PK
        string serialNumber
        string model
        string status
    }

    STOCK_MOVEMENT {
        int id PK
        int equipmentId FK
        string type
        datetime createdAt
    }

    AUDIT_LOG {
        int id PK
        int userId FK
        string action
        datetime createdAt
    }
```

---

# Core Entities

The database is organized into the following domains:

## User Management

- Roles
- Users

---

## Customer Management

- Customers
- Service Plans
- Subscriptions

---

## Billing

- Invoices
- Payments

---

## Hotspot

- Voucher Profiles
- Vouchers
- Agents

---

## Network

- Sites
- Routers
- Monitoring Logs

---

## Inventory

- Suppliers
- Warehouses
- Equipment
- Stock Movements

---

## Technical Support

- Support Tickets

---

## Security

- Audit Logs

---

# Database Design Principles

The AriTech NEXUS database follows these principles:

- Normalized relational database design.
- Primary keys uniquely identify each record.
- Foreign keys enforce referential integrity.
- Relationships minimize data duplication.
- Audit logging provides accountability.
- Modular entities support future scalability.

---

# Future Expansion

Additional entities planned for future releases include:

- Permissions
- Notifications
- Receipts
- Installation Requests
- Site Surveys
- Contracts
- SMS Logs
- Email Logs
- Backup Jobs
- Scheduled Tasks
- API Keys
- Customer Documents
- Network Alerts
- Payment Gateways
- Multi-Tenant Organizations

---

# Summary

This ERD represents the logical foundation of the AriTech NEXUS database and will serve as the blueprint for implementing the PostgreSQL schema using Prisma ORM.