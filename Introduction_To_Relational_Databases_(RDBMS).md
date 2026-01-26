## **Subject: Review of Data Fundamentals & RDBMS**

### **1. What is Data?**

* **Definition:** Data refers to unorganized information (facts, observations, perceptions, numbers, symbols, images) that undergoes processing to become meaningful.
* **Key Insight:** The **structure** of data determines how efficiently it can be managed, stored, and analyzed.

---

### **2. The Three Main Types of Data Structures**

**A. Structured Data**

* **Definition:** Highly organized data that follows a predefined format.
* **Characteristics:** Adheres to a strict **Schema** and is typically organized in **Rows & Columns**.
* **Pros:** Ensures consistency and allows for easy search and retrieval.
* **Examples:**
* **Excel Spreadsheets:** Data arranged in specific cell addresses.
* **SQL Databases:** Data stored in predefined tables.
* **Online Forms:** Designated fields (e.g., Name, Address, Credit Card #).



**B. Unstructured Data**

* **Definition:** Data that lacks a specific format or organization.
* **Characteristics:** Does not follow predefined rules or sequences.
* **Cons:** Challenging to process and analyze using traditional methods.
* **Examples:**
* **Text Files:** Free-form documents.
* **Media:** Images, Audio, and Video files.
* **Social Media:** Posts/Tweets containing mixed text, images, and links.



**C. Semi-Structured Data**

* **Definition:** Data with some organizational properties but no strict tabular structure.
* **Characteristics:** Uses **Tags** or **Keys** to mark elements; often hierarchical.
* **Pros:** Balances flexibility with structure.
* **Examples:**
* **JSON Files:** Uses arrays and objects.
* **XML Documents:** Uses tags and attributes.
* **Emails:** Structured headers (To, From, Subject) combined with an unstructured message body.



---

### **3. Common File Formats for Data Transfer**

* **Delimited Text Files:** Data resides in rows, separated by a specific character.
* **CSV (Comma-Separated Values):** Separated by commas.
* **TSV (Tab-Separated Values):** Separated by tabs.


* **Spreadsheets:** Data exists in rows and columns; often used to generate CSV files.
* **Language Files:** Formats with set rules for encoding data to send over the internet.
* **XML:** Extensible Markup Language.
* **JSON:** JavaScript Object Notation.



---

### **4. Data Repositories**

This is where data is actively stored, managed, and organized.

#### **Relational Databases (RDBMS)**

* **Structure:** Structured data stored in **related tables**.
* **Key Feature:** Links between tables minimize data duplication and preserve relationships.
* **Examples:** IBM DB2, Microsoft SQL Server, Oracle, MySQL.
* **Primary Use (OLTP):**
* **OLTP (Online Transaction Processing):** Supports day-to-day business activities (e.g., customer transactions, HR workflows).
* **Focus:** Transactional integrity and fast, routine operations.



#### **Non-Relational Databases (NoSQL)**

* **Structure:** Flexible storage for diverse or **unstructured data**.
* **Examples:** MongoDB (Document-oriented), Cassandra, Redis.
* **Use Case:** Best when data is too varied to fit into strict tables.

#### **OLAP (Online Analytical Processing)**

* **Focus:** Querying and **analyzing** large datasets to extract insights (e.g., generating sales projections).
* **Storage:** Data Warehouses, Data Lakes, Big Data stores.
* **Difference:** Unlike OLTP (which manages *transactions*), OLAP manages *analysis*.

---

### **5. Summary & Actionable Takeaways**

* **Identify the Structure:** Always check if your data is **Structured** (Rows/Columns), **Unstructured** (Free text/Media), or **Semi-Structured** (JSON/XML).
* **Choose the Right Database:**
* Use **RDBMS (SQL)** for structured, transactional business data.
* Use **Non-Relational (NoSQL)** for flexible or unstructured data.


* **Know Your Systems:** **OLTP** is for running the business (day-to-day); **OLAP** is for understanding the business (analytics).
