# Windows File Permissions Lab

## Overview

This lab demonstrates how to manage file and folder permissions in Windows using multiple user accounts. The goal was to restrict access to a folder and then restore access by modifying security settings.

---

## Lab Setup

* Environment: Windows 11 Virtual Machine (UTM on macOS)
* Accounts used:

  * Administrator (Bryan)
  * Standard User (employee1)

---

## Objectives

* Create a folder under one user account
* Restrict access to that folder
* Verify access is denied
* Restore access using proper permissions

---

## Steps Performed

### 1. Create Folder

Logged in as `employee1` and created a folder:

```
C:\Users\employee1\Desktop\HR_Files
```

---

### 2. Modify Permissions (Admin)

Switched to Administrator account and:

* Opened folder properties
* Navigated to Security tab
* Disabled inheritance
* Removed `employee1` from permissions

---

### 3. Verify Access Denied

Logged back in as `employee1` and attempted to open the folder.

Result:

* Access was denied

---

### 4. Restore Access

Returned to Administrator account and:

* Added `employee1` back to permissions
* Granted Full Control

---

### 5. Verify Access Restored

Logged back in as `employee1` and confirmed:

* Folder opened successfully

---

## Screenshots

See `/screenshots` folder for:

* Folder creation
* Permission settings
* Access denied message
* Access restored

---

## Key Takeaways

* Windows uses user-based access control for files and folders
* Permissions can be inherited from parent directories
* Disabling inheritance allows manual control of access
* Proper permission management is essential for security

---

## Skills Demonstrated

* File system permissions
* User access control
* Troubleshooting access issues
* Windows administration basics
