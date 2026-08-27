# Manual Close Cases

Follow these steps to properly close a case in Salesforce. This ensures accurate reporting and sends a clear resolution summary to the customer.

<div style="background-color: #f4f7f9; border-left: 8px solid #005a8c; padding: 10px 20px; margin-top: 30px; margin-bottom: 20px;">
    <h2 style="margin: 0; color: #005a8c; font-size: 1.5rem; font-weight: 300; border-bottom: none; padding: 0;">Steps to Close a Support Case</h2>
</div>

1. Navigate to the **Close Case** tab for the relevant support case.
2. Set the **Status** to **Closed**.
3. Select the appropriate **Sub-Status** (e.g., "Solution Completed" if the fix is confirmed, or "Solution Offered" if you've provided a solution without confirmation).
4. Verify the **Case Type** is correct (e.g., Product, Issue, Incident). This is critical for reporting.
5. Select the most fitting **Case Cause** and **Case Resolution** from the dropdown lists.
6. In the **Resolution Description** box, write a brief, clear summary of the resolution. **This text is visible to the customer** in their case closure notification email.
7. Click **Save** to officially close the case and trigger the notification.

---


!!! note "Handling Jira-Related Cases (Bugs & Feature Requests)"

	* The **Case Type** must be set to **Issue**.
	* A **Jira #** must be captured in the **Jira ID** field on the case.
	* If a workaround is available, use the Sub-Status **"Solution Offered"**. If not, use **"No Resolution"**.
	* Set the **Case Cause** depending on whether the issue is a bug or a feature request.
	* Set the **Case Resolution** to **"Logged with Product Development"**.
	* The **Resolution Description** field should contain a short summary of the resolution. This content will be included in the Case Closed receipt and is visible to the customer. Inform the customer that the issue has been logged with the development team and include the Jira ID for their reference.

---

!!! warning "Workflow for 'Product Development' Status"
    **Do not use the "Product Development" case status.** While it sends an automated notification, it does not integrate with Jira and leaves the case open until it is manually closed.
    
    **Instead, follow this workflow:**
    
    1. When Support logs a new Jira issue for a bug or feature request, inform the customer.
    2. **Close the support case manually** using the steps outlined above.
    3. When the Jira issue is eventually closed, it is best practice to inform the customer that the issue has been resolved in a separate communication.

!!! info "Important Notes"
    * If the Case Type is "Product", the **Case Product** field must be filled in on the "Case Coding" tab before you can close the case.
    * **Topic and Sub-Topic** fields are not used by the Structures team and can be ignored.