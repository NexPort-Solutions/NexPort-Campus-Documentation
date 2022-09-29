---
description: >-
  NexPort Campus 6.6.7 is part of our series of regular point releases. This
  version addresses serval bugs and adds a few minor enhancements.
coverY: 0
---

# NexPort Campus v6.6.7 Release Notes

## New Features

### Admins need to be able to validate student identity at the beginning and end of a section (154943)&#x20;

NexPort now has a new assignment type; Student Verification Assignment. This assignment type will allow admins and instructors to require a student to correctly answer a question about their profile.&#x20;

## Enhancements

### Add CreateSubscription API Method (155785) Recalculate Training Plan Enrollment (155534)&#x20;

Subscriptions can now be directly created using the web api.

### System ID for Users should be available to all administrators that can view a user (155179)&#x20;

### Update the Login to NRS link in NexPort (154644)&#x20;

## Bug Fixes

### 504 error thrown while navigating through beta campus (155149)&#x20;

### Nexport Campus My Events initial view page is not loading completely until forced Refresh (155460)&#x20;

### Word 'Test' is displayed in TP Detail Card (155988)&#x20;

### When trying to save Student Verification Assignment error is thrown (156146)&#x20;

### The impersonate courseware assignment option should obey the permissions of the enrollment group (154249)&#x20;

The impersonate student option for courseware assignments was using the group/org the section belonged to to calculate permissions. This meant many instructors and administrators were unable to access the feature if the section was shared from elsewhere. It now obeys the permissions of the org the enrollment belongs to.

### Administrators must select an owner org to add a user even if an owner org is displayed in the form (154211)&#x20;

### Object reference not set to an instance of an object error when selecting Enrollments > Training Plan button (154659)&#x20;

### Accessing training plan in Enrollments tab is throwing a null reference exception (154517)&#x20;

### Errors found in beta error logs. Need to Add Validation for UserId and OrgId in AdminApiController (153757)&#x20;

### Recalculating training plan enrollment is throwing an error for a Not Started training plan enrollment (153985)&#x20;

### Duplicate orgs displayed in owner org dialog (154212)&#x20;

### Group Shared Bookshelves ONLY allow the owner of the bookshelf to share them (154463)&#x20;

### GPA's do not update on enrollments when the GPA scale is updated (153959)&#x20;

### A message is not sent to the NexPort Inbox when someone uses the Login As feature with your account. (154496)&#x20;

### Discussion Assignment Replies do not always order properly (154134)&#x20;

### Timeout Error when trying to remove/delete an assignment with MANY assignment statuses (152077)&#x20;

### Event validation should ignore meeting room overlaps since meeting rooms are going away (154598)&#x20;

### ExpirationDate in Welcome Letter Should Support Extensions for Date Formats (154196)
