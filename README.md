# UserManager Utility

## Assignment Overview

The **UserManager Utility** is a Bash shell script designed to automate common Linux user and group management tasks. It simplifies administrative operations such as creating teams, adding users, assigning permissions, modifying user accounts, and removing users or groups through a single command-line utility.

---

# Objectives

- Create Linux teams (groups)
- Add users under a specific team
- Automatically create user home directories
- Create `team` and `ninja` directories
- Assign ownership and permissions
- Change user shell
- Change user password
- Delete users
- Delete teams
- List all users and teams

---

# Technologies Used

- Ubuntu Linux
- Bash Shell Scripting
- Linux User Management Commands

---

# Project Structure

```text
Assignment2/
│
├── Problem-Statement 
├── UserManager.sh
└── README.md
   
```

---

# Script Usage

## 1. Create Team

**Command**

```bash
sudo ./UserManager.sh addTeam amigo
sudo ./UserManager.sh addTeam unixkings
```

**Output**

<img width="960" height="218" alt="image" src="https://github.com/user-attachments/assets/5d89a53c-534e-42f7-8f63-fc523454e091" />


---

## 2. Add User

**Command**

```bash
sudo ./UserManager.sh addUser Rakesh amigo
sudo ./UserManager.sh addUser Sandeep unixkings
```

**Output**

<img width="960" height="212" alt="image" src="https://github.com/user-attachments/assets/2f9b23f3-27dd-4d7a-adb5-5ca5b755e7f3" />

---

## 3. Verify User Information

**Commands**

```bash
id Rakesh
groups Rakesh

id Sandeep
groups Sandeep
```

**Output**

<img width="960" height="308" alt="image" src="https://github.com/user-attachments/assets/bd0d0dce-6fb5-427a-b0bc-1c3436760a6b" />

---

## 4. Home Directory Structure

**Commands**

```bash
tree /home/Rakesh
tree /home/Sandeep
```

If `tree` is not installed:

```bash
ls -R /home/Rakesh
ls -R /home/Sandeep
```

**Output**

<img width="960" height="389" alt="image" src="https://github.com/user-attachments/assets/bdd7ccc8-eb97-4448-aa8a-1132e072f7cf" />

---

## 5. Directory Permissions

**Commands**

```bash
ls -ld /home/Rakesh

ls -ld /home/Rakesh/team

ls -ld /home/Rakesh/ninja
```

**Output**

<img width="960" height="286" alt="image" src="https://github.com/user-attachments/assets/94c69c2b-7b8b-4a67-983a-7a408ce32a54" />

---

## 6. Change User Shell

**Command**

```bash
sudo ./UserManager.sh changeShell Rakesh /bin/bash
```

**Output**

<img width="960" height="192" alt="image" src="https://github.com/user-attachments/assets/4a0e02eb-e154-4204-90fb-34fcac508d30" />

---

## 7. Change User Password

**Command**

```bash
sudo ./UserManager.sh changePasswd Rakesh
```

**Output**

<img width="960" height="192" alt="image" src="https://github.com/user-attachments/assets/a4803804-733f-42e6-acde-42c38a4ecd2a" />

---

## 8. List Users and Teams

**Commands**

```bash
sudo ./UserManager.sh ls User

sudo ./UserManager.sh ls Team
```

---

## 9. Delete User and Team

**Commands**

```bash
sudo ./UserManager.sh delUser Rakesh

sudo ./UserManager.sh delTeam amigo
```

**Output**

<img width="960" height="191" alt="image" src="https://github.com/user-attachments/assets/432589be-6174-4ef3-b419-1d4f3e23445e" />

---

# Permissions Used

| Directory | Permission | Description |
|-----------|:----------:|-------------|
| `/home/username` | **751** | Owner has Read, Write and Execute permissions. Group has Read and Execute permissions. Others have Execute permission only. |
| `/home/username/team` | **770** | Owner and Team members have full access. |
| `/home/username/ninja` | **770** | Owner and Group members have full access. |

---

# Sample Workflow

```bash
sudo ./UserManager.sh addTeam amigo

sudo ./UserManager.sh addUser Rakesh amigo

sudo ./UserManager.sh changeShell Rakesh /bin/bash

sudo ./UserManager.sh changePasswd Rakesh

sudo ./UserManager.sh ls User

sudo ./UserManager.sh ls Team

sudo ./UserManager.sh delUser Rakesh

sudo ./UserManager.sh delTeam amigo
```

---

# Learning Outcomes

This assignment provided practical experience with:

- Bash Shell Scripting
- Linux User Management
- Linux Group Management
- File Ownership
- File Permissions
- Command Line Arguments
- Case Statements
- Linux Administration Commands

---

# Conclusion

The UserManager Utility provides a simple command-line solution for performing common Linux user administration tasks. It demonstrates the practical implementation of Bash scripting concepts and Linux user management commands while improving automation and reducing manual administrative effort.

---
