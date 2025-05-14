# 👤 IDENTIFICATION

### Name: NGANUCYE SINGIZWA Valentin
### ID: 27201
### Course: Database Development with PL/SQL (INSY 8311)
### Lecturer: Eric Maniraguha
### Academic Year: 2024–2025
### GROUP B




# ⚖️ UBUTABERA BWIHUSE (Fast Justice) – Phase I

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

⚙️ Reduce delays in civil case resolutions.

📈 Support decision-makers with accurate reports on case timelines and bottlenecks.

🤖 Assign cases automatically to the right courts and judges.

🚨 Alert the system when a case is taking too long.

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

✅ Auto-assign cases to judges based on specialization and court jurisdiction

⏰ Flag overdue cases to help courts take quick action

📊 Track performance of courts and judges using resolution time data

🧠 Support data-driven reforms in the justice system

## 🚀 Expected Outcomes

The successful implementation of this system is expected to:

⏱️ Reduce the time required to resolve civil cases, especially divorces

⚖️ Ensure justice is delivered fairly and without unnecessary delay

🏛️ Improve court efficiency by streamlining workflows

📢 Promote transparency in legal processes and public trust in justice

📉 Help reduce social issues like violence, stress, and instability related to unresolved legal conflicts

📚 Provide clear data insights for government and judicial reforms












