# 🔄 Azure SQL Database to Synapse Link Integration

## Overview

In this project, I configured **Azure Synapse Link for Azure SQL Database** to replicate transactional data from an operational SQL database to a **dedicated SQL pool** in **Azure Synapse Analytics**. This setup supports **real-time analytics** on application data without impacting the source system.

## 🧠 What I Did

### 🧾 Configured Azure SQL Database Server
- Enabled **managed identity** on the SQL server
- Allowed Azure service access via firewall rules
- Verified and explored the **AdventureWorksLT** sample transactional database

### 🔗 Set Up Synapse Link for SQL
- Started the dedicated SQL pool in Synapse Studio
- Created a new `SalesLT` schema as the target for replication
- Configured a **linked service** and **link connection** to the AdventureWorksLT database
- Mapped and modified table structures (heap/columnstore, round-robin distribution)
- Synchronized key tables:
  - `SalesLT.Customer`
  - `SalesLT.Product`
  - `SalesLT.SalesOrderHeader`
  - `SalesLT.SalesOrderDetail`

### 📊 Validated Replication
- Monitored the link connection until synchronization was live
- Queried the replicated tables inside the **dedicated SQL pool**
- Joined customer, product, and order data for analytical insights without impacting transactional systems

## ✅ Key Takeaways

- Azure Synapse Link provides a **low-latency, no-ETL** solution for syncing data from Azure SQL DB to Synapse Analytics
- Data replication enables scalable, real-time **analytics over operational data**
- With Synapse Link, **data engineering and analytics teams** can work on clean, query-optimized copies of production data without adding load to the source systems

---

🔗 **Let’s connect on [LinkedIn](https://www.linkedin.com/in/eyilan/)** to explore more real-world cloud data engineering projects.
