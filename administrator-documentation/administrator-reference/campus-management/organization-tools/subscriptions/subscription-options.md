---
description: >-
  Describes the functionality of the Subscription Options tab under the
  Subscriptions menu.
---

# Subscription Options

This section is located under the Subscription menu and furthest tab to the right.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2024-04-17 at 9.07.30 AM.png" alt=""><figcaption><p>Subscription Options location</p></figcaption></figure>

The purpose of the Subscription Options area is to allow an organization administrator to set specific statuses to students inside specific subscriptions.

***

## <mark style="color:blue;">Creating a Subscription Status</mark>

<mark style="color:blue;">**Step 1:**</mark> Click the Add New button at the bottom of the page.

<mark style="color:blue;">**Step 2:**</mark> In the opened dialog box enter the label for the status (example: Active, Pending, etc.)

<figure><img src="../../../../../.gitbook/assets/Screenshot 2024-04-18 at 7.59.59 AM.png" alt=""><figcaption><p>Highlighted ADD NEW button with the corresponding dialog box to create a status.</p></figcaption></figure>

<mark style="color:blue;">**Step 3:**</mark> Next set the initial state of the new status. If the state will not be used immediately you can leave the state as 'no change'.

<mark style="color:blue;">**Step 4:**</mark> If you are satisfied with your selections then click the green checkmark to create the status.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2024-04-18 at 8.17.04 AM.png" alt=""><figcaption><p>Subscription Options tab with a status.</p></figcaption></figure>

***

## <mark style="color:blue;">Setting the Default Status</mark>

At the bottom of the Subscription Options page is the setting for the Default Status. The Default Status will be applied to every new subscription.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2024-04-18 at 9.27.57 AM.png" alt=""><figcaption></figcaption></figure>

Click on the drop-down menu to view the available statuses. A status must be enabled to appear in this list. If the desired status does not appear in the list, then locate the value in the Subscription Workflow Editor above and change the Active value to Enabled.

***

## <mark style="color:blue;">Configuring the Status Changes</mark>

Automatic status changes can be configured for each Status listed in the Subscription Workflow Editor by clicking on the Details icon <img src="../../../../../.gitbook/assets/image (57).png" alt="" data-size="line"> on the right side of the Status row.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2024-04-19 at 2.02.02 PM.png" alt=""><figcaption><p>The Edit Status Changes dialog box</p></figcaption></figure>

When the Edit Status Changes dialog box appears, any existing status changes will appear here. Click the Add New button to create a new status change event.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2024-04-19 at 2.03.09 PM.png" alt=""><figcaption><p>The Edit Status Changes dialog box show a list of change events.</p></figcaption></figure>

When adding a new status change the administrator can choose from the following trigger types:

> <mark style="color:blue;">**First Enrollment Activity**</mark>: fires the first time any linked enrollment records activity (launching a course, submitting an assignment, etc.).
>
> <mark style="color:blue;">**All Enrollments Passed**</mark>: fires after every enrollment tied to the subscription has reached a passed/completed state.
>
> <mark style="color:blue;">**Inactivity Threshold Reached**</mark>: fires when a learner has gone the specified number of days without any assignment activity. Use this to move long–inactive students into statuses such as “Active‑NP” automatically.

Selecting **Inactivity Threshold Reached** reveals an additional **Threshold (days)** field. Enter the number of inactive days that should elapse before the status transition occurs. The scheduler examines assignment activity nightly (or on the cadence configured by your administrator) and transitions any subscriptions whose current status matches the trigger’s **From** status and exceed the threshold. If a learner returns and records new assignment activity, the built-in **Assignment Activity Recorded** trigger can return them to an “Active” status.

Next select whether you want the Status Change to begin Enabled or disabled. ( this can be changed at any time by coming back to the Status Changes dialog box )

Finally select the status that will show when the trigger condition is activated.

<figure><img src="../../../../../.gitbook/assets/Screenshot 2024-04-19 at 2.03.26 PM.png" alt=""><figcaption></figcaption></figure>

Click the Green Checkmark to save thee Status Change and click Close to leave the Status Changes window.

***

### <mark style="color:blue;">Automation Tips</mark>

- The inactivity scheduler is resilient: missed runs are caught up during the next execution, and running it multiple times per day will not duplicate transitions.
- Manual overrides are respected. If you move a subscription into a different status manually, automation will only act again when the subscription returns to a status that has an active trigger.
- Review the **Status History** panel after enabling new automation to confirm transitions are occurring as expected.
