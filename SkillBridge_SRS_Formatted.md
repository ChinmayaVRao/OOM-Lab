# Software Requirements Specification (SRS)

## SkillBridge – Academia–Industry Collaboration Platform

| Document Field | Details |
|---|---|
| **Project** | SkillBridge |
| **Problem Statement ID** | SIH 26044 |
| **Document Type** | Software Requirements Specification |
| **Standard** | IEEE-style SRS |
| **Version** | 1.0 |
| **Status** | Initial Draft – Repository-Based Analysis |
| **Source Repository** | https://github.com/dipanjan2907/Skill_Bridge_SIH |

---

# Table of Contents

1. [Introduction](#1-introduction)
2. [Overall Description](#2-overall-description)
3. [System Features and Functional Requirements](#3-system-features-and-functional-requirements)
4. [External Interface Requirements](#4-external-interface-requirements)
5. [Non-Functional Requirements](#5-non-functional-requirements)
6. [System Data Requirements](#6-system-data-requirements)
7. [Use Case Specifications](#7-use-case-specifications)
8. [System Workflow Requirements](#8-system-workflow-requirements)
9. [Business Rules](#9-business-rules)
10. [System Constraints and Limitations](#10-system-constraints-and-limitations)
11. [Future Enhancements](#11-future-enhancements)
12. [Acceptance Criteria](#12-acceptance-criteria)
13. [Traceability Matrix](#13-traceability-matrix)
14. [Items Requiring Further Validation](#14-items-requiring-further-validation)
15. [Conclusion](#15-conclusion)

---

# 1. Introduction

## 1.1 Purpose

The purpose of this Software Requirements Specification (SRS) is to define the functional and non-functional requirements of SkillBridge, an online platform designed to establish collaboration between academic institutions and industries.
The platform aims to reduce the skill gap between university graduates and industry expectations by providing skill assessments, proficiency verification, skill-gap analysis, opportunity recommendations, recruitment management, and academic-industry collaboration.
This document serves as a reference for developers, testers, project managers, administrators, institutions, industry partners, and other stakeholders.

## 1.2 Scope

SkillBridge is a centralized, multi-stakeholder web application that connects students, educational institutions, faculty members, and industries.
The system provides the following capabilities:

User registration and authentication.
Role-based access control.
Student profile and digital portfolio management.
Technical skill assessment and proficiency verification.
Skill-gap analysis.
Industry skill-demand analysis.
Skill-based internship and placement recommendations.
Opportunity publication and application management.
Applicant screening and recruitment tracking.
Faculty and industry question-bank contributions.
Administrative question moderation.
Academic and industry collaboration initiatives.
Institution-level student analytics.
Skill registry management.
[V] These capabilities are described in the repository documentation and associated API and database architecture.

## 1.3 Intended Audience

This document is intended for:

Software developers responsible for implementation.
Quality assurance engineers responsible for testing.
Project managers responsible for project planning.
Students using the platform.
Industry recruiters and partners.
Faculty members and academicians.
Institutional administrators.
System administrators.

## 1.4 Definitions and Abbreviations

Term  Description
SRS Software Requirements Specification
SIH Smart India Hackathon
RBAC  Role-Based Access Control
JWT JSON Web Token
API Application Programming Interface
CGPA  Cumulative Grade Point Average
MCQ Multiple Choice Question
FDP Faculty Development Programme
FR  Functional Requirement
NFR Non-Functional Requirement
UI  User Interface
DBMS  Database Management System

## 1.5 References

SkillBridge GitHub Repository: https://github.com/dipanjan2907/Skill_Bridge_SIH
IEEE-style Software Requirements Specification structure.
React and Vite documentation.
Node.js and Express documentation.
MySQL documentation.
JSON Web Token documentation.

## 1.6 Requirement Evidence Classification

Requirements in this document use the following classifications:
[V] Verified in documentation: Explicitly described in the repository README, architecture, API listing, or database description.

[I] Inferred: Derived from the documented system design and expected behavior, but not explicitly guaranteed by the repository.

[T] To validate: Requires confirmation through source-code inspection, deployment testing, or stakeholder approval.

# 2. Overall Description

## 2.1 Product Perspective

SkillBridge is a web-based client-server application consisting of:
A React-based frontend.
A Node.js and Express backend.
A MySQL relational database.
RESTful APIs for communication.
Authentication and authorization middleware.
Rule-based skill assessment and matching services.
The frontend provides role-specific dashboards and user interfaces. The backend processes requests, evaluates assessments, manages business logic, and communicates with the database.
The system is documented as being deployed using Vercel for the frontend and Render for the backend, with a cloud-hosted MySQL database.

## 2.2 Product Functions

The major functions of the system are:
Module  Main Function
Authentication  Registration, login and identity management
Student Management  Student profiles and digital portfolios
Skill Assessment  Technical tests and proficiency scoring
Skill Gap Analysis  Identification of missing skills
Industry Demand Aggregation of industry skill requirements
Opportunity Management  Job and internship publication
Matching Engine Candidate-opportunity compatibility calculation
Application Management  Submission and tracking of applications
Question Management Question contributions and moderation
Collaboration Workshops, mentorships and academic initiatives
Institution Dashboard Student and departmental analytics
Administration  Verification and platform governance

## 2.3 User Classes and Characteristics

### 2.3.1 Student

Students use the platform to evaluate their technical skills, identify competency gaps, develop their professional profiles, and apply for industry opportunities.
Main activities:
Register and log in.
Maintain academic and personal information.
Take technical assessments.
View verified skill scores and badges.
Analyze skill gaps.
Browse recommended opportunities.
Apply for jobs and internships.
Track application status.
Maintain a digital portfolio.

### 2.3.2 Industry Partner

Industry partners use the platform to identify qualified candidates and publish recruitment opportunities.
Main activities:
Register as an industry partner.
Complete organization profiles.
Obtain account verification.
Publish jobs, internships, apprenticeships, and live projects.
Define required skills and proficiency levels.
Review applicant profiles.
Evaluate candidate matching scores.
Update application statuses.
Contribute technical assessment questions.
Organize collaboration initiatives.

### 2.3.3 Faculty / Academician

Faculty members contribute to technical skill evaluation and academic-industry collaboration.
Main activities:
Contribute technical questions.
Request new skills.
Organize workshops and faculty development programmes.
Participate in academic-industry initiatives.
Monitor relevant student skill information.

### 2.3.4 Institution

Institutions use the platform to monitor student readiness and facilitate academic-industry collaboration.
Main activities:
Manage institutional information.
Participate in collaboration initiatives.
View student rosters and analytics.
Monitor departmental skill readiness.
Evaluate industry placement alignment.

### 2.3.5 Administrator

Administrators are responsible for platform governance.
Main activities:
Manage user verification.
Approve or reject industry accounts.
Manage assessment questions.
Approve or reject skill requests.
Configure assessment question targets.
Monitor platform activities.
Maintain the master skill registry.

## 2.4 Operating Environment

Frontend
React 19.2
TypeScript 5.7
Vite 8.1
React Router DOM 7.18
CSS3
Tailwind CSS 4.3
Backend
Node.js
Express 5.2
TypeScript 5.7
REST API architecture
JSON Web Tokens
bcrypt
Zod validation
Database
MySQL 8.0 or higher
mysql2 database driver
Relational database architecture
Deployment
Vercel – frontend hosting
Render – backend hosting
Aiven – documented cloud database hosting
[V] These technologies and environments are listed in the repository documentation.

## 2.5 Design and Implementation Constraints

The frontend shall use the documented React and TypeScript architecture.
The backend shall expose RESTful APIs.
The database shall use a relational MySQL structure.
Authentication shall use JWT-based mechanisms.
Passwords shall be handled using password hashing.
Role-specific operations shall be protected by backend authorization middleware.
Assessment answers shall be evaluated on the server.
Sensitive configuration values shall be maintained through environment variables.

## 2.6 User Documentation

The system should provide appropriate user guidance for:
Account registration and login.
Profile creation and maintenance.
Skill assessment.
Opportunity applications.
Recruiter operations.
Faculty contributions.
Administrative moderation.
[I] A centralized user manual and contextual help system are recommended but are not explicitly established by the repository documentation.

## 2.7 Assumptions and Dependencies

Users have access to an internet-connected device.
Users have a compatible modern web browser.
The backend server is available.
The MySQL database is configured and accessible.
Industry accounts must be verified before accessing restricted recruitment functionality.
Students provide accurate academic and professional information.
Administrators are responsible for approving contributed assessment content.
The availability of matching opportunities depends on industry participation.

# 3. System Features And Functional Requirements

## 3.1 User Registration and Authentication

Description
The authentication module manages user registration, login, identity verification, and role-based access.
Functional Requirements
FR-001 [V]: The system shall allow users to register using the supported registration process.

FR-002 [V]: The system shall support multiple user roles, including Student, Industry Partner, Faculty, Institution, and Administrator.

FR-003 [V]: The system shall allow registered users to log in.

FR-004 [V]: The system shall authenticate users using JWT-based authentication.

FR-005 [V]: The system shall provide an API to retrieve the authenticated user's identity.

FR-006 [V]: The system shall enforce role-based access using backend authorization middleware.

FR-007 [I]: The system should provide password recovery functionality.

FR-008 [I]: The system should provide session expiration and secure logout functionality.

## 3.2 Student Profile Management

Description
This module enables students to maintain academic, professional, and personal information.
Functional Requirements
FR-009 [V]: The system shall allow students to view their profiles.

FR-010 [V]: The system shall allow students to update profile information.

FR-011 [V]: The system shall maintain academic information, including degree, department, CGPA, and institution.

FR-012 [V]: The system shall allow students to add academic and personal projects.

FR-013 [V]: The system shall allow students to maintain certification information.

FR-014 [V]: The system shall maintain student work experience records.

FR-015 [V]: The system shall support resume metadata and resume storage references.

FR-016 [V]: The system shall support professional profile links such as GitHub, LinkedIn, and portfolio URLs.

FR-017 [V]: The system shall compile student activities into a digital portfolio.

FR-018 [I]: The system should allow students to preview their portfolios before sharing them.

## 3.3 Skill Management

Description
This module maintains a centralized registry of technical and professional skills.
Functional Requirements
FR-019 [V]: The system shall maintain a master list of skills.

FR-020 [V]: The system shall categorize skills into categories such as Programming, Web Development, Database, DevOps, AI/ML, and Soft Skills.

FR-021 [V]: The system shall associate students with relevant skills.

FR-022 [V]: The system shall allow industry partners and faculty members to request new skills.

FR-023 [V]: The system shall allow administrators to review skill requests.

FR-024 [V]: The system shall allow administrators to approve or reject skill requests.

FR-025 [V]: The system shall add approved skills to the master skill registry.

## 3.4 Skill Assessment

Description
The assessment module evaluates students' technical knowledge through objective assessments.
Functional Requirements
FR-026 [V]: The system shall allow students to select a skill for assessment.

FR-027 [V]: The system shall retrieve approved questions associated with the selected skill.

FR-028 [V]: The system shall support multiple-choice assessment questions.

FR-029 [V]: The system shall prevent correct answers from being exposed to the student during assessment delivery.

FR-030 [V]: The system shall accept submitted answers through the assessment API.

FR-031 [V]: The system shall evaluate submitted answers on the backend.

FR-032 [V]: The system shall calculate the proficiency score based on correct answers and total questions.

Proficiency calculation:
Proficiency Score (%) = (Correct Answers / Total Questions) × 100
FR-033 [V]: The system shall save assessment scores against the corresponding student and skill.

FR-034 [V]: The system shall award a proficiency badge when the assessment score is at least 70%.

FR-035 [V]: The system shall identify assessment-verified skills using the verification source.

FR-036 [V]: The system shall maintain assessment attempt history.

FR-037 [V]: The system shall prevent students from manually changing server-calculated assessment scores.

FR-038 [V]: The system shall select approved questions using configured question targets and difficulty distribution.

FR-039 [V]: The system shall minimize repeated questions across assessment attempts.

FR-040 [V]: The system shall support skill-family fallback when an exact skill has no approved assessment questions.

## 3.5 Question Bank Management

Description
This module enables authorized stakeholders to contribute technical questions and allows administrators to moderate them.
Functional Requirements
FR-041 [V]: The system shall maintain a centralized question bank.

FR-042 [V]: The system shall allow authorized industry partners and faculty members to contribute questions.

FR-043 [V]: The system shall classify questions by skill, difficulty, contributor, and approval status.

FR-044 [V]: The system shall assign newly contributed questions a pending moderation status.

FR-045 [V]: The system shall allow administrators to approve contributed questions.

FR-046 [V]: The system shall allow administrators to reject questions with a mandatory rejection reason.

FR-047 [V]: The system shall allow administrators to edit question content and answer keys.

FR-048 [V]: The system shall allow administrators to filter questions by skill, difficulty, and contributor source.

FR-049 [V]: The system shall support pagination of question records.

FR-050 [V]: The system shall display question-bank statistics, including approved, pending, and rejected questions.

FR-051 [V]: The system shall allow administrators to configure target question counts for individual skills.

## 3.6 Skill Gap Analysis

Description
The skill-gap module compares students' assessed competencies against relevant skill requirements.
Functional Requirements
FR-052 [V]: The system shall retrieve a student's assessed skills.

FR-053 [V]: The system shall retrieve relevant industry skill-demand information.

FR-054 [V]: The system shall identify skills that are missing or below required proficiency levels.

FR-055 [V]: The system shall provide skill-gap analysis through the corresponding student interface and API.

FR-056 [I]: The system should prioritize skill gaps based on industry demand and opportunity relevance.

FR-057 [I]: The system should recommend suitable learning resources for identified skill gaps.

## 3.7 Industry Skill Demand Analysis

Description
This module provides insights into the skills required by participating industries.
Functional Requirements
FR-058 [V]: The system shall maintain skill requirements associated with industry opportunities.

FR-059 [V]: The system shall aggregate industry demand information.

FR-060 [V]: The system shall provide skill-demand statistics through the skills demand API.

FR-061 [V]: The system shall provide an industry demand report to students.

FR-062 [I]: The system should support filtering demand information by industry, skill category, and time period.

## 3.8 Opportunity Management

Description
This module enables verified industry partners to publish employment and learning opportunities.
Functional Requirements
FR-063 [V]: The system shall allow authorized industry partners to create opportunities.

FR-064 [V]: The system shall support full-time jobs, internships, apprenticeships, and live projects.

FR-065 [V]: The system shall maintain opportunity descriptions and requirements.

FR-066 [V]: The system shall associate required skills and proficiency benchmarks with opportunities.

FR-067 [V]: The system shall maintain opportunity application deadlines.

FR-068 [V]: The system shall allow students to browse active opportunities.

FR-069 [V]: The system shall prevent applications to opportunities whose deadlines have expired.

FR-070 [I]: The system should allow industry partners to edit or deactivate published opportunities.

## 3.9 Skill-Based Matching Engine

Description
The matching engine calculates the compatibility between student proficiency and opportunity requirements.
Functional Requirements
FR-071 [V]: The system shall retrieve required skills for an opportunity.

FR-072 [V]: The system shall retrieve assessed student proficiency for corresponding skills.

FR-073 [V]: The system shall calculate individual skill compatibility scores.

Individual Match (%) = MIN(100, FLOOR(Student Proficiency / Required Proficiency × 100))
FR-074 [V]: The system shall calculate an overall opportunity compatibility score.

Overall Match (%) = MIN(100, ROUND(Sum of Individual Match Scores / Number of Required Skills))
FR-075 [V]: The system shall classify matching scores into the following categories:

| Score | Classification |
| --- | --- |
| 80–100% | Excellent Match |
| 60–79% | Good Match |
| 40–59% | Moderate Match |
| 0–39% | Low Match |
| No assessed skills | Incomplete Profile |

FR-076 [V]: The system shall provide opportunity matching information to students.

FR-077 [V]: The system shall provide applicant skill-match information to recruiters.

FR-078 [V]: The system shall provide matched, partially matched, and missing skill information.

FR-079 [I]: The system should allow students to sort opportunities by compatibility score.

## 3.10 Application Management

Description
This module manages student applications and the recruitment lifecycle.
Functional Requirements
FR-080 [V]: The system shall allow eligible students to apply for opportunities.

FR-081 [V]: The system shall support resume references and application details.

FR-082 [V]: The system shall validate application deadlines on both client and server sides.

FR-083 [V]: The system shall allow students to view their submitted applications.

FR-084 [V]: The system shall allow industry partners to view applicants for their opportunities.

FR-085 [V]: The system shall display applicant compatibility and skill-match information.

FR-086 [V]: The system shall support application status updates.

FR-087 [V]: The system shall support statuses including Shortlisted, Accepted, and Rejected.

FR-088 [I]: The system should notify students when application statuses change.

## 3.11 Collaboration Management

Description
This module facilitates academic and industry collaboration through organized initiatives.
Functional Requirements
FR-089 [V]: The system shall maintain collaboration initiatives.

FR-090 [V]: The system shall support initiatives such as workshops, mentorships, guest lectures, hackathons, and FDPs.

FR-091 [V]: The system shall allow authorized stakeholders to create collaboration initiatives.

FR-092 [V]: The system shall allow users to browse collaboration initiatives.

FR-093 [V]: The system shall allow users to register for collaboration initiatives.

FR-094 [V]: The system shall associate relevant skills with collaboration initiatives.

FR-095 [I]: The system should allow initiative organizers to monitor registration and participation.

## 3.12 Institution Dashboard and Analytics

Description
The institution module provides institutional insights into student readiness and academic-industry alignment.
Functional Requirements
FR-096 [V]: The system shall provide institution-specific dashboard functionality.

FR-097 [V]: The system shall support student roster viewing.

FR-098 [V]: The system shall provide student skill-readiness analytics.

FR-099 [V]: The system shall support departmental analytics.

FR-100 [V]: The system shall provide information relevant to industry placement alignment.

FR-101 [I]: The system should support downloadable institutional reports.

## 3.13 Administration and Governance

Description
The administration module provides centralized control over platform governance.
Functional Requirements
FR-102 [V]: The system shall provide an administrative dashboard.

FR-103 [V]: The system shall allow administrators to review industry verification requests.

FR-104 [V]: The system shall allow administrators to approve or reject industry accounts.

FR-105 [V]: The system shall provide question moderation functionality.

FR-106 [V]: The system shall allow administrators to approve or reject skill requests.

FR-107 [V]: The system shall allow administrators to manage skill assessment targets.

FR-108 [V]: The system shall restrict administrative operations to authorized users.

FR-109 [I]: The system should maintain an auditable history of important administrative actions.

# 4. External Interface Requirements

## 4.1 User Interface Requirements

The application shall provide a responsive web-based interface.
The interface shall provide:
Registration and login screens.
Role-specific dashboards.
Student profile and portfolio screens.
Skill assessment interfaces.
Skill-gap analysis dashboards.
Industry opportunity management screens.
Applicant screening interfaces.
Collaboration management pages.
Question moderation console.
Institutional analytics dashboards.
[V] The repository documents these interface categories and associated frontend pages and components.

## 4.2 Hardware Interface Requirements

[I] The application does not require specialized hardware.

Supported devices should include:

Desktop computers.
Laptop computers.
Tablets.
Smartphones.

## 4.3 Software Interface Requirements

The system interacts with:
Software  Purpose
React frontend  User interaction
Express backend Request processing
MySQL Data storage
JWT Authentication
bcrypt  Password hashing
REST APIs Frontend-backend communication
Vercel  Frontend deployment
Render  Backend deployment

## 4.4 Communication Interface Requirements

[V] The application uses HTTP-based REST API communication.

The documented API categories include:

| API Base Path | Purpose |
| --- | --- |
| /api/auth | Authentication |
| /api/profile | Student profile |
| /api/skills | Skill registry and analysis |
| /api/assessments | Assessment operations |
| /api/assessment | Question contributions |
| /api/admin | Administrative operations |
| /api/opportunities | Opportunity management |
| /api/applications | Application management |
| /api/collaborations | Collaboration management |
| **5. | **NON-FUNCTIONAL REQUIREMENTS |

The following section distinguishes documented technical characteristics from recommended quality requirements.

## 5.1 Security

NFR-001 [V]: The system shall use JWT-based authentication.

NFR-002 [V]: The system shall hash user passwords using bcrypt.

NFR-003 [V]: The system shall enforce backend role-based access control.

NFR-004 [V]: Correct assessment answers shall not be exposed through the student-facing assessment delivery interface.

NFR-005 [V]: The system shall use environment variables for sensitive configuration.

NFR-006 [I]: The system should protect against SQL injection, cross-site scripting, and cross-site request forgery where applicable.

NFR-007 [I]: The system should use HTTPS for production communication.

NFR-008 [I]: Sensitive student and recruitment information should only be accessible to authorized users.

## 5.2 Performance

NFR-009 [I]: The system should provide responsive user interactions under normal operating conditions.

NFR-010 [I]: Database queries should be optimized for assessment, opportunity, and application retrieval.

NFR-011 [V]: The administrative question-management interface shall support server-side pagination.

NFR-012 [I]: The system should support concurrent access from students, recruiters, faculty, and administrators.

No numerical response-time or concurrency targets are specified in the available project documentation.

## 5.3 Reliability and Availability

NFR-013 [I]: The system should maintain data consistency during assessment submission and application processing.

NFR-014 [I]: The system should handle unexpected backend errors without exposing sensitive technical information.

NFR-015 [I]: The system should provide database backup and recovery procedures.

NFR-016 [I]: The production deployment should provide appropriate availability monitoring.

## 5.4 Usability

NFR-017 [I]: The application should provide an intuitive interface for all five user roles.

NFR-018 [I]: The application should provide understandable validation messages.

NFR-019 [I]: The application should display assessment results and matching information clearly.

NFR-020 [I]: The application should provide consistent navigation and visual design.

## 5.5 Maintainability

NFR-021 [V]: The application shall follow a modular frontend and backend architecture.

NFR-022 [V]: The backend shall separate routing, controllers, services, and middleware.

NFR-023 [V]: The application shall use TypeScript for its documented frontend and backend architecture.

NFR-024 [I]: The project should maintain automated testing and technical documentation.

## 5.6 Portability and Compatibility

NFR-025 [I]: The application should operate on modern web browsers.

NFR-026 [I]: The application should support different screen sizes.

NFR-027 [V]: The frontend and backend shall support the documented separate deployment environments.

## 5.7 Scalability

NFR-028 [I]: The system should support growth in registered students, institutions, industry partners, and assessment questions.

NFR-029 [I]: The system should support increased opportunity and application records without significant degradation of performance.

# 6. System Data Requirements

## 6.1 Database Overview

[V] The repository documents a relational MySQL database comprising 20 major tables.

## 6.2 Major Database Entities

Entity  Description
users User accounts and roles
institutions  Institution details and verification
student_profiles  Student academic profiles
skills  Master skill registry
student_skills  Student proficiency information
assessment_questions  Technical assessment questions
assessment_attempts Assessment attempt records
assessment_attempt_questions  Questions associated with attempts
skill_requests  Requests for new skills
industry_profiles Industry organization information
opportunities Jobs and internships
opportunity_skills  Skills required by opportunities
applications  Student opportunity applications
student_projects  Student project information
student_certifications  Certification records
student_resumes Resume metadata
student_work_experiences  Work experience information
collaborations  Academic-industry initiatives
collaboration_skills  Skills associated with initiatives
collaboration_participants  Initiative registrations

## 6.3 Data Integrity Requirements

[I] The system should:

Maintain unique user identifiers.
Preserve valid relationships between database entities.
Validate references to existing skills.
Maintain valid application-to-opportunity relationships.
Prevent unauthorized modification of assessment results.
Maintain consistent approval statuses.
Protect sensitive personal information.

# 7. Use Case Specifications

## 7.1 Use Case: Student Takes a Skill Assessment

Use Case ID: UC-001
Primary Actor: Student
Preconditions:
Student has an active account.
Student is authenticated.
The selected skill exists.
Approved questions are available.
Main Flow:
Student logs into SkillBridge.
Student navigates to skill assessment.
Student selects a skill.
System retrieves eligible approved questions.
System presents the questions without exposing correct answers.
Student answers the questions.
Student submits the assessment.
Backend evaluates submitted answers.
System calculates the proficiency score.
System stores the assessment result.
System awards a badge if the score is at least 70%.
Student views the result.
Alternative Flow:
If no questions exist for the selected skill, the system may retrieve questions from a related skill family.
If submission fails, the system should communicate the failure.
Postconditions:
Assessment attempt is recorded.
Proficiency information is updated.

## 7.2 Use Case: Student Applies for an Opportunity

Use Case ID: UC-002
Primary Actor: Student
Preconditions:
Student is authenticated.
Opportunity is active.
Application deadline has not expired.
Main Flow:
Student opens the opportunities page.
System displays available opportunities.
Student selects an opportunity.
System calculates the compatibility score.
Student reviews the required skills and matching information.
Student submits an application and resume reference.
Backend validates the request.
System records the application.
Application becomes available to the relevant recruiter.
Alternative Flow:
If the deadline has expired, the application is rejected.
If required information is missing, the system requests correction.
Postconditions:
Application is stored.
Application status is available for tracking.

## 7.3 Use Case: Industry Partner Screens Applicants

Use Case ID: UC-003
Primary Actor: Industry Partner
Preconditions:
Industry account is verified.
Partner has published an opportunity.
Applicants exist.
Main Flow:
Industry partner logs in.
Partner opens the recruitment dashboard.
Partner selects an opportunity.
System displays applicants.
System displays candidate compatibility scores.
Partner examines individual skill-match details.
Partner reviews applicant information.
Partner updates application status.
Postconditions:
Application status is updated.

## 7.4 Use Case: Administrator Moderates Assessment Questions

Use Case ID: UC-004
Primary Actor: Administrator
Preconditions:
Administrator is authenticated.
Pending questions exist.
Main Flow:
Administrator opens the moderation dashboard.
System displays pending questions.
Administrator selects a question.
System displays question details.
Administrator reviews the content.
Administrator approves or rejects the question.
If rejected, the administrator provides a reason.
System updates the question status.
Postconditions:
Question status is updated.
Approved questions become eligible for student assessments.

## 7.5 Use Case: Faculty Contributes Assessment Questions

Use Case ID: UC-005
Primary Actor: Faculty Member
Preconditions:
Faculty member is authenticated.
Selected skill exists.
Main Flow:
Faculty member opens the question contribution interface.
Faculty member selects a skill.
Faculty member enters question text and answer options.
Faculty member selects the correct answer and difficulty.
Faculty member submits the question.
System stores the question with pending status.
Administrator reviews the submission.
Postconditions:
Question is stored for moderation.

## 7.6 Use Case: Institution Monitors Student Readiness

Use Case ID: UC-006
Primary Actor: Institution
Preconditions:
Institution account is authorized.
Relevant student information exists.
Main Flow:
Institution representative logs in.
Representative opens the institution dashboard.
System retrieves relevant student information.
System displays student rosters and analytics.
Representative reviews departmental skill readiness.
Postconditions:
Institution can view available readiness information.

# 8. System Workflow Requirements

## 8.1 Student Skill Evaluation Workflow

Student selects a skill.
System retrieves approved questions.
Student completes the assessment.
Backend evaluates answers.
System calculates proficiency.
System updates student skill records.
System awards a badge when the threshold is achieved.
System updates skill-gap information.

## 8.2 Recruitment Workflow

Industry partner creates an opportunity.
Industry partner defines required skills.
Student browses opportunities.
Matching engine evaluates student compatibility.
Student submits an application.
Industry partner reviews applicants.
Industry partner updates application status.
Student tracks application progress.

## 8.3 Question Moderation Workflow

Faculty or industry partner contributes a question.
System marks the question as pending.
Administrator reviews the question.
Administrator approves or rejects it.
Approved questions enter the common question bank.
Students can receive approved questions during assessments.

# 9. Business Rules

| Rule ID | Business Rule |
| --- | --- |
| BR-001 | Assessment proficiency shall be calculated by the backend. |
| BR-002 | Students shall not manually change assessment scores. |
| BR-003 | A score of 70% or above earns a proficiency badge. |
| BR-004 | Only approved questions are eligible for student assessments. |
| BR-005 | Contributed questions require administrative moderation. |
| BR-006 | Rejected questions require a rejection reason. |
| BR-007 | Only verified industry partners may publish opportunities, as documented. |
| BR-008 | Applications must comply with opportunity deadlines. |
| BR-009 | Opportunity matching shall use assessed student proficiency. |
| BR-010 | Administrative functionality shall be restricted to administrators. |
| BR-011 | Approved skill requests shall be added to the master skill registry. |
| BR-012 | Matching scores shall be classified into the documented compatibility categories. |
| **10. | **SYSTEM CONSTRAINTS AND LIMITATIONS |
| The | application depends on internet connectivity. |
| The | backend depends on a functioning MySQL database. |
| Skill | matching depends on available student assessments and opportunity skill requirements. |
| Assessment | quality depends on approved question-bank content. |
| Recruitment | effectiveness depends on active industry participation. |
| Institution | analytics depend on available and authorized student records. |
| The | platform uses rule-based matching as documented; advanced AI-based matching is not established as a current core feature. |
| The | repository lists resume parsing, proctored assessments, LMS integrations, and OCR-based document verification as future enhancements. |
| **11. | **FUTURE ENHANCEMENTS |

The following features are explicitly documented as future enhancements and must not be treated as confirmed current requirements.
AI-Based Resume Parsing: Automatically extract skills from uploaded resumes.
Proctored Assessments: Introduce webcam and tab-switch monitoring.
LMS Integration: Integrate external learning platforms such as Coursera and NPTEL.
Automated Document Verification: Use OCR to verify certificates and industry credentials.
Additional recommendations:
Automated email and in-app notifications.
Advanced analytics and report exports.
Personalized learning-path recommendations.
Enhanced accessibility features.

# 12. Acceptance Criteria

The system shall be considered acceptable when the following conditions are demonstrated through testing.
| Test ID | Acceptance Criterion |
| --- | --- |
| AC-001 | Users can register and authenticate. |
| AC-002 | Role-based access restrictions are enforced. |
| AC-003 | Students can create and update profiles. |
| AC-004 | Students can complete skill assessments. |
| AC-005 | Assessment answers are evaluated on the backend. |
| AC-006 | Proficiency scores are calculated correctly. |
| AC-007 | Scores of 70% or higher earn badges. |
| AC-008 | Unauthorized users cannot access administrative functions. |
| AC-009 | Question contributions enter the moderation workflow. |
| AC-010 | Administrators can approve and reject questions. |
| AC-011 | Students can view skill-gap information. |
| AC-012 | Industry partners can publish eligible opportunities. |
| AC-013 | Matching scores are calculated according to documented rules. |
| AC-014 | Students can submit eligible applications. |
| AC-015 | Expired opportunities cannot receive applications. |
| AC-016 | Recruiters can review applicants and update application statuses. |
| AC-017 | Users can access collaboration initiatives. |
| AC-018 | Institutions can access authorized analytics. |

These acceptance criteria are proposed verification tests derived from the documented requirements. Passing them requires execution against the actual application.

# 13. Traceability Matrix

The following matrix connects major system modules to their functional requirements.
Module  Requirement IDs
Authentication  FR-001 to FR-008
Student Profiles  FR-009 to FR-018
Skill Management  FR-019 to FR-025
Skill Assessment  FR-026 to FR-040
Question Bank FR-041 to FR-051
Skill Gap Analysis  FR-052 to FR-057
Industry Demand FR-058 to FR-062
Opportunity Management  FR-063 to FR-070
Matching Engine FR-071 to FR-079
Applications  FR-080 to FR-088
Collaboration FR-089 to FR-095
Institution Analytics FR-096 to FR-101
Administration  FR-102 to FR-109

# 14. Items Requiring Further Validation

The repository documentation does not establish all implementation and operational details. The following items should be confirmed before final approval of this SRS.
Item  Classification  Validation Required
Password reset  [I] Confirm whether implemented
Email verification  [T] Inspect authentication implementation
Notification system [I] Confirm available notification channels
Application status notifications  [I] Verify implementation
API rate limiting [T] Inspect backend middleware
Backup and recovery [T] Confirm deployment configuration
Numerical performance targets [T] Obtain stakeholder targets
Concurrent user capacity  [T] Perform load testing
Data retention policy [T] Obtain organizational requirements
Accessibility compliance  [T] Conduct accessibility testing
Resume file validation  [T] Inspect upload handling
Privacy and consent requirements  [T] Obtain stakeholder and legal review
Audit logging [T] Inspect backend implementation

# 15. Conclusion

SkillBridge provides a centralized platform for improving collaboration between academic institutions and industries.
The system addresses the skill mismatch problem by integrating objective technical assessments, verified student proficiency, skill-gap analysis, industry demand aggregation, opportunity matching, and recruitment management.
Its multi-stakeholder architecture enables students, faculty members, institutions, industry partners, and administrators to participate in a shared ecosystem.
This SRS defines the principal requirements and expected system behavior based on the available GitHub repository documentation. It provides a foundation for software development, testing, maintenance, and stakeholder review.
Document Status: Initial Repository-Based SRS Draft
Recommended Next Step: Validate all documented requirements against the actual source code and obtain stakeholder approval before treating this document as the final baseline specification.
END OF SOFTWARE REQUIREMENTS SPECIFICATION
