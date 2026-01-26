
Here are your structured study notes based on the lecture transcript.

## **Subject: Review of Data Fundamentals & RDBMS**

### **1. What is Data?**

**Definition:** Data refers to unorganized information (facts, observations, perceptions, numbers, symbols, images) that undergoes processing to become meaningful.

* **Key Insight:** The *structure* of data determines how efficiently it can be managed, stored, and analyzed.

---

### **2. The Three Main Types of Data Structures**

Data is categorized by how organized it is.

| Data Type | Definition | Key Characteristics | Examples |
| --- | --- | --- | --- |
| **Structured** | Highly organized data that follows a **predefined format**. | • Adheres to a strict **Schema**.<br>

<br>• Organized in **Rows & Columns**.<br>

<br>• Easy to search and retrieve. | • **Excel/Spreadsheets** (Cells)<br>

<br>• **SQL Databases** (Tables)<br>

<br>• **Online Forms** (Designated fields like Name, Credit Card #) |
| **Unstructured** | Lacks a specific format or organization. | • No predefined rules/sequences.<br>

<br>• Challenging to process/analyze with traditional methods. | • **Text Files** (Free-form documents)<br>

<br>• **Media** (Images, Audio, Video)<br>

<br>• **Social Media** (Tweets, mixed content) |
| **Semi-Structured** | Possesses some organizational properties but **no strict tabular structure**. | • Uses **Tags** or **Keys** to organize elements.<br>

<br>• Balances flexibility and structure.<br>

<br>• Often hierarchical. | • **JSON Files** (Arrays/Objects)<br>

<br>• **XML Documents** (Tags/Attributes)<br>

<br>• **Emails** (Structured headers like "To/From" + Unstructured body) |

---

### **3. Common File Formats for Data Transfer**

Systems use specific formats to hold or transfer data.

* **Delimited Text Files:** Data in rows, separated by a specific character.
* **CSV:** Comma-Separated Values.
* **TSV:** Tab-Separated Values.


* **Spreadsheets:** Data in rows and columns (facilitates easy human access/manipulation). Often used to create CSVs.
* **Language Files:** Encoded text with set rules for internet transfer.
* **XML:** Extensible Markup Language.
* **JSON:** JavaScript Object Notation.



---

### **4. Data Repositories**

Where data is actively stored, managed, and organized.

#### **A. Relational Databases (RDBMS)**

* **Definition:** Structured data stored in **related tables**.
* **Function:** Uses links between tables to **minimize data duplication** and preserve relationships.
* **Examples:** IBM DB2, Microsoft SQL Server, Oracle, MySQL.
* **Primary Use Case (OLTP):**
* **OLTP (Online Transaction Processing):** Systems supporting day-to-day business activities.
* **Focus:** Transactional integrity, concurrent access, fast routine operations.
* *Examples:* Customer transactions, HR workflows, ATM withdrawals.



#### **B. Non-Relational Databases (NoSQL)**

* **Definition:** flexible databases designed to handle diverse or **unstructured data**.
* **Examples:** MongoDB (Document-oriented), Cassandra, Redis.
* **Use Case:** When data doesn't fit into strict tables (e.g., massive social media feeds, sensor data).

#### **C. OLAP (Online Analytical Processing)**

* **Definition:** Systems focused on **querying and analyzing** large datasets to extract insights.
* **Storage:** Can use Data Warehouses, Data Lakes, or Big Data stores.
* **Focus:** Analytics and complex reporting (e.g., generating sales projections from CRM data).

---

### **5. Summary & Key Takeaways**

* **Data Types:** Remember the difference: **Structured** (Tables) vs. **Unstructured** (Text/Media) vs. **Semi-Structured** (JSON/XML).
* **RDBMS vs. NoSQL:** RDBMS is for strict, related, structured data. NoSQL is for flexible, unstructured data.
* **OLTP vs. OLAP:**
* **OLTP** = *Day-to-day operations* (Writing data fast).
* **OLAP** = *Analysis & Insights* (Reading massive data for reports).
