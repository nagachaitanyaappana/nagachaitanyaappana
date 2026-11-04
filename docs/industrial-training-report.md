# Industrial Training Report

## Trainee Details

| Field | Details |
|---|---|
| Name | Appana Naga Chaitanya |
| Register Number | 24010-CM-001 |
| Branch | CME (Computer Engineering) |
| Institution | Andhra Polytechnic, Kakinada |
| Academic Batch | 2024–2027 |
| Training Organization | National Informatics Centre (NIC), Kakinada |
| Training Period | 15 May 2026 – 20 November 2026 |
| Duration | Approximately six months |
| Project | ITI Admissions Portal |

## Acknowledgement

I sincerely thank the National Informatics Centre (NIC), Kakinada, for providing the opportunity to undertake industrial training and gain practical exposure to software development. I express my gratitude to my training guides, Kalyan Sir and Srinivas Sir, for their guidance and support throughout the training.

I also thank the faculty members of Andhra Polytechnic, Kakinada — Anasuya Madam, Pratusha Madam, Pravalika Madam and Veerababu Sir — for their encouragement and support.

## Introduction

The industrial training provided practical exposure to the development and maintenance of a web-based ITI admissions portal. The system supports activities associated with trainee admissions, application verification, admission scheduling and report generation.

The work involved understanding an existing departmental application and its modules, reviewing the redesigned system, and working with the frontend, backend and database components.

## Project Overview

The ITI Admissions Portal is a web-based application used to support admission-related workflows and administrative reporting. Its functionality is organized into modules, including student registration and application activities, application verification and re-verification, admission and merit-list related activities, STRIVE information pages, and ITI, District, Nodal and State/Directorate reports.

The project documentation describes a modular application with a JSP, HTML, CSS and JavaScript frontend; Spring Boot and Java backend components; a Node.js and Express.js API component; and PostgreSQL for data storage. Maven and NPM are used as build and package-management tools.

## System Analysis

### Existing System

The earlier departmental portal supported admission registration, verification, image uploads, report generation, schedule entry, admission updates and verified-form reprinting. As the application grew, tightly connected modules and older interface patterns made maintenance and updates difficult.

### Rebuilt System

The rebuilt portal organizes functionality into separate modules. The documented goals include improving maintainability, usability, data handling, report generation and the ability to extend the system.

### Main Functional Areas

- **Login:** Staff and administrators access the portal through the login workflow.
- **Student Area:** Student registration, ITI applications, editing registration details and Registration ID recovery.
- **STRIVE:** Information about the STRIVE project and related training initiatives.
- **Verification:** Verification reports and workflows for verified, unverified and rejected applications.
- **Admissions:** Merit-list generation, permitted shift/unit information, admission slips, schedule entry and Phase 2 admission activities.
- **Reports:** Reports for ITIs, districts, nodal users and state/directorate-level users.

## Reports Module

The Reports module provides administrative information in report form. The report catalogue documented during the project includes the following groups.

### ITI Reports

- Applicant Report
- ITI-Wise Admission Status Report
- Admission Report
- DSC List
- ITI API Dashboard

### District Reports

- Verified Application Count
- ITI Wise District Year
- Applicant Address with Mobile
- District API Dashboard
- Caste Wise Admissions Abstract
- District Shift Unit Report and Shift Unit Verify
- District DSC List

### Nodal Reports

- Total Applicants Count
- 24 Months Trade Seats Abstract
- State/Nodal API Dashboard
- Phase Wise Admissions Details
- Today Schedule ITIs
- Trade Wise
- District Wise Applicant
- District/ITI/Trade Wise Seats Abstract
- Duration Wise Trade Seats Abstract
- Govt or Pvt District Wise Seats Abstract
- Student Registration Details
- Students Not Admitted

### State/Directorate Reports

- District Counselling Schedule
- Admitted Seats Abstract
- District-wise Admitted Seats Abstract
- Trade/District Wise Admission
- Trade-wise Vacant Position
- All Resource Role

### Public and Compliance Reports

- Verification Report
- DGT Permitted Shift Unit
- ITI Profile
- ITI List
- STRIVE Project Report and Disclosure
- Central Reports Dashboard

## Technical Structure

The repository documentation describes two Spring Boot applications in a monorepo:

- **Backend/** — backend application, configured for port 6050.
- **Frontend/** — frontend application, configured for port 6051.

The project uses Java, Spring Boot, Maven, JSP, JavaScript and PostgreSQL. The documented local setup uses JDK 22 and the Maven Wrapper. The backend is started before the frontend. Frontend JavaScript tests can be run with npm test.

The backend report functionality is organized around the reports API and its controller, service and service-implementation layers. The frontend exposes report pages through its reports controller and JSP views under:

Frontend/src/main/webapp/WEB-INF/reports/

## Work Carried Out

The training work included studying the ITI Admissions Portal, understanding its modular organization, reviewing the reporting workflows and working with the Reports module.

The Reports module was independently developed by the trainee. This work involved understanding the report requirements and the existing application structure, and working across the report-related frontend and backend components.

The project team also included M. Ramya, K. Varshitha and Bhavani. The Reports module work described here was completed independently by the trainee.

## Shift Unit Verification Workflow

The project includes a shift/unit verification workflow. The documented ShiftUnitVerifyService works with records in admissions.iti_admissions whose rec_status is E. It updates the shift and unit information and marks processed records with rec_status set to D. The operation is transactional.

The admission-year resolution logic checks public.iti_params for parameter code 7.

## Learning Outcomes

The industrial training provided practical exposure to:

- Understanding an existing, multi-module web application.
- Working with frontend and backend application structure.
- Understanding Spring Boot controller and service layers.
- Working with JSP-based report pages.
- Understanding database-driven reporting workflows using PostgreSQL.
- Following a multi-application project structure and its local run sequence.
- Understanding the importance of modularity, maintainability and validation in application development.

## Conclusion

The industrial training at NIC, Kakinada, provided practical experience with a real-world web application used for ITI admission-related activities. Working with the ITI Admissions Portal helped strengthen understanding of application architecture, backend and frontend integration, database-driven reports and software maintenance.

The independent development work on the Reports module was a significant part of the training and provided hands-on experience in implementing administrative reporting functionality.

---

*This Markdown document is a text-based project and training overview. It does not reproduce the screenshots and diagram images contained in the original training document.*
