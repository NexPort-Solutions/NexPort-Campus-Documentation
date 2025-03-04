---
description: >-
  You can view an existing list of courseware currently owned and uploaded by
  your organization.
---

# View and Manage Owned Courseware

It displays the title of the courseware with manifest identification number, CPlayer Version, file size, and types of courseware. You can also download the SCORM compliant courseware package.

{% hint style="info" %}
The manifest identification number is extracted from the manifest stored in the SCORM package that is uploaded. The ID must be unique within the organization. If a courseware package with the same ID is uploaded, then it overwrites the existing courseware within your organization.
{% endhint %}

## **To view and manage the owned courseware**

<mark style="color:blue;">**Step 1:**</mark> Click <mark style="color:blue;">**Administration**</mark> <mark style="color:blue;">></mark> <mark style="color:blue;">**Manage Campus**</mark> <mark style="color:blue;">></mark> <mark style="color:blue;">**Organization Tools**</mark> <mark style="color:blue;">></mark> <mark style="color:blue;">**Courseware**</mark><mark style="color:blue;">.</mark>

<mark style="color:blue;">**Step 2:**</mark> The <mark style="color:blue;">**Owned**</mark> tab is displayed. You can view the list of all owned courseware.

{% hint style="info" %}
In the <mark style="color:blue;">**Option**</mark> column, click the download link to download the original SCORM package.
{% endhint %}

![](../../../../../.gitbook/assets/OrganizationManagement_Courseware.png)

#### Title

This is the title of the course, pulled from the course manifest file.

#### Manifest Id

This is the unique identifier pulled from the course manifest file. When uploading a course,  the system will replace any existing course on the Owned tab with the same manifest id as the newly uploaded one.

#### Uploaded

This is the date the course was uploaded.

#### Schema

This is the schema for the course. Currently, this will either show up as SCORM12 or SCORM2004.

#### Player Version

This is the version of the courseware player currently installed with the course, specifically with courses made using NexPort Studio.

#### Upload Status

Keep track of the status of the courseare upload. The states are Uploaded, Unpackaging, Installing, Installed, and Failed. &#x20;

#### Report Commit Log

Use the report commit log option to enable commit logging for this courseware. This feature can be enabled for debugging purposes. It may add additional overhead to commits so enabling it should be done sparingly. The commit logs can be seen through the [student record](../../../user-management/manage-enrollments/section-enrollment/manage-scorm-assignment-sessions.md).

#### Disable Exit Notice

By default the course launcher will add a notice to the end of a course when LMSFinish is called. This notice can be disabled for courses that wish to use a custom notice.

#### Use Async Api

Use the async api option to allow courses to use asynchronous SCORM api calls. This is especially important for review mode when using SCORM 2004 courses made using Articulate or other authoring tools that expect API calls to be asynchronous. This setting is currently ignored for SCORM 1.2 courses.

#### © NexPort Solutions 2022. All Rights Reserved.
