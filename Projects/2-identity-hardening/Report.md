# Report – 2: Identity Hardening with Microsoft Entra ID

## 1. What Identity Security Controls Were Implemented?

During this lab, the following identity-focused controls were implemented to enhance access security and privilege management within the Azure environment:

- **User and Group Provisioning:**
  - Created two standard test users: `demo-user1` and `demo-user2`.
  - Created a dedicated security group named `grp-security-testers` to manage access policies collectively.

- **Conditional Access Policy:**
  - Enforced **Multi-Factor Authentication (MFA)** for all users in `grp-security-testers`.
  - Targeted access to the **Microsoft Azure Management portal**, ensuring that sensitive resources require strong authentication.

- **Privileged Identity Management (PIM):**
  - Assigned the **Security Administrator** role to `demo-user1` using *eligible* role assignment.
  - Required **just-in-time role activation** with justification and optional approval, minimizing standing privileges.

---

## 2. What Did Microsoft Entra ID Recommend or Detect?

- **MFA Enforcement:**  
  Entra ID flagged the users as not registered for MFA initially. Once Conditional Access was enforced, users were prompted to register MFA during login.

- **PIM Recommendation:**  
  Microsoft recommends using **PIM** for all privileged roles. This best practice was implemented during the lab with an eligible assignment and on-demand activation.


---

## Summary

| Control Implemented        | Status         |
|----------------------------|----------------|
| Users and Groups           | Configured   |
| Conditional Access         | Enforced MFA |
| PIM Role Assignment        | Activated    |
| Audit and Sign-in Logs     | Reviewed     |

---

## Next Steps

- Simulate risky sign-ins in the future using a VPN or TOR.
- Explore **Defender for Identity** for deeper threat detection.
- Implement **Access Reviews** and **Entitlement Management** under Entra ID Governance.
