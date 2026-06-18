# ATS-V3

ATS-V3 is a multi-tenant Applicant Tracking System (ATS) designed to automate and streamline the end-to-end recruitment workflow.

The platform is being built as a generic, configurable recruitment system that can be used by individuals, recruiters, agencies, and organisations without requiring hardcoded CV formats, CSV structures, industries, or job types.

\---

## Core Principles

### Generic CV Management

ATS-V3 does not assume any specific CV structure, profession, industry, or naming convention.

Users can:

* Upload multiple CVs
* Store CV versions
* Tag CVs
* Search CVs
* Select the most appropriate CV for a job

### Generic CSV Management

ATS-V3 supports user-defined CSV imports.

The system does not require:

* Fixed column names
* Fixed file names
* Fixed templates

Users can create mapping profiles that connect CSV columns to ATS-V3 fields.

### Multi-Tenant Architecture

ATS-V3 is designed as a SaaS-ready platform.

Each tenant has isolated access to:

* Users
* CVs
* Jobs
* Applications
* Reports
* Configuration

\---

## Business Workflow

The primary workflow is:

Job Specification
→ Job Profile

CV Upload
→ Candidate Profile

Candidate Profile + Job Profile
→ Match Score

Match Score
→ Best CV Recommendation

Application Submission
→ Tracking

Tracking
→ Interview / Failure / Offer

Reporting
→ Daily Summary / Metrics

\---

## Technology Stack

### Backend

* Laravel 12
* PHP 8.3+
* PostgreSQL
* Redis
* Laravel Sanctum
* Spatie Permission
* Spatie Multitenancy

### Frontend

* React
* Inertia.js
* Tailwind CSS

### Infrastructure

* Docker
* MinIO
* AWS Compatible Storage

### Testing

* Pest PHP

\---

## Current Modules

### Authentication \& Tenancy

* User Management
* Authentication
* Role Management
* Tenant Isolation

### CV Library

* CV Upload
* CV Storage
* CV Metadata
* CV Versioning
* CV Search
* CV Tagging

### CSV Import Centre

* CSV Upload
* Mapping Profiles
* Validation
* Import History

### Candidate Profiles

* CV Parsing
* Skills Extraction
* Employment Extraction
* Education Extraction
* Certification Extraction

### Job Profiles

* Job Parsing
* Metadata Extraction
* Requirements Extraction
* Skill Extraction

### Matching Engine

* Candidate Matching
* Job Matching
* Match Scores
* Gap Analysis
* Best CV Recommendation

### Application Lifecycle

* Submission Tracking
* Interview Tracking
* Failure Tracking
* Timeline Management

### Reporting

* Daily Summary
* KPI Tracking
* Trend Analysis
* Reporting Services

\---

## MVP Goal

The first working MVP delivers:

1. Create Job
2. Upload CV
3. Parse CV
4. Parse Job Description
5. Run Match Engine
6. Generate Match Score
7. Display Matched Skills
8. Display Missing Skills

\---

## Repository Structure

app/
Models/
Services/
Repositories/
Http/

database/
migrations/

resources/
js/

tests/

docs/

\---

## Development Status

Current focus:

MVP-01

* Job Creation
* CV Upload
* CV Parsing
* Match Engine
* Match Results

Future phases:

* Application Automation
* Cover Letter Generation
* Reporting Dashboards
* Workflow Automation
* Production Hardening

\---

## Design Rules

* No hardcoded CV names
* No hardcoded CSV names
* No hardcoded professions
* No hardcoded industries
* User-supplied data only
* Tenant-isolated data
* Configurable workflows
* Extensible architecture

