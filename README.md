# Import-Data-using-Transform-Maps-Spreadsheet-

# Employee Data Management using ServiceNow Import Sets and Transform Maps

An automated, duplicate-safe employee data management solution implemented on the ServiceNow platform. This project replaces manual data entry with a repeatable bulk import framework that stages, validates, and maps spreadsheet records into a target database while providing real-time data insights via interactive HR dashboards.

## 👥 Team Details
* **Team ID:** SWTID-2026-6228
* **Team Members:**
  * **Sabibaa Bhanu B** (Team Lead)
  * **Sridevi G** (Member)
  * **Kotteeswari G** (Member)
  * **Aswathi S** (Member)
  * **Potturu Charuhasini** (Member)

---

## 🚀 Project Overview
In enterprise environments, employee records are frequently updated and shared via external spreadsheet files. Manual record management is highly error-prone and generates massive duplicate histories. 

This solution uses **ServiceNow System Import Sets** to temporarily stage raw `.xlsx` data, then applies a customized **Transform Map** to dynamically push records to a target table (`u_employee_test`). By setting a strict **Coalesce on Employee ID**, the architecture prevents data redundancy—automatically updating existing records and inserting new entries uniquely.

### Core Key Features
* **Bulk Data Ingestion:** Rapid processing of Excel (`.xlsx`) datasets instead of row-by-row manual input.
* **Data Integrity & De-duplication:** Enforced through conditional field mapping and `Coalesce` constraints on primary fields.
* **Role-Based Reporting:** Real-time visibility into employee metrics broken down by location and operational department.

---

## 🛠️ Technology Stack
* **Core Platform:** ServiceNow
* **Data Ingestion:** System Import Sets (Load Data & Import Set Tables)
* **Data Mapping & Logic:** Transform Maps (Field Maps & Coalesce configuration)
* **Target Database:** Custom Employee Test Table (`u_employee_test`)
* **Analytics Engine:** ServiceNow Reports and Dashboards

---

## 📊 System Architecture & Data Flow
1. **Source Layer:** Google Sheets / Microsoft Excel spreadsheet containing raw employee data.
2. **Staging Layer (Import Set Table):** Data acts as a temporary buffer to undergo automated validation checks.
3. **Processing Layer (Transform Map):** Matches fields (ID, Name, Email, Department, Location) and applies the `Coalesce` rule to determine update vs. insert actions.
4. **Target & Presentation Layer:** Data landing in the `u_employee_test` table populates the **Employee Analytics Dashboard**.

---

## 📈 Dashboard Analytics
The platform leverages customized reporting visual panels to view:
* **Employee List Report:** Full tabular overview of current active workforce details.
* **Employees by Location:** Geographical breakdown tracking employee concentrations.
* **Employees by Department:** Visual pie charts analyzing operational metrics (e.g., ServiceNow vs. Salesforce distribution).

---

## 🔮 Future Scope
* Schedule fully automated file retrievals using Scheduled Data Imports from external cloud environments.
* Introduce programmatic validation using advanced Transform Map scripts.
* Implement custom HR email notifications utilizing ServiceNow email engines for handling failed transforms.
* Transition the framework from file ingestion to scalable REST API / Integration Hub endpoints.
*