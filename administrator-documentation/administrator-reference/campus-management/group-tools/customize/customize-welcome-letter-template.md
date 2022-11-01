---
description: You can create a custom login message to communicate with the students.
cover: ../../../../../.gitbook/assets/Untitled-1-01.png
coverY: 0
---

# Customize Welcome Letter Template

You can create a welcome letter to be sent to new subscribers. The body of the welcome letter allows the use of the [**Velocity Template Language (VTL)**](http://velocity.apache.org/engine/1.6/user-guide.html).

## **To customize the welcome letter**

<mark style="color:blue;">**Step 1:**</mark>  Click <mark style="color:blue;">**Administration**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">></mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Manage Campus**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">></mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Group Tools**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">></mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Customize**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">></mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Welcome Letter**</mark>.

![](/.gitbook/assets/Welcome_Letter_550x239.png)

<mark style="color:blue;">**Step 2:**</mark>  In the <mark style="color:blue;">**Subject Template**</mark> box, type the subject for the welcome letter.

<mark style="color:blue;">**Step 3:**</mark>  In the <mark style="color:blue;">**Body Template box**</mark>, type a welcome message.

<mark style="color:blue;">**Step 4:**</mark>  The Rich Text Editor allows to format the text, upload images, create table, add hyperlinks, insert code snippet, and other Rich Text Editor features.

<mark style="color:blue;">**Step 5:**</mark>  In the <mark style="color:blue;">**Custom Email**</mark> <mark style="color:blue;"></mark><mark style="color:blue;">‘</mark><mark style="color:blue;">**From**</mark><mark style="color:blue;">’</mark> <mark style="color:blue;"></mark><mark style="color:blue;">**Address**</mark> box, type the email address.

<mark style="color:blue;">**Step 6:**</mark>  Click <mark style="color:blue;">**Save**</mark>. The welcome letter template details are updated and saved.

#### The following is the list of available VTL properties that are used in the welcome letter.

| Properties    | Description                                     |
| ------------- | ----------------------------------------------- |
| `$Login`      | The login name of the user.                     |
| `$Password`   | The password of the user.                       |
| `$Email`      | The email address of the user.                  |
| `$FirstName`  | The first name of the user.                     |
| `$MiddleName` | The middle name of the user.                    |
| `$LastName`   | The last name of the user.                      |
| `$Nickname`   | The nick name of the user.                      |
| `$Title`      | The title of the user. For example, Mr or Ms.   |
| `$Culture`    | The culture of the user. For example, en or es. |

#### The following is the list of available [Velocity Template Language (VTL)](http://velocity.apache.org/engine/1.6/user-guide.html) properties for contact information.

| Properties  | Description               |
| ----------- | ------------------------- |
| `$City`     | The city of the user.     |
| `$State`    | The state of the user.    |
| `$Country`  | The country of the user.  |
| `$Postal`   | The zip code of the user. |
| `$Address1` | The address of the user.  |
| `$Address2` | The address of the user.  |
| `$Phone`    | The phone of the user.    |
| `$Fax`      | The fax of the user.      |

#### The following is the list of available VTL properties for subscription information.

| Properties               | Description                                                                               |
| ------------------------ | ----------------------------------------------------------------------------------------- |
| `$Provider`              | The full name of the provider.                                                            |
| `$OrganizationName`      | The full name of the organization.                                                        |
| `$OrganizationShortName` | The short name for the organization.                                                      |
| `$Memberships`           | The list of memberships from the spreadsheet.                                             |
| `$ExpirationDate`        | The date that this user's subscription expires, displays as "never" if it doesn't expire. |
| `$BillingCode`           | The billing code for the subscription.                                                    |
| `$LoginUrl`              | The login url for the organization.                                                       |

#### The following is the list of available VTL properties for miscellaneous.

| Properties | Description                                                    |
| ---------- | -------------------------------------------------------------- |
| `$Notes`   | The notes provided in the spreadsheet.                         |
| `$Cc`      | The list of emails that the letter are carbon copied to.       |
| `$Bcc`     | The list of emails that the letter are blind carbon copied to. |

#### © NexPort Solutions 2022. All Rights Reserved.
