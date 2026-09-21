# CampCare

### Healthcare Documentation Platform

**TypeScript · Electron · Node.js · SQLite · HTML/CSS/JavaScript**

CampCare is an offline-first desktop healthcare documentation platform designed around the workflows of residential camp health centres.

## The Problem

While working in the infirmary as a Health Care Attendant (an unofficial "camp nurse") at an overnight summer camp, I encountered a healthcare documentation system that relied heavily on paper records for medication administration and clinical documentation.

I was given the opportunity to restructure the existing system, including redesigning medication administration records and standardizing clinical documentation. Although these changes improved organization, the underlying limitations of a paper-based workflow remained. Medication records had to be manually recreated and updated each week, and staff frequently had to search through paper records to locate the correct camper information during medication passes and other healthcare encounters.

After working with the redesigned system, the idea emerged to explore whether software could reduce some of this repetitive work. This led to "Camp Med Log", an initial collaborative project focused primarily on improving the efficiency of morning and evening medication passes.

## The Solution

Working on Camp Med Log demonstrated how much of the camp healthcare workflow could benefit from digitization, but I knew a good EMR would need more than medication administration to make a coherent infirmary.

Using my nursing education I independantly continued to build *Camp Med Log* using my day-to-day experience providing care at camp. I continued identifying opportunities to improve camper records, clinical encounters, follow-up documentation, and medication management. Working in the infirmary also allowed me to see how these digital workflows performed in a real healthcare environment and identify what was missing or needed to change.

After camp ended, I used those lessons to independently design and develop CampCare as a new application, separate from the Camp Med Log codebase. CampCare was designed around the complete camp healthcare documentation workflow rather than medication administration alone, combining my BScN education, practical community clinical experience, and workflow knowledge I gained in the infirmary.

I designed CampCare to centralize camper health records, medication administration, healthcare visits, follow-up documentation, and operational health information in a single desktop application.

The system is designed to support real-world camp healthcare workflows while keeping operational data locally controlled.

## Key Features

- Searchable camper roster and individual health records
- Medication administration and scheduling workflows
- Walk-in assessment and treatment documentation
- Follow-up documentation and longitudinal camper history
- Structured medical-form importing
- Role-based staff authentication and permissions
- Clinical audit logging
- Separate camp/session management
- Printable healthcare documentation
- Local SQLite data persistence
- Optional local multi-device host/client operation
- Password recovery and account management

## Screenshots

### Overview

*Screenshot coming here.*

### Medication Administration

*Screenshot coming here.*

### Camper Health Record

*Screenshot coming here.*

### Walk-In Documentation

*Screenshot coming here.*

## Technical Design

CampCare is built as an Electron desktop application using TypeScript and Node.js, with SQLite for local persistence.

The application separates its user interface from privileged application and database operations. Database access and other privileged operations are handled through the Electron main process and application services rather than directly through the renderer.

CampCare can operate independently on a single workstation or use a local host/client architecture to support multiple authorized devices working with the same active dataset.

## Healthcare-Informed Design

CampCare was designed from direct experience with camp healthcare workflows rather than as a generic record-management application.

The system maintains a distinction between information that can be imported electronically and information that still requires human clinical verification. For example, medication information requiring in-person verification is withheld from automatic medication import rather than being treated as clinically verified simply because it appears in an electronic source.

CampCare supports documentation and information management; it does not replace professional clinical judgment, medication orders, organizational policies, or emergency procedures.

## Privacy & Demonstration Data

**All camper records, health information, medications, and other data visible in this public repository and its screenshots are synthetic demonstration data. No real camper or patient health information is included.**

The production source code, operational databases, credentials, private deployment materials, and real-world health records are not included in this public repository.

## Project Status

**Version 1.0.0 — Active Development**

CampCare currently supports core camper-record, medication-administration, clinical-documentation, authentication, audit, import, printing, session-management, and local networking workflows.

---

**Designed and developed by Jessica Gyamfi**
