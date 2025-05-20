# Microsoft Fabric Security: Access Control Implementation

This hands-on lab demonstrates how to implement multi-layered security in Microsoft Fabric, covering workspace roles, item-level permissions, and OneLake data access roles.

## Lab Objectives

✔️ Implement **workspace-level** access controls  
✔️ Configure **item-level** security for warehouses/lakehouses  
✔️ Apply **granular OneLake folder permissions**  
✔️ Validate security through multi-user testing  

## Prerequisites

- Microsoft Fabric tenant with admin access
- Two user accounts for permission testing
- Basic understanding of:
  - Fabric workspace structure
  - SQL analytics endpoints
  - Lakehouse architecture

## Step-by-Step Implementation

### 1. Workspace Setup

1. Create workspace with Fabric capacity
2. Build sample assets:
   - Data Warehouse (Sample dataset)
   - Lakehouse (Public Holidays sample)

### 2. Workspace Role Assignment

1. Assign "Viewer" role to test user
2. Validate:
   - Workspace visibility
   - Warehouse table access (ReadData)
   - Lakehouse SQL endpoint access

### 3. Item-Level Security

1. Remove workspace role assignment
2. Grant warehouse-specific permissions:
   - CONNECT
   - ReadData via SQL
3. Verify restricted access to lakehouse

### 4. OneLake Data Roles (Preview)

1. Enable OneLake access management
2. Create custom role for /publicholidays folder
3. Assign role to test user
4. Validate:
   - Folder-level access restrictions
   - Table-specific data visibility

### Key Security Concepts Demonstrated

▸ RBAC Hierarchy:
Workspace → Item → Folder-level controls

▸ Permission Inheritance:
How workspace roles differ from item permissions

▸ Least Privilege Principle:
Restricting access to only necessary resources

### Cleanup

1. Remove test user assignments
2. Delete workspace via Settings → Remove workspace

### 👤 Author: Sefa Öztürk

IT Intern | Azure Data Engineer (Ongoing)

📇 LinkedIn: https://www.linkedin.com/in/sefa-ozturk1972
