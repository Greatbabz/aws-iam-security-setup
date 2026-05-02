#  AWS IAM Security Setup

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws&logoColor=white)
![Security](https://img.shields.io/badge/Focus-Security-blue)
![IAM](https://img.shields.io/badge/Service-IAM-yellow)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

##  Project Overview
This project demonstrates secure AWS account configuration by replacing root account usage with a dedicated IAM admin user and enforcing Multi-Factor Authentication (MFA), following cloud security best practices.

It applies the **Principle of Least Privilege** to improve identity and access security.

---

##  Lab Context
This project was completed as part of AWS hands-on training, focusing on identity management and security best practices in cloud environments.

---

##  Objectives
- Eliminate daily use of the root account  
- Create a secure IAM admin user  
- Enable Multi-Factor Authentication (MFA)  
- Apply least privilege access control  
- Strengthen AWS account security posture  

---

##  Architecture

```
Root Account (setup only)
        │
        ▼
IAM Admin User (Basestack-admin)
        │
        ├── Password Authentication
        └── MFA (Authenticator App)
```

##  Implementation Steps

### 1. Secure Root Account
- Strong password configured  
- Root account restricted to setup only  

### 2. Create IAM Admin User
- Created user: `Basestack-admin`  
- Enabled console access  

### 3. Assign Permissions
- Attached **AdministratorAccess** policy (lab environment only)  

### 4. Enable MFA
- Configured MFA using authenticator app  
- Verified using authentication codes  

### 5. IAM Login Configuration
- Used IAM sign-in URL instead of root login  

---

##  Screenshots

### 1. Console sign-in as IAM user
![Console sign-in as IAM user](screenshots/iam-login.png)

---

### 2. IAM dashboard showing your Administrators group
![IAM dashboard showing Administrators group](screenshots/iam-admin-group.png)

---

### 3. IAM Security recommendations showing green-resolved items
![IAM Security recommendations showing green-resolved items](screenshots/iam-security-recommendations.png)

---

### 4. IAM user listed with MFA assigned
![IAM user listed with MFA assigned](screenshots/mfa-setup.png)

---

##  Key Security Concepts

- **Principle of Least Privilege**  
  Grant only required permissions for users.

- **Multi-Factor Authentication (MFA)**  
  Adds a layer of identity verification.

- **Root Account Protection**  
  The root account should only be used for initial setup and emergency access.

- **:contentReference[oaicite:0]{index=0}**  
  Central AWS service for managing users, roles, and permissions securely.

---

##  Outcome
- Root account usage eliminated for daily tasks  
- IAM-based access control implemented  
- MFA successfully enabled for secure authentication  
- Improved overall AWS security posture  

---

##  Lessons Learned
- AWS follows a default-deny security model  
- Permissions must be explicitly granted  
- IAM is foundational to AWS security design  
- MFA significantly reduces account compromise risk  

---

##  Future Improvements
- Implement IAM Groups and Roles  
- Enforce MFA for all users via policy  
- Create least-privilege custom policies  
- Explore AWS Organizations for multi-account security  

---

##  Tags
`AWS` `IAM` `Cloud Security` `MFA` `DevOps` `Beginner Project`
