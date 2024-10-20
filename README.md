# Scalable-Data-Engineering-of-Hospital-Lentgth-of-Stay

Overview
This repository contains the code and documentation for a project aimed at predicting hospital Length of Stay (LoS) using advanced data engineering techniques. The focus is on building a scalable data warehousing solution and using MySQL Connector for efficient database management.

Project Structure
- data/: Contains sample data files simulating patient records, including demographics, medical conditions, and lab results.
- schema/: SQL scripts for setting up the star schema in MySQL.
- scripts/: Python scripts for data extraction, transformation, and loading (ETL) using MySQL Connector.
- models/: Python classes for interacting with the MySQL database using MySQL Connector.
   
Data Warehousing
- The data warehousing solution for this project is designed using a star schema to enable efficient querying and storage of patient records:

Star Schema Design:
- fact_stay - Stores core data on patient stays, such as admission dates, length of stay, diagnosis codes, and associated patient and facility IDs.
- dim_date - Contains detailed date information used to track admission and discharge dates.
- dim_diagnosis - Stores information about various diagnoses associated with patient stays.
- dim_facility - Details about the healthcare facilities where patient stays occurred.
- dim_patient - Contains demographic details of the patients, including age, gender, and other relevant information.

-Data Storage: The MySQL database is hosted on Amazon RDS, providing scalability and automated backups for data integrity and availability.

*Database Interaction using MySQL Connector*
- The project uses MySQL Connector to facilitate interactions between Python and the MySQL database, making it easy to perform database operations directly:

- Database Connections: Python scripts use MySQL Connector to establish connections with the MySQL database, allowing for execution of queries.
- CRUD Operations: The repository includes Python scripts for performing Create, Read, Update, and Delete (CRUD) operations, allowing seamless data manipulation directly through Python.
- Custom Queries: Python scripts can execute custom SQL queries to interact with the star schema, ensuring flexibility in how data is accessed and processed.
