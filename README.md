# dvd-rental-data-warehouse-
Project Overview
This project aims to design a data warehouse for a DVD rental service using a star schema. The star schema is an essential data model in data warehousing and business intelligence, optimizing query performance and simplifying complex data relationships. The project involves transforming a traditional relational database schema into a star schema, enabling efficient analysis and reporting, such as identifying top-paying customers and other critical metrics.

Table of Contents
Download and Unzip the Data
Import Database into PostgreSQL
Explain the ERD (Entity-Relationship Diagram)
Define the Star Schema
Fact Table
Dimension Tables
Analysis
Top-Paying Customers
1. Download and Unzip the Data
To begin, download the DVD rental dataset from the provided source. After downloading, unzip the file in your desired directory using the following command in the Linux terminal:

bash
Copy code
unzip dvd_rental.zip
2. Import Database into PostgreSQL
Once the data is unzipped, import the database into PostgreSQL using the following command in the Linux terminal. Ensure you replace <host>, <username>, <database_name>, and <password> with your specific PostgreSQL credentials:

bash
Copy code
psql -h <host> -U <username> -d <database_name> -f dvd_rental.sql
You'll be prompted to enter the PostgreSQL password for the specified user.

3. Explain the ERD (Entity-Relationship Diagram)
The Entity-Relationship Diagram (ERD) provides a visual representation of the relationships between different entities in the DVD rental database. Key entities include:

Customer: Contains details such as customer ID, name, and contact information.
Film: Includes film details like title, description, and release year.
Store: Represents store information, including location and manager details.
Rental: Captures rental transactions, linking customers to films and stores.
Understanding the ERD is crucial as it lays the foundation for transforming the relational database into a star schema.

4. Define the Star Schema
The star schema is designed to facilitate efficient querying and analysis. It consists of a central fact table surrounded by dimension tables, resembling a star shape.

Fact Table
FactRental: This table records rental transactions and serves as the central fact table in the star schema. Key metrics like rental amount and rental duration are stored here.
Dimension Tables
DimCustomer: Contains detailed information about customers, such as customer ID, name, and contact info.
DimFilm: Stores details about the films, including film ID, title, genre, and release year.
DimStore: Includes store-related information, such as store ID, location, and manager details.
DimDate: Represents the dates related
