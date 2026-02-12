# Review of Data Fundamentals & RDBMS

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

# Information and Data Models

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

---

# Entity Relationship Diagrams (ERDs) & Database Mapping

## 1. ERD Fundamentals

An **Entity Relationship Diagram (ERD)** is a visual representation that illustrates the logical structure of a database system by showing the relationships and interactions between entities.

### Key Components

* **Entities (Rectangles):**
* Represent people, objects, or concepts that store data (e.g., *Book*, *Author*).
* Serve as the fundamental building blocks of the database.


* **Attributes (Ovals):**
* Specific properties or characteristics that describe an entity.
* *Example:* A "Book" entity has attributes like *Title, Edition, Year,* and *Price*.


* **Relationship Sets (Diamonds/Lines):**
* Illustrate how entities are interconnected.
* Show how instances of one entity type relate to instances of another.


* **Crow's Foot Notation:**
* Uses symbols (vertical lines, greater-than, less-than) to indicate the nature and quantity of relationships.



---

## 2. Types of Relationships

Relationships define how data in one entity is linked to data in another.

| Relationship Type | Description | Visual Representation |
| --- | --- | --- |
| **One-to-One** | Each entity is linked to exactly **one** instance of another entity. | Often denoted by a simple line or specific notation (e.g., vertical bar). |
| **One-to-Many** | One entity is linked to **multiple** instances of another entity. | Uses a "crow's foot" or less-than symbol (<) on the "many" side. |
| **Many-to-Many** | Multiple instances of one entity are linked to **multiple** instances of another. | Uses symbols (crow's feet) on **both** sides of the relationship line. |

---

## 3. Mapping Entities to Tables

This process translates the conceptual ERD into a practical Relational Database schema.

### The Mapping Process

1. **Entity  Table:**
* The Entity (Rectangle) becomes a **Table** in the database.
* *Example:* The "Book" entity becomes the "Book" table.


2. **Attributes  Columns:**
* The Attributes (Ovals) become the **Columns** of the table.
* *Example:* Attributes *ISBN, Title,* and *Author* become columns within the "Book" table.


3. **Data Entry:**
* Actual data values are added into the rows of the table to complete the transformation from concept to storage.



---

## 4. Best Practices for Relational Database Design

To ensure efficiency, accuracy, and maintainability, follow these five key practices:

* **Primary Key Designation:**
* Assign a unique identifier (e.g., *Book ID*) to every record to uniquely identify it.


* **Data Validation:**
* Implement checks to ensure data consistency (e.g., ensuring *Published Year* is a number within a valid range).


* **Default Values:**
* Assign automatic values to columns to streamline data entry (e.g., setting *Author* to "Unknown" if left blank).


* **Use of Views:**
* Create customized, simplified perspectives of data for complex queries (e.g., a view combining Book and Author info).


* **Concurrency Control:**
* Manage simultaneous user access to prevent conflicts.
* *Example:* Adding a "Last Modified" timestamp to track changes.

---

# Database Data Types

## 1. Introduction to Data Types

A database table represents a singular entity, where columns symbolize the attributes of that entity. The data type assigned to a column dictates exactly what kind of information can be stored there.

* **Concept:** If a table represents a **Book**, its columns have specific types:
* *Title Column*  Textual Data
* *Publish Date Column*  Valid Date Format
* *Pages Column*  Numeric Data


* **Purpose:** Ensures that a text column holds alphanumeric data, while a numeric column only holds numbers.

---

## 2. The VARCHAR Data Type

**VARCHAR** (Variable Character) is one of the most common data types used for storing text.

* **Key Feature:** It holds varying lengths of characters up to a specified maximum.
* **Example:** `VARCHAR(100)`
* Allocates storage for *up to* 100 characters.
* If you store a string of only 50 characters, it uses space for only those 50 characters (plus a small overhead), not the full 100.


* **Benefits:**
* **Efficiency:** More space-efficient than fixed-length types because it only allocates necessary space.
* **Flexibility:** Ideal for data with significant length variation (e.g., names, addresses, descriptions).



---

## 3. Common Data Types Overview

| Category | Type | Description | Usage Example |
| --- | --- | --- | --- |
| **Date & Time** | **DATE** | Stores year, month, and day. | `2023-10-31` |
|  | **TIME** | Stores time of day. | `14:30:00` |
|  | **DATETIME / TIMESTAMP** | Combines both date and time. | `2023-10-31 14:30:00` |
| **Numeric (Fractional)** | **FLOAT** | Floating-point number with *approximate* precision. | Scientific calculations where exact precision isn't vital. |
|  | **DECIMAL** | Numeric type for *exact* arithmetic. | Financial calculations (e.g., `DECIMAL(5,2)` stores 5 digits total, 2 after decimal). |
| **Numeric (Whole)** | **INT / SMALLINT** | Stores whole numbers within specific ranges. | Counts, IDs. (`INT` range: ~ -2.1B to +2.1B). |
| **Binary** | **BLOB** | Binary Large Object. Stores sequence of bytes. | Non-textual data like images or files. |
| **Fixed String** | **CHAR** | Fixed-length string. | Always uses specified length, padding with spaces if the value is shorter. |

---

## 4. Advantages of Suitable Data Types

Choosing the correct data type is crucial for efficient database design and offers four main advantages:

1. **Data Integrity:** Prevents the insertion of incorrect data (e.g., prevents text from being saved in a date column).
2. **Accurate Sorting:** Ensures `Date`, `Time`, and `Numeric` values sort logically rather than alphabetically.
3. **Range Selection:** Allows for accurate querying of ranges (e.g., "all orders between Jan 1 and Jan 31").
4. **Calculations:** Enables valid mathematical operations (e.g., calculating the total cost of an order).

---

# Relational Model Concepts

## 1. Introduction

The relational model (introduced in 1970) organizes data based on two fundamental mathematical concepts: **Sets** and **Relations**.

---

## 2. Sets and Set Operations

A **Set** is a collection of unique elements without a specified order. It is typically denoted by curly braces, e.g. {1,2,3}.

### Basic Set Operations

| Operation | Symbol | Definition |
| --- | --- | --- |
| **Membership** | ∈ | a∈A means object a is an element of set A. |
| **Subset** | ⊆ | A⊆B means every element of A is also an element of B. |
| **Union** | ∪ | A∪B is the set of elements in A, in B, or in **both**. |
| **Intersection** | ∩ | A∩B is the set of elements strictly in **both** A and B. |
| **Difference** | − | A−B is the set of elements in A but **not** in B. |

### Additional Set Concepts

* **Empty Set (∅):** A unique set with no elements. It is a subset of every set.
* **Power Set (P(A)):** The set of *all possible subsets* of A (including the empty set and A itself).
* **Universal Set (U):** The set containing all objects under consideration.
* **Disjoint Sets:** Two sets that have no elements in common.

---

## 3. Relations and Properties

A **Relation** describes the connection between elements of sets.

* **Binary Relation:** A connection between two elements.
* **Ordered Pairs:** A subset of a Cartesian product, denoted as (a,b).

### Key Properties of Relations

1. **Reflexivity:** Each element relates to itself (a=a).
* *Example:* The equality definition (=).


2. **Symmetry:** If a relates to b, then b also relates to a.
* *Example:* "Is a sibling of".


3. **Transitivity:** If a relates to b, and b relates to c, then a relates to c.
* *Example:* "Less than" (<) relation (1<2 and 2<3, therefore 1<3).


4. **Antisymmetry:** If a relates to b and b relates to a, then a must equal b.
* *Example:* "Less than or equal to" (≤).



---

## 4. Relational Database Components

In a database, a "Relation" corresponds to a table. It is defined by two main components:

### A. Relation Schema (The Structure)

* **Definition:** Specifies the name of the relation and the definitions of its attributes (columns).
* **Example:**
* **Relation Name:** `Author`
* **Attributes:** `Author_ID` (Char), `Last_Name` (Varchar), `Email` (Varchar).



### B. Relation Instance (The Data)

* **Definition:** Represents the real-world data stored in the table at a specific moment.
* **Composition:** It is made up of rows (tuples) and columns (attributes).

---

## 5. Degree vs. Cardinality

These terms describe the dimensions of a relation.

* **Degree:** The number of **Attributes** (Columns).
* *Example:* A table with columns [Name, Age, Email] has a Degree of 3.


* **Cardinality:** The number of **Tuples** (Rows).
* *Example:* A table with 5 user records has a Cardinality of 5.

---

# Database Architecture & Deployment Topologies

## 1. Overview

**Deployment Topology** refers to the arrangement or configuration of hardware, software, and network components in a system deployment.

* **Key Selection Factors:**
* Scalability
* Performance
* Reliability
* Nature of the Application



---

## 2. Common Deployment Topologies

### A. Single-Tier Architecture

All components of the application reside on a **single server or machine**.

* **Components:** User Interface (UI), Application Logic, and Data Storage.
* **Environment:** The entire stack operates within one unified environment.
* **Usage:** Simple, standalone applications.

### B. Two-Tier (Client-Server) Architecture

This topology divides the application into two distinct logical layers.

* **Structure:**
1. **Client Layer:** Responsible for the User Interface (UI).
2. **Server Layer:** Manages Application Logic and Data Storage.


* **Workflow:**
* A remote server hosts the database.
* Users access the server via client systems (web pages or local apps).
* **Communication:** The client establishes a connection via a database interface (API or Framework) to the server.


* **Server Internals (DBMS Layers):**
* **Data Access Layer:** Provides interfaces for clients (Standard APIs like JDBC/ODBC, Command Line Processors, Vendor-specific interfaces).
* **Database Engine Layer:** Compiles queries, processes data, and returns results.
* **Database Storage Layer:** Manages the physical storage of data.



### C. Three-Tier Architecture

This is the standard for most **production environments**. It introduces a "Middle Tier" between the client and the database.

* **Structure:**
1. **Presentation Layer:** The UI (Desktop app, Web browser, Mobile app).
2. **Application Layer (Middle Tier):** Encapsulates Business Logic and Application Logic.
3. **Database Layer:** Stores the data.


* **Workflow:**
* The Client interacts *only* with the Application Server.
* The Application Server communicates with the Database Server via drivers/APIs.
* *Example:* An Internet Banking App (Mobile phone  Bank App Server  Account Database).


* **Why use Three-Tier? (Benefits):**
* **Security:** Direct access to the database is restricted to administrators only.
* **Performance:** Prevents overloading the database with unnecessary traffic.
* **Maintainability:** Admins can modify the database schema without disrupting the client application.



### D. Cloud-Based Deployment

Increasingly popular topology where the database resides within a cloud environment.

* **Key Characteristics:**
* Eliminates the need for local software installation.
* Removes the burden of maintaining physical infrastructure.


* **Advantages:**
* **Accessibility:** Users can access data from anywhere, anytime, with just an internet connection.
* **Flexibility:** Suitable for Development, Testing, and Full-scale Production.


* **Interaction:** Users/Clients interact via an application server or interface hosted in the cloud.

---

# Distributed Architecture & Clustered Databases

## 1. Overview

For critical or large-scale workloads where **High Availability (HA)** and **Scalability** are paramount, single-server configurations are often insufficient. Relational Database Management Systems (RDBMS) utilize distributed architectures to solve this.

* **Definition:** Clusters of machines interconnected through a network that distribute data processing and storage tasks.
* **Key Benefits:**
* **Enhanced Scalability:** Grows with demand.
* **Fault Tolerance:** Resists hardware/software failures.
* **Performance:** Improved speed through parallel processing.



---

## 2. Types of Database Architecture

There are three common deployment architectures for distributed systems:

### A. Shared Disk Architecture

* **Concept:** Multiple database servers process workloads in parallel.
* **Mechanism:**
* All servers connect to the **same shared storage**.
* Servers communicate via high-speed interconnections.


* **Key Feature:** If one server fails, mechanisms automatically reroute clients to another active server, ensuring high availability.

### B. Shared Nothing Architecture

* **Concept:** Each node (server) has its own private memory and storage.
* **Mechanism:** Uses **Replication** or **Partitioning** techniques to distribute workloads.
* **Key Feature:** Promotes efficient resource utilization and fault tolerance by rerouting clients to alternative nodes if a failure occurs.

### C. Specialized / Combination Architecture

* **Concept:** specific hybrid approaches that mix Shared Disk and Shared Nothing techniques.
* **Hardware:** Often utilizes specialized hardware components to achieve extreme availability or scalability goals.

---

## 3. Data Management & Optimization Techniques

To optimize performance and manage vast amounts of data, distributed systems employ specific strategies:

### A. Database Replication

The process of copying changes from a primary database server to one or more replicas.

* **High Availability (HA) Replica:**
* *Location:* Same physical location as the primary.
* *Purpose:* Protects against server hardware or software failure.


* **Disaster Recovery (DR) Replica:**
* *Location:* Geographically distributed (different region/city).
* *Purpose:* Protects against site-wide disasters (power loss, floods, earthquakes).



### B. Partitioning and Sharding

Used for handling massive datasets (e.g., Data Warehousing, Business Intelligence).

1. **Partitioning:**
* Splitting tables with substantial data into logical segments (e.g., separating sales records by Quarter: Q1, Q2, Q3, Q4).


2. **Sharding:**
* Placing these logical partitions on **separate physical nodes** in a cluster.
* **Resources:** Each shard has its own compute, memory, and storage.


3. **Process:**
* Client queries are processed in **parallel** across multiple shards.
* Results are synthesized and returned to the client.


4. **Scalability:**
* As workloads increase, you can seamlessly add more shards/nodes to the cluster.


---


# Database Usage Patterns


## 1. Overview

Different job roles require different tools and access patterns when interacting with a database. The primary users are categorized into three distinct groups:

1. **Data Engineers & Database Administrators (DBAs)**
2. **Data Scientists & Business Analysts**
3. **Application Developers**

---

## 2. Group 1: Data Engineers & Database Administrators (DBAs)

**Primary Focus:** Administrative tasks, establishing database objects, implementing access controls, monitoring performance, and ensuring a solid foundation for data storage.

### Tools & Mechanisms Used

* **A. Graphical User Interfaces (GUIs) & Web Tools**
* Common for interacting with cloud databases and mobile apps.
* Used when vendor tools are insufficient.
* *Example:* Oracle SQL Developer.


* **B. Command-Line Interfaces (CLI) & Utilities**
* Crucial for specific, efficient tasks despite the prevalence of GUIs.
* **Direct Commands:** Issuing single commands (e.g., `db2 create database sample`, `mysqldump sakila > sakila.sql`).
* **Interactive Shells:** Using dedicated environments (e.g., `sqlplus` for Oracle, `db2 clp`).
* **Scripts:** Executing SQL scripts or batch files.


* **C. Administrative APIs**
* Programmatic interfaces used for automation.
* Helps manage objects and monitor performance via custom tools.



---

## 3. Group 2: Data Scientists & Business Analysts

**Primary Focus:** Data analysis, insight derivation, and making data-driven predictions. They primarily **read** data but may create objects in sandbox environments.

### Tools Used

* **Data Science & Machine Learning Tools:**
* Jupyter, R Studio, Zepplin, SAS, SPSS.


* **Business Intelligence (BI) & Dashboarding Tools:**
* Microsoft Excel, Microsoft PowerBI, Tableau, MicroStrategy.


* **Access Methods:**
* These tools often interact via SQL interfaces or APIs, abstracting the complex SQL away from the user.
* Users may also use **Ad-hoc SQL query tools** for specific, one-off questions.



---

## 4. Group 3: Application Developers

**Primary Focus:** Creating applications that require both **Read** and **Write** access to the database. They rarely access the database directly; instead, their code does it.

### Development Stack

* **Programming Languages:** C++, C#, Java, JavaScript, PHP, Python, Ruby, .NET.
* **Connection Interfaces:**
* **SQL APIs:** ODBC (Open Database Connectivity) and JDBC (Java Database Connectivity).
* **REST APIs:** Common in cloud-based databases.



### Modern Development: Object Relational Mapping (ORM)

In the past, developers used lower-level APIs (ODBC/JDBC). Today, most use **ORM Frameworks**.

* **Definition:** Tools that facilitate interaction between relational databases and object-oriented programming languages.
* **Benefit:** They conceal the complexity of SQL and make database interaction user-friendly.

**Popular ORM Examples:**

* **Ruby:** ActiveRecord
* **Python:** Django
* **Java:** Hibernate
* **.NET:** Entity Framework
* **JavaScript:** Sequelize

---

# Introduction to PostgreSQL

## 1. History & Origins

* **Origin:** The **POSTGRES** project began at the University of California over 30 years ago.
* **Early Usage:** Used in research and production for aviation, financial services, and medicine.
* **Evolution:**
* **1994:** "Postgres95" was released (open source with an SQL language interpreter).
* **Renaming:** Soon renamed to **PostgreSQL** (commonly pronounced as "Postgres").


* **Common Stack:** Often used in the **LAPP** stack (**L**inux, **A**pache, **P**ostgreSQL, **P**HP).
* **Extensions:** Supports extensions like **PostGIS** for geographic/spatial data handling.

---

## 2. Core Definition

PostgreSQL is defined as a **Free, Open Source, Object-Relational Database Management System (ORDBMS)**.

* **Open Source:** You can freely use, modify, and distribute the source code to meet business requirements.
* **Object-Relational:** Unlike standard relational DBs, it supports Object-Oriented concepts:
* **Inheritance**
* **Overloading**
* *Benefit:* Simplifies design and allows for the reuse of database objects.


* **Compatibility:**
* Runs on most modern Operating Systems.
* Low maintenance threshold.
* Supports ANSI-SQL standards.
* Compatible with many programming languages for web integration.



---

## 3. Data Functionality

Postgres is versatile, handling both traditional and modern data structures.

* **Standard Relational Constructs:**
* Keys, Transactions, Views, Functions, Stored Procedures.


* **NoSQL Functionality:**
* **JSON:** For storing structured data.
* **HSTORE:** For non-hierarchical (key-value) data.



---

## 4. Replication & High Availability (HA)

PostgreSQL supports various replication methods to ensure data safety and uptime.

### A. Two-Node Synchronous Replication

* **How it works:** Stores a copy of data on a second server. Every change to Node 1 is immediately applied to Node 2.
* **Benefit:**
* Read loads can be shared across both servers.
* **Failover:** If Node 1 fails, Node 2 takes over immediately.



### B. Multi-Node Asynchronous Replication

* **How it works:** One "Master" node distributes changes to multiple "Read-Only" replicas.
* **Benefit:** Great for **Scalability**. If the master fails, a read-only replica can be promoted to replace it.

### C. Multi-Master Read/Write Replication (Commercial)

* *Note: Usually requires commercial additions like EDB PostgreSQL Replication Server.*
* **How it works:** Runs multiple databases that can **all** accept Read/Write traffic and replicate changes to each other.
* **Benefit:** Maximum flexibility; users are redirected seamlessly if any single instance fails.

---

## 5. Scalability Techniques

Recent releases have added technologies to handle larger datasets:

1. **Partitioning:**
* Splits a large table into smaller, manageable sections (partitions) to improve query performance.


2. **Sharding:**
* Enables the storage of horizontal partitions across multiple **remote servers**.



---

# Introduction to IBM Db2

## 1. Introduction & History

**Db2** (Database 2) is a family of data management products developed by IBM.

* **Origins:** First released in **1983** as an early Relational Database Management System (RDBMS).
* **Evolution:** Originally built for IBM Mainframes, it expanded to support OS/2, Unix, Linux, and Windows.
* **Codebase:** Eventually rewritten to use a common codebase across multiple operating systems, allowing for easy porting of applications between platforms.

## 2. The Db2 Product Family

Today, Db2 is a comprehensive suite of products designed for various environments (On-Premises, Cloud, Hybrid).

| Product | Description | Deployment |
| --- | --- | --- |
| **Db2 Database** | Enterprise-ready RDBMS optimized for **OLTP** (Online Transaction Processing). | On-Premises (Linux, Unix, Windows) |
| **Db2 Warehouse** | Data warehouse optimized for **Analytics**, Machine Learning, and MPP (Massively Parallel Processing). | On-Premises |
| **Db2 on Cloud** | Fully managed SQL database with features similar to the on-prem version. | Cloud (IBM Cloud, AWS) |
| **Db2 Warehouse on Cloud** | Fully managed, elastic data warehouse. | Cloud (IBM Cloud, AWS) |
| **Db2 Big SQL** | SQL-on-Hadoop engine. Queries diverse sources (HDFS, NoSQL, Object Stores). | Hybrid / Data Lakes |
| **Db2 for z/OS** | Mission-critical enterprise data server for IBM Z mainframes. | Mainframe |

## 3. Key AI-Powered Features

All Db2 products utilize AI and Machine Learning to optimize performance and management.

* **ML Query Optimization:** Uses algorithms to improve query efficiency.
* **Column Store:**
* *Function:* Directs queries to specific columns rather than processing entire rows.
* *Benefit:* Reduces overhead and drastically improves performance for **Analytic Workloads**.


* **Data Skipping:** Automatically avoids processing data irrelevant to a specific query.
* **Common SQL Engine:** Write a query once, and it works across all Db2 family products, simplifying migration.

## 4. Db2 on Cloud: Plans & Access

Db2 on Cloud is a fully managed service available on IBM Cloud and AWS.

### Subscription Plans

1. **Lite Plan:** Free, time-unlimited, 200MB storage, 15 connections. (Ideal for dev/learning).
2. **Standard Plan:** Flexible scaling of compute/storage + 3-Node High Availability (HA) clustering.
3. **Enterprise Plan:** Dedicated instance + Flexible scaling + 3-Node HA clustering.

### Access Methods

* **Command Line:** `CLPPlus` interface.
* **GUI:** Db2 on Cloud Console.
* **APIs:** Standard ODBC, JDBC, and REST APIs.
* **Data Loading:** direct load from Excel, CSV, Amazon S3, or IBM Cloud Object Storage.

## 5. High Availability & Scalability

### High Availability Disaster Recovery (HADR)

Used to ensure continuous uptime and data safety.

* **Mechanism:** Replicates changes from a **Primary** database to multiple **Standby** servers.
* **Failover:** If the Primary fails (hardware/network issue), a Standby is promoted to Primary. Clients are redirected automatically.
* **Failback:** When the original Primary returns, it can rejoin as a Standby or resume its Primary role.

### Scalability & Partitioning (MPP)

Particularly in **Db2 Warehouse**, scalability is achieved through **Massively Parallel Processing**.

* **Partitioning:** Data is transparently split across multiple partitions and servers.
* **Scaling Up:** Add a node  Workloads automatically rebalance.
* **Scaling Down:** Remove a node  Workloads return to original state.

## 6. Cloud Pak for Data

A fully integrated data and AI platform running on **Red Hat OpenShift**.

* **Containerized:** Can be deployed on private, public, or hybrid clouds.
* **Integration:** Connects to Db2 or any other data source.
* **Capabilities:** Organizing data (Watson Knowledge Catalog), Analytics, and Infusing AI (Watson services).

---

# Introduction to MySQL

## 1. Overview & History

**MySQL** is an Object-Relational Database Management System (ORDBMS) known for its reliability, scalability, and ease of use. It is a cornerstone of modern web development.

* **Origins:**
* Developed by the Swedish company **MySQL AB**.
* Named after "My," the daughter of co-founder Monte Widenius.
* **Logo:** A dolphin named "Sakila" (named via a user contest).


* **Ownership Timeline:**
1. MySQL AB
2. Acquired by **Sun Microsystems**
3. Acquired by **Oracle Corporation**


* **The LAMP Stack:**
* MySQL gained massive popularity in the late 90s/early 2000s as the database component of the LAMP stack, which powered many early web giants.
* **L**inux (OS)
* **A**pache (Web Server)
* **M**ySQL (Database)
* **P**HP (Scripting Language)


* **Licensing:**
* **Dual Licensing:** Available under the Open Source **GNU GPL** and a Commercial license (for embedding in proprietary apps).
* **Forks:** The open nature led to forks like **MariaDB** (led by original developers).



---

## 2. Key Attributes of Working with MySQL

* **Compatibility:** Runs on Unix, Linux, and Windows.
* **Languages:** Client apps can be written in almost any modern programming language.
* **SQL Syntax:** Uses standard SQL but includes extensions for extra functionality.
* *Example:* `LOAD DATA` statement for swift bulk imports from text files.


* **Data Types:** Primarily Relational, but also supports **JSON** data.

---

## 3. Storage Engines

A unique feature of MySQL is its **pluggable storage engine architecture**. The engine handles SQL operations for a table and defines its features (locking, transaction support, etc.).

| Storage Engine | Characteristics & Use Cases |
| --- | --- |
| **InnoDB** | **(Default)** |
||• Supports **Transactions** (ACID compliance).|
||• **Row-level locking** (better multi-user performance).|
||• Clustered indexes on Primary Keys.|
||• Foreign Key support.|
||• *Best for:* General purpose, high performance, and reliability.|
| **MyISAM** | • Optimized for **Read-heavy** workloads (e.g., Data Warehousing, simple web apps).|
||• **Table-level locking** (poor performance for Read/Write mixes).|
||• Does *not* support transactions. |
| **NDB** | • Supports **Clustering**.|
||• Allows multiple MySQL server instances to run in a cluster.|
||• *Best for:* High availability and redundancy. |

---

## 4. Scalability & High Availability (HA)

### Replication

* **Process:** Creates copies of data on one or more replicas. Changes in the source are executed on the replicas.
* **Benefits:**
* **Scalability:** Distribute read loads across multiple replicas.
* **Availability:** If the source fails, failover to a replica.



### Clustering Options

Clustering connects multiple independent computing resources to work as a unified system. MySQL offers two main paths:

#### A. InnoDB with Group Replication

* **Topology:** One Read-Write Primary server + Multiple Secondary servers.
* **MySQL Router:** Used to load balance clients across instances.
* **Failover:** If a server fails, the Router automatically reconnects clients to an available server.

#### B. MySQL Cluster Edition (NDB Engine)

* **Topology:** Multiple MySQL Server nodes accessing a set of **Data Nodes** (usually in-memory).
* **Redundancy:** Data nodes provide high availability; if one fails, others take over.
* **Scalability:** Multiple Server nodes handle increased traffic.

---

# Types of SQL Statements

## 1. Overview

SQL statements are the primary method for interacting with Relational Databases. They allow you to work with:

* **Entities:** Tables
* **Attributes:** Columns
* **Tuples:** Rows with data values

SQL statements are broadly categorized into two types: **Data Definition Language (DDL)** and **Data Manipulation Language (DML)**.

---

## 2. Data Definition Language (DDL)

DDL statements are used to **define, change, or drop** database objects (like tables) themselves. They deal with the *structure* of the database, not the specific data inside the rows.

### Common DDL Commands:

* **CREATE:** Used for creating new tables and defining their columns.
* **ALTER:** Used for modifying existing tables (e.g., adding/dropping columns, changing data types).
* **TRUNCATE:** Used for deleting **all data** inside a table, but keeps the table structure intact.
* **DROP:** Used for deleting the table entirely (structure + data).

---

## 3. Data Manipulation Language (DML)

DML statements are used to **read and modify** the actual data within the tables. These are often referred to as **CRUD** operations (Create, Read, Update, Delete).

### Common DML Commands:

* **INSERT:** Adds a single row or multiple rows of data into a table. *(Create)*
* **SELECT:** Reads or retrieves specific rows from a table. *(Read)*
* **UPDATE:** Edits existing rows in a table. *(Update)*
* **DELETE:** Removes specific rows of data from a table. *(Delete)*

---

# The CREATE TABLE Statement

## 1. Overview

The `CREATE TABLE` statement is the most common **Data Definition Language (DDL)** command. It is used to define a new entity (table) and its attributes (columns) within a relational database.

## 2. Basic Syntax

To create a table, you must specify the table name and define the columns within parentheses.

**Structure:**

```sql
CREATE TABLE table_name (
    column1 datatype [optional_constraints],
    column2 datatype [optional_constraints],
    ...
);

```

* **Process:**
1. Start with `CREATE TABLE`.
2. Specify the `table_name`.
3. Open parentheses `( ... )`.
4. List column names followed by their **Data Type** and optional **Constraints**.
5. Separate each column definition with a comma.



---

## 3. Example 1: Creating a Simple Table

**Scenario:** Creating a table to store Canadian Provinces.

**SQL Code:**

```sql
CREATE TABLE provinces (
    id CHAR(2) PRIMARY KEY NOT NULL,
    name VARCHAR(24)
);

```

**Breakdown of Data Types:**

* **CHAR(2):** A character string of **fixed length** (always 2 characters). Used for abbreviations like 'AB', 'BC'.
* **VARCHAR(24):** A character string of **variable length** (up to 24 characters). Used for full names like 'Alberta' or 'British Columbia'.

---

## 4. Example 2: Complex Table with Constraints

**Scenario:** Creating an `Author` table for a library database.

**SQL Code:**

```sql
CREATE TABLE author (
    Author_ID CHAR(2) PRIMARY KEY NOT NULL,
    Lastname VARCHAR(15) NOT NULL,
    Firstname VARCHAR(15) NOT NULL,
    Email VARCHAR(40),
    City VARCHAR(15),
    Country CHAR(2)
);

```

**Key Constraints Explained:**

* **PRIMARY KEY:**
* Designates a column (or set of columns) as the unique identifier for the table.
* Ensures there are **no duplicate values** (e.g., two authors cannot have the same ID).
* Uniquely identifies each tuple (row).


* **NOT NULL:**
* Ensures that a column **cannot be left empty**.
* In the example above, `Lastname` and `Firstname` must have values because every author must have a name.

---

# Modifying and Deleting Tables (DDL)

## 1. The ALTER TABLE Statement

The `ALTER TABLE` statement is used to modify the structure of an existing table without deleting it. It allows you to:

* Add or remove columns.
* Modify the data type of columns.
* Add or remove keys and constraints.

**Key Syntax Note:** Unlike the `CREATE TABLE` statement, `ALTER TABLE` **does not** use parentheses to enclose parameters.

### A. Adding a Column

Used when you need to store new information in an existing table.

* **Syntax:** `ALTER TABLE table_name ADD COLUMN column_name data_type;`
* **Example:** Adding a telephone number column to the author table.
```sql
ALTER TABLE author ADD COLUMN telephone_number BIGINT;

```

*(Note: `BIGINT` can hold numbers up to 19 digits long).*

### B. Modifying a Column (Data Type)

Used to change the data type of an existing column (e.g., changing a numeric field to a character field to allow dashes and brackets).

* **Syntax:** `ALTER TABLE table_name ALTER COLUMN column_name SET DATA TYPE new_data_type;`
* **Example:** Changing the telephone number to `CHAR` to allow formatting.
```sql
ALTER TABLE author ALTER COLUMN telephone_number SET DATA TYPE CHAR(20);

```

> **Warning:** Altering a column that already contains data can cause errors if the existing data is incompatible with the new type (e.g., trying to convert text "ABC" into a Numeric type).

### C. Dropping a Column

Used when a column is no longer needed in the table specification.

* **Syntax:** `ALTER TABLE table_name DROP COLUMN column_name;`
* **Example:** Removing the telephone number column.
```sql
ALTER TABLE author DROP COLUMN telephone_number;

```
---

## 2. The DROP TABLE Statement

The `DROP TABLE` statement is used to completely remove a table from the database.

* **Effect:** It deletes the **Table Structure** AND all **Data** contained within it.
* **Syntax:** `DROP TABLE table_name;`
* **Example:**
```sql
DROP TABLE author;

```

---

## 3. The TRUNCATE TABLE Statement

The `TRUNCATE TABLE` statement is used to delete **all rows** of data in a table while keeping the table structure intact.

* **Efficiency:** It is generally faster and more efficient than using a `DELETE` statement without a `WHERE` clause.
* **Keyword:** The `IMMEDIATE` keyword is often used to indicate immediate processing and emphasizes that the action **cannot be reversed**.
* **Syntax:** `TRUNCATE TABLE table_name IMMEDIATE;`
* **Example:**
```sql
TRUNCATE TABLE author IMMEDIATE;

```
---

# Data Movement Utilities

## 1. Overview

Data Engineers and Database Administrators (DBAs) frequently move data in and out of databases.
**Common Reasons for Data Movement:**

* **Populating:** Filling the database and objects (tables) with initial data.
* **Duplication:** Creating copies of the database for development or testing environments.
* **Disaster Recovery:** Creating snapshots of the database state.
* **Integration:** Generating new tables using data from external sources or files.
* **Appending:** Adding data into existing tables.

---

## 2. Methods for Data Movement

There are three primary categories of tools used for moving data:

1. **Backup and Restore**
2. **Import and Export**
3. **Load**

---

## 3. Backup and Restore

This method is used to create an exact replica of the database.

* **Backup Operation:**
* Creates a file (or set of files) that encapsulates **all** database objects and their data.
* **Preserves:** Schemas, tables, views, functions, stored procedures, constraints, triggers, security settings, and relationships.


* **Restore Operation:**
* Creates an exact copy of the original database from the backup files.


* **Use Cases:**
* **Disaster Recovery:** Essential for preserving production data.
* **Cloning:** Creating identical environments for Dev/Test teams.

---

## 4. Import and Export

These operations focus on moving data between the database and external files.

* **Import Operation:**
* Reads data from a file.
* Performs a series of **INSERT statements** against the target table.


* **Export Operation:**
* Retrieves data from a designated table.
* Stores it in a chosen file format.

### Supported File Formats

| Format | Description |
| --- | --- |
| **DEL (Delimited ASCII)** | Uses special characters to separate column values (e.g., **CSV**). Common for data exchange between different systems. |
| **ASC (Non-delimited ASCII)** | Used for flat text files where columns are aligned by fixed width (no delimiters). |
| **PC/IXF (Integration Exchange Format)** | A structured format that includes a description of the table + the data. Preferred for moving data *within* the same database manager family. |
| **JSON** | Increasingly popular due to REST web services; supported by modern tools for structured/semi-structured data. |

---

## 5. The Load Utility (vs. Import)

While **Import** uses SQL `INSERT` commands, **Load** is a high-performance alternative for massive datasets.

* **Mechanism:** Writes formatted pages **directly** into the database (bypassing the SQL engine).
* **Pros:**
* Significantly faster than Import.
* Ideal for **large volumes** of data.


* **Cons:**
* **Bypasses Checks:** Does *not* perform referential integrity or table constraint checking.
* **Logging:** May bypass database logging (which increases speed but affects recoverability during the load).

---

## 6. DB2 Examples

Different interfaces exist for these operations:

* **Command Line (CLI):** Allows typing file names, formats, and table names directly.
* *Note:* The Export utility can use a **SQL Query** to export only a specific subset of data.


* **DB2 Cloud Web Console:** A visual interface.
* *Steps:* Select Table  View Data  Export Button  Export to CSV.

---
Database Objects and Hierarchy
