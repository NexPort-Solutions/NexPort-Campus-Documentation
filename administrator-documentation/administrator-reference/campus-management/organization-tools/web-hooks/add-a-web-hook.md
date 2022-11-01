---
description: You can add a new web hook to connect a new or additional external system.
---

# Add a Web Hook

## **To add a web hook**

<mark style="color:blue;">**Step 1:**</mark> Click <mark style="color:blue;">**Administration**</mark> > <mark style="color:blue;">**Manage Campus**</mark> > <mark style="color:blue;">**Organization Tools**</mark> > <mark style="color:blue;">**Web Hooks**</mark>.

> The <mark style="color:blue;">**Web Hooks**</mark> page is displayed.

![](/.gitbook/assets/WebHooks_Add_550x97.png)

<mark style="color:blue;">**Step 2:**</mark>  Click <mark style="color:blue;">**Add**</mark><mark style="color:blue;">.</mark>

> The <mark style="color:blue;">**Manage Web hook Interface**</mark> dialog box is displayed.

![](/.gitbook/assets/ManageWebHookInterface.png)

<mark style="color:blue;">**Step 3:**</mark>  In the <mark style="color:blue;">**Name**</mark> box, type the name of the web hook.

> The name is displayed on the <mark style="color:blue;">**Web Hooks**</mark> page.

<mark style="color:blue;">**Step 4:**</mark>  In the <mark style="color:blue;">**Url**</mark> box, type the http:// or https:// URL where the web hook body (refer to Step 8) should be sent when this web hook is executed.

> _<mark style="color:red;background-color:yellow;">This is a mandatory field.</mark>_

<mark style="color:blue;">**Step 5:**</mark>  In the <mark style="color:blue;">**Event Type**</mark> list, enter the event type for which the notification is triggered such as <mark style="color:blue;">**Complete Enrollment**</mark>, <mark style="color:blue;">**Enrollment Created**</mark>**, **<mark style="color:blue;">**Subscription Created**</mark>, <mark style="color:blue;">**Subscription Status Changed**</mark>, <mark style="color:blue;">**Subscription Updated**</mark>, and <mark style="color:blue;">**Assignment Complete**</mark>.

> When the event occurs within this organization, the web hook is executed.

<mark style="color:blue;">**Step 6:**</mark>  In the <mark style="color:blue;">**Verb**</mark> list, enter the HTTP methods such as <mark style="color:blue;">**Get**</mark>, <mark style="color:blue;">**Post**</mark>, <mark style="color:blue;">**Update**</mark>, and <mark style="color:blue;">**Delete**</mark>.

<mark style="color:blue;">**Step 7:**</mark>  In the <mark style="color:blue;">**Query String**</mark>, click <mark style="color:blue;">**Manage QueryString**</mark>, and then enter the query string that the remote server requires.

{% hint style="info" %}
The <mark style="color:blue;">**Manage QueryString**</mark> button is disabled, when you are creating a web hook for the first time. The <mark style="color:blue;">**Manage QueryString**</mark> button is enabled, after you create a web hook and try to edit it later.
{% endhint %}

<mark style="color:blue;">**Step 8:**</mark>  In the <mark style="color:blue;">**Body**</mark> box, type the XML, JSON, and other formats that HTTPS request allows.

> The body can be built by using the [Velocity Template Language (VTL)](http://velocity.apache.org/engine/1.6/user-guide.html) properties. Click the ![](/.gitbook/assets/Help.png) icon to access the available VTL properties.

{% hint style="info" %}
The <mark style="color:blue;">**Body**</mark> box is disabled if you enter <mark style="color:blue;">**Get**</mark> and is enabled when you enter <mark style="color:blue;">**Post**</mark>, <mark style="color:blue;">**Update**</mark>, and <mark style="color:blue;">**Delete**</mark> in the Verb list.  The body content must match the <mark style="color:blue;">**Content Type**</mark>.
{% endhint %}

<mark style="color:blue;">**Step 9:**</mark>  In the <mark style="color:blue;">**Content Type**</mark> box, type the content of the body text.

<mark style="color:blue;">**Step 10:**</mark> Click <mark style="color:blue;">**Save**</mark>.

> The new web hook is saved.

#### © NexPort Solutions 2022. All Rights Reserved.
