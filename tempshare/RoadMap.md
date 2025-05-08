# Sphynx PMS - Prioritized Development Roadmap

## Overview

This roadmap outlines the prioritized epics and user stories for Sphynx PMS development. It reflects the current state of the codebase, addresses key gaps identified, incorporates partner feedback regarding scope, and aims to deliver a robust V1 product iteratively. Priorities focus on establishing core PMS functionality, refining existing modules, and then tackling larger integrations and new feature areas.

---

## Phase 1: Solidifying the Core PMS

### Epic 1: Robust Reservation System

*   **Goal:** Ensure a fully functional, reliable reservation system supporting various booking types.
*   **User Stories:**
    *   **Title:** Group Booking Management (Size: 5)
        *   As a Hotel Manager, I want to manage group bookings, including room blocks and separate folios, so that I can handle group reservations efficiently.
    *   **Title:** Direct Booking Handling (Size: 3)
        *   As a Front Desk Agent, I want to easily handle direct bookings (phone, email, walk-in) with rate adjustments and room allocation, so that I can manage non-online reservations.
    *   **Title:** Refine Direct Booking Engine (Size: 3)
        *   As a Developer, I want to refine the existing direct booking engine on the guest portal for enhanced usability, customization, and commission-free operation, so that hotels can maximize direct revenue.
    *   **Title:** Rate Management Foundation (Size: 3)
        *   As a Hotel Manager, I want robust rate management capabilities, including seasonal rates and clear integration points for future dynamic pricing, so that I can control pricing strategies effectively.
    *   **Title:** Automated Booking Confirmations (Size: 3)
        *   As a Guest, I want to receive automated booking confirmations via email/SMS, so that I have a record of my reservation details.
    *   **Title:** Reservation Error Handling & Logging (Size: 3)
        *   As a Developer, I want comprehensive error handling and logging for all reservation operations to ensure system stability and debuggability.

### Epic 2: Comprehensive Billing & Folio Management

*   **Goal:** Implement a complete billing system to handle guest charges, payments, and invoicing accurately.
*   **User Stories:**
    *   **Title:** Folio Management System (Size: 5)
        *   As a Front Desk Agent, I want a folio management system to accurately track all guest charges (room, F&B, activities, misc.), so that guest bills are correct.
    *   **Title:** Process Folio Payments (Stripe) (Size: 2)
        *   As a Front Desk Agent, I want to process payments directly against guest folios using the existing Stripe integration, so that check-out is seamless.
    *   **Title:** Configurable Tax Rates/Fees (Size: 2)
        *   As a Hotel Manager, I want the system to support configurable tax rates and fees (e.g., tourism tax), so that billing complies with local regulations.
    *   **Title:** Generate Guest Invoices (Size: 3)
        *   As a Front Desk Agent, I want to generate clear guest invoices (viewable and printable), so that guests understand their charges.
    *   **Title:** Basic Accounts Receivable Tracking (Size: 2)
        *   As a Hotel Manager, I want basic Accounts Receivable tracking within the manager dashboard, so that I can monitor outstanding payments.
    *   **Title:** Split Billing Functionality (Size: 3)
        *   As a Front Desk Agent, I want to handle split billing scenarios (e.g., shared rooms, corporate accounts), so that complex billing needs are met.

### Epic 3: Essential Front Desk Operations

*   **Goal:** Provide staff with the tools needed for efficient daily front desk tasks.
*   **User Stories:**
    *   **Title:** Check-in/Check-out Workflows (Staff App) (Size: 5)
        *   As a Front Desk Agent, I want clear check-in and check-out workflows in the staff app (Flutter), so that I can process guest arrivals and departures smoothly.
    *   **Title:** Room Assignment Logic (Size: 3)
        *   As a Hotel Manager, I want room assignment logic based on availability, guest preferences (from profile), and housekeeping status, so that rooms are assigned optimally.
    *   **Title:** Guest Profile Database (Size: 2)
        *   As a Hotel Manager, I want a guest profile database to store contact info, stay history, and basic preferences, so that we can offer personalized service.
    *   **Title:** Online/Mobile Check-in/Check-out (Guest Portal) (Size: 3)
        *   As a Guest, I want the option for online/mobile check-in and check-out (leveraging existing portal/app), so that I can save time at the front desk.

### Epic 4: Channel Manager Reliability & Completion

*   **Goal:** Finalize existing Channel Manager integrations and ensure robust, reliable synchronization.
*   **User Stories:**
    *   **Title:** Complete MyAllocator Integration (Size: 3)
        *   As a Developer, I want to complete the MyAllocator integration, including obtaining and configuring API keys, so that hotels using MyAllocator can sync with Sphynx.
    *   **Title:** Channel Sync Error Handling & Alerting (Size: 3)
        *   As a Developer, I want to implement comprehensive error handling and alerting for all channel sync operations (availability, rates, bookings), so that failures are detected and addressed quickly.
    *   **Title:** Channel Sync Detailed Logging (Size: 2)
        *   As a Developer, I want detailed logging for channel manager interactions to facilitate debugging and support.
    *   **Title:** Ensure Real-time Sync Reliability (Goal Story - Covered by others) (Size: N/A)
        *   As a Hotel Manager (Premium), I want to confidently rely on real-time, two-way synchronization with connected OTAs/Channel Managers to prevent overbookings and rate discrepancies.

### Epic 5: Foundational Security & Compliance Enhancements

*   **Goal:** Strengthen security posture and ensure core compliance requirements are met.
*   **User Stories:**
    *   **Title:** Handle GDPR Data Subject Requests (Backend) (Size: 5)
        *   As a Developer, I want to implement backend processes for handling GDPR data subject requests (access, rectification, erasure, portability), so that the system is compliant.
    *   **Title:** Implement Data Retention Policies (Size: 3)
        *   As a Developer, I want to define and implement data retention policies for guest data to comply with GDPR.
    *   **Title:** Build Dedicated Audit Trail System (Size: 8)
        *   As a Developer, I want to build a dedicated audit trail system logging key actions (e.g., booking creation/modification/cancellation, folio adjustments, user login), so that changes can be tracked for security and accountability.
    *   **Title:** Review/Implement Field-Level Encryption (Size: 3)
        *   As a Developer, I want to review and potentially implement field-level encryption for highly sensitive guest data (e.g., payment details not handled solely by Stripe tokens) stored in the database.
    *   **Title:** Define Granular User Roles & Permissions (Size: 3)
        *   As a Hotel Manager, I want clearly defined user roles (e.g., Front Desk, Housekeeper, Manager) with specific, granular permissions beyond the current basic model, so that access is strictly controlled.

---

## Phase 2: Expanding Capabilities & Addressing Feedback

### Epic 6: Enhanced Housekeeping & Maintenance

*   **Goal:** Improve operational efficiency with better housekeeping and maintenance tools.
*   **User Stories:**
    *   **Title:** Update Room Status (Staff App) (Size: 2)
        *   As a Housekeeper, I want to update room status (Clean, Dirty, Inspected, Out of Order) in the staff app, so that the front desk has real-time information.
    *   **Title:** Create Cleaning Schedules (Size: 3)
        *   As a Head Housekeeper, I want tools to create and manage daily cleaning schedules, prioritizing rooms based on arrivals/departures, so that room readiness is optimized.
    *   **Title:** Log/Track Maintenance Requests (Staff App) (Size: 3)
        *   As any Staff Member, I want to log maintenance requests (e.g., broken AC) via the staff app, assign them, and track their status, so that repairs are handled efficiently.
    *   **Title:** Basic Housekeeping Inventory Tracking (Size: 2)
        *   As a Housekeeping Manager, I want basic inventory tracking for key housekeeping supplies (e.g., linens, towels, toiletries) within the system, so that stock levels can be monitored.

### Epic 7: Advanced Reporting & Analytics

*   **Goal:** Provide deeper insights and decision-making tools for managers.
*   **User Stories:**
    *   **Title:** AI Forecasting Integration (Dashboard) (Size: 5)
        *   As a Hotel Manager, I want to see AI-driven forecasting for occupancy and revenue integrated into the dashboard, so that I can anticipate future performance.
    *   **Title:** Standard Financial Reports (Dashboard) (Size: 3)
        *   As a Hotel Manager, I want standard financial reports (e.g., basic P/L, revenue breakdowns by source) available in the dashboard, so that I can track financial health.
    *   **Title:** Dynamic Pricing / Competitor Analysis Tools (Size: 8)
        *   As a Hotel Manager, I want tools for managing dynamic pricing strategies and viewing competitor rate analysis (as outlined in `MajorGoals.md`), so that I can optimize revenue (RevPAR, ADR).
    *   **Title:** Enhanced Guest Analytics (Patterns/Segmentation) (Size: 3)
        *   As a Hotel Manager, I want enhanced guest analytics, including booking patterns and segmentation, so that I can understand guest behavior better.
    *   **Title:** Use Real Analytics Data (Fix Mock Data) (Size: 2)
        *   As a Developer, I want to ensure the underlying data for sentiment and repeat guest analytics uses real data instead of mock data.

### Epic 8: Activity & Spa Management Enhancements

*   **Goal:** Add resource management and reporting to the existing Activities module.
*   **User Stories:**
    *   **Title:** Activity/Spa Resource Allocation (Size: 5)
        *   As a Spa Manager, I want to define and assign specific resources (e.g., treatment rooms, therapists) to activity/treatment time slots, so that bookings are allocated correctly and avoid conflicts.
    *   **Title:** Basic Activity Commission Reporting (Size: 2)
        *   As a Hotel Manager, I want basic reporting on staff commissions related to activity/spa bookings, so that performance can be tracked and compensated.

### Epic 9: Streamlined Guest Experience

*   **Goal:** Automate communication and improve guest interactions.
*   **User Stories:**
    *   **Title:** Automated Pre/Post-Stay Communication (Size: 3)
        *   As a Hotel Manager, I want to configure automated pre-arrival and post-stay emails/SMS messages (via SendGrid/Twilio), so that guests receive timely information and opportunities for feedback.
    *   **Title:** Automated Post-Stay Surveys & Sentiment Analysis (Size: 5)
        *   As a Hotel Manager, I want a system for sending automated post-stay surveys and analyzing feedback, including basic sentiment analysis, so that we can continuously improve service.
    *   **Title:** AI Concierge - Local Suggestions (Size: 3)
        *   As a Guest, I want the AI Concierge to provide helpful suggestions for local events, attractions, or dining based on my query, so that I can plan my stay better.

### Epic 10: F&B Enhancements

*   **Goal:** Add table management and prepare for inventory integration.
*   **User Stories:**
    *   **Title:** Table Reservation System (Visual Layout) (Size: 8)
        *   As a Restaurant Manager, I want a table reservation system, ideally with a visual layout, so that I can manage restaurant bookings efficiently.
    *   **Title:** Link F&B Sales to Inventory (Backend Logic) (Size: 2)
        *   As a Developer, I want to implement the logic to link F&B `OrderItem` records to the future inventory system (Epic 12) to track consumption automatically.
    *   **Title:** Explore Digital KOT Integration (Size: 3)
        *   As a Developer, I want to explore options for integrating with digital KOT display systems.

### Epic 11: Foundational Sales & Marketing Tools

*   **Goal:** Provide basic tools to help hotels drive direct bookings.
*   **User Stories:**
    *   **Title:** Basic Email Promotion Tools (Size: 3)
        *   As a Hotel Manager, I want basic tools to create and send simple email promotions to guest segments based on stay history or profile data, so that I can encourage repeat bookings.
    *   **Title:** Customizable Direct Booking Engine (Size: 2)
        *   As a Hotel Manager, I want the Direct Booking Engine to be easily customizable (basic branding, rate display) and demonstrably commission-free.

---

## Phase 3: Advanced Modules & Integrations

### Epic 12: Comprehensive Back-Office Management

*   **Goal:** Implement core back-office functions for full operational support.
*   **User Stories:**
    *   **Title:** Detailed Inventory Tracking (F&B, Retail, Supplies) (Size: 8)
        *   As a Stock Controller, I want detailed inventory tracking for F&B, retail, and general supplies, including stock levels, reorder points, and usage reporting, so that we can manage stock efficiently and control costs.
    *   **Title:** Auto-Decrement Inventory on Sale (Size: 2)
        *   As an F&B Manager, I want inventory levels to automatically decrease when items are sold via the POS/order system.
    *   **Title:** Procurement Module (Purchase Orders) (Size: 8)
        *   As a Purchasing Manager, I want a procurement module to create purchase orders, manage approvals, and track receiving, so that purchasing is streamlined.
    *   **Title:** Vendor Management System (Size: 5)
        *   As an Accounts Manager, I want a vendor management system to track supplier contracts, contacts, and basic payment information, so that vendor relationships are managed effectively.
    *   **Title:** Basic Event Management Module (Size: 5)
        *   As an Events Coordinator, I want basic event management features for booking function spaces, managing event billing, and allocating resources/staff, so that small events can be handled within the PMS.

### Epic 13: Comprehensive HR Management Module

*   **Goal:** Build a dedicated HR module covering the employee lifecycle.
*   **User Stories:**
    *   **Title:** Recruitment / Applicant Tracking System (ATS) (Size: 5)
        *   As an HR Manager, I want a recruitment/applicant tracking system within Sphynx, so that I can manage hiring processes.
    *   **Title:** Employee Document Management (Size: 5)
        *   As an HR Manager, I want the employee database to support document management (contracts, visas, certifications), so that employee records are complete and compliant.
    *   **Title:** Payroll Processing / Integration (Size: 8)
        *   As an HR Manager, I want basic payroll processing capabilities or robust integration with common payroll systems.
    *   **Title:** Rota / Schedule Management Tools (Size: 8)
        *   As a Department Manager, I want tools for creating, publishing, and managing staff rotas/schedules.
    *   **Title:** Training / Compliance Tracking (Size: 3)
        *   As an HR Manager, I want modules for tracking employee training and compliance requirements.
    *   **Title:** Leave / Holiday Management (Size: 5)
        *   As an Employee, I want a system to request and track leave/holiday entitlement.
    *   **Title:** Performance Review Tools (Size: 3)
        *   As a Manager, I want tools to conduct and record formal performance reviews.

### Epic 14: Key Third-Party Integrations

*   **Goal:** Connect Sphynx seamlessly with essential external hotel systems.
*   **User Stories:**
    *   **Title:** Deep POS Integration (Order Sync - Square/Toast) (Size: 13)
        *   As a Hotel Manager, I want deep integration with popular POS systems (e.g., Square, Toast) for two-way order synchronization (not just printing), so that F&B operations are unified.
    *   **Title:** Door Lock System Integration (Keys - Assa/Salto) (Size: 13)
        *   As a Hotel Manager, I want integration with common door-locking systems (e.g., Assa Abloy, Salto) for key card generation or mobile key functionality linked to check-in/out.
    *   **Title:** Additional Payment Gateway Support (Adyen/PayPal) (Size: 8)
        *   As a Hotel Manager, I want support for additional payment gateways (e.g., Adyen, PayPal, relevant local providers) beyond Stripe, including robust deposit management, so that I have flexibility and potentially lower costs.
    *   **Title:** Accounting Package Integration (Xero/QuickBooks) (Size: 13)
        *   As an Accountant, I want integration with common accounting packages (e.g., Xero, QuickBooks) to automatically export financial data (folios, payments, revenue), so that bookkeeping is simplified.
    *   **(Lower Priority Integration User Stories)** (Size: TBD)
        *   *(Lower Priority User Stories for other integrations like Phone, WiFi, CCTV, Energy Management, Legacy Hardware to be detailed based on partner demand)*

### Epic 15: Existing PMS Data Migration Wizard

*   **Goal:** Provide a guided process for hotels to import core data (guests, reservations, rates) from their existing PMS into Sphynx, minimizing manual effort. Leverage AI for parsing where possible.
*   **User Stories:**
    *   **Title:** Migration Wizard UI Framework (Size: 5)
        *   As a Hotel Manager, I want a step-by-step wizard interface for migrating data, so that the process is clear and guided.
    *   **Title:** Guest Data Import & Mapping (CSV/AI) (Size: 8)
        *   As a Hotel Manager, I want to upload guest profile data (e.g., CSV export) and have the wizard map or use AI to parse fields (name, contact, history notes) into Sphynx guest profiles, so that guest records are transferred.
    *   **Title:** Reservation History Import & Mapping (CSV/AI) (Size: 13)
        *   As a Hotel Manager, I want to upload past reservation data (e.g., CSV) and have the wizard map or use AI to parse fields (guest, dates, room, rate, notes) into Sphynx booking records, so that historical context is preserved.
    *   **Title:** Future Bookings Import & Mapping (CSV/AI) (Size: 8)
        *   As a Hotel Manager, I want to upload future reservation data (e.g., CSV) and have the wizard map or use AI to parse and create corresponding active bookings in Sphynx, so that ongoing operations are not disrupted.
    *   **Title:** Room Type & Rate Plan Import (CSV/AI) (Size: 5)
        *   As a Hotel Manager, I want to upload room type and rate plan data (e.g., CSV) and have the wizard map or use AI to parse and create these structures in Sphynx, so that the hotel's inventory and pricing setup is replicated.
    *   **Title:** Data Validation & Error Reporting during Import (Size: 5)
        *   As a Hotel Manager, I want the migration wizard to validate imported data, flag errors or inconsistencies (e.g., invalid dates, missing required fields), and provide clear reports, so that I can correct issues before finalizing the import.
    *   **Title:** AI Parsing Engine for Common PMS Exports (Size: 8)
        *   As a Developer, I want to enhance the AI parsing engine (used for menus/activities) to handle common data structures found in exports from major legacy PMS systems, reducing the need for manual mapping during migration.

### Epic 16: Scalability & Usability Enhancements

*   **Goal:** Improve usability for multi-property managers and ensure long-term scalability.
*   **User Stories:**
    *   **Title:** Multi-Property Dashboard Toggle (Size: 3)
        *   As a Multi-Property Manager, I want a toggle or dropdown in the manager dashboard to easily switch context between the different hotels I manage, so that I can oversee operations efficiently.
    *   **Title:** Module Enable/Disable Interface (Size: 2)
        *   As a Hotel Manager, I want a clear interface to enable or disable major optional modules (like F&B, Spa/Activities) for my property, so that I only pay for and use the features I need.
    *   **Title:** Continuous Cloud Optimization (Ongoing) (Size: N/A)
        *   As a DevOps Engineer, I want to continuously monitor and optimize cloud infrastructure for performance, cost-efficiency, and scalability as the user base grows.

### Epic 17: Differentiating AI Features

*   **Goal:** Enhance and implement unique AI capabilities.
*   **User Stories:**
    *   **Title:** AI Personalized Recommendations (Upselling) (Size: 13)
        *   As a Guest, I want the AI Concierge to provide personalized recommendations for dining, activities, or upgrades based on my profile, past behavior, or current context, so that my experience is enhanced and the hotel can upsell effectively.
    *   **(Further AI User Stories)** (Size: TBD)
        *   *(Further user stories based on refining AI chat, forecasting, dynamic pricing, etc.)* 
