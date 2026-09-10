# Service Team Salesforce Quick Text

A centralized repository of standardized quick text templates for use in Salesforce. Use these snippets to ensure consistent, professional, and efficient communication with our customers.

---

!!!info "General Best Practices"

	* **Efficiency (Save Time):** Use these templates in Salesforce to quickly respond to common inquiries without typing from scratch.
	* **Adaptability (Personalize):** Always review and fill in bracketed fields like `[Customer Name]` to maintain a personal touch.
	* **Tone (Brand Voice):** These texts are written to reflect Trimble's professional, helpful, and appreciative brand voice.
	* **Flexibility (Use Judgment):** Templates are a starting point. Modify the text as needed to perfectly fit the customer's specific situation.

---

## Salesforce Quick Text Library

!!! info "CSAT Survey Request"
    *Use this text when confirming resolution and officially closing a support case to encourage survey completion. (Optional: Do not use for escalated cases)*

    ```text
    I am glad we were able to resolve your issue! 

    Shortly after this case is closed, you will receive a brief survey regarding your support experience. We would greatly appreciate it if you could take a minute to share your feedback. Your insights directly help us improve our service.

    Thank you for choosing Trimble!
    ```

!!! info "Reset License for Tekla Structures"
    *Use this text when you have manually reset a Tekla Structures license and need to instruct the user on how to correctly release the license upon closing the software.*

    ```text
    We have manually reset the license from our end.

    Please note that the online license can be reserved for up to 3 days on the device it was last used on for offline work.
    Should you need to use the license on another device, please ensure ALL DEVICES using Tekla Structures now or in the future are set to release the license upon closing.

    To do this, please ensure the "Keep this license reserved on this device" checkbox is CLEARED (unchecked) in the confirmation dialog box whenever you close the software.

    This requirement also applies if you use different year versions of Tekla Structures. Please ensure this checkbox is cleared for ALL DEVICES and ALL VERSIONS of Tekla Structures.

    Tip for future use: To prevent the license from getting locked by accident, you can set the software to leave this box unchecked by default. In Tekla Structures, go to File > Settings > Advanced Options, search for XS_DEFAULT_KEEP_ONLINE_LICENSE_CHECKBOX, and set its value to FALSE.

    You may refer to this link for a visual guide on releasing your license: [https://support.tekla.com/article/subscription-license-release-issues-in-tekla-structures-including-the-all-in-use-message](https://support.tekla.com/article/subscription-license-release-issues-in-tekla-structures-including-the-all-in-use-message)
    ```

!!! info "Reset License for Structural Design (TEDDS/TSD)"
    *Use this text when you have manually reset a structural design (TEDDS/TSD) license and need to instruct the user on modifying their retention settings.*

    ```text
    We have manually reset the license from our end.

    Please note that online license is by default set to keep for 3 days on the device it was last log in. 
    Should you need to use it on another device, please ensure ALL DEVICES using TEDDS/Tekla Structural Designer (TSD) now or in the future are set to retain as NO.

    This also applies to ALL other TEKLA product if your online license can access multiple software.

    Please set retain to NO for ALL DEVICES and ALL TEKLA PRODUCTS.

    You may refer to this link for guide: [https://support.tekla.com/article/can-i-use-my-online-license-when-not-connected-to-the-internet](https://support.tekla.com/article/can-i-use-my-online-license-when-not-connected-to-the-internet)
    ```