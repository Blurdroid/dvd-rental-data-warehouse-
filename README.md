# dvd-rental-data-warehouse-

## Project Overview

This project aims to design a data warehouse for a DVD rental service using a star schema. The star schema is a data model optimized for data warehousing and business intelligence, which simplifies complex data relationships into a more intuitive format. This project involves transforming a relational database schema into a star schema and performing analyses to derive insights, such as identifying top-paying customers.

## Table of Contents

1. [Download and Unzip the Data](#1-download-and-unzip-the-data)
   - Instructions to download the dataset and unzip it.
   - Steps to import the database into PostgreSQL using the terminal, including host, password, and database name.


![Screenshot from 2024-08-22 11-21-33](https://github.com/user-attachments/assets/93e2e4ff-e360-4ff3-bb0f-f13a55ef80a8)


     
2. [Explain the ERD (Entity-Relationship Diagram)](#2-explain-the-erd-entity-relationship-diagram)
   - A detailed description of the ERD, highlighting the relationships between entities in the DVD rental database.

![Screenshot from 2024-08-23 17-53-11](https://github.com/user-attachments/assets/1a5933e1-3958-44df-8918-505a6e6986cd)




3. [Define the Star Schema](#3-define-the-star-schema)
   - Explanation of the star schema structure, including the identification of the fact table and dimension tables.
   - Description of the fact table, which records transactions, and the dimension tables that provide context (e.g., customer information, film details, store data).

4. [Analysis](#4-analysis)
   - Perform analyses such as identifying the top-paying customers and other relevant metrics that can be derived from the star schema.

---

### Detailed Instructions

#### 1. Download and Unzip the Data

To begin, download the dataset from the provided source. After downloading, unzip the file using the following command:

```bash
unzip dvd_rental.zip
```

Next, import the database into PostgreSQL using the terminal:

```bash
psql -h <host> -U <username> -d <database_name> -f dvd_rental.sql
```

Replace `<host>`, `<username>`, and `<database_name>` with your PostgreSQL credentials.

#### 2. Explain the ERD (Entity-Relationship Diagram)

The Entity-Relationship Diagram (ERD) illustrates the relationships between different entities in the DVD rental database. Key entities include:

- **Customer**: Contains customer details such as ID, name, and contact information.
- **Film**: Includes film details like title, description, and release year.
- **Store**: Represents store information, including location and manager details.
- **Rental**: Captures rental transactions, linking customers to films and stores.

#### 3. Define the Star Schema

In the star schema, the central fact table is the **Rental** table, which records rental transactions. Dimension tables include:

- **DimCustomer**: Customer details.
- **DimFilm**: Film details.
- **DimStore**: Store details.
- **DimDate**: Date of the transaction.

This structure allows for efficient querying and analysis.

#### 4. Analysis

Using the star schema, perform analyses such as determining the top-paying customers. This can be achieved through SQL queries that aggregate rental amounts by customer, providing insights into customer behavior and preferences.

---

This README structure provides a clear and organized guide for users to navigate through the project effectively. Each section is linked to its content, making it easy to find relevant information.
