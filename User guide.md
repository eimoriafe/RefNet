# 🩺 **User Guide – RefNet Power App**  
**Author:** Emmanuel E. Imoriafe  
**Date:** 2025-06-01  
**System Name:** RefNet – Referral Network Management System  
**Category:** End-User Documentation  

---

## 1. Introduction  

**RefNet Power App** is a secure, cloud-based system that allows authorized staff to refer **migrant returnees** to **approved external medical service providers**, track treatments, and manage **payment approvals** efficiently through automated workflows.  

This guide provides step-by-step instructions for end users — including **Medical Staff**, **Unit Focals**, **Program Managers**, and **Finance Officers** — to perform their assigned tasks within RefNet.

---
<img width="1121" height="559" alt="image" src="https://github.com/user-attachments/assets/404b4407-1219-4853-8bbf-6d094f09adbb" />



## 2. Access and Authentication  

### 2.1 System Access Requirements  
- Microsoft 365 account linked to **Azure Active Directory (AAD)**  
- Assigned **RefNet user role** (Doctor, Unit Focal, Program Manager, or Finance Team)  
- Internet access via a **modern browser** (Edge, Chrome, or Firefox)  

### 2.2 How to Log In  
1. Visit the RefNet App Portal (Power Apps URL):  
   `[https://apps.powerapps.com/play/refnet-app](https://apps.powerapps.com/play/refnet-app)`  
2. Click **Sign in with Microsoft**  
3. Enter your organizational email and password  
4. Upon authentication, you’ll be redirected to your **role-specific dashboard**  

---

## 3. User Roles & Permissions  

| Role | Access Scope | Primary Actions |
|------|---------------|-----------------|
| **Doctor / Medical Staff** | Create and track referrals | Submit referral forms for approval |
| **Internal Medical Approver** | Approve referrals | Validate provider assignments |
| **Unit Focal** | Manage invoices | Raise and submit payment requests |
| **Program Manager** | Approve payments | Review and authorize financial requests |
| **Finance Team** | Process payments | Complete payments and log transactions |

> 🔐 **Note:** Role-Based Access Control (RBAC) ensures that each user can only view and perform actions relevant to their assigned role.

---

## 4. Key Workflows  

### 4.1 Referral Submission  
**Performed by:** Doctor / Authorized User  

1. Open RefNet Power App  
2. Select **New Referral**  
3. Fill in the following fields:  
   - Beneficiary Name  
   - Medical Condition / Assessment  
   - Assigned Service Provider (from approved list)  
   - Additional Notes or Attachments (if any)  
4. Click **Submit Referral**  
5. System automatically routes referral to the **Internal Medical Review Team**

---

### 4.2 Medical Review & Approval  
**Performed by:** Internal Medical Professional  

1. Navigate to the **Pending Reviews** tab  
2. Open a submitted referral  
3. Review details and supporting documents  
4. Select **Approve** or **Reject**  
5. Approved referrals are routed to the **External Provider** for treatment  

---

### 4.3 Invoice Submission  
**Performed by:** External Medical Provider (through internal focal interface)  

1. After service completion, submit treatment invoice and report via the linked SharePoint portal  
2. Internal **Unit Focal** validates the invoice  
3. Focal raises a **Payment Request** in RefNet  

---

### 4.4 Payment Request Workflow  
**Performed by:** Unit Focal → Program Manager → Finance Team  

1. Go to **Finance → Payment Requests**  
2. Select **New Request**  
3. Attach the **Service Invoice** and **Treatment Report**  
4. Click **Submit for Approval**  
5. **Program Manager** reviews and approves the request  
6. Once approved, it routes automatically to **Finance Team** for action  

---

### 4.5 Finance Processing & Completion  
**Performed by:** Finance Officer  

1. Review the approved payment record  
2. Verify attached documents and internal budget codes  
3. Record payment details and mark status as **Paid**  
4. Click **Complete Transaction**  
5. System triggers automated notifications to:  
   - Doctor / Medical Staff  
   - Unit Focal  
   - Program Manager  

---

## 5. Notifications  

RefNet uses **Power Automate Flows** to send automatic email and in-app notifications at every workflow stage:  

| Event | Recipients | Trigger |
|--------|-------------|----------|
| New Referral Submitted | Medical Reviewers | Doctor submits referral |
| Referral Approved | External Provider | Internal medical approval |
| Payment Request Submitted | Program Manager | Unit focal submits request |
| Payment Approved | Finance Team | Manager approves payment |
| Payment Completed | All Stakeholders | Finance finalizes payment |

---

## 6. Data Management  

- All data is stored in **SharePoint Lists**  
- Data can be migrated to **Microsoft Dataverse** if scaling is required  
- Data retention and audit logs comply with **organizational data policies**  

### Backup Policy  
- Daily snapshot backup via Azure Backup  
- Retention period: **90 days**  
- Recovery Point Objective (RPO): **< 24 hours**  

---

## 7. Security Features  

| Control | Description |
|----------|-------------|
| **Azure AD Authentication** | Enforces single sign-on and MFA |
| **RBAC** | Ensures fine-grained access control |
| **Encryption** | AES-256 encryption at rest; TLS 1.2+ in transit |
| **Audit Logs** | Automatically logged in SharePoint and Power Automate |
| **Compliance** | Aligns with NIST, ISO 27001, and GDPR standards |

---

## 8. Troubleshooting  

| Issue | Possible Cause | Recommended Action |
|--------|----------------|--------------------|
| Cannot sign in | User not in Azure AD group | Contact IT Admin for access |
| Missing approval button | Insufficient permissions | Confirm role assignment |
| Power Automate flow failed | Connection expired | Refresh Power Automate connection |
| Data not saving | SharePoint connectivity issue | Retry or contact system administrator |

---

## 9. Support & Feedback  

For assistance, contact:  

**System Architect:** Emmanuel E. Imoriafe  
**Department:** ICT  
**Email:** ``  
**Documentation Repo:** [RefNet GitHub Repository](https://github.com/organization/refnet-docs)  

> 💬 *Users are encouraged to submit feedback through the in-app “Help & Support” button.*

---

## 10. Version Control  

| Version | Date | Changes |
|----------|------|----------|
| **v1.0** | 2025-06-11 | Initial user guide publication |
| **v1.1** | _Pending_ | Add Dataverse integration and Power BI visualization steps |

---

**RefNet Power App** — *Simplifying healthcare referrals and financial workflows through secure, cloud-powered automation.*
