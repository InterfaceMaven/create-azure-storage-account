# Azure Storage Account Lab

## 🎯 Overview
This repository documents my hands-on learning experience with Azure Storage services as part of the DP-900: Azure Data Fundamentals certification path.

## 📚 What I Learned

### Azure Storage Services Explored:
- **Blob Storage** - Object storage for unstructured data
- **Data Lake Storage Gen2** - Hierarchical namespace for big data analytics
- **Azure Files** - Cloud-based file shares with SMB/NFS protocols
- **Azure Tables** - NoSQL key-value store for structured data

## 🏗️ Lab Architecture
```
Azure Storage Account
├── Blob Storage (Container: data)
│   └── Virtual folder: product_data/
│       ├── product1.json
│       └── product2.json
├── Data Lake Gen2 (Hierarchical namespace enabled)
├── Azure Files (Share: files)
└── Azure Tables (Table: products)
```

## 🔧 Configuration Details

### Storage Account Settings:
- **Performance Tier:** Standard
- **Redundancy:** LRS (Locally Redundant Storage)
- **Access Tier:** Hot
- **Hierarchical Namespace:** Enabled (for Data Lake Gen2)

## 📝 Key Learnings

### 1. Blob Storage vs Data Lake Storage Gen2
**Before Hierarchical Namespace:**
- Folders are virtual (just prefixes in blob names)
- Cannot rename or set permissions on folders
- Designed for massive scale with flat namespace

**After Hierarchical Namespace (Gen2):**
- Folders become real directories
- Can rename folders and set granular permissions
- Supports POSIX-compliant ACLs
- Better for big data analytics workloads (Spark, Hadoop)

### 2. Azure Files Use Cases
- Lift-and-shift scenarios requiring traditional file systems
- SMB/NFS protocol support for cross-platform access
- File locking capabilities
- Can be mounted as network drives

### 3. Azure Tables Design
- NoSQL key-value store
- **PartitionKey + RowKey** = Composite primary key
- Schema-on-write (flexible schema)
- Ultra-low cost for simple structured data
- Trade-off: No complex queries or joins

## 🛠️ Lab Tasks Completed

- [x] Provisioned Azure Storage Account
- [x] Created blob container with virtual folders
- [x] Uploaded JSON files to blob storage
- [x] Upgraded to Data Lake Storage Gen2
- [x] Explored hierarchical namespace capabilities
- [x] Created and connected to Azure File Share
- [x] Created Azure Table and inserted entities
- [x] Compared schema flexibility in Table Storage

## 📂 Repository Structure
```
.
├── README.md                          # This file
├── LICENSE                            # MIT License
├── data/                              # Sample data files
│   ├── product1.json
│   └── product2.json
├── docs/                              # Detailed documentation
│   ├── 01-blob-storage.md
│   ├── 02-data-lake-gen2.md
│   ├── 03-azure-files.md
│   └── 04-azure-tables.md
└── screenshots/                       # Visual documentation
    └── (Azure Portal screenshots)
```

## 🔑 Key Concepts

### Storage Redundancy Options:
- **LRS** - 3 copies in one datacenter (used in lab)
- **ZRS** - 3 copies across availability zones
- **GRS** - Geo-redundant across regions
- **RA-GRS** - Geo-redundant with read access

### When to Use Each Service:

| Service | Best For | Not Ideal For |
|---------|----------|---------------|
| **Blob Storage** | Unstructured data, media files, backups | Data requiring file system semantics |
| **Data Lake Gen2** | Big data analytics, hierarchical data | Small-scale projects (overhead) |
| **Azure Files** | Lift-and-shift, shared file systems | High-throughput object storage |
| **Azure Tables** | Simple NoSQL data, logs, IoT data | Complex relational queries |

## 💡 Best Practices Learned

1. **Resource Groups** - Group related resources for easy management and cleanup
2. **Soft Delete** - Disable for hierarchical namespace compatibility
3. **Private Access** - Default to private containers for security
4. **Partition Keys** - Design for even distribution to optimize performance
5. **Cost Optimization** - Use LRS for non-critical data, Standard tier for learning

## 🔗 Resources

- [Microsoft Learn: DP-900 Lab](https://microsoftlearning.github.io/DP-900T00A-Azure-Data-Fundamentals/Instructions/Labs/dp900-02-storage-lab.html)
- [Azure Storage Documentation](https://docs.microsoft.com/azure/storage/)
- [DP-900 Certification Path](https://docs.microsoft.com/learn/certifications/azure-data-fundamentals/)

## 🎓 Certification Progress

This lab is part of my preparation for:
- **Microsoft Certified: Azure Data Fundamentals (DP-900)**



**Author:** InterfaceMaven  
**Date:** October 2025  
**Lab Duration:** ~15 minutes (as per Microsoft estimate)
