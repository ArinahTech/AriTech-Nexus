# AriTech NEXUS Development Log

---

# Sprint 1: Project Initialization

**Date:** 1 July 2026

**Status:** ✅ Completed

## Objective

Establish the project's development environment, initialize version control, and create the foundational project structure.

## Activities Completed

- Created the AriTech NEXUS repository on GitHub.
- Configured Git user information.
- Cloned the repository to the local development environment.
- Opened the project in Visual Studio Code.
- Created the initial project folder structure.
- Added project documentation files.
- Initialized version control.
- Created the first Git commit.
- Successfully pushed the project to GitHub.

## Challenges Encountered

- Git configuration contained multiple `user.name` entries.
- DNS issues initially prevented GitHub access.
- GitHub password authentication was rejected because GitHub requires a Personal Access Token (PAT) or SSH.
- Authentication was successfully completed using a Personal Access Token.

## Lessons Learned

- How to initialize a professional Git project.
- How to use GitHub as a remote repository.
- How Git commits and pushes work.
- How to troubleshoot Git authentication issues.

## Git Commit

```
Project structure initialized
```

---

# Sprint 2: Frontend Initialization

**Date:** 1 July 2026

**Status:** ✅ Completed

---

## Objective

The objective of Sprint 2 was to establish the frontend foundation of AriTech NEXUS by setting up a modern web application using Next.js and its recommended development tools. This sprint aimed to prepare the project for the implementation of user interface components and future business modules.

---

## Activities Completed

During this sprint, the following tasks were successfully completed:

* Installed and configured **Node.js** using Node Version Manager (NVM).
* Verified the Node.js and npm development environment.
* Initialized the **Next.js** frontend application.
* Configured **TypeScript** for type-safe development.
* Configured **ESLint** to enforce coding standards.
* Installed and configured **Tailwind CSS** for responsive user interface development.
* Enabled the **Next.js App Router** architecture.
* Created the frontend project inside the `frontend` directory.
* Successfully installed all required project dependencies.
* Generated application route types.
* Started the local development server.
* Verified successful application deployment by accessing the project through **[http://localhost:3000](http://localhost:3000)**.
* Committed all frontend files to the local Git repository.
* Successfully pushed the updated project to the remote GitHub repository.

---

## Project Structure Created

The following frontend structure was generated:

```text
frontend/
│
├── public/
├── src/
│   └── app/
│       ├── favicon.ico
│       ├── globals.css
│       ├── layout.tsx
│       └── page.tsx
│
├── package.json
├── package-lock.json
├── tsconfig.json
├── next.config.ts
├── postcss.config.mjs
├── eslint.config.mjs
└── README.md
```

---

## Git Milestone

The following Git milestone was achieved during Sprint 2:

**Commit Message**

```text
Initialize Next.js frontend with TypeScript and Tailwind CSS
```

**GitHub Status**

* Repository successfully synchronized with GitHub.
* Frontend source code uploaded successfully.
* Development history preserved through Git commits.

---

## Challenges Encountered

Several challenges were experienced and successfully resolved during this sprint:

* Initially installed a frontend configuration using the recommended defaults before deciding to recreate the project using customized settings.
* Learned the updated **create-next-app** installation workflow introduced in newer versions of Next.js.
* Waited for dependency installation, which required approximately five minutes due to package downloads.
* Successfully authenticated with GitHub using a Personal Access Token (PAT) after learning that password authentication is no longer supported.

---

## Lessons Learned

Sprint 2 provided practical experience in:

* Installing and managing Node.js using NVM.
* Creating modern React applications using Next.js.
* Configuring TypeScript projects.
* Using Tailwind CSS for utility-first styling.
* Understanding the App Router architecture.
* Managing project dependencies using npm.
* Running and testing local development servers.
* Managing Git commits and synchronizing projects with GitHub.

---

## Outcome

Sprint 2 was successfully completed. The AriTech NEXUS frontend is now fully operational and provides a stable development environment for implementing future modules such as authentication, dashboards, customer management, hotspot operations, billing, network monitoring, and reporting.

The project now has a professional frontend foundation that supports scalable and maintainable software development.

---

## Sprint 2 Summary

| Item                            | Status |
| ------------------------------- | :----: |
| Next.js Installed               |    ✅   |
| TypeScript Configured           |    ✅   |
| Tailwind CSS Installed          |    ✅   |
| ESLint Configured               |    ✅   |
| App Router Enabled              |    ✅   |
| Local Development Server Tested |    ✅   |
| Git Commit Created              |    ✅   |
| GitHub Repository Updated       |    ✅   |

---


Sprint 3: System Architecture & Foundation

This sprint will produce the following deliverables:

Sprint 3
│
├── 1. Project Architecture
├── 2. Folder Structure
├── 3. Technology Stack
├── 4. Database Design
├── 5. Backend Modules
├── 6. Frontend Modules
├── 7. UI Design System
├── 8. Authentication & Authorization
├── 9. MikroTik Integration
├──10. ISP Monitoring Architecture
├──11. Billing Engine
├──12. Notifications
├──13. Deployment Architecture
└──14. Development Standards
Deliverable 1 — Overall System Architecture
                    AriTech NEXUS
                          │
         ┌────────────────┴────────────────┐
         │                                 │
     Frontend                         Backend API
      Next.js                           NestJS
         │                                 │
         │                         Business Logic
         │                                 │
         ├──────────────┬──────────────────┤
         │              │                  │
     PostgreSQL      MikroTik API      Notification Services
         │              │                  │
         │              │                  │
 Customer Data     Routers & APs      SMS • Email • WhatsApp

This separation makes each part easier to develop and maintain.

Deliverable 2 — Complete Project Structure
AriTech-Nexus/
│
├── frontend/
│
├── backend/
│
├── database/
│
├── docs/
│
├── diagrams/
│
├── api/
│
├── deployment/
│
├── tests/
│
├── scripts/
│
├── docker/
│
├── .github/
│
├── CHANGELOG.md
├── DEVLOG.md
├── TASKS.md
├── LICENSE
└── README.md

Each directory will have a specific purpose, making the project easy to navigate.

Deliverable 3 — Technology Stack
Layer	Technology
Frontend	Next.js
UI	Tailwind CSS
Language	TypeScript
Backend	NestJS
ORM	Prisma
Database	PostgreSQL
Authentication	JWT + Refresh Tokens
API	REST (GraphQL can be added later if needed)
Queue	Redis + BullMQ
Monitoring	SNMP + RouterOS API + ICMP
Charts	Recharts
Maps	Leaflet
File Storage	Local (development), S3-compatible storage (production)
Deployment	Docker + Nginx
Deliverable 4 — Backend Modules
Authentication

Users

Roles

Permissions

Customers

Subscriptions

Billing

Invoices

Payments

Hotspots

Vouchers

Agents

Network Monitoring

Routers

Sites

Equipment

Inventory

Tickets

Notifications

Reports

Audit Logs

Settings

Each module will have its own controller, service, DTOs, and database models.

Deliverable 5 — Frontend Modules
Dashboard

Customers

Billing

Payments

Subscriptions

Hotspot

Voucher Management

Agents

ISP Monitoring

Site Survey

Tickets

Reports

Inventory

Settings

Profile

Each section will be accessible through the main navigation.

Deliverable 6 — Database Modules

Our PostgreSQL database will include tables such as:

Users

Roles

Permissions

Customers

CustomerLocations

Subscriptions

Invoices

Payments

PaymentMethods

Routers

RouterGroups

Hotspots

Sites

Devices

AccessPoints

NetworkAlerts

Vouchers

VoucherSales

Agents

Tickets

Notifications

Surveys

Equipment

AuditLogs

Settings

We'll design the relationships before implementing them in Prisma.

Deliverable 7 — UI Design System

To keep the interface consistent:

Primary Color

Deep Blue (#1E3A8A)

Secondary

Emerald Green (#10B981)

Warning

Amber (#F59E0B)

Danger

Red (#EF4444)

Background

Light Gray (#F8FAFC)

Cards

White (#FFFFFF)

We'll also standardize typography, spacing, buttons, tables, forms, and icons.

Deliverable 8 — Authentication

We'll support:

Super Administrator
ISP Administrator
Operations Manager
Finance Officer
Support Engineer
Field Technician
Agent
Customer (optional portal)

Role-Based Access Control (RBAC) will ensure each user only sees the features they are authorized to access.

Deliverable 9 — MikroTik Integration

The system will connect to MikroTik routers using the RouterOS API to:

Monitor router status.
Manage hotspots.
Create and revoke users.
Generate and synchronize vouchers.
Monitor bandwidth usage.
Receive router health information.
Execute administrative commands where appropriate.
Deliverable 10 — ISP Monitoring

The monitoring engine will:

Check router uptime.
Monitor latency.
Monitor packet loss.
Track bandwidth utilization.
Detect offline access points.
Monitor CPU and memory usage.
Generate alerts for outages or thresholds.
Display a centralized Network Operations Center (NOC) dashboard.
Deliverable 11 — Billing

The billing module will support:

Subscription billing.
Recurring invoices.
Hotspot vouchers.
Agent voucher commissions.
Payment tracking.
Customer balances.
Automated reminders.
Service suspension and reactivation based on payment status (with configurable policies).
Deliverable 12 — Notifications

Notifications can be sent through:

SMS
Email
WhatsApp (where available)
In-app notifications

Examples include:

Invoice reminders.
Network outage alerts.
Payment confirmations.
Voucher sales notifications.
Site maintenance notices.
Deliverable 13 — Deployment
Internet
      │
Nginx Reverse Proxy
      │
Frontend (Next.js)
      │
Backend (NestJS)
      │
PostgreSQL
      │
Redis

This supports a clean separation of responsibilities and is suitable for scaling.

Deliverable 14 — Development Standards

We'll follow these practices:

Use Git feature branches for major work.
Make small, meaningful commits.
Use consistent TypeScript naming conventions.
Keep modules independent.
Write documentation alongside development.
Test new features before merging.


# Sprint 3 – System Architecture & Documentation

## Date
July 2026

## Objective
Complete the software design documentation before backend development.

## Completed

- System Architecture
- Technology Stack
- Database Design
- API Design
- UI Design System
- Security Architecture
- Development Roadmap
- Modules
- Project Proposal
- Requirements Specification
- Complete Software Requirements Specification (10 Chapters)

## Git Commit

Complete Software Requirements Specification and project documentation

## Outcome

AriTech NEXUS now has a complete software blueprint covering architecture, database design, APIs, security, interfaces, business rules, and system requirements. This documentation will guide the implementation of the backend, frontend, and infrastructure.


# AriTech NEXUS Development Log

This document records the day-to-day progress, milestones, challenges, and decisions made during the development of AriTech NEXUS.

---

# Sprint 1 — Project Initialization

## Objective

Establish the project repository and development environment.

## Completed

- Created GitHub repository.
- Cloned the repository locally.
- Configured Git.
- Created the initial project structure.
- Added the initial project documentation.
- Performed the first commit.
- Successfully pushed the project to GitHub.

## Challenges

- Initial Git authentication issues.
- Repository cloning problems due to network configuration.
- Git username configuration conflicts.

## Solutions

- Corrected Git configuration.
- Configured GitHub authentication successfully.
- Verified repository synchronization.

## Outcome

AriTech NEXUS repository was successfully initialized and version controlled.

---

# Sprint 2 — Frontend Initialization

## Objective

Prepare the frontend development environment.

## Completed

- Installed Node.js.
- Installed npm.
- Installed Next.js.
- Configured TypeScript.
- Configured Tailwind CSS.
- Configured ESLint.
- Successfully started the development server.

## Challenges

- Installation delays while downloading dependencies.
- VS Code (Code OSS) became unresponsive during setup.
- Process management issues on Kali Linux.

## Solutions

- Restarted the editor.
- Terminated hanging processes.
- Verified Node.js and npm installations.
- Confirmed successful frontend initialization.

## Outcome

A modern Next.js frontend environment was successfully configured.

---

# Sprint 3 — System Design & Documentation

## Objective

Design the entire software architecture before implementation.

## Completed

### Repository Documentation

- Professional README
- CONTRIBUTING Guide
- CODE OF CONDUCT
- CHANGELOG
- TASKS
- DEVLOG

### System Documentation

- System Architecture
- Technology Stack
- Database Design
- API Design
- UI Design System
- Security Architecture
- Development Roadmap
- Modules Documentation
- Project Proposal
- Requirements Specification

### Software Requirements Specification

Completed all chapters including:

- Introduction
- Overall Description
- System Features
- External Interfaces
- Non-Functional Requirements
- Database Requirements
- Security Requirements
- Use Cases
- Business Rules
- Appendices

## Major Decisions

- Adopt Next.js for the frontend.
- Adopt NestJS for the backend.
- Use PostgreSQL as the primary database.
- Use Prisma ORM.
- Implement JWT authentication.
- Implement Role-Based Access Control (RBAC).
- Design the system using a modular architecture.

## Outcome

The project now has a complete software blueprint that will guide implementation.

---

# Sprint 4 — Repository Finalization

## Objective

Prepare the repository for active software development.

## Completed

- Repository documentation finalized.
- Development workflow established.
- Versioning strategy documented.
- Contribution standards documented.
- Task management system established.
- Development history documented.

## Outcome

The repository now follows professional software engineering practices and is ready for implementation.

---

# Lessons Learned

Throughout the planning phase, several important lessons were identified:

- Proper planning reduces future development effort.
- Documentation improves maintainability.
- Git should be used from the beginning of the project.
- Consistent commit messages improve project history.
- A modular architecture simplifies future expansion.
- Database design should precede backend implementation.

---

# Upcoming Work

The next major milestone is software implementation.

Planned activities include:

1. Design the PostgreSQL database.
2. Create the Prisma schema.
3. Initialize the NestJS backend.
4. Configure authentication.
5. Develop backend modules.
6. Build frontend interfaces.
7. Integrate MikroTik RouterOS.
8. Implement network monitoring.
9. Perform system testing.
10. Deploy the application.

---

# Project Milestones

| Sprint | Milestone | Status |
|----------|-----------|--------|
| Sprint 1 | Project Initialization | ✅ Completed |
| Sprint 2 | Frontend Setup | ✅ Completed |
| Sprint 3 | Architecture & Documentation | ✅ Completed |
| Sprint 4 | Repository Finalization | ✅ Completed |
| Sprint 5 | Database Design | ⏳ Planned |
| Sprint 6 | Backend Development | ⏳ Planned |
| Sprint 7 | Authentication | ⏳ Planned |
| Sprint 8 | Customer Management | ⏳ Planned |
| Sprint 9 | Billing & Payments | ⏳ Planned |
| Sprint 10 | Hotspot Management | ⏳ Planned |
| Sprint 11 | Network Monitoring | ⏳ Planned |
| Sprint 12 | Inventory & Support | ⏳ Planned |
| Sprint 13 | Dashboard & Reports | ⏳ Planned |
| Sprint 14 | Testing & Deployment | ⏳ Planned |

---

# Closing Note

AriTech NEXUS has progressed from an initial idea into a well-documented software engineering project with a clearly defined architecture, development roadmap, and implementation strategy.

The project is now ready to transition from planning into active development while maintaining a strong foundation of documentation, version control, and engineering best practices.


Sprint 4
──────────────
✅ NestJS
✅ PostgreSQL
✅ Prisma
✅ Authentication
✅ Users
✅ Roles

Sprint 5
──────────────
Customers
Plans
Subscriptions

Sprint 6
──────────────
Billing
Invoices
Payments
Receipts

Sprint 7
──────────────
Hotspot
Voucher System
Agents

Sprint 8
──────────────
MikroTik API
Provisioning
Synchronization

Sprint 9
──────────────
Inventory
Warehouses
Equipment

Sprint 10
──────────────
Monitoring
Router Status
Traffic
Alerts

Sprint 11
──────────────
Reports
Dashboard
Analytics

Sprint 12
──────────────
Frontend Integration
Testing
Deployment