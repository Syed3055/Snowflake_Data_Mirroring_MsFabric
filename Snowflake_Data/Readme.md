# 📘 README – Snowflake to Microsoft Fabric Mirroring (Incremental Load Validation)
## 📌 Project Title
Snowflake_Mirror_Check – Incremental Data Validation using Microsoft Fabric Mirroring

## 📝 Overview
This project demonstrates how Snowflake data **(Database: SYED_DB)** can be ingested into Microsoft Fabric using the Snowflake Mirroring feature without the need to build, schedule, or maintain any traditional ETL/ELT pipelines.
The goal was to test incremental data updates from Snowflake and validate that Microsoft Fabric automatically synchronizes changes without requiring additional orchestration.

## 🎯 Objective

Mirror the Snowflake database SYED_DB **(containing CUSTOMER, PRODUCT, and SALES tables)** into Microsoft Fabric.
Validate incremental data ingestion without configuring pipelines or schedules.
Build a Power BI report (Snowflake_Mirror_Check) to verify row counts and table records during incremental loads.
Confirm that Microsoft Fabric can replace traditional ingestion pipelines with zero‑maintenance, near real‑time mirroring.


## 📌 Initial Situation / Problem
Traditionally, getting Snowflake data into Power BI or downstream storage requires:

Building complex ingestion pipelines
Managing incremental refresh logic
Scheduling pipelines with triggers
Maintaining ETL code, copy activities, time partitions, or manually created delta logic
Re‑processing failures manually

This becomes even more difficult when dealing with:

Multiple tables
Frequent inserts
Large datasets
High refresh frequency

Syed needed a solution where:

No pipelines were required
No scheduling or orchestration was needed
Incremental data could flow automatically
Power BI could always reflect the latest Snowflake data


## 🚀 Our Approach
We used Microsoft Fabric’s Snowflake Mirroring capability, which allows:

Direct mirroring of Snowflake databases
Automatic synchronization of table updates
No ETL
No pipelines
No complex scheduling
Near real‑time change pickup
Direct access inside Fabric Lakehouse

Once the mirror was created:

The tables (CUSTOMER, PRODUCT, SALES) appeared directly inside Fabric.
Any new rows added to Snowflake synced automatically to Fabric’s mirrored database.
Power BI datasets connected instantly to the Fabric mirrored tables.

This allowed Syed to validate live incremental behavior simply by inserting new data into Snowflake and refreshing Power BI.

## 🎉 Final Outcome
--> ✔ Snowflake Database SYED_DB was successfully mirrored into Microsoft Fabric

--> ✔ All three tables (CUSTOMER, PRODUCT, SALES) synchronized correctly

--> ✔ Incremental inserts in Snowflake were recognized in Fabric without any pipeline or schedule

--> ✔ A Power BI report (Snowflake_Mirror_Check) was built to compare:


Table counts
Incrementally added rows
Data integrity validation
##### ✔ The entire process required zero ETL, zero orchestration, and zero maintenance

##### --> Syed successfully completed the task and confirmed that Fabric Mirroring works seamlessly for incremental ingestion.

###### ------------------------Thank You 💐💐💐 😊---------------------------------
