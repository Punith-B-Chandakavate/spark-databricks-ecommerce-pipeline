# 📦 Azure Data Lake Storage Gen2 (ADLS Gen2)

![Azure](https://img.shields.io/badge/Microsoft-Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![ADLS](https://img.shields.io/badge/Azure-Data%20Lake%20Storage%20Gen2-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

# 📖 Overview

Azure Data Lake Storage Gen2 (ADLS Gen2) is Microsoft's enterprise-grade cloud storage service designed for big data analytics workloads.

This guide walks through the complete setup process, including:

- Create Azure Storage Account
- Configure ADLS Gen2
- Enable Hierarchical Namespace
- Deploy Storage Account
- Create Blob Container
- Upload Dataset
- Verify Uploaded Files

---

# 🏗️ Architecture

```text
Azure Portal
      │
      ▼
Storage Account
      │
      ▼
Azure Data Lake Storage Gen2
      │
      ▼
Blob Container
      │
      ▼
CSV Files
      │
      ▼
Azure Databricks
```

---

# 📌 Step 1 — Create Azure Storage Account

Navigate to

```
Azure Portal

↓

Storage Accounts

↓

Create
```

Configure:

- Subscription
- Resource Group
- Storage Account Name
- Region
- Primary Service

<p align="center">
<img src="images/01_create_storage_account.png" width="100%">
</p>

---

# 📌 Step 2 — Configure Storage Account

Configure the storage account with the following settings:

| Setting | Value |
|----------|------|
| Performance | Standard |
| Region | East US |
| Primary Service | Azure Blob Storage / ADLS |
| Redundancy | Geo-Redundant Storage (GRS) |

Click **Next**

<p align="center">
<img src="images/02_storage_account_configuration.png" width="100%">
</p>

---

# 📌 Step 3 — Enable Azure Data Lake Storage Gen2

Enable the **Hierarchical Namespace**.

This converts Azure Blob Storage into **Azure Data Lake Storage Gen2**.

Configuration:

- ✅ Enable Hierarchical Namespace
- Access Tier = Hot

Click

```
Review + Create
```

<p align="center">
<img src="images/03_enable_hns.png" width="100%">
</p>

---

# 📌 Step 4 — Deploy Storage Account

Azure validates the configuration and deploys the storage account.

After deployment completes,

Click

```
Go to Resource
```

<p align="center">
<img src="images/04_deployment_complete.png" width="100%">
</p>

---

# 📌 Step 5 — Create Blob Container

Navigate to

```
Storage Account

↓

Data Storage

↓

Containers

↓

Add Container
```

Container Name

```
ecomm-raw-data
```

Click

```
Create
```

<p align="center">
<img src="images/05_create_container.png" width="100%">
</p>

---

# 📌 Step 6 — Open the Container

Open the newly created container.

Container

```
ecomm-raw-data
```

You are now ready to upload the dataset.

<p align="center">
<img src="images/06_open_container.png" width="100%">
</p>

---

# 📌 Step 7 — Upload Dataset

Click

```
Upload
```

Drag & Drop your files or browse manually.

Example datasets

```
brands.csv
category.csv
customers.csv
date.csv
products.csv
order_items.csv
order_returns.csv
order_shipments.csv
```

Click

```
Upload
```

<p align="center">
<img src="images/07_upload_files.png" width="100%">
</p>

---

# 📌 Step 8 — Verify Uploaded Files

After uploading, verify that all folders/files are available.

Expected Dataset

```
brands/

category/

customers/

date/

products/

order_items/

order_returns/

order_shipments/
```

<p align="center">
<img src="images/08_uploaded_files.png" width="100%">
</p>

---

# 📂 Final Data Lake Structure

```text
Storage Account
│
└── ecomm-raw-data
    │
    ├── brands/
    ├── category/
    ├── customers/
    ├── date/
    ├── products/
    ├── order_items/
    ├── order_returns/
    └── order_shipments/
```

---

# ✅ Best Practices

- Use lowercase storage account names.
- Enable Hierarchical Namespace for Data Lake workloads.
- Use meaningful container names.
- Organize datasets into separate folders.
- Enable RBAC using Microsoft Entra ID.
- Enable Soft Delete and Versioning.
- Configure Lifecycle Management policies.
- Restrict public access to containers.
- Monitor storage usage using Azure Monitor.

---

# 🎯 Key Benefits

| Feature | Description |
|----------|-------------|
| 🚀 High Performance | Optimized for analytics workloads |
| 🔒 Secure | Microsoft Entra ID & RBAC |
| 📂 Hierarchical Namespace | Native folder support |
| 📈 Scalable | Petabyte-scale storage |
| 💰 Cost Optimized | Multiple storage tiers |
| ⚡ Analytics Ready | Integrates with Azure Databricks |

---

