

# Policy Update: Retirement of Maintenance & Support Services

!!! info "Internal Enablement Session: Friday, Sept 25"
    This policy guide is based on the enablement session hosted on **Friday, September 25**. Ahead of the October 1 public rollout, all support team members must align on these policy principles, legal groundings, and decision frameworks.
    
	**Presenters:** Panu Laasonen & Anne Palsala
    
	**Meeting Link / Recording:** [Google Meet ↗️](https://drive.google.com/file/d/1XlBQNMrWu_xonsEecqC_EH5SZYh_1f1Z/view)
    (Note: The event was recorded and distributed for those unable to attend live).

![Perpetual License Support Retirement Guide](assets/Perpetual_License_Support_Retirement_Guide.png)

## 1. Announcement Overview

| Event | Date | Status / Impact |
| :--- | :--- | :--- |
| [**Prior Announcement (End of Life)** ↗️](https://www.tekla.com/terms-and-conditions/end-of-life){:Target="blank"} | June 11, 2024 | <span style="color:green">Completed</span> |
| **Retirement Announcement** | October 1, 2026 | <span style="color:green">Completed</span> |
| **Maintained Licenses (EOL Date)** | Dec 31, 2027 | Final Support Deadline |
| **Unmaintained Licenses** | Immediate | No replacement keys/support |

!!! warning "Executive Insights: Affected Services"
    Trimble will **cease active support** for obsolete/non-supported software versions, license activation services, license re-hosting services, and the provision of replacement keys (e.g., due to hardware failure). This immediately impacts all perpetual licenses without a valid maintenance contract.

---

## 2. Key Milestones & Support Boundaries

| License Status | Support Eligibility | Target End Date |
| :--- | :--- | :--- |
| **With Valid Maintenance** | Eligible for full support, activation, re-hosting, and replacement keys. | **31 December 2027** |
| **Without Valid Maintenance** | Trimble will not issue replacement keys or provide support. | <span style="color:red; font-weight:bold;">Effective Immediately</span> |

!!! warning "Emergency License Restriction"
    * **Policy:** Losing access to an unmaintained license or experiencing server failure does not entitle the customer to an emergency license.
    * **Reasoning:** Providing an emergency license falls under support services, which are unavailable for non-maintained licenses. 
    * **Action:** Adhere strictly to the policy to ensure a consistent customer experience; do not provide exceptions.

### Ceased Services Breakdown (Post-EOS)

<table style="width: 100%; text-align: left; border-collapse: collapse;">
  <thead>
    <tr style="border-bottom: 1px solid #e5e7eb;">
      <th style="padding: 12px; width: 30%;">Service Category</th>
      <th style="padding: 12px; width: 70%; border-right: 1px solid #e5e7eb;">Description of Ceased Action</th>
    </tr>
  </thead>
  <tbody>
    <tr style="border-bottom: 1px solid #e5e7eb;">
      <td style="padding: 12px; font-weight: bold; color: #0063a3;">Activations</td>
      <td style="padding: 12px; border-right: 1px solid #e5e7eb;">No longer processing initial license activations for legacy perpetual software.</td>
    </tr>
    <tr style="border-bottom: 1px solid #e5e7eb;">
      <td style="padding: 12px; font-weight: bold; color: #0063a3;">Re-Hosting</td>
      <td style="padding: 12px; border-right: 1px solid #e5e7eb;">Stopping all license re-hosting services to move licenses between servers.</td>
    </tr>
    <tr style="border-bottom: 1px solid #e5e7eb;">
      <td style="padding: 12px; font-weight: bold; color: #0063a3;">Replacement Keys</td>
      <td style="padding: 12px; border-right: 1px solid #e5e7eb;">No provision of replacement keys in the event of hardware failure or lost licenses.</td>
    </tr>
    <tr>
      <td style="padding: 12px; font-weight: bold; color: #0063a3;">Legacy Support</td>
      <td style="padding: 12px; border-right: 1px solid #e5e7eb;">No active support for obsolete, non-supported software versions.</td>
    </tr>
  </tbody>
</table>

---

## 3. Customer Risk Management

| Recommendation | Action Required |
| :--- | :--- |
| **Server Security** | Ensure license server hardware is secure and up to date. |
| **OS & Patches** | Install the latest available supported OS and security patches to keep the environment stable. |
| **Software Updates** | Keep license server software updated to ensure compatibility with Tekla applications. |

!!! warning "Critical Actions to Avoid (Unmaintained Licenses)"
    If using licenses without a maintenance contract, customers must **NOT**:
    
    1. Deactivate, return, or rehost licenses to a different server machine.
    2. Change hardware components on the server.
    3. Rename the server.
    
    *Every operation that requires activation to different hardware possesses a risk of technical failure.*

---

## 4. Contractual Basis & Liability

| Concept | Definition |
| :--- | :--- |
| **Perpetual Right Scope** | Grants permanent permission to run the specific version delivered at purchase on original hardware. |
| **Contractual Fulfillment** | Delivery is fulfilled on the date the initial license key is made available. |
| **Maintenance Services** | License activation, key replacement, and server re-hosting are electronic services provided *only* during an active Maintenance Term. |

### EULA Clause 4.13 Compliance

!!! info "EULA Clause 4.13: Hardware Risk & Disposal"
    * **Risk Transfer:** Risk of hardware malfunction or installation environment failure passes to the customer upon delivery.
    * **Disposal Requirement:** "When disposing of Equipment in any manner whatsoever, You shall uninstall and remove and ensure that any Authorized Affiliates or Professional Consultants uninstall and remove the Software from such equipment prior to disposal, and take all other steps necessary to prevent the Software or any part thereof from coming into the possession of any third parties".
    * **Liability:** "A failure to do so shall be deemed to constitute breach of this EULA".
    
    [Eula 2021 ↗️](https://www.tekla.com/terms-and-conditions/eula-2021){:Target="blank"} | [Eula 2024 revB ↗️](https://www.tekla.com/terms-and-conditions/eula){:Target="blank"}

---

## 5. Support Decision Framework & Escalation Path

<br>
<br>
```mermaid
graph TD
    A[Does customer have active<br/>maintenance contract for licenses?]
    
    A -->|YES| B[Is the request for a supported<br/>legacy version activation on<br/>new/failed hardware?]
    A -->|NO| C[Has customer been informed<br/>of EULA / Offering Terms?]
    
    B -->|YES| D[<b>Resolution</b><br/>Proceed to Technical Support.<br/>Full support SLA applies.<br/>Generate replacement key<br/>or assist with migration.]
    B -->|NO| E[<b>Resolution</b><br/>Use the 'Initial Response'<br/>template to explain Clause 4.13<br/>and Service boundaries.]
    
    C -->|NO| E
    C -->|YES| F[Is the customer willing to<br/>explore NUL subscription<br/>options with Sales?]
    
    F -->|NO| G[<b>Resolution</b><br/>Reiterate that non-maintained<br/>perpetual licenses are out<br/>of support and close ticket.]
    F -->|YES| H[<b>Resolution</b><br/>Inform Sales or<br/>Account Manager]

    %% Applying border colors to match the image
    classDef resolutionGreen fill:#fff,stroke:#2e7d32,stroke-width:2px,color:#000;
    classDef resolutionRed fill:#fff,stroke:#c62828,stroke-width:2px,color:#000;
    classDef standardBox fill:#fff,stroke:#1565c0,stroke-width:2px,color:#000;
    
    class A,B,C,F standardBox;
    class D,H resolutionGreen;
    class E,G resolutionRed;
```

## 6. Standard Support Response Templates

### Template 1: Initial Response (Hardware Failure/Loss)

```text
Subject: Regarding your Tekla License Activation Request

Dear [Customer Name],

Thank you for reaching out to us regarding your Tekla software license. We understand that you have experienced a hardware failure and are looking to reactivate your perpetual license on new equipment.

After reviewing your account, we have noted that the Maintenance Services for this license expired on [Date].

According to the Tekla End-User License Agreement (EULA) and our Lifecycle Policy:

*   Infrastructure Liability: The responsibility for maintaining the hardware and the environment required to run perpetually licensed software rests with the licensee (EULA Clause 4.13).
*   Service Dependency: Technical services such as license re-hosting, activation, and entitlement resets are provided exclusively as part of an active Maintenance Term (EULA Clause 5.2).

As this license is no longer covered by an active maintenance contract, we are unable to provide a new activation key or reset the entitlement for your new hardware.

Next Steps: While we cannot reactivate the legacy perpetual license, we want to ensure your business remains operational. Our Sales team can provide you with details on our modern Named User Subscription model, which offers greater flexibility, identity-based access (no more hardware-locked keys), and continued software updates.

I have cc'd your Account Manager, [Name], who can discuss transition options with you.

Best regards,

[Your Name] 
Tekla Support
```

### Template 2: Explaining "Perpetual" vs. "Support"

```text
Subject: Clarification on Perpetual License Rights

Dear [Customer Name],

I understand the frustration caused by the current situation. I would like to clarify the distinction between your license rights and the services required to manage them.

A Perpetual License grants you the indefinite right to use the specific version of the software delivered to you at the time of purchase. It is similar to owning a piece of equipment; you have the right to keep and use it.

However, Activation and Re-hosting Services are part of our Maintenance and Support package. These are active electronic services that require Trimble to maintain server infrastructure and provide technical resets. These services are only available while a maintenance contract is in place.

When hardware fails on an unsupported system, the "delivery" of the original contract is considered complete, and the risk for the installation environment has passed to the user (EULA Clause 4.13). Without a maintenance agreement, we do not have a contractual vehicle to provide "re-delivery" to new hardware.

We highly recommend moving to our subscription model to avoid hardware-based lock-ins in the future.

Best regards,

[Your Name] 
Tekla Support
```



## 7. Frequently Asked Questions (FAQ)

!!! info "Reference" 
	Source: [End of Sales of Tekla Maintenance Products for Perpetual License ↗️](https://support.tekla.com/article/end-of-sales-of-tekla-maintenance-products-for-perpetual-license?_gl=1*glopb2*_gcl_au*MTAyMTMxNDQ5MS4xNzg5NTMwMTI3*_ga*MjAzMDk2MjU4OS4xNzg5NTMwMTI3*_ga_X88YXSWCN1*czE3OTI0NzY2NDYkbzE3MyRnMSR0MTc5MjQ3NzMwNSRqNjAkbDAkaDA.){:Target="blank"}

??? faq "1. What has been announced?" 
	Trimble announced the end of sale of maintenance products for all perpetual license types of Tekla software.

??? faq "2. Which products are affected by this change?" 
	End of Sale is announced for the following maintenance products:

	```
	* **Tekla Structures**
	  * Project Viewer
	  * Production Planner - Concrete
	  * Drafter
	  * Construction Modeling
	  * Engineering
	  * Rebar Detailing
	  * Precast Concrete Detailing
	  * Steel Detailing
	  * Primary
	  * Full
	* **Tekla Structural Designer**
	* **Tekla Structural Designer LT**
	* **Tekla Tedds**
	* **Tekla Tedds LT**
	* **Tekla Portal Frame Designer**
	* **Tekla Portal Frame Designer LT**
	* **Tekla Connection Designer**
	* **Tekla EPM**
	  * Tekla EPM Maintenance
	  * Tekla EPM Additional maintenance
	  * Tekla EPM Estimating maintenance
	  * Tekla EPM Go maintenance
	  * Tekla EPM Go Unlimited maintenance
	  * Tekla EPM Inventory maintenance
	  * Tekla EPM LT150 maintenance
	  * Tekla EPM Production maintenance
	  * Tekla EPM Production Additional maintenance
	```

??? faq "3. When will the last maintenance contracts be available for purchase?" 
	The last maintenance contracts can be renewed in the fourth quarter of 2026, with all contracts ending no later than December 31, 2027.

??? faq "4. What happens to existing customers with active maintenance contracts?" 
	If you have an active maintenance contract, you may choose to renew annually until 2026. Maintenance service renewed in 2026 will be provided until December 31, 2027. We recommend starting to plan for your transition to subscription. We offer an upgrade path for our existing customers.

??? faq "5. Are Tekla products available only via subscription?" 
	Tekla products are currently available via subscription and starting from January 1, 2028, all Tekla software products will be available exclusively through subscription.

??? faq "6. What is the subscription offering for Tekla products?" 
	Tekla subscription offering covers all our software products available as subscription:

	```
	* Tekla Structures
	* Tekla Tedds
	* Tekla Structural Designer
	* Tekla PowerFab
	* Trimble Connect

	For more information, please check our Tekla software products website or contact your local Tekla representative.
	```

??? faq "7. Can I renew my maintenance contract now to extend beyond 2027?" 
	No, all maintenance contracts will expire no later than December 31, 2027, and will not be renewable beyond that date.

??? faq "8. Why is Trimble ending the sale of maintenance products for Tekla perpetual licenses?" 
	Trimble is transitioning towards a subscription-based model to align with the evolving software landscape and customer needs. This approach aims to provide more flexible, scalable, and up-to-date solutions.

??? faq "9. Can I continue to use my existing perpetual licenses after 2027?" 
	Yes, you can use the latest version you own. However, after the end of your maintenance contract, you will no longer have access to newer versions of the software, service packs, and all the benefits included in the maintenance plan, such as local help desk services. As stated in our Tekla Software Lifecycle Policy, if using old versions beyond the Recommended Age, data might be exposed to risks or other sudden problems might occur. It is recommended to use the latest Tekla product versions and install service packs or other possible security updates to utilize the benefits and ensure reliability and security. Trimble shall not be liable for any claims or damages related to the use of a product after its Recommended Age.

??? faq "10. What support will be available once maintenance can no longer be purchased (for perpetual license)?" 	
	Starting in 2028, the help desk support will be available for customers on subscription only. Product version support is available according to our Tekla Software Lifecycle Policy.

??? faq "11. I am off maintenance now, can I buy a new maintenance contract?" 
	No, we do not offer new maintenance contracts any longer. For customers currently off maintenance, we recommend subscription plans.

??? faq "12. Will I be able to deactivate and activate my perpetual license if using them without maintenance even after 2027?" 
	No. Support for license activation and re-hosting services for legacy perpetual licenses depends on your maintenance status leading up to December 31, 2027, and will end completely after that date:

	**Licenses without a valid maintenance contract:** Trimble no longer issues replacement keys or supports license activation or re-hosting services, effective immediately.
	
	**Licenses with a valid maintenance contract:**  You can continue to activate and re-host your perpetual licenses through December 31, 2027.
	
	After December 31, 2027: Trimble will no longer support re-hosting, activation services, or replacement keys for any legacy perpetual licenses, regardless of whether they previously had an active maintenance contract.
	Note: If you choose to remain on a perpetual license, ensure it is set up in a modern, stable server environment prior to December 31, 2027. Any hardware failure after this date will result in the permanent loss of the license.