---
description: >-
  Recommendations for SCORM 1.2 and SCORM 2004 developers creating content for
  NexPort Campus
---

# SCORM Best Practices

NexPort Campus allows content developers to import SCORM 1.2 and SCORM 2004 packages and deliver them as assignments. Below we list a few best practices. Most of these recommendations are technical in nature. These instructions assume that the developer is familiar with the SCORM 1.2 Runtime Specification or the SCORM 2004 Runtime Environment Specification.



{% file src="../../.gitbook/assets/SCORM-12-RunTimeEnv.pdf" %}

{% file src="../../.gitbook/assets/SCORM_2004_4ED_RTE.pdf" %}

<details>

<summary>All Courseware</summary>

## Set _Lesson Status_ Immediately

According to the **SCORM 1.2 specification**, _cmi.core.lesson\_status_ will be set to _**completed**_ if a Sharable Content Object (SCO) finishes without setting the status on the first launch. NexPort Campus obeys this behavior. If a SCO fails to set the lesson\_status during the initial attempt by a student and the student exits the SCO then NexPort Campus will set the status to completed.

For SCORM 2004 this behavior is less specific. It's still a good idea to set the _cmi.completion\_status_ immediately upon launch to in progress.

If this is the desired behavior then the SCO should do nothing. If your SCO intends to set the _cmi.core.lesson\_status_ itself you should make sure it is set to "_incomplete_" immediately after the SCO calls LmsInitialize() or Initialize() (SCORM 2004).

## Do Not Try to Close the Window

Many SCORM LMSs will launch a SCORM course in a popup window. NexPort Campus does not use popup windows. NexPort Campus has 2 options for launching a SCORM course.

First, is the "courseware launcher" with opens the courseware separately from the classroom but in the same window/tab. A menu at the top of the courseware launcher has a button that the student can use to "Return to Classroom."

Second, is the "embeded" mode. This mode provides the best experience for students. In this mode the courseware is displayed in the classroom directly. The SCO may call LMSFinish as it likes and the classroom will automatically pickup changes to the grade and status.

## QA Your Courses in NexPort

Curriculum developers frequently QA their course in their authoring environment only to find that it behaves differently in the Learning Management Environment. Small differences in how courses are launched or delivered can change, drastically, the experience for your students. You should always verify the behavior of your courses in NexPort Campus before publishing them.

</details>

<details>

<summary>SCORM 1.2</summary>

##

## Setting cmi.core.lesson\_status to completed can not be reversed

If the lesson status is set to completed and LMSCommit is called the status can no longer be changed. In fact the course automatically goes into review mode and no further updates to any CMI value will be written.

## Call _LMSCommit_ Often

According to the SCORM 1.2 specification, CMI data is only required to be persisted when LMSFinish is called OR when LMSCommit is called. To ensure that student progress is properly tracked LMSCommit should be called frequently.

## Manifest Identifiers Should Contain no Special Characters

The manifest identifiers should only contain letter, numbers, dashes and underscores.

```xml
<organization identifier="acme_course_101">
      <title>Acme Course 101</title>
      <item identifier="acme_course_101" isvisible="true" identifierref="__6pvVJupxRfVhiv_RES">
        <title>acme_course_101</title>
      </item>
    </organization>
  </organizations>
```

## Consider Implementing Improved SCORM (iSCORM)

Not all tools support the iSCORM specification.

The IScorm Spec is a Super Set of the ADL SCORM 1.2 Specification. IScorm is designed to provide a few missing features to the SCORM 1.2 API while still mostly supporting the original SCORM 1.2 specification. Here are a few goals:

* Add ASYNC callbacks to LMSInitialize, LMSCommit and LMSFinish
* Expose an alternative to the standard window.api object instance that is less generic
* Expose versioning

[Click here to learn more about iSCORM](https://app.gitbook.com/o/8jter5exvHg3A0oWSmxn/s/X48Kz2UK6EcOyV7eH5PZ/).

</details>

<details>

<summary>SCORM 2004</summary>

## Using Asynchronous API Calls in Articulate Courses

The async API option allows SCORM 2004 courses, especially those made with Articulate, to use asynchronous API calls. This is particularly useful in review mode.

#### Key Points

* **SCORM 2004 Support**: Async API calls are supported for SCORM 2004 courses.
* **Review Mode**: Improves stability when reviewing completed courses.
* **SCORM 1.2**: This setting is ignored for SCORM 1.2 courses.

#### Enabling Async API Calls

1. Go to course settings.
2. Find API settings.
3. Enable asynchronous API calls.
4. Save and test the course.

#### Default Behavior for Articulate Courses

By default, the **Use Async API** option is enabled when uploading a course created with Articulate. While this does not fully align with the SCORM 2004 specification, it is necessary for proper functionality in review mode. This approach also provides greater flexibility for potential future updates to the specification, ensuring better compatibility with evolving browser behaviors and minimizing interruptions in the learner experience.

This setting enhances compatibility with Articulate-authored SCORM 2004 courses, especially in review mode.

## Updating Articulate Rise Courseware

Before replacing an Articulate Rise SCORM 2004 package that active learners
have started, test whether the updated package can resume the existing learner
data. See [Troubleshoot Rise SCORM 2004 Updates](../administrator-reference/campus-management/organization-tools/courseware/troubleshoot-rise-scorm-2004-updates.md)
for the diagnostic and release process.

</details>
