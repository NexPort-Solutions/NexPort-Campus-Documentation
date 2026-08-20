---
description: >-
  Diagnose and safely recover when an updated Articulate Rise SCORM 2004
  package will not open for learners who already started the course.
---

# Troubleshoot Rise SCORM 2004 Updates

An updated Articulate Rise SCORM 2004 package can work for new learners but
fail for learners who started an earlier version. This usually happens when
the updated package no longer recognizes the learner's saved SCORM resume
data.

## Recognize the Issue

This problem is likely when all of the following are true:

* Learners who are newly enrolled can open the updated course.
* Learners who previously opened the course receive a page-not-found or
  similar error when they resume it.
* Uploading the previous package allows affected learners to open the course
  again.
* The update was created by duplicating or rebuilding the Rise course, or by
  using a different publishing method.

> Note: A browser console cross-origin warning is not, by itself, evidence
> that NexPort Campus cannot launch the course. If the same warning appears
> for new learners whose course opens successfully, investigate the saved
> SCORM data and the authored package first.

## Why This Happens

NexPort Campus stores the progress that a learner reports through SCORM,
including the learner's last location and resume state. An Articulate Rise
update can change the package's internal page identifiers when the source
course is duplicated, rebuilt, or republished differently.

When the updated package is uploaded in place of the existing courseware,
NexPort Campus preserves the learner's earlier SCORM data. The updated package
may then try to resume at a page identifier that no longer exists, so the
course cannot load the requested page.

## Contain the Problem

1. Stop replacing additional affected courseware packages until the update has
   been tested.
2. Restore the previous package when continued access for existing learners is
   urgent.
3. Confirm the rollback with a learner who had already started the course and
   with a newly enrolled test learner.
4. Keep a copy of both the prior and updated SCORM ZIP files and record the
   courseware name, upload time, and affected learners before making further
   changes.

## Diagnose One Affected Learner

Compare a returning learner with a new test learner in the same updated course.

1. Confirm whether the new learner opens the course successfully.
2. Confirm whether the returning learner fails before selecting a different
   lesson or page.
3. Review the learner's SCORM assignment session and, when appropriate, enable
   logging for future attempts. See [Manage SCORM Assignment Sessions](../../../user-management/manage-enrollments/section-enrollment/manage-scorm-assignment-sessions.md).
4. Compare the saved SCORM location/resume data with the locations used by the
   updated package. A location that points to an older Rise page identifier
   supports this diagnosis.

> Warning: Changing a learner's SCORM CMI data can change what they see when
> they launch the course and can discard or alter recorded progress. Do not
> bulk-edit learner data or change package files as a first response. Preserve
> the original data and work with NexPort Support and the course author on a
> recovery plan.

## Provide New Enrollments While the Update Is Investigated

If the updated package is required for new learners, do not overwrite the
courseware used by active learners. Instead, work with NexPort Support to
publish the updated package as separate courseware in a separate organization
and use a separate section for new enrollments. This keeps existing learners
on the compatible package while the updated package is validated.

## Prevent Resume Problems in Future Rise Updates

Before replacing any SCORM 2004 package that learners may have already started:

1. Update the original Rise source course whenever possible; avoid creating
   the update by duplicating the course and treating it as the same course.
2. Keep the same publishing approach and SCORM version unless the change is
   explicitly tested for resume compatibility.
3. Retain the prior published ZIP and note its package and manifest identifiers.
4. Test the new ZIP in NexPort Campus with two test learners:
   * A new learner with no saved SCORM data.
   * A returning learner who launched the prior version and exited after
     visiting several pages.
5. Verify that the returning learner resumes correctly after the updated ZIP
   is uploaded.
6. If the course cannot resume correctly, publish it as new courseware for
   future enrollments or ask the course author to produce an update that
   preserves the required Rise page identifiers.

## Information to Provide to Support

When requesting help, include:

* The organization, courseware name, and section.
* The names or IDs of one affected returning learner and one successful new
  test learner.
* The previous and updated SCORM ZIP files, if they can be shared securely.
* Whether the Rise course was edited in place, duplicated, rebuilt, or
  published with a different method.
* The date and time of the package replacement.
* Screenshots of the learner-visible error and relevant SCORM session logs.

For general packaging and testing guidance, see [SCORM Best Practices](../../../../administrator-quick-start/scorm-best-practices.md).
