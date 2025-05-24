# Vacation Tracking System

## 📌 Vision

The **Vacation Tracking System** empowers employees to independently manage their vacation time, sick leave, and personal time off. System eliminates the need for users to be experts in company or facility-specific leave policies by streamlining leave requests and approvals through a centralized, rules-based system.

---

## ✅ Functional Requirements

- Flexible rules-based engine for leave request validation and verification.
- Optional manager approval workflow.
- Request history available for the past year and future requests allowed up to 18 months in advance.
- Email notifications for:
  - Manager approval requests
  - Status updates for employees
- Integrated with the company's intranet portal (SSO-enabled).
- Activity logging for all transactions.
- HR and system administrators can override system restrictions (with logs).
- Managers can award personal leave (within system-defined limits).
- Web service interface for querying employee vacation summaries.
- Interfaces with legacy HR systems to retrieve and update employee data.

---

## 📉 Non-Functional Requirements

- Reuses existing hardware and middleware infrastructure.

---

## ⛓️ Constraints

- One physical server hosts the web application, database, and application server.
- Legacy stack usage is mandatory (e.g., Apache Tomcat, Cloudscape DB).
- HTTP-based communication (no HTTPS).
- Must reuses existing hardware and middleware infrastructure.

---

## 👤 Actors and Roles

- **Employee**: 
  - Main user.
  - Submits and manages personal leave requests.

- **Manager**: 
  - Has all employee permissions.
  - Reviews and approves vacation requests from direct reports.
  - May award compensatory leave (within set limits).

- **HR Clerk**:
  - Maintains accurate employee data across HR systems.
  - Can add or remove records.
  - Uses distinct logins if also an employee.

- **System Administrator**:
  - Maintains system performance, backups, and log archival.
  - Ensures server/database uptime and technical integrity.

