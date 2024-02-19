---
description: >-
  You can add or update multiple users in a Microsoft Excel spreadsheet template
  and then upload that sheet into NexPort Campus.
---

# Bulk Upload Users

## **To upload multiple users**

<mark style="color:blue;">**Step 1:**</mark> Click <mark style="color:blue;">**Administration**</mark> > <mark style="color:blue;">**Manage Users**</mark> > <mark style="color:blue;">**Upload Users**</mark>.

![](../../../.gitbook/assets/Upload\_Users.png)

<mark style="color:blue;">**Step 2:**</mark> Do the following to upload users in NexPort Campus:

<mark style="color:blue;">**Step 2a:**</mark> Download the Microsoft Excel spreadsheet template, and then save it on your computer.

<mark style="color:blue;">**Step 2b:**</mark> Type the user information in the Microsoft Excel spreadsheet template for the users you need to add to NexPort Campus.

<mark style="color:blue;">**Step 2c:**</mark> Upload the Microsoft Excel spreadsheet.

<mark style="color:blue;">**Step 2d:**</mark> Select or clear the <mark style="color:blue;">**Send Welcome Letters**</mark>, <mark style="color:blue;">**Resend Welcome Letters**</mark><mark style="color:blue;">,</mark> or <mark style="color:blue;">**Update Existing Users**</mark> check boxes.

| Check box                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                             |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <mark style="color:blue;">**Send Welcome Letters**</mark>   | <p>If selected, all <strong>new</strong> users receive a welcome letter from the organization that they receive a subscription from. Existing users do not receive a welcome letter.</p><p>For more information about how to customize a welcome letter, see <a href="https://www.nexportcampus.com/Content/Guides/aweb/Content/Module_Topics/Campus_Management/Group_Tools/Customize/Customize.htm">Customize</a>.</p> |
| <mark style="color:blue;">**Resend Welcome Letters**</mark> | All **existing** users receive a new welcome letter from their organization. For more information about how to customize a welcome letter, see [Customize](../Campus\_Management/Group\_Tools/Customize/Customize.htm).                                                                                                                                                                                                 |
| <mark style="color:blue;">**Update Existing Users**</mark>  | If selected, then any users identified that already exist are updated with the new information found on the spreadsheet. If not selected, the existing users are ignored.                                                                                                                                                                                                                                               |

<mark style="color:blue;">**Step 2e:**</mark> Click <mark style="color:blue;">**Process Users**</mark>.

> The user information is updated.
>
> ## Bulk User Upload Spreadsheet Reference
>
> To assist NexPort Campus administrators with the process of uploading new users or changing existing users via the provided spreadsheet, here is a comprehensive guide on what to input in each column of the spreadsheet. Ensure that the first row consists of the headers as listed below, and each subsequent row represents a single user to be added or modified.
>
> #### Spreadsheet Columns and Descriptions
>
> 1. **Login**: The user's unique login identifier. It's typically their username used for logging into the system.
> 2. **Email**: The user's email address. This should be a valid and active email as it may be used for communication and password resets.
> 3. **First Name**: The user's first name.
> 4. **Middle Name**: The user's middle name. This field can be left blank if the user does not have a middle name.
> 5. **Last Name**: The user's last name or surname.
> 6. **Culture**: The user's locale or culture code, indicating their preferred language and regional settings (e.g., en-US for English, United States). [Look here for a list of supported culture codes.](../supported-language-and-culture-codes.md)
> 7. **Password**: The initial password for the user's account. Ensure it meets the system's security requirements. If updating an existing user the password can be left blank.
> 8. **Provider**: The authentication provider for the user. Specify if the system uses multiple authentication sources.
> 9. **Subscription Group Shortname**: The short name for the [subscription organization](../campus-management/organization-tools/subscriptions/) to which the user should be added.&#x20;
> 10. **Expiration Date**: The date when the user's account or subscription expires. Format: MM/DD/YYYY. Leave blank if not applicable.
> 11. **Activation Duration in Days**: The number of days from the account creation or activation until it expires. Leave blank if using a specific expiration date.
> 12. **Memberships**: Any groups, the user should be assigned a membership to within the system. This is a comma separated list of group short names.&#x20;
> 13. **Billing Code**: If applicable, the billing code or department code associated with the user for accounting or HR purposes.
> 14. **Title**: The user's title (mr, mrs, etc) or position within the organization.
> 15. **Nickname**: Any nickname or informal name the user prefers to go by.
> 16. **City**: The city part of the user's address.
> 17. **State**: The state, province, or region part of the user's address.
> 18. **Country**: The country part of the user's address.
> 19. **Postal Code**: The postal or ZIP code part of the user's address.
> 20. **Address Line 1**: The first line of the user's street address.
> 21. **Address Line 2**: Additional address information, such as apartment or suite number.
> 22. **Phone**: The user's primary telephone number.
> 23. **Fax**: The user's fax number, if applicable.
> 24. **Notes**: Any additional notes or information relevant to the user's account.
> 25. **Welcome Letter CC**: Email addresses to carbon copy (CC) on the welcome letter, if any are sent out upon account creation.
> 26. **Welcome Letter BCC**: Email addresses to blind carbon copy (BCC) on the welcome letter, ensuring privacy of the recipients.
>
> #### Guidelines for Completion
>
> * Ensure all mandatory fields are completed for each user. Mandatory fields typically include Login, Email, First Name, and Last Name.
> * Use consistent formats for dates (MM/DD/YYYY) and phone numbers to ensure data integrity.
> * For fields not applicable to a user, leave them blank. Do not input "N/A" or similar text unless specified by your system requirements.
> * Double-check the spreadsheet for accuracy and completeness before uploading to avoid errors in user creation or updates.
>
> This documentation should help streamline the process of adding or updating users in the NexPort Campus system, ensuring that all necessary information is accurately captured and processed.

#### © NexPort Solutions 2022. All Rights Reserved.
