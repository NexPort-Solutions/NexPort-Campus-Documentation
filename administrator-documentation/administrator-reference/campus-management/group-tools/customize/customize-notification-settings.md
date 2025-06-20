# Customize Notification Settings

## Intended Audience

* Campus Administrators
* Instructors with Org/Group Management Permissions

***

## Overview

### Notification Scope and Inheritance

NexPort Campus supports a flexible notification system where settings can be applied at both the **organization** and **group** levels.

* **Organization-level settings** act as defaults for all nested groups.
* **Group-level settings** may inherit these defaults or explicitly override them.
* When overridden, templates are not affected by changes at the organization level unless reset.
* The **Reset** button reverts a template to its inherited configuration.

This guide outlines how to configure notification settings via the **Notification Settings** tab in **Group Tools > Customize**.

***

## Prerequisites

* Administrative or instructor access to a group or organization
* Group must be active (not archived)
* Users must have valid email addresses and notification preferences enabled

***

## Step-by-Step Instructions

### Step 1: Navigate to Group Tools > Customize

* Log into [NexPort Campus](https://nexportsolutions.com/login).
* Navigate to: `Organizations > [Your Org] > Groups > [Your Group]`
* Expand **Group Tools** and select **Customize**.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-05-16 125304 (1).png" alt=""><figcaption></figcaption></figure>

### Step 2: Open the Notification Settings Tab

Select the **Notification Settings** tab in the horizontal menu.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-05-16 125231 (1).png" alt=""><figcaption></figcaption></figure>

### Step 3: Choose a Notification Template to Edit

* Click the dropdown labeled `All emails sent`.
* Select the event you wish to customize.
* The default subject and body will populate in the editor.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-05-16 125200.png" alt=""><figcaption></figcaption></figure>

### Step 4: Click the Override Button

Click the **Override** button to enable group/org-specific editing of the message template. Note: If the message template is empty, no notification will be delivered.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-05-16 125123.png" alt=""><figcaption></figcaption></figure>

### Step 5: Customize the Message

* Edit the **Subject** with variables like `$message.Subject`.
* Update the **Body** with rich formatting, tokens, and conditions.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-05-16 125029.png" alt=""><figcaption></figcaption></figure>

### Step 6: Save or Reset

* Click **Save** to apply changes.
* Click **Reset** to revert to the default (inherited) message.

### Step 7: (Optional) Disable Notification

To suppress delivery for this notification, check **Disable Notifications**.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2025-05-16 124831.png" alt=""><figcaption></figcaption></figure>

***

### Notification Event Types

Below is a list of commonly used notification types and their purposes:

<table data-header-hidden><thead><tr><th></th><th></th><th></th><th width="95"></th></tr></thead><tbody><tr><td>Notification Event</td><td>Description</td><td>Recipient</td><td>Editable</td></tr><tr><td>Student submits writing assignment</td><td>Confirms submission of a writing assignment, letting the student know it was successfully received.</td><td>Student</td><td>Yes</td></tr><tr><td>Instructor requires writing resubmission</td><td>Informs the student that the submitted assignment requires revisions and must be resubmitted.</td><td>Student</td><td>Yes</td></tr><tr><td>Instructor provides feedback</td><td>Alerts the student that instructor feedback is available for a submitted assignment.</td><td>Student</td><td>Yes</td></tr><tr><td>Instructor grades writing assignment</td><td>Notifies the student of the official grade along with any scoring criteria or comments.</td><td>Student</td><td>Yes</td></tr><tr><td>Student submits student input assignment</td><td>Acknowledges submission of an input-type assignment, such as a survey.</td><td>Student</td><td>Yes</td></tr><tr><td>Panelist is invited to a meeting</td><td>Sends an invitation with event details to a panelist, typically for live review sessions.</td><td>Panelist</td><td>Yes</td></tr><tr><td>Welcome letter sent to new subscribers</td><td>Sends a welcome email with account info, orientation resources, and how to get started. This is sent when a student is initially subscribed or in specific cases with uploading user spreadsheets.</td><td>Student</td><td>Yes</td></tr><tr><td>Student receives certificate</td><td>Notifies the student that they have successfully completed training and can access their certificate.</td><td>Student</td><td>Yes</td></tr><tr><td>Message to users when confirming email</td><td>Verifies a user's email address during initial registration or profile updates.</td><td>User</td><td>Yes</td></tr></tbody></table>

## Troubleshooting

| Problem                         | Cause                               | Solution                                |
| ------------------------------- | ----------------------------------- | --------------------------------------- |
| Notification not received       | User email disabled or invalid      | Check profile settings and verify email |
| Custom message not appearing    | Override not applied                | Click 'Override' and save changes       |
| Changes not reflected in emails | Still using inherited template      | Ensure override is enabled              |
| Emails go to spam               | Spam filter trigger or domain issue | Check formatting and verify domain      |
| Reset doesn’t work              | Caching delay                       | Refresh or reselect template            |

***

## Related Resources

* [Understanding Permissions in NexPort Campus](https://docs.nexportsolutions.com/nexport-user-documentation/administrator-documentation/administrator-reference/campus-management/group-tools/permissions/understanding-permissions-in-nexport-campus)
* [Administrator Quick Start Guide](https://docs.nexportsolutions.com/nexport-user-documentation/administrator-documentation/administrator-quick-start/)
* Message Template Variables Guide (coming soon)
