# SQL Server Data Warehouse Practice

This repository contains SQL Server scripts for practicing a sales-oriented data warehouse setup. The project concept uses ERP and CRM source data, with Bronze, Silver, and Gold layers as the intended architecture.

## Current repository contents

The checked-in scripts currently cover database/schema initialization and Bronze-layer table definitions/loading. Do not assume that the full Silver/Gold transformations and analytics pipeline are implemented in this repository unless those scripts are added and verified.

## Available scripts

- [Database initialization](./scripts/init_database.sql) — creates the `DataWarehouse` database and the `bronze`, `silver`, and `gold` schemas.
- [Bronze table definitions](./scripts/bronze/ddl_bronze.SQL) — defines raw CRM and ERP tables.
- [Bronze loading procedure](./scripts/bronze/proc_load_bronze.sql) — Bronze-layer loading logic.
- [Project license](./LICENSE)

## Prerequisites

- SQL Server and a SQL client such as SQL Server Management Studio or Azure Data Studio
- The project source CSV files, placed in the locations expected by the loading scripts

## Important safety note

**The initialization script drops and recreates the `DataWarehouse` database if it already exists.** Do not run it against a database containing data you need. Review the script first and use a disposable local development database.

## Next steps for this project

1. Confirm and document the expected source CSV paths.
2. Run the database initialization and Bronze scripts against a disposable local database.
3. Add and verify the Silver transformation and Gold/analytics scripts before describing this as a complete end-to-end warehouse.

## Scope

This is a learning project. The presence of database setup and Bronze-layer scripts is not a claim that the full warehouse pipeline has been run or deployed.
