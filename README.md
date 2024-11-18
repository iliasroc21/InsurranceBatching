# Mutuelle Dossier Management with Spring Batch

This project is a batch processing application built using Spring Batch.
It automates the management of mutual insurance claim files, validates data, 
calculates reimbursements, and archives processed files in a database.

## Features
* Read: Load claim files from a JSON source.
* Validate: Ensure that key fields (e.g., insured person's name, affiliation number) meet the required constraints.
* Process:
        * Calculate reimbursements for consultations and prescribed medications.
        * Map medications to reference data for accurate calculations.
* Write: Save processed claim files to a database or export them for archiving.

## Project Workflow

1. JsonItemReader: Reads insurance claim data from a JSON file.
2. ValidationProcessor: Validates the input data (e.g., non-empty fields, positive amounts).
3. CalculationProcessor: Calculates reimbursement amounts for consultations and medications.
4. CompositeItemProcessor: Chains multiple processors for sequential processing.
5. JpaItemWriter: Saves processed data into a relational database.

## Technologies Used

* Java 17
* Spring Batch
* Spring Boot
* Hibernate / JPA
* HSQLDB (In-memory database for testing)
* JSON Processing (Jackson)
* Lombok

