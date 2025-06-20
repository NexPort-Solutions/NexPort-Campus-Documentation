---
description: A Smarter, Smoother Learning Experience — UX Upgrades and More
---

# NexPort Campus 6.7.8.1 Release Announcement

We are excited to unveil NexPort Campus 6.7.8.1, a release that brings critical enhancements and refinements to your online education environment. This update focuses on improving user experience while addressing several important bugs and behaviors that elevate the platform’s overall performance and reliability.

### Highlights of the 6.7.8.1 Release

#### Workflow Enhancements

* **Ticket Workflow Enhancements**: The ticket redemption process has been overhauled to provide a smoother, more informative user experience. Administrators can now customize the screen content shown to users during redemption and receive email notifications each time a ticket is redeemed. A new option allows displaying tailored instructions directly on the redemption interface, reducing confusion and streamlining self-registration ([Case 207643](https://darwin-global.fogbugz.com/f/cases/207643/)).
* **Welcome Letter Triggers for New Subscriptions**: Welcome emails are now automatically sent when users subscribe, creating a smoother onboarding experience ([Case 208055](https://darwin-global.fogbugz.com/f/cases/208055/)). Previously, welcome letters were only sent to users added through spreadsheet upload. This feature is now configurable for all new subscribers via the Notifications tab, providing better control and visibility over communications.
* **Documentation Improvements**: End-user guidance has been updated to reflect new features and clarify workflows ([Case 208180](https://darwin-global.fogbugz.com/f/cases/208180/)). This includes step-by-step documentation for automated welcome communications.
* **Ticket Redemption Login Fix**: Fixed an issue where users were not logged in after redeeming a ticket, resulting in a misleading error message. Now, successful redemptions ensure the user is authenticated and granted access ([Case 207712](https://darwin-global.fogbugz.com/f/cases/207712/)).

#### API and Integration Enhancements

* **Invoice Redemption API Improvements**: Enhanced the `RedeemInvoiceItem` API to support rollback on failure, similar to `UpdateInvoiceItem`, preventing partial transactions and improving system stability ([Case 206625](https://darwin-global.fogbugz.com/f/cases/206625/)).
* **Invoice Redemption Stability**: Improved behavior for open-ended invoice redemptions where the syllabus context was not explicitly defined. Ensures correct assignment continuity across repeated redemptions ([Case 206782](https://darwin-global.fogbugz.com/f/cases/206782/)).
* **DropEnrollment Behavior Corrected**: Administrative API users can now drop enrollments even when the 'AllowDrop' option is disabled in the syllabus. This correction aligns API behavior with administrative permissions ([Case 206898](https://darwin-global.fogbugz.com/f/cases/206898/)).

#### SCORM 2004 Improvements

* **Improved SCORM Package Detection**: NexPort now recognizes a broader range of SCORM 2004 schema versions declared in `imsmanifest.xml`, including variations like "CAM 1.3" and "2004 2nd Edition." This enhancement increases compatibility with diverse SCORM content and improves clarity for administrators ([Case 207936](https://darwin-global.fogbugz.com/f/cases/207936/)).
* **SCORM Retake Setting Honored**: Fixed a bug where SCORM 2004 assignments ignored the `CanRetakePassedAttempt` setting. Learners who pass an assignment are now properly prompted with the option to retake it for a higher score, and each attempt is logged correctly as a separate SCORM session ([Case 207554](https://darwin-global.fogbugz.com/f/cases/207554/)).
* **SCORM Interaction Truncation Fix**: Addressed a failure where long interaction descriptions exceeded database limits, causing SCORM module crashes. These are now gracefully logged and prevented from disrupting progress ([Case 207990](https://darwin-global.fogbugz.com/f/cases/207990/)).

#### System Stability and Admin Tools

* **Certificate Notification Fix**: Restored missing help text in the certificate notification template, improving clarity and setup ease for administrators ([Case 208108](https://darwin-global.fogbugz.com/f/cases/208108/)).
* **Circular Prerequisite Protection**: Added validation to detect and block circular training plan prerequisites, ensuring stability in learning path design ([Case 199013](https://darwin-global.fogbugz.com/f/cases/199013/)).
* **Support Flow Optimization**: Improved the “Send Support Request” workflow to reduce accidental repeat submissions and lower support burden ([Case 206872](https://darwin-global.fogbugz.com/f/cases/206872/)).

### Why It Matters

These updates reflect NexPort’s continued commitment to delivering a secure, intuitive, and adaptable platform. Whether you're onboarding learners, tracking progress, or refining courseware, these enhancements create a more efficient experience for administrators, instructors, and learners.

### What’s Next

Looking ahead, we're focused on performance, automation, and expanding SCORM capabilities—including enhanced tracking and integration tools.

***

For more on how to use these new features or to explore updated documentation, visit [docs.nexportsolutions.com](https://docs.nexportsolutions.com/). As always, we welcome your feedback and look forward to supporting your success.

Stay tuned for the next leap forward in online learning.

**— The NexPort Solutions Team**

### Case Reference Index

* [Case 208055: New subscriptions should trigger a welcome letter](https://darwin-global.fogbugz.com/f/cases/208055/)
* [Case 208180: Write end user documentation for the welcome letter feature](https://darwin-global.fogbugz.com/f/cases/208180/)
* [Case 206625: Improve RedeemInvoiceItem API rollback behavior](https://darwin-global.fogbugz.com/f/cases/206625/)
* [Case 207936: Detect SCORM 2004 Packages using CAM 1.3 schema](https://darwin-global.fogbugz.com/f/cases/207936/)
* [Case 207554: SCORM 2004 assignments ignore CanRetakeAssignment setting](https://darwin-global.fogbugz.com/f/cases/207554/)
* [Case 207990: SCORM interaction description exceeds length and crashes](https://darwin-global.fogbugz.com/f/cases/207990/)
* [Case 208108: Certificate notification help field missing](https://darwin-global.fogbugz.com/f/cases/208108/)
* [Case 206782: Resolve syllabus context in invoice redemptions](https://darwin-global.fogbugz.com/f/cases/206782/)
* [Case 207712: Ticket redemption did not log in user](https://darwin-global.fogbugz.com/f/cases/207712/)
* [Case 206898: Allow DropEnrollment API override despite syllabus flag](https://darwin-global.fogbugz.com/f/cases/206898/)
* [Case 199013: Prevent circular training plan prerequisite chains](https://darwin-global.fogbugz.com/f/cases/199013/)
* [Case 206872: Reduce support case spam on feedback page](https://darwin-global.fogbugz.com/f/cases/206872/)
* [Case 207643: Show custom message during ticket redemption](https://darwin-global.fogbugz.com/f/cases/207643/)
