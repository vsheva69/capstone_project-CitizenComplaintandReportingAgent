# 📮 COMPLAINT AGENT — CITIZEN COMPLAINT AUTOMATION SYSTEM  
✨ *Powered by Google Agent Development Kit (ADK)*

---
## 📝 **PROJECT DESCRIPTION**
This project contains the core logic for the Complaint Agent (`complaint_agent`), a system designed to streamline and automate citizen complaint handling. The agent is built using the Google Agent Development Kit (ADK) and focuses on immediate classification, routing, and monitoring of public feedback to ensure swift governmental response.

---

## 📘 **USE CASE: CITIZEN COMPLAINT AND REPORTING AGENT**
**Description:** Automatically receives and classifies citizen reports/complaints by urgency, routes them to the correct governmental department, and monitors follow-up status until resolution.

**Benefit:** Ensures rapid response and accountability in handling public issues.

---

## ❗ **PROBLEM STATEMENT**
Manually managing citizen reports is inherently inefficient and prone to error. Public complaints arrive through diverse channels (social media, calls, web forms) and must be manually reviewed, categorized, prioritized (urgency), and forwarded to the correct departmental unit (e.g., Public Works vs. Environment).

This manual triage process leads to:

- **Response Delays:** Slow classification means critical issues (like infrastructure failure) face significant latency.  
- **Misrouting:** Mistakes in identifying the responsible agency lead to circular referrals and citizen frustration.  
- **Lack of Accountability:** Without automated tracking, monitoring the status and completion of a follow-up action is difficult, reducing public trust.

---

## 💡 **SOLUTION STATEMENT**
AI Agents can automatically process incoming reports, overcoming the limitations of manual triage. The Complaint Agent (`complaint_agent`) uses the Gemini model's reasoning capabilities combined with specialized tools to:

1. **Analyze and Extract:** Instantly read the complaint text (from any input format) and extract key entities, location, severity, and implied category (`e.g., Infrastructure, Health, Administration`).

2. **Automate Triage:** Use predefined tools/rules to match the extracted category against the governmental organizational structure, determining the correct responsible Department (Agency) and prioritizing the response queue (`High / Medium / Low urgency`).

3. **Transparent Monitoring:** Provide an automated interface for citizens to check the real-time status of their reports using a unique Report ID, and enable authorized updates to the report lifecycle, ensuring full transparency from submission to resolution.

4. **System Integration:** Automatically log the complaint into the central database and trigger notifications to the responsible unit, effectively turning the manual administrative chore into a streamlined, data-driven workflow.

---

## 🏛️ **ARCHITECTURE OVERVIEW**
The core of this system is the Complaint Agent (`complaint_agent`), which functions as the primary orchestrator. Its definition includes:

- **model:** Utilizing a fast, reliable model like gemini-2.5-flash for rapid classification and reasoning.  
- **system_instruction:** A strict set of instructions guiding the agent to prioritize information extraction and compulsory tool use.  
- **tools:** Essential utilities defined to interact with external government systems and knowledge bases.

### 🔄 **Workflow — Chain of Responsibility:**  
The Agent analyzes the report, determines the category and urgency, and uses its specialized tools to validate the routing path and record the data.

---

## 🧰 **ESSENTIAL TOOLS AND UTILITIES (5 Tools)**  
The `complaint_agent` is equipped with specific, reliable tools to interact with backend government systems.

### 1. **Routing Logic**  (`tentukan_unit_penanggung_jawab`) 
🧭 **Function:** Receives the raw category and returns the official name of the responsible Department (e.g., "Public Works Department (PWD)").

### 2. **Complaint Logging**   (`catat_laporan`)
🗂️ **Function:** Simulates logging the data into the central complaint database and generates a unique Report ID (e.g., LAP-4521).

### 3. **Urgency Checker**   (`check_urgency_level`)
⏱️ **Function:** Analyzes the description of a report to classify its urgency (High, Medium, or Low) based on predefined keywords.

### 4. **Knowledge Base Search** (`search_knowledge_base`)  
📚 **Function:** Allows the Agent to search for answers, FAQs, or procedural guidance for general inquiries using real-time results.

### 5. **Status Monitor & Updater**  (`monitor_and_update_status`)
🔄 **Function:** Enables the Agent to both retrieve the current status of an existing report (using its unique Report ID) and update that status upon authorization.

### 6. **Location Verifier** (`verify_incident_location`)
📍 **Function**: Verifies and determines the precise geographical coordinates of the reported incident to provide accurate location data to the response team.

---

## 🧾 **CONCLUSION**
The Citizen Complaint and Reporting Agent demonstrates the immediate value of AI Agents in enhancing public service delivery. The system transforms the time-consuming and error-prone process of manual report triage into a fast, transparent, and accountable workflow.

---

## 📈 **Value Statement**  
Implementing the Complaint Agent is projected to reduce the average time from report submission to responsible agency notification from **4 hours** (manual) to **under 5 minutes**.

---

## 🗺️ **If I Had More Time**  
I would integrate the system with a third-party mapping tool (via an additional specialized tool) to automatically verify and resolve the exact geographic coordinates of the reported incident.

## 🗺️ **If I Had More Time**  
I would integrate the system with a third-party mapping tool (via an additional specialized tool) to automatically verify and resolve the exact geographic coordinates of the reported incident.
