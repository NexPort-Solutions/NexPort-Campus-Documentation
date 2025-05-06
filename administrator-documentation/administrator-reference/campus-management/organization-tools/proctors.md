# Proctors

## Setting Up Proctoring in NexPort Campus

This guide explains how to enable proctoring for assignments in NexPort Campus, add proctors to your organization, and manage student access using access codes. These steps are intended for administrators and proctors responsible for secure exam delivery.

### Overview

Proctoring in NexPort Campus provides an added layer of security for assessments by requiring students to enter a unique access code before beginning a proctored assignment. These access codes are created and managed by users with the "Proctor" role. Assignments can be flagged as proctored during creation or editing, ensuring only authorized students can begin them.

Key features of the proctoring system include:

* Role-based access control for managing proctor privileges
* Custom access codes tied to individual students
* Real-time monitoring of code usage
* Compatibility with high-stakes and regulated assessment workflows

This guide includes detailed steps and **UI screenshots** to help you:

* Add a proctor to your organization
* Configure an assignment for proctoring
* Create and assign access codes
* Monitor and troubleshoot access issues

<figure><img src="../../../../.gitbook/assets/Desktop Screenshot 2025.05.06 - 15.45.37.10.png" alt=""><figcaption></figcaption></figure>

***

### Assign a Proctor to Your Organization

Before a user can manage or oversee proctored assignments, they must be added as a **proctor**.

#### To assign a proctor:

1. Navigate to **Manage Campus > Organization > Organization Tools > Proctors**.
2. Click the **Add Proctors** tab.
3. In the search bar, enter the name of the user you want to designate as a proctor.
4. In the results list, click the **Add** button next to the user's name.

<figure><img src="../../../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Add Proctors Menu</p></figcaption></figure>

The selected user now has access to proctoring tools, including access code creation and assignment tracking.

***

### Enable Proctoring for an Assignment

To restrict an assignment so that students can only access it through a proctor, you must enable the **Proctored** setting.

#### When creating a new assignment:

1. Navigate to **Manage Campus > Sections > Assignments**.
2. Click **Create New Assignment**.
3. Fill in the assignment name, type, and other required fields.
4. In the **Proctored Assignments** section, check the **Proctored** box.
5. Click **Save** to finish.

#### To update an existing assignment:

1. Navigate to **Manage Campus > Sections > Assignments**.
2. Locate the assignment and click **Edit**.
3. In the **Proctored Assignments** section, check the **Proctored** box.
4. Click **Save**.

<figure><img src="../../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

> **Note:** Once proctoring is enabled, students must enter an active access code before they can open the assignment.

***

### Manage Access Codes

Proctors use access codes to control when students are allowed to begin their assignments. Codes are created and assigned through the **Proctors** tab.

#### To create a new access code:

1. Log in as an Administrator or Proctor.
2. In the main navigation menu, select the **Proctors** tab.
3. The **Access Codes** page will open and show a list of currently active codes.
4. Click **Create Code** to add a new one.

> **Note:** Proctors will not be able to create access codes unless they have been granted the appropriate permissions in the **Proctors** tab under **Organization Tools**.

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Proctors tab on Main Menu</p></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Proctors Organization Tool</p></figcaption></figure>

The access code appears in the list and is ready to assign.

#### To assign a code to a student:

1. Navigate to **Manage Campus > Organization > Organization Tools > Proctors > Access Codes**.
2. In the list of access codes, click the **Edit** icon (pencil) next to the code you want to assign.
3. In the **Access Code Assignment** menu that appears, select the student from the dropdown.
4. Click **Save**.

> **Tip:** Each access code can only be assigned to one student.
>
>

<figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Assign Access Code to student</p></figcaption></figure>

***

### What Students Experience During Proctoring

When a student opens a proctored assignment:

* They are prompted to enter their access code.
* If the code is valid and assigned to them, the assignment unlocks.
* If the code is invalid or expired, they receive an error and cannot proceed.

All access code usage is tracked automatically.

<figure><img src="../../../../.gitbook/assets/image (7).png" alt=""><figcaption><p>Proctor Access Code Prompt</p></figcaption></figure>

***

### View Access Code Usage

Proctors and administrators can monitor how and when each access code is used.

#### To check usage:

1. Go to the **Access Codes** tab in the **Proctors** section.
2. Find a used code and click on it.
3. A details panel appears showing:
   * The student assigned
   * Timestamp of use
   * Status of the access

<figure><img src="../../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

***

### Troubleshooting

| Problem                        | What to Check                                                                 |
| ------------------------------ | ----------------------------------------------------------------------------- |
| Student can’t access test      | Ensure the access code is assigned and not expired.                           |
| Access code is missing         | Verify that the code was created and saved under **Proctors > Access Codes**. |
| Assignment doesn’t prompt code | Confirm the **Proctored** checkbox is enabled in the assignment settings.     |

***

### Need Help?

* Email: tier2@nexportengineering.com
* Documentation Portal: [docs.nexportsolutions.com](https://docs.nexportsolutions.com)
