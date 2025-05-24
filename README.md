# 👤 IDENTIFICATION

### Name: NGANUCYE SINGIZWA Valentin
### ID: 27201
### Course: Database Development with PL/SQL (INSY 8311)
### Lecturer: Eric Maniraguha
### Academic Year: 2024–2025
### GROUP B




# ⚖️ UBUTABERA BWIHUSE (Fast Justice) SYSTEM – Phase I

### 📌 Overview
In Rwanda’s legal system, criminal cases are often resolved relatively quickly. However, civil cases especially divorce proceedings suffer from long delays, sometimes taking over a year (average 454 days) to reach a resolution. This growing backlog is not just a legal issue; it’s a serious social problem. The consequences of delayed civil justice are real and widespread causing: 
- 🏚️Increased domestic violence and family instability.
- 😞Rising levels of mental health issues.
- ⚖️Reduced public trust in the legal justice system.
- 🚨 Rising crime rates linked to unresolved disputes

In 2016, Rwanda recorded only 21 divorce cases. By 2024, that number had exploded to 2,833 cases. These numbers tell a deeper story- one of real people caught in the cracks of a slow system.

To address this urgent issue, this project introduces “Ubutabera Bwihuse”, which means “Fast Justice” in Kinyarwanda. It is a PL/SQL-based Oracle database solution that aims to streamline the resolution of civil cases in Rwanda. The goal is to leverage technology to automate processes, monitor performance, and help the judiciary deliver justice faster and more fairly.


 

## 🎯Project Objective

### The main goal is to build a database that helps:

- ⚙️ Reduce delays in civil case resolutions.

- 📈 Support decision-makers with accurate reports on case timelines and bottlenecks.

- 🤖 Assign cases automatically to the right courts and judges.

- 🚨 Alert the system when a case is taking too long.

  

## 👥 Who Will Use It?

- 👩‍⚖️ Judges – to manage workloads and track performance.

- 🏛️ Court Administrators – to monitor delays and allocate resources.

- 🧑‍💼 Policy Makers – to access trend data and plan reforms.

- 👨‍👩‍👧‍👦 Citizens – to get faster, fairer resolutions for their legal issues.




## 🧱 What the System Includes

The system is built around the following entities:

### Entity & Description
| 🧩 **Entity Name** | 📄 **Description**                                                                                    |
| ------------------ | ----------------------------------------------------------------------------------------------------- |
| `Cases`            | Stores all case details such as case type, filing/resolution dates, status, court, and judge involved |
| `Courts`           | Represents court locations and jurisdictions                                                          |
| `Judges`           | Contains judge names and their legal specialization                                                   |
| `Litigants`        | Individuals involved in each case, with contact and role info                                         |
| `LegalProcedures`  | Step-by-step process for each type of case, including expected duration                               |
| `CaseLitigants`    | Junction table to manage the many-to-many relationship between cases and litigants                    |


  
### Relationships include:

- One court → many cases

- One judge → many cases

- Many litigants ↔ many cases (via linking table)



## ⚙️ Main Features (Business Logic)

- ✅ Auto-assign cases to judges based on specialization and court jurisdiction.

- ⏰ Flag overdue cases to help courts take quick action.

- 📊 Track performance of courts and judges using resolution time data.

- 🧠 Support data-driven reforms in the justice system.




## 🚀 Expected Outcomes

The successful implementation of this system is expected to:

- ⏱️ Reduce the time required to resolve civil cases, especially divorces.

- ⚖️ Ensure justice is delivered fairly and without unnecessary delay.

- 🏛️ Improve court efficiency by streamlining workflows.

- 📢 Promote transparency in legal processes and public trust in justice.

- 📉 Help reduce social issues like violence, stress, and instability related to unresolved legal conflicts.

- 📚 Provide clear data insights for government and judicial reforms.




# 🧩 PHASE II: BUSINESS PROCESS MDEL 🏛️📈🧠


The Ubutabera Bwihuse BPMN diagram illustrates the key steps in managing and resolving civil cases in Rwanda’s legal system, focusing on divorces. The process begins with litigants submitting their case, which is then recorded by a clerk. An automated system assigns the case to a judge based on jurisdiction and specialization. The system continuously monitors the time taken for resolution. If the case exceeds the expected duration, an alert is triggered for supervisor intervention. After resolution, the system logs performance data, which is then used by the Ministry of Justice for decision-making through MIS reports.

 ### A BPMN Model Image

 <img width="794" alt="Screenshot 2025-05-11 153359" src="https://github.com/user-attachments/assets/6e5a0039-c15c-4f9c-adf0-c3d60367d70c" />




## 🧭 Step-by-Step Process Description

### Step 1

 📥 Case Submission by Litigants
The process starts when individuals involved in a civil dispute (e.g., divorce) submit their case through a public intake system or directly at a courthouse.

### Step 2

 🧾 Case Recording by Court Clerk
A clerk enters all case details (case type, litigants, filing date, etc.) into the system, initiating the workflow.

### Step 3

 🤖 Automated Assignment to Judge
Using built-in PL/SQL logic, the system automatically assigns each case to a judge based on:

- The jurisdiction of the court.

- The specialization of the judge (e.g., family law).

### Step 4

⏱️ Case Monitoring
The system monitors how long the case remains unresolved. Each case type has a target resolution timeframe based on historical legal procedure data.

### Step 5

🚨 Alert Generation for Delays
If a case exceeds the expected time, an alert is sent to a supervising authority (e.g., court manager or administrative judge) to intervene or follow up.

 ### Step 6
 
 ✅ Case Resolution
Once a decision is reached, the judge marks the case as resolved. The outcome and closing date are entered into the system.

### Step 7

📊 Performance Logging
After resolution, the system logs:

- Resolution time.

- Judge’s performance.

- Case complexity (optional).

- Any delays and interventions.

### Step 8

📤 MIS Reporting to Ministry of Justice
The data collected is automatically compiled into reports accessible to the Ministry of Justice, enabling:

- Insight into systemic delays.

- Performance comparisons between courts.

- Evidence-based legal reforms.


Once a case is resolved and closed in the system, all the information related to how that case was handled (how long it took, who handled it, whether it was delayed, etc.) is stored in the database.This information is then used by the system to automatically generate reports, which are shared with the Ministry of Justice.

### 🧠 What Is MIS?
MIS stands for Management Information System. It’s a computerized system that helps managers and government officials make better decisions using data.

In this context, the MIS takes case data from the court system and transforms it into meaningful insights like:

- 📊 How long cases are taking to be resolved in each court

- 👩‍⚖️ Which judges have the most or least delays

- 🏛️ Which courts are overloaded

- 📅 How many cases were resolved this month or this year

- 🚨 Where the most delays or problems are happening

### 🧩 Why It Matters
This reporting helps the Ministry of Justice (or other government leaders) to:

- See which courts are doing well and which are struggling

- Know where to send more judges or resources

- Create new policies to fix recurring problems

- Make the whole justice system more transparent and accountable to the public

### ✅ In Summary:
The MIS takes the raw data from the case management system and turns it into clear reports for the Ministry of Justice. These reports help improve planning, fairness, and efficiency in Rwanda’s civil court system.



# 🧩 Phase III: Logical Model Design 🗂️🛠️🔗
### 📘 Overview
In Phase III of the Ubutabera Bwihuse (Fast Justice) project, the focus is on transforming the conceptual idea of the justice system into a well-structured logical data model. This phase ensures that all necessary data elements are clearly defined, related, and ready for implementation in the Oracle PL/SQL environment.

The logical model is the foundation for building the actual database. It describes what data will be stored, how different entities relate to each other, and which rules or constraints will be applied to maintain data integrity. It serves as a blueprint for the physical implementation in later phases.


### Here is a detailed breakdown of your six entities and their key attributes:

| 🧩 Entity           | 🔑 Primary Key           | 🧾 Key Attributes                                                        |
| ------------------- | ------------------------ | ------------------------------------------------------------------------ |
| **Cases**           | `CaseID`                 | CaseType, FilingDate, ResolutionDate, Status, CourtID (FK), JudgeID (FK) |
| **Courts**          | `CourtID`                | Location, Jurisdiction                                                   |
| **Judges**          | `JudgeID`                | Name, Specialization                                                     |
| **Litigants**       | `LitigantID`             | Name, ContactInfo, Role                                                  |
| **LegalProcedures** | `ProcedureID`            | CaseType, StepDescription, ExpectedDuration                              |
| **CaseLitigants**   | (`CaseID`, `LitigantID`) | (Junction table for many-to-many link between Cases and Litigants)       |



## 🔗 Relationship Summary Table

| 👥 Entities Involved           | 🔁 Relationship Type | 🔑 Foreign Key Reference           | 🔢 Cardinality     | ✅ Valid |
|-------------------------------|-----------------------|------------------------------------|--------------------|---------|
| CaseTypes → LegalProcedures  | One-to-Many           | `LegalProcedures.CaseType` → `CaseTypes.CaseType` | 1 ➝ *              | ✅       |
| CaseTypes → Cases            | One-to-Many           | `Cases.CaseType` → `CaseTypes.CaseType`           | 1 ➝ *              | ✅       |
| Courts → Cases               | One-to-Many           | `Cases.CourtID` → `Courts.CourtID`               | 1 ➝ *              | ✅       |
| Judges → Cases               | One-to-Many           | `Cases.JudgeID` → `Judges.JudgeID`               | 1 ➝ *              | ✅       |
| Cases ↔ Litigants (via CaseLitigants) | Many-to-Many   | `CaseLitigants.CaseID`, `LitigantID` ↔ `Cases`, `Litigants` | * ↔ *              | ✅       |



## Logical Model Design Image

The diagram below shows the main entities and relationships in the Ubutabera Bwihuse system. It clearly illustrates how cases are linked to courts, judges, litigants, and legal procedures, forming the foundation for the database structure.
The ER diagram provides a visual overview of the normalized data model for this PL/SQL-based system. It captures key entities, attributes, and their interconnections to support efficient data organization and integrity.



<img width="928" alt="image" src="https://github.com/user-attachments/assets/f1283881-fb24-4b3a-b488-2813b5e9af73" />


## 🧪 Handling Real-World Data Scenarios

The following scenario demonstrates how the Ubutabera Bwihuse database model can manage a complete civil case—from submission to resolution—and support decision-making through MIS reports.

#### Divorce Case of Mr. & Mrs. Uwimana

Mr. Jean Uwimana and Mrs. Claudine Uwimana file for divorce at Nyarugenge Civil Court. The case is registered under CaseID `C0001`, linked to Judge Umwali (specialized in family law), and involves both litigants as Plaintiff and Defendant. The system monitors the resolution time and triggers an alert when the case exceeds 61 days. After 69 days, the judge finalizes the case, and performance data is logged. MIS reports are generated showing delays and court efficiency.



# 🧩 Phase IV: Database Creation and Setup 🗃️🛡️
### 📘 Overview
In Phase IV, the goal is to turn the logical model into an actual Oracle database environment. This involves creating a new user schema where all tables, data, and PL/SQL objects will live. Once the schema is created, it's connected to Oracle tools like SQL Developer or Oracle Enterprise Manager (OEM) for management and monitoring.

This setup ensures the system is secure, accessible, and ready for development in future phases.


### 📸 Screenshots Included
Below are screenshots that demonstrate the successful setup:

1️⃣ User Schema Created
This screenshot shows the command to create the user and grant DBA privileges.

<img width="959" alt="PDB CREATION" src="https://github.com/user-attachments/assets/9b725af1-4057-4f12-adbd-a7d4b0fedcbb" />

2️⃣ Oracle Enterprise Manager

<img width="959" alt="oracle enterprise manager(OEM)" src="https://github.com/user-attachments/assets/c13bdfb6-e486-48a8-b258-a9834c215ebd" />



# 🧩 Phase V: Table Implementation and Data Insertion 🧱💾

### 📘 Overview

In this phase, we create all tables based on the logical model from Phase III and insert meaningful data that reflects real-life legal case scenarios in Rwanda. This step is critical for:

- Testing queries and procedures in later phases

- Validating the structure and relationships between entities

- Simulating civil case workflows (e.g., divorce case lifecycle)


#### 📸 Screenshots Included

1️⃣ All in one Tables Creation

<img width="959" alt="ALL IN ONE TABLE CREATION" src="https://github.com/user-attachments/assets/5f960301-7ee9-4fdd-94fb-67018adf1e4b" />


2️⃣ Data Insertion

### Inserting Into Judges Table

<img width="959" alt="INSRT JUDGES TB " src="https://github.com/user-attachments/assets/f1aa9e2c-4701-4f44-b67f-2efb55fd6003" />


### Inserting Into Litigant Table

<img width="956" alt="INSRT IN LITIGANT TB" src="https://github.com/user-attachments/assets/aedc49f5-4e95-4e36-89d9-4728c292f103" />

### Inserting Into Legal Procedures Table

<img width="948" alt="LEGAL PROCEDURES TB" src="https://github.com/user-attachments/assets/8ab6720f-6505-46d7-9354-5d630aff4325" />

### Inserting Into Cases Table

<img width="956" alt="INSRT CASES TB" src="https://github.com/user-attachments/assets/05390d84-8925-4399-b67f-227d2fed2ae6" />

### Inserting Into Courts Table

<img width="956" alt="INSRT IN COURTS TB" src="https://github.com/user-attachments/assets/954c21bc-45fa-4adf-9b67-b8085f781476" />

### Inserting Into Case Litigant Table

<img width="956" alt="CASELITIGANT" src="https://github.com/user-attachments/assets/c0eacf77-64d3-4196-8c37-e9268a1ba596" />



# 🧩 Phase VI: Database Interaction and Transactions 🔄🧑‍💻📊

### 📘 Overview

In Phase VI, the project transitions from static data to dynamic interaction with the database. This phase focuses on writing and executing PL/SQL programs to perform real-time tasks such as retrieving data, updating case statuses, calculating delays, and generating insights.

Through the use of procedures, functions, cursors, exception handling, and packages, the system becomes intelligent and responsive—capable of automatically managing court processes and helping legal administrators make better decisions.

This phase demonstrates how the Ubutabera Bwihuse (Fast Justice) system can be used not only to store legal data but also to process and analyze it in real time, simulating real-world operations in the justice system of Rwanda.


### 💡 Why This Phase Matters

This phase brings your database to life. Courts don't just collect information—they need to interact with it, detect delays, assign resources, and take action. Phase VI proves your system is not just a data container but a functional tool for justice efficiency.

By simulating daily court operations, this phase prepares your project for full integration with reports, dashboards, and judicial monitoring systems in later phases.



### 🔍 1. Define a Simple Problem Statement (Using Windows Functions)
### Problem Statement:

Identify the top 3 fastest judges in terms of average case resolution time, grouped by court. This will help the Ministry of Justice reward high-performing judges and balance workloads more fairly across courts.

We’ll solve this using a Window Function: RANK() OVER(PARTITION BY CourtID ORDER BY AvgDays ASC).



### 🔁 1. Function: Count Total Cases by Judge

<img width="959" alt="image" src="https://github.com/user-attachments/assets/321b8630-acc1-4db0-ab6e-8a5d929b526c" />

🧪 Function Test or Calling

<img width="959" alt="image" src="https://github.com/user-attachments/assets/aa1e55e2-1268-479f-89e5-a5c779358a4f" />


### 🔍 2. Procedure: Show Resolved Cases by Judge

<img width="959" alt="image" src="https://github.com/user-attachments/assets/4b94cd08-d4be-43cd-8c43-01013807680a" />


🧪 Procedure Test or Calling

<img width="956" alt="image" src="https://github.com/user-attachments/assets/8c8dab96-f0fc-434e-a11f-1c0d1595cb69" />


### 📦 3. Package: CaseTools (Function + Procedure)

<img width="959" alt="image" src="https://github.com/user-attachments/assets/a73b9dd4-9ce6-4b90-93ea-32121f7eca8b" />

🧪 Package Function and Procedure Test in Package

<img width="959" alt="image" src="https://github.com/user-attachments/assets/aa4e8d86-0f85-472e-bad0-a58980349a78" />


## 💾 4. DML OPERATIONS (Data Manipulation Language)

 🔁 INSERT

<img width="959" alt="image" src="https://github.com/user-attachments/assets/fff562d1-01be-4d02-86e3-b0181c0338aa" />


🔄 UPDATE


<img width="959" alt="image" src="https://github.com/user-attachments/assets/324aa4bd-7f23-4d47-9776-5a904c4b6bec" />


❌ DELETE

<img width="959" alt="image" src="https://github.com/user-attachments/assets/bb14a610-3dec-47d1-b8ba-abfb48ae4d58" />

### 🧱 5. DDL OPERATIONS (Data Definition Language)

 CREATE TABLE example

<img width="956" alt="image" src="https://github.com/user-attachments/assets/fa08e51a-bb4a-4b68-ad09-4e2bd1811017" />

ALTER TABLE example

<img width="959" alt="image" src="https://github.com/user-attachments/assets/f8477008-44da-40ab-b39c-bb10fa07a307" />


 DROP TABLE example

<img width="959" alt="image" src="https://github.com/user-attachments/assets/a1c402db-aebe-49be-9ea9-1c8f76307eb6" />



# 🧩 Phase VII: Advanced Database Programming and Auditing – Ubutabera Bwihuse

### 1️⃣ Problem Statement and Justification
Problem Statement:
In the Ubutabera Bwihuse (Fast Justice) system, unauthorized data manipulation on weekdays and public holidays may lead to fraud, data tampering, and loss of trust in Rwanda’s judicial processes. To protect integrity, the system must restrict DML operations (INSERT, UPDATE, DELETE) during official business days and holidays, and log all such attempts for auditing.

### Justification:

🔒 Triggers prevent unauthorized data changes automatically.

🧠 Packages and procedures standardize audit logging and make logic reusable.

📋 Audit logs ensure full traceability for every action attempted.

## 2️⃣ Step-by-Step Setup and Insertion

### a) Create Holiday Table with Real Rwandan July Holidays


<img width="957" alt="HOLIDAY TABLE CREATION" src="https://github.com/user-attachments/assets/042c2b27-7c0e-4c4c-934c-90ac3424cd15" />

### Inserting real holidays for July because there are no holidays in June (

<img width="958" alt="inserting in holiday table" src="https://github.com/user-attachments/assets/8b4195b3-eeb7-4ddd-985a-4a944c94f851" />


### b) Creating Audit Log Table

<img width="955" alt="AUDIT LOG TABLE" src="https://github.com/user-attachments/assets/ba674ebf-08af-4041-a3ef-2ae00f4a796d" />

### c) Creating Auditing Package

<img width="958" alt="CREATING AUDITING PACKAGE" src="https://github.com/user-attachments/assets/d69e9408-279b-4e7a-89ed-0300dc8059f3" />

### d) Creating Sample Protected Table(case_records)

<img width="959" alt="SAMPLE TABLE OF CASERECORDS CREATED TO BE PROTECTED" src="https://github.com/user-attachments/assets/5bb43dc3-9a5c-4e85-acaa-d5bd3c6e86fb" />

### e) Creating Trigger to Block DML on Weekdays or Holidays

<img width="959" alt="TRIGGER ON CASERECORDS TABLE CREATED " src="https://github.com/user-attachments/assets/4edcb638-f333-4b95-9ec2-09c39cd30bbf" />

## 3️⃣ How to Test the Security Features

### ✅ Test 1: Try DML on a Weekday(FRIDAY 23/05/2025)

```sql
INSERT INTO case_records (case_id, case_title)
VALUES (1, 'Land dispute in Kigali');
```

<img width="987" alt="image" src="https://github.com/user-attachments/assets/eadec410-c527-4133-8e8a-95567717f574" />




### ✅ Test 2: Try DML on a Public Holiday (e.g., July 1)

### I Simulated today as a holiday 
```sql
INSERT INTO holiday_reference VALUES (TO_DATE('2025-07-04', 'YYYY-MM-DD'), 'Liberation Day');
COMMIT;
```
<img width="959" alt="image" src="https://github.com/user-attachments/assets/facbe1b8-6d2e-47a6-a79f-ef377137bd66" />

### Then I tried to insert into Case_records
```sql
INSERT INTO case_records (case_id, case_title)
VALUES (4, 'Simulated Case on Liberation Day');
```
<img width="959" alt="image" src="https://github.com/user-attachments/assets/b3577013-fb3e-44d0-a686-a75cca134942" />



### ✅ Test 3: Try DML on a Weekend (Saturday 24/05/2025)

```sql
INSERT INTO case_records (case_id, case_title)
VALUES (4, 'Family inheritance case');
```

<img width="972" alt="image" src="https://github.com/user-attachments/assets/f89bef5f-beab-449b-a7c1-846b2c65aebf" />


## 📜 Check the Audit Log Anytime

```sql
SELECT * FROM audit_log ORDER BY action_time DESC;
```

<img width="958" alt="image" src="https://github.com/user-attachments/assets/8013592f-a9c5-4c22-a3d4-1bc74cef1207" />

By implementing real-time DML restrictions tied to weekdays and public holidays, Phase VII has transformed the Ubutabera Bwihuse system into a secure, policy-compliant, and intelligent legal database. Every action is now audited, every breach attempt is logged, and data manipulation is only allowed when legally appropriate. The use of packages and triggers has ensured that the system not only protects itself, but also holds users accountable for every action. These enhancements uphold the very principles of justice that the system was built to support: fairness, transparency, and accountability.

This phase proves that the system is not just functional it is trustworthy. It respects Rwandan national holidays, adapts to judicial regulations, and provides court administrators and the Ministry of Justice with the confidence that no unauthorized changes go unnoticed.


# ***Conclusion***

The Ubutabera Bwihuse PL/SQL database system stands as a complete, intelligent solution designed to support Rwanda’s legal sector in the digital age. Through all development phases—from data modeling and table creation to analytical queries, procedural logic, and real-time auditing—the system has evolved into a tool that is robust, efficient, and deeply aligned with the needs of justice delivery.

It does more than store court cases. It tracks performance, flags inefficiencies, enforces rules, and defends the system from errors or misuse. With built-in triggers, auditing, and holiday-based restrictions, the solution offers both operational power and legal integrity.

This project not only meets academic standards but could also serve as the foundation for a real-world digital justice platform. With minimal extensions, it could integrate with case portals, user dashboards, or national e-justice frameworks.




