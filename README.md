

# 🛠️ Citizen Complaint and Reporting Agent

**Automating Triage and Accountability in Public Service**

---

## 📌 Overview

The **Complaint Agent (`complaint_agent`)** is an AI-powered system designed to automate the classification, routing, and monitoring of citizen complaints. Built using the **Google Agent Development Kit (ADK)**, it enables rapid and accurate processing of public reports, ensuring faster government response and increased accountability.

---

## 🚀 Key Features

* **Automatic Classification** of complaint categories & severity
* **Intelligent Routing** to responsible government departments
* **Complaint Logging** with unique Report ID generation
* **Real-time Monitoring** of follow-up status
* **Modular Architecture** powered by Google ADK tools

---

## 📘 Use Case: Citizen Complaint and Reporting Agent

### **Description**

Automatically receives and classifies citizen reports, determines urgency, routes the issue to the correct department, and tracks resolution progress.

### **Benefits**

* Faster government response
* Reduced human error
* Improved transparency and accountability
* Efficient use of administrative resources

---

## ❗ Problem Statement

Handling citizen reports manually creates bottlenecks:

* **Delayed responses** due to manual triage
* **Misrouting** between departments
* **Weak accountability** without automated tracking
* **High administrative workload** for repetitive tasks

As reports come from diverse channels (social media, calls, web forms), staff struggle to review, categorize, prioritize, and route them consistently.

---

## 💡 Solution

The **Complaint Agent** automates end-to-end handling of complaints using AI reasoning and structured tools.

### **1. Analyze & Extract**

The agent extracts:

* Entities
* Location
* Severity
* Category (e.g., Infrastructure, Environment, Health)

### **2. Automated Triage**

Uses rules + tools to:

* Map categories to government departments
* Assign urgency (High / Medium / Low)

### **3. System Integration**

The agent:

* Logs complaints into the central database
* Generates a unique **Report ID**
* Notifies responsible units instantly

---

## 🏛️ Architecture

The system uses a modular ADK-based structure where the **Complaint Agent** acts as the orchestrator.

### **Agent Components**

* **Model:** `gemini-2.5-flash`
* **System Instructions:** Strict flow enforcing extraction → classification → tool calls
* **Tools:** For routing, logging, and utilities

### **Workflow**

1. Citizen submits a report
2. Agent analyzes text & extracts details
3. Category + urgency classified
4. Tool calls validate routing & log complaint
5. System responds with routed department & Report ID

---

## 🧰 Tools

### **🔧 1. `tentukan_unit_penanggung_jawab` (Routing Logic)**

* Maps raw category to an official department
* Normalizes text (case-insensitive, cleaned)
* Prevents misrouting
* Example:

  * “jalan rusak” → **Public Works Department (PWD)**

---

### **📝 2. `catat_laporan` (Complaint Logging)**

* Saves:

  * Title
  * Description
  * Category
* Generates a **unique Report ID (e.g., LAP-4521)**
* Ensures immediate accountability

---

### **⏱️ 3. `check_urgency_level` (Future Tool)**

Intended to:

* Detect urgent keywords (“fire”, “flood”, “collapse”)
* Auto-flag High Urgency cases
* Trigger real-time alerts

---

## 📈 Value Impact

Implementation reduces complaint routing time from:

⏳ **4 hours** (manual)
➡️
⚡ **< 5 minutes** (automated)

This leads to:

* Higher citizen satisfaction
* Improved public trust
* Stronger workflow transparency
* More efficient government operations

---

## 🗺️ Future Enhancements

If extended further:

* Integration with mapping tools to extract precise geographic coordinates
* Dashboard for real-time monitoring of complaint statuses
* Analytics for policy support and public service improvements

---

## 📂 Repository Structure (Optional Suggestion)

```
.
├── complaint_agent/
│   ├── agent.py
│   ├── tools/
│   │   ├── routing.py
│   │   ├── logging.py
│   │   └── utils.py
├── examples/
│   └── sample_complaints.json
├── README.md
└── requirements.txt
```

---

## 🧑‍💻 Tech Stack

* **Google Agent Development Kit (ADK)**
* **Gemini Model (2.5 Flash)**
* **Python 3.10+**
* (Optional) PostgreSQL / Firestore for logging

---

## 📬 Contact

If you have suggestions, questions, or need improvements, feel free to open an **Issue** or a **Pull Request**.

---


Cukup beri tahu!
