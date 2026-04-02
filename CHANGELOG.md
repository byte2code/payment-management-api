# Changelog

All notable changes to this project are documented in this file.

## [v2.0.0] - 2026-04-03

### Summary
Second version of the Payment Management API that expands the project from read/create operations into a fuller CRUD-style payment management service.

### Highlights

- Added `DELETE /payment/delete/id/{id}` for removing payment records.
- Added `PUT /payment/update` for updating full payment records.
- Added `PUT /payment/update/{id}/description/{description}` for targeted description updates.
- Extended the DAL and service layers with delete and update operations.
- Refreshed the README to present the project as a stronger CRUD and JPA learning showcase.

### Notes

This version improves the project’s usefulness as a portfolio project by covering more of the typical payment-record lifecycle.

## [v1.0.0] - 2026-04-03

### Summary
Initial publication of the Payment Management API as a clean, portfolio-ready Spring Boot REST project.

### Highlights

- Added a recruiter-friendly README with API overview, features, run steps, and project structure.
- Added a changelog for future version tracking.
- Cleaned IDE files, build artifacts, and system clutter before publishing.
- Preserved the original payment CRUD and query logic, JPA entity mapping, and exception flow.

### Notes

This version establishes the project as a layered Spring Boot and JPA learning showcase for managing payment records in MySQL.
