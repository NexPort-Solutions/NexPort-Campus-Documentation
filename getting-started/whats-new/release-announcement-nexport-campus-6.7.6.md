---
cover: ../../.gitbook/assets/what's new.avif
coverY: 0
---

# Release Announcement: NexPort Campus 6.7.6

{% hint style="info" %}
v6.7.6 Released 5/15/2024
{% endhint %}

We are excited to announce that NexPort Campus 6.7.6 has been successfully released to production! This release includes a variety of enhancements and bug fixes aimed at improving the overall user experience and system functionality. Here are the key updates in this release:

**Enhancements**

1. **Case 181218: Certificate Development**
   * Certificate developers can now see a list of available VTL properties that can be used in the PDF certificate templates, enhancing flexibility and ease of use.
2.  **Case 180937: Syllabus VTL Template Properties**

    * Added missing properties to the syllabus VTL template, providing more options and control to users.

    The following properties are now available for both PDF and HTML templates. These are also available to assignment descriptions and assignment titles.\


    `$enrollment.Syllabus.SectionCeus`: The ceus for the syllabus. Null for training plans.

    `$enrollment.Syllabus.SectionDuration`: The duration of the syllabus. Null for training plans.

    `$enrollment.Syllabus.SectionMasteryScore`: The mastery score for the syllabus. Null for training plans.

    `$enrollment.Syllabus.SectionNumber`: Section number for the syllabus. Null for training plans.

    `$enrollment.Syllabus.SectionObjectives` The objectives for the syllabus. Null for training plans.

**Bug Fixes**

1. **Case 181120: Template Properties Button**
   * Fixed the issue where the Template Properties button was broken on HTML certificates, ensuring smooth access to template settings.
2. **Case 180336: Not Graded Media Assignments**
   * Resolved the issue where not graded media assignments were being incorrectly set back to "In Progress" after completion. They will now stay set to completed, improving the accuracy of assignment statuses.

**Documentation Update**

1. **Case 180973: GitBook Documentation**
   * Expanded the "Customize Group Pages" section in the GitBook documentation to provide more comprehensive guidance for users.

We appreciate the efforts of our dedicated team in resolving these cases and continuously improving our platform. As always, we value your feedback and encourage you to share your experiences with us to help us make NexPort Campus even better.
