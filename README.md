# SQL Server Data Warehouse Practice

This project practices building a sales-oriented data warehouse with SQL Server. It is organized around source CSV files from ERP and CRM systems, data cleansing and integration, and SQL analytics for customers, products, and sales trends.

## Intended workflow

1. Set up the `DataWarehouse` database and `bronze`, `silver`, and `gold` schemas.
2. Create Bronze-layer tables for the CRM and ERP source entities.
3. Continue with the repository's loading, transformation, and analytics scripts.
4. Document and query the integrated data model.

## Repository structure

- [Database initialization](./scripts/init_database.sql)
- [Bronze table definitions](./scripts/bronze/ddl_bronze.SQL)
- [Bronze loading procedure](./scripts/bronze/proc_load_bronze.sql)
- [Project license](./LICENSE)

## Prerequisites

- SQL Server and a SQL client such as SQL Server Management Studio or Azure Data Studio
- The project source CSV files, placed in the locations expected by the loading scripts

## Important safety note

**The initialization script drops and recreates the `DataWarehouse` database if it already exists.** Do not run it against a database containing data you need. Review the script first and use a disposable local development database.

## Scope

The README describes the intended warehouse workflow. Review the available scripts and source-data requirements before running the complete pipeline; this repository should be treated as a learning project rather than a deployed warehouse.
