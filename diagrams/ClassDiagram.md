# AriTech NEXUS Class Diagram

## Overview

This class diagram provides a high-level object-oriented view of the AriTech NEXUS platform. It illustrates the primary classes, their attributes, methods, and relationships that support ISP management, billing, hotspot services, inventory, monitoring, and technical support.

---

# Class Diagram

```mermaid
classDiagram

class User{
+int id
+string firstName
+string lastName
+string email
+string password
+string phone
+boolean active

+login()
+logout()
+changePassword()
}

class Role{
+int id
+string name
+string description

+assignRole()
}

class Customer{
+int id
+string accountNumber
+string fullName
+string phone
+string email
+string address
+string status

+register()
+updateProfile()
+suspend()
}

class Plan{
+int id
+string name
+decimal price
+string speed

+createPlan()
+updatePlan()
}

class Subscription{
+int id
+date startDate
+date endDate
+string status

+activate()
+suspend()
+terminate()
}

class Invoice{
+int id
+decimal amount
+date dueDate
+string status

+generate()
+cancel()
}

class Payment{
+int id
+decimal amount
+string method
+datetime paidAt

+recordPayment()
}

class Voucher{
+int id
+string code
+decimal price
+string profile
+string status

+generateVoucher()
+expireVoucher()
}

class Router{
+int id
+string hostname
+string ipAddress
+string model

+connect()
+disconnect()
+synchronize()
}

class MonitoringLog{
+int id
+float cpuUsage
+float memoryUsage
+datetime recordedAt

+collectMetrics()
}

class Equipment{
+int id
+string serialNumber
+string model
+string status

+assign()
+returnEquipment()
}

class SupportTicket{
+int id
+string subject
+string priority
+string status

+openTicket()
+closeTicket()
}

Role "1" --> "*" User
User "1" --> "*" Customer
Customer "1" --> "*" Subscription
Plan "1" --> "*" Subscription
Customer "1" --> "*" Invoice
Invoice "1" --> "*" Payment
Customer "1" --> "*" Voucher
Router "1" --> "*" MonitoringLog
Customer "1" --> "*" SupportTicket
Equipment "1" --> "*" Customer
```

---

# Main Classes

## User

Responsible for authentication and access to the platform.

---

## Role

Defines permissions and system access.

---

## Customer

Stores subscriber information.

---

## Plan

Defines internet service plans.

---

## Subscription

Links customers to service plans.

---

## Invoice

Stores billing records.

---

## Payment

Stores payment transactions.

---

## Voucher

Represents hotspot access vouchers.

---

## Router

Represents MikroTik routers managed by the platform.

---

## Monitoring Log

Stores router monitoring statistics.

---

## Equipment

Tracks ISP equipment and assignments.

---

## Support Ticket

Tracks customer support requests.

---

# Design Principles

- Single Responsibility Principle
- Modular Architecture
- Encapsulation
- Separation of Business Logic
- High Cohesion
- Low Coupling

---

# Summary

This class diagram provides the conceptual object model for AriTech NEXUS and serves as a guide for implementing the backend services and domain models.