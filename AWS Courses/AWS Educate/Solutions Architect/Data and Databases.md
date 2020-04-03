# Data and Databases

## Non-Relational

A non-relational database is a database that does not incorporate the table/key model that relational database management systems (RDBMS) promote. These kinds of databases require data manipulation techniques and processes designed to provide solutions to big data problems that big companies face. The most popular emerging non-relational database is called NoSQL (Not Only SQL).

## Relational

A relational database (RDB) is a collective set of multiple data sets organized by tables, records and columns. RDBs establish a well-defined relationship between database tables. Tables communicate and share information, which facilitates data searchability, organization and reporting. RDBs use Structured Query Language (SQL), which is a standard user application that provides an easy programming interface for database interaction. RDB is derived from the mathematical function concept of mapping data sets and was developed by Edgar F. Codd.

## Data Management and Data Migration

### Data Management

A database management system (DBMS) is system software for creating and managing databases. The DBMS provides users and programmers with a systematic way to create, retrieve, update and manage data.

### Data Migration

Data migration is the process of transporting data between computers, storage devices or formats. It is a key consideration for any system implementation, upgrade or consolidation.

The AWS Schema Conversion Tool makes heterogeneous database migrations predictable by automatically converting the source database schema and a majority of the database code objects, including views, stored procedures, and functions, to a format compatible with the target database.

### Data Structures

Data structures are a critical part of software development, and one of the most common topics for developer job interview questions. The good news is that they're basically just specialized formats for organizing and storing data.

### Data Warehouse

A data warehouse is a collection of corporate information and data derived from operational systems and external data sources. A data warehouse is designed to support business decisions by allowing data consolidation, analysis and reporting at different aggregate levels. Data is populated into the DW through the processes of extraction, transformation and loading.

### Data Lake

A data lake is a storage repository that holds a vast amount of raw data in its native format until it is needed. While a hierarchical data warehouse stores data in files or folders, a data lake uses a flat architecture to store data.

Unlike a data warehouse, a data lake is a centralized repository for all data, including structured and unstructured. A data warehouse utilizes a pre-defined schema optimized for analytics. In a data lake, the schema is not defined, enabling additional types of analytics like big data analytics, full text search, real-time analytics, and machine learning.

Characteristics | Data Warehouse | Data Lake
----------------|----------------|----------
Data | Relational data from transactional systems, operational databases, and line of business applications | Non-relational and relational data from IoT devices, web sites, mobile apps, social media, and corporate applications
Schema | Designed prior to the data warehouse implementation (schema-on-write) | Written at the time of analysis (schema-on-read)
Price/Performance | Fastest query results using higher cost storage | Query results getting faster using low-cost storage
Data Quality | Highly curated data that serves as the central version of the truth | Any data that may or may not be curated (i.e. raw data)
Users | Business analysts, data scientists, and data developers | Data scientists, data developers, and business analysts (using curated data)
Analytics | Batch reporting, BI, and visualizations | Machine learning, predictive analytics, data discovery, and profiling
