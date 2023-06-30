---
description: Recommendations for SCORM 1.2 developers creating content for NexPort Campus
---

# SCORM Best Practices

NexPort Campus allows content developers to import SCORM 1.2 packages and deliver them as assignments. Below we list a few best practices. Most of these recommendations are technical in nature. These instructions assume that the developer is familiar with the SCORM 1.2 Runtime Specification.

{% file src="../../.gitbook/assets/SCORM-12-RunTimeEnv.pdf" %}

## Set _cmi.core.lesson\_status_ Immediately

According to the SCORM specification, _cmi.core.lesson\_status_ will be set to _**completed**_ if a Sharable Content Object (SCO) finishes without setting the status on the first launch. NexPort Campus obeys this behavior. If a SCO fails to set the leson\_status during the initial attempt by a student and the student exits the SCO then NexPort Campus will set the status to completed.

If this is the desired behavior then the SCO should do nothing. If your SCO intends to set the _cmi.core.lesson\_status_ itself you should make sure it is set to "_incomplete_" immediately after the SCO call LmsInitialize().

## Setting cmi.core.lesson\_status to completed can not be reversed

If the lesson status is set to completed and LMSCommit is called the status can no longer be changed. In fact the course automatically goes into review mode and no further updates to any CMI value will be written.

## Call _LMSCommit_ Often

According to the SCORM 1.2 specification, CMI data is only required to be persisted when LMSFinish is called OR when LMSCommit is called. To ensure that student progress is properly tracked LMSCommit should be called frequently.

## Do Not Try to Close the Window

Many SCORM LMSs will launch a SCORM course in a popup window. NexPort Campus does not use popup windows. NexPort Campus has 2 options for launching a SCORM course.

First, is the "courseware launcher" with opens the courseware separately from the classroom but in the same window/tab. A menu at the top of the courseware launcher has a button that the student can use to "Return to Classroom."

Second, is the "embeded" mode. This mode provides the best experience for students. In this mode the courseware is displayed in the classroom directly. The SCO may call LMSFinish as it likes and the classroom will automatically pickup changes to the grade and status.

## QA Your Courses in NexPort

Curriculum developers frequently QA their course in their authoring environment only to find that it behaves differently in the Learning Management Environment. Small differences in how courses are launched or delivered can change, drastically, the experience for your students. You should always verify the behavior of your courses in NexPort Campus before publishing them.

## Manifest Identifiers Should Contain no Special Characters

The manifest identifiers should only contain letter, numbers, dashes and underscores.

## Consider Implementing Improved SCORM (iSCORM)

Not all tools support the iSCORM specification.

The IScorm Spec is a Super Set of the ADL SCORM 1.2 Specification. IScorm is designed to provide a few missing features to the SCORM 1.2 API while still mostly supporting the original SCORM 1.2 specification. Here are a few goals:

* Add ASYNC callbacks to LMSInitialize, LMSCommit and LMSFinish
* Expose an alternative to the standard window.api object instance that is less generic
* Expose versioning

[Click here to learn more about iSCORM](http://localhost:5000/o/8jter5exvHg3A0oWSmxn/s/X48Kz2UK6EcOyV7eH5PZ/).
