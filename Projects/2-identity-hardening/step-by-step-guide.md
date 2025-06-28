# Step-by-Step Identity Hardening Lab with Screenshots

This visual guide walks through **Identity Security with Microsoft Entra ID**, showing actual screenshots captured during each step of the hands-on lab.

---

## Step 1: Create Test Users and Security Group

- Created two test users:  
  - `demo-user1`  
  - `demo-user2`

- Created a **Security Group** named `grp-security-testers`
- Added both users to the group

 **Screenshot:** `Screenshots/Step1-users-created.png`

---

## Step 2: Conditional Access Policy – Require MFA

- Created a Conditional Access Policy named `MFA for Security Testers`
- Targeted group: `grp-security-testers`
- Targeted app: **Microsoft Admin Portals**
- Access control: **Require MFA**

- Tested policy:
  - Signed in as `demo-user1` using **Incognito Window**
  - **MFA Prompt triggered successfully**

 **Policy Summary Screenshot:** `Screenshots/Step2-ca-policy-summary.png`  
 **MFA Prompt Screenshot:** `Screenshots/Step2-mfa-prompt.png`

---

##  Step 3: Role Assignment via PIM

- Assigned `Security Administrator` role to `demo-user1` as **Eligible**
- Activated role using **Privileged Identity Management (PIM)**

 **Role Assignment Summary:** `Screenshots/Step4-role-assignment.png`  
 **PIM Activation Screen:** `Screenshots/Step4-pim-activation.png`

---

##  Final Notes

- For analysis and observations, refer to `Report.md`

---
