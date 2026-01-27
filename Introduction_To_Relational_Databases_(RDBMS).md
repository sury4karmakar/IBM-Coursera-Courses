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

## **Subject: Information and Data Models**

## 1. Overview

Understanding data management is fundamental in the modern digital landscape. This lecture defines the two key concepts for data organization: **Information Models** and **Data Models**, and explores how they function within Database Management Systems (DBMS).

---

## 2. Information Models (Conceptual)

An information model provides a high-level, abstract framework. It allows stakeholders to understand the structure of data without worrying about technical implementation.

* **Definition:** Represents entities, properties, relationships, and operable functions abstractly.
* **Key Aspects:**
* **Framework:** Helps identify different types of information an organization uses.
* **Abstraction:** Hides the complexity of real-world entities.
* **Broad Scope:** Encompasses concepts applicable across various organizational areas.
* **Business Focus:** Used to define business concepts and rules.



---

## 3. Data Models (Practical)

A data model acts as a specific blueprint. It translates the conceptual information model into a practical structure for a database.

* **Definition:** Operates at a tangible level to define the organization, storage, and retrieval mechanisms within a database system.
* **Key Aspects:**
* **Specificity:** Defines elements, structures, constraints, and relationships.
* **DBMS Tailored:** Often designed for a specific Database Management System.
* **Schema Definition:** Specifies tables, columns, data types, indexes, and foreign keys.
* **Normalization:** Involves processes to ensure data integrity and reduce redundancy.



---

## 4. Comparison: Information vs. Data Models

| Feature | Information Model | Data Model |
| --- | --- | --- |
| **Level of Detail** | Low (Abstract & Broad) | High (Specific & Tangible) |
| **Focus** | Comprehending business concepts and relationships. | Technical implementation of storage and querying. |
| **Primary Users** | Business Analysts & Stakeholders. | Database Designers & Developers. |
| **Goal** | To agree on concepts without technicalities. | To construct the database system. |

---

## 5. The Hierarchical Model

The hierarchical model is a specific, physical implementation of an information system, rooted in early database history.

* **Structure:** Organizes data physically in a **tree-like format**.
* **Relationship to Info Models:** While the Information Model conceptualizes relationships abstractly, the Hierarchical Model stores them physically.
* **Limitations:**
* Struggles with **many-to-many** relationships.
* Can lead to data redundancy due to its rigid structure.



---

## 6. Common Types of Data Models

### A. The Relational Model

* **Usage:** The most widely used model for databases.
* **Structure:** Stores data in **tables** (rows and columns).
* **Advantages:** Simplicity, flexibility, ease of use, and provides data independence.

### B. Entity-Relationship (ER) Data Model

* **Concept:** Views the database as a collection of independent entities and objects.
* **ER Diagram Components:**
* **Entities (Rectangles):** The objects (e.g., *Books*, *Authors*). These become **Tables**.
* **Attributes (Ovals):** The data elements describing the entity (e.g., *Last Name*, *Email*). These become **Columns**.


* **Process:**
1. Identify Entities (e.g., Borrowers, Books).
2. Map relationships.
3. Convert the final diagram into database tables.



---

## 7. Key Database Management Concepts (Data Independence)

To ensure adaptability and efficiency, modern databases rely on three types of independence:

1. **Logical Data Independence**
* **Definition:** The ability to modify the database structure (schema) without impacting user data access.
* *Example:* Adding new fields or altering data types without breaking the application.


2. **Physical Data Independence**
* **Definition:** The ability to tweak the internal organization of the database without affecting user views or applications.
* *Example:* Changing indexing strategies or data storage types.


3. **Physical Storage Independence**
* **Definition:** The ability to move or reorganize data on physical storage hardware without impacting the application programs.
* *Example:* Moving data from one hard drive to another.
