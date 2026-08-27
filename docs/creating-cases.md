# Creating Support Cases

Standard workflows for finding, evaluating, and managing support cases within Salesforce Service Cloud.

<div style="background-color: #f4f7f9; border-left: 8px solid #005a8c; padding: 10px 20px; margin-top: 30px; margin-bottom: 20px;">
    <h2 style="margin: 0; color: #005a8c; font-size: 1.5rem; font-weight: 300; border-bottom: none; padding: 0;">Steps</h2>
</div>

1. **Start the Case:** Click <span style="color: #0063A3; font-style: italic;">New</span> on the "Cases" tab, or find a Contact and click <span style="color: #0063A3; font-style: italic;">New Case</span> from their related items.
	
	<img src="/assets/SF_NewCases.png" style="width: 100%; border: 1px solid #d1d5db; border-radius: 4px; transition: transform 0.3s ease;" onmouseover="this.style.transform='scale(1.5)'; this.style.zIndex='100'; this.style.position='relative';" onmouseout="this.style.transform='scale(1)'; this.style.zIndex='1';">
	
2. Select Case Record Type as <span style="color: #0063A3; font-style: italic;">Support Case</span>.

    ![Select Case Record Type Screenshot](assets/SF_supportcases.png){ width="50%" }

3. **Fill in Key Details:** Fill in all required fields (marked with a red asterisk *). The most important are:
    *   <span style="color: #0063A3; font-style: italic;">**Contact Name:**</span> Search for or create the customer contact. This confirms their support entitlement.
    *   <span style="color: #0063A3; font-style: italic;">**Subject & Description:**</span> A brief title and full details of the issue for the customer to see.
    *   <span style="color: #0063A3; font-style: italic;">**Impact & Urgency:**</span> These determine the case priority (e.g., P1-Critical).
    *   <span style="color: #0063A3; font-style: italic;">**Support Case:**</span> Choose the category (e.g., Product, General, Issue).
    *   <span style="color: #0063A3; font-style: italic;">**Case Product:**</span> If "Support Case" is "Product," select the specific product.

4. **Save and Assign the Case:**
    *   <span style="color: #0063A3; font-style: italic;">**To assign to yourself:**</span> Just click <span style="color: #0063A3;">**Save**</span>.
    *   <span style="color: #0063A3; font-style: italic;">**To assign to a queue:**</span> Check the **Assign using active assignment rule** box before clicking <span style="color: #0063A3;">**Save**</span>.

---

!!! info "Important Notes"
    **For Product cases:** You must go to the "Case Coding" tab to add the Product, Application, and Support Category details. This is required to route and close the case correctly.

!!! warning "Update for Manual Cases (WhatsApp, Line, etc.)"
    **Problem:** When manual cases are closed immediately, the "First Response Time" (FRT) is empty, which affects team reports.
    
    **Solution:** Before closing a manual case, please do **one** of the following to log the FRT:
    
    *   📞 **Log a Call Activity:** Add a call log describing the solution given.
    *   ✉️ **Send an Email:** Email the customer the solution from the case. (This also encourages them to use official email support!)

---

<div style="background-color: #f4f7f9; border-left: 8px solid #005a8c; padding: 10px 20px; margin-top: 30px; margin-bottom: 20px;">
    <h2 style="margin: 0; color: #005a8c; font-size: 1.5rem; font-weight: 300; border-bottom: none; padding: 0;">Priority Matrix Logic</h2>
</div>


By default, when a case is created, its Impact is set to "Localized" and Urgency is set to "Medium", which will lead to Priority 'P3-Medium' upon creation. Use the matrix below to determine the correct priority.

| Urgency / Impact | Widespread | Large | Localized | Individualized |
| :--- | :---: | :---: | :---: | :---: |
| **Critical** | P1 | P1 | P2 | P2 |
| **High** | P1 | P2 | P2 | P3 |
| **Medium** | P2 | P3 | P3 | P3 |
| **Low** | P4 | P4 | P4 | P4 |