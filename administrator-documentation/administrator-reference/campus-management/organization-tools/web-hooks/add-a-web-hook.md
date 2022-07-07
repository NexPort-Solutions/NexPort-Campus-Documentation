---
description: You can add a new web hook to connect a new or additional external system.
---

# Add a Web Hook

## **To add a web hook**

Step 1:  Click **Administration** > **Manage Campus** > **Organization Tools** > **Web Hooks**.

> The **Web Hooks** page is displayed.

![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/OT\_Web\_Hooks/WebHooks\_Add\_550x97.png)

Step 2:  Click **Add**.

> The **Manage Web hook Interface** dialog box is displayed.

![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/OT\_Web\_Hooks/ManageWebHookInterface.png)

Step 3:  In the **Name** box, type the name of the web hook.

> The name is displayed on the **Web Hooks** page.

Step 4:  In the **Url** box, type the http:// or https:// URL where the web hook body (refer to Step 8) should be sent when this web hook is executed.

> This is a mandatory field.

Step 5:  In the **Event Type** list, enter the event type for which the notification is triggered such as **Complete Enrollment**, **Enrollment Created, Subscription Created**, **Subscription Status Changed**, **Subscription Updated**, and **Assignment Complete**.

> When the event occurs within this organization, the web hook is executed.

Step 6:  In the **Verb** list, enter the HTTP methods such as **Get**, **Post**, **Update**, and **Delete**.

Step 7:  In the **Query String**, click **Manage QueryString**, and then enter the query string that the remote server requires.

{% hint style="info" %}
The **Manage QueryString** button is disabled, when you are creating a web hook for the first time. The **Manage QueryString** button is enabled, after you create a web hook and try to edit it later.
{% endhint %}

Step 8:  In the **Body** box, type the XML, JSON, and other formats that HTTPS request allows.

> The body can be built by using the [Velocity Template Language (VTL)](http://velocity.apache.org/engine/1.6/user-guide.html) properties. Click the ![](https://www.nexportcampus.com/Content/Guides/aweb/Content/Resources/Images/Common\_Screens\_Icons/Help.png) icon to access the available VTL properties.

{% hint style="info" %}
The **Body** box is disabled if you enter **Get** and is enabled when you enter **Post**, **Update**, and **Delete** in the Verb list.  The body content must match the **Content Type**.
{% endhint %}

Step 9:  In the **Content Type** box, type the content of the body text.

Step 10:  Click **Save**.

> The new web hook is saved.

#### © NexPort Solutions 2022. All Rights Reserved.
