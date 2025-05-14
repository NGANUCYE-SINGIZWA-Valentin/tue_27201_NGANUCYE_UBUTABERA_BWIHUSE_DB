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





















































