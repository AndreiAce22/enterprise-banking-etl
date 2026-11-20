# Enterprise Banking Data Integration & Regulatory Reporting

## Project Overview

This project simulates an enterprise banking data integration environment, focusing on extracting data from an Oracle source database, transforming and validating banking data, and loading it into Microsoft SQL Server using SQL Server Integration Services (SSIS).

The project aims to demonstrate practical data engineering skills, ETL development, data migration, data quality validation, and SQL performance optimization.

## Technology Stack

- Oracle Database
- Microsoft SQL Server
- SQL Server Integration Services (SSIS)
- SQL
- Git and GitHub
- Visual Studio

## Project Architecture

```text
Oracle Database (Source)
        |
        v
SSIS (ETL and Data Integration)
        |
        v
SQL Server (Target)
        |
        v
Regulatory Reporting and Analytics
```

## SSIS Packages

The SSIS solution contains seven packages that implement the banking data warehouse ETL workflow.

| Package | Description |
|---|---|
| `PKG_01_Load_Staging.dtsx` | Extracts Oracle source data and loads it into SQL Server staging tables. |
| `PKG_02_Dimensions.dtsx` | Creates the required dimension tables. |
| `PKG_03_Load_Dimensions.dtsx` | Loads and maintains dimension data, including historical changes. |
| `PKG_04_Create_Facts.dtsx` | Creates the fact tables in the data warehouse. |
| `PKG_05_Load_Facts.dtsx` | Loads data into the fact tables. |
| `PKG_06_Validate_Warehouse.dtsx` | Executes warehouse validation and data quality checks. |
| `PKG_Master_ETL.dtsx` | Orchestrates the complete ETL workflow by executing the child packages. |

## Key Learning Objectives

- Develop ETL workflows using SSIS.
- Perform Oracle-to-SQL Server data migration.
- Handle large-scale banking datasets.
- Implement data quality checks and reconciliation.
- Optimize SQL queries and database performance.
- Analyze execution plans and indexing strategies.
- Apply Git version control and source management.

## Project Status

- [x] Source database setup
- [x] SQL Server staging database
- [x] Data warehouse development
- [x] Dimension and fact table implementation
- [x] SSIS ETL package development
- [x] Master package orchestration
- [x] Data quality validation and reconciliation
- [ ] SSISDB deployment and SQL Server Agent scheduling

## Repository Structure

```text
Enterprise-Banking-ETL/
|
+-- database/
|   +-- oracle/
|   +-- sql_server/
|
+-- documentation/
|
+-- EnterpriseBankingETL/
|   +-- EnterpriseBankingETL.sln
|   +-- EnterpriseBankingETL/
|       +-- EnterpriseBankingETL.dtproj
|       +-- EnterpriseBankingETL.database
|       +-- Project.params
|       +-- PKG_01_Load_Staging.dtsx
|       +-- PKG_02_Dimensions.dtsx
|       +-- PKG_03_Load_Dimensions.dtsx
|       +-- PKG_04_Create_Facts.dtsx
|       +-- PKG_05_Load_Facts.dtsx
|       +-- PKG_06_Validate_Warehouse.dtsx
|       +-- PKG_Master_ETL.dtsx
|
+-- scripts/
+-- ssis/
+-- tests/
|
+-- .gitignore
+-- README.md
```

## Deployment

The SSIS project is designed for deployment to the SQL Server Integration Services Catalog (SSISDB).

Deployment configuration, connection manager settings, and SQL Server Agent scheduling documentation will be added as the deployment phase progresses.