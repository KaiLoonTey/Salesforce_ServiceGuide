# Expired License Support Guide

*Effective Date: Jan 2, 2026* | [Open Master GSheet Tracker](https://docs.google.com/spreadsheets/d/1TjwjLZDlcrQf-YUYeYpSXAbxuB9PpJDYQdCD_hcw9oM/edit?gid=1389052985#gid=1389052985)

![Renewal Resolution Workflow](assets/Renewal%20Guide.png)

---

## 1. Core Strategy & Communication

We operate on a **Passive / Reactive** basis. We will not engage customers prior to expiration. Our role is to act only **after** the license has lapsed and services have stopped. 

*   **Primary Action:** Handover to Renewal Specialist, Nadzmi Naim.
*   **System Rule:** All correspondence MUST be sent and logged via the Salesforce System. Do not use personal email.

!!!note "CC Protocol (Always Include):"

	| Role / Region | Name | Email |
	| :--- | :--- | :--- |
	| **Renewal Specialist** | Nadzmi Naim | nadzmi_naim@trimble.com |
	| **Singapore** | Mark Tung | mark.tung@trimble.com |
	| **Malaysia** | Engyau Wee | engyau.wee@trimble.com |
	| **Thailand** | Pongsura | pongsura.angkananuchat@trimble.com |
	| **Indonesia** | Ajie | ajie.pamadaraji@trimble.com |

!!! info "Inbound Response Template (Copy/Paste into Salesforce):"

    ```text
    Thank you for your inquiry.

    According to the system, the subscription for [Software Name] ended on 31st Dec 2025. As the date has passed, the license is currently inactive.
    
    To assist you further, I will hand over your case to our Renewal Specialist, [Nadzmi Naim] (cc'd). 
	They will be able to discuss the next steps to resolve this with you directly.
    ```

---

## 2. Emergency License Policy

Due to the volume of accounts, we utilize a single shared pool of licenses for emergency usage.

> **⛔ RESTRICTED ACCESS:**
> Support **shall not initiate** or mention Emergency Licenses until the customer explicitly complains. The **Sales Representative** must explicitly agree to and request the license issuance via email.

*   **Allocation:** First-come, first-served (one-time issuance per company).
*   **Issuance:** 5 Days default duration.
*   **Admin Tools Tracking:** Allocate using the *Trimble SEA* or *Trimble Malaysia* Emergency organization. Update the "Office Location" field immediately (Format: `[Support Name] - [Customer Company] - RW`).
*   **Log & Tag:** Update the Master GSheet Tracker.

---

## 3. Exit Plan

Once the renewal is active, execute the following closure steps:

*   **Notification:** Paste the Exit Notification (below) into the Salesforce reply.
*   **Removal:** Revoke emergency access 24 hours later.
*   **Cleanup:** Remove the "RW/BACKUP" tag from the Admin Panel and set the Tracker status to "Completed".


!!!note "Exit Notification Template:"
	
	```text
	"Your official license is now active. Please **reply to this email to acknowledge** that you have received and accessed the license.

	**Note:** If we do not receive a reply from you, the Emergency License will be removed at the end of the day."
	```