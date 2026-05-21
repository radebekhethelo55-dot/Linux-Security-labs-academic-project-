## 🐧 Linux User & Group Management

This is a hands-on Linux lab completed as part of my Pre-Degree in Cybersecurity. This lab covers creating and managing user accounts and groups, applying security policies such as password expiry and account lockout.

---

## 🎯 Objective
Create and manage user accounts and groups on a Linux system, applying real-world security policies used in enterprise environments.

---

## 🛠️ Commands Used

| Command | Purpose |
|--------|---------|
| `sudo groupadd` | Create a new user group |
| `sudo adduser` | Create a new user account |
| `sudo members` | Display members of a group |
| `sudo chage -M 60` | Set password to expire every 60 days |
| `sudo chage -E` | Set an account expiry date |
| `sudo passwd -l` | Lock a user account |

---

## 📋 What Was Done

### Group & User Creation
Created groups `eduvos_staff` and `eduvos_students` using `sudo groupadd`. Created 6 user accounts and assigned 2 users to each group using `sudo adduser`.

1

### Verifying Group Members
Installed and used the `members` command to verify correct group assignments:
```bash
sudo apt install members
members eduvos_students
members eduvos_staff
```
3

### Password Expiry Policy
Applied a 60-day password renewal policy to all student accounts:
```bash
sudo chage -M 60 username
```
This reduces the risk of compromised credentials being used long-term.

4

### Account Expiry Date
Set staff member Ike's account to automatically close on 31 December 2025:
```bash
sudo chage -E 2025-12-31 ike
```
Useful for managing temporary or contractor access.

### Account Lockout
Locked student member Tendai's account to immediately revoke access:
```bash
sudo passwd -l tendai
```
last
---

## 📚 What I Learned
- How Linux handles user and group permissions
- Why password expiry policies matter in enterprise security
- How to immediately revoke access by locking accounts
- The principle of least privilege in a Linux environment

---

## 🎓 About This Lab
Completed as part of the **Higher Certificate in Cybersecurity** at **Eduvos (2025)**.

**Certifications:** Cisco Networking Academy | IBM Cybersecurity Fundamentals

**Currently Studying:** CompTIA Network+ | Security+ | CySA+
