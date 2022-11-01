---
cover: ../../.gitbook/assets/Untitled-1-01.png
coverY: 0
---

# Choose a Learning Distribution Model

NexPort Campus allows you to distribute your instructional content using one of 4 distribution models; Point of Sale Model, Organizational Model, Ticketing Model, and Mixed Model steps to add course catalog, invoice, and ticketing batch. After creating learning resources, you need to connect with the students.

## What is the Point of Sale model? <a href="#what" id="what"></a>

In this model, the access to the learning assets that includes catalogs, training plans, and sections, are provided through invoices. The individual catalogs, training plans, and sections are directly sold to customers. They obtain access to these learning resources after the user redeems redemption codes that are produced by NexPort invoices.

![](/.gitbook/assets/POS_Invoicing_Model.png)

## How to create an invoice? <a href="#how" id="how"></a>

NexPort allows you to distribute sections and training plans directly to students by creating an invoice. After an invoice is executed in NexPort an administrator can share the invoice redemption codes with students to allow them access to the training. Invoicing can also be created using the Invoicing API.

1. Click **Administration** > **View Invoices**.
2. The **Invoices** page, containing the list of invoices, is displayed.
3. Click the **Create New Invoice** link.
4. Type information in the various tabs in the wizard that opens: Select User, Select Organization, Select Items, Review Items, and Add Payments.
5. On the **Finish** tab, review the purchase details.
6. Click **Finish**.
7. Note:
8. The invoice that is generated and issued is displayed in the customer’s member area on the **My Purchases** tab.

#### For more information about creating an invoice.

{% content-ref url="../administrator-reference/invoice-management/" %}
[invoice-management](../administrator-reference/invoice-management/)
{% endcontent-ref %}

## What is the Organizational model? <a href="#what2" id="what2"></a>

This is the most common model used by customers. In this model, the student is subscribed to an organization or university. Within that organization, they may be assigned membership to various groups. Learning resources or assets that include catalogs, sections, and training plans, are shared with different groups. Students who subscribe to an organization can view the courses available to them, based on the membership they have, when they log on. To illustrate, if a student is a member of three different groups, and each group has four different catalogs, the student would have access to 12 different catalogs containing SCORM compliant courseware.

In essence, the Organizational Model is based on group membership.

![](/.gitbook/assets/Organizational_model.png)

## What is the Ticketing Model? <a href="#what3" id="what3"></a>

In NexPort you can create batches of tickets to be distributed to students. These tickets, when redeemed by a student, can give students access to organizations and membership into groups. The ticketing model essentially uses the Organizational model for controlling access. Access to content is still controlled through memberships. All membership rules for tickets are stored in the ticket batch. So, all tickets in a batch have the same rules. Ticket batches can contain as many number of tickets and your organization can create as many number of ticket batches.

![](/.gitbook/assets/POS_Ticketing_Model.png)

## How to add ticket batches? <a href="#how2" id="how2"></a>

A ticket can be used to grant users access to various groups in your organization. When redeemed, a ticket creates subscriptions and memberships for the redeeming user in accordance with the rules defined on the ticket batch it belongs to. A redeem link is sent to the users to redeem a ticket or an entire spreadsheet of tickets is sent through an external purchasing agent to distribute at a later date. In this way ticketing offers a very flexible way to distribute content to your students.

![](/.gitbook/assets/Add_TicketBatch_535x404.png)

1. Click **Administration** > **Manage Campus** > **Organization Tools** > **Ticketing**.
2. The **Ticketing** page is displayed.
3. Click Add and type the details such as the batch name, order number, customer, number of tickets, date of activation of the tickets, validity period of the subscription as required.
4. Click **Create**.
5. The ticketing batch is created.

For more information about adding a ticketing batch, see [Ticketing](/administrator-documentation/administrator-reference/Campus_Management/Organization_Tools/Ticketing/Ticketing.htm).

## How to apply membership settings? <a href="#how3" id="how3"></a>

You must apply **Force Membership** or **Selectable Membership** settings for students to redeem the tickets in a batch. The Force Membership automatically gives the redeeming user a membership in the selected groups. The Selectable Membership option displays a list of groups that the user can self-join.

1. Click the **Membership Settings** tab.
2. On the **Membership Settings** page, do one of the following:
3.
   * In the **Force Memberships** area, select the check box next to the group to which you need to assign the forced membership. The selected group is displayed in the **Selected Groups** column.
   * or
   * In the **Selectable Memberships** area, select the check box next to the group to which you provide the ability to choose membership. The selected group is displayed in the **Selected Groups** column.
4. The membership settings are applied to the ticketing batch.

## What is the Mixed Model? <a href="#what4" id="what4"></a>

NexPort Campus does not impose any restrictions on how these models are applied. Campus Administrators are free to organize their campus in any way by using any mix of invoices, tickets, and memberships.

#### &#x20;© NexPort Solutions 2022. All Rights Reserved.
