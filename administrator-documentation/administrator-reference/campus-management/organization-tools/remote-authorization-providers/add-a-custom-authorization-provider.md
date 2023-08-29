---
description: >-
  You can add an authorization provider to verify the users who are taking your
  training.
---

# Add a Custom Authorization Provider

## **To add a custom authorization provider**

<mark style="color:blue;">**Step 1:**</mark> Click <mark style="color:blue;">**Administration**</mark> > <mark style="color:blue;">**Manage Campus**</mark> > <mark style="color:blue;">**Organization Tools**</mark> > <mark style="color:blue;">**Remote Authorization Providers**</mark>.

> The <mark style="color:blue;">**Remote Authorization Providers**</mark> page is displayed.

![](../../../../../.gitbook/assets/RemoteAuthProviders.png)

<mark style="color:blue;">**Step 2:**</mark> Select Custom Authorization Provider from the dropdown and click <mark style="color:blue;">**New Provider**</mark><mark style="color:blue;">.</mark>

> The <mark style="color:blue;">**Create New Authorization Provider**</mark> form is displayed.

<figure><img src="../../../../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

<mark style="color:blue;">**Step 3:**</mark> In the <mark style="color:blue;">**Name**</mark> box, type the name of the authorization provider.

<mark style="color:blue;">**Step 4:**</mark> In the <mark style="color:blue;">**Authorization Endpoint Url**</mark> box, type the url of the endpoint your authorization will use.

<mark style="color:blue;">**Step 5:**</mark> In the <mark style="color:blue;">**Authorization TTL**</mark> box, type the number of seconds your authorization request will use for the time to live.

<mark style="color:blue;">**Step 6:**</mark> In the <mark style="color:blue;">**Trigger Type**</mark> dropdown, select what action should trigger your authorization request.

<mark style="color:blue;">**Step 7:**</mark> In the <mark style="color:blue;">**Trigger Body**</mark> box, type the data you would like to send in your authorization request. This must include $remoteAuthorization.SuccessUrl property.

<mark style="color:blue;">**Step 8:**</mark> In the <mark style="color:blue;">**Content Type**</mark> box, type the content type you would like to send in your authorization request.  Eg: application/json.

<mark style="color:blue;">**Step 9:**</mark> Click the <mark style="color:blue;">**Create**</mark> button. A green <mark style="color:blue;">**Saved**</mark> alert will appear. Click the <mark style="color:blue;">**Back**</mark> button to return to the provider listing.
