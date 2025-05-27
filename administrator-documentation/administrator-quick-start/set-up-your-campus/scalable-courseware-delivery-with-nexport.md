# Scalable Courseware Delivery with NexPort

In large-scale, multi-tenant education environments, efficiency and content integrity are paramount. One of the most effective architectural strategies in NexPort is to designate one organization as a central **Content Repository** and another as the **Delivery Sub-Organization**. This guide outlines how to implement this model using NexPort tools and best practices.

> 📌 **Recommended for:** Large organizations or those anticipating future growth. This model provides the structure and flexibility needed to scale efficiently.

***

### Overview of the Model

* **Repository Organization**: A centralized environment for developing, versioning, and QA'ing curriculum and sections.
* **Delivery Organization (Sub-Org)**: The learner-facing organization that delivers shared or copied content from the repository.

This approach ensures content consistency, simplifies updates, and streamlines QA and deployment processes.

***

### Preparing Your Campus for Scalable Delivery

Before implementing a repository and delivery org model, ensure your campus is structured to support it:

* Confirm that your **top-level organization** represents your administrative or parent entity.
* Set up any **shared resources**, such as system-wide enrollment settings or assets.
* Establish a clear **naming convention** for sub-organizations (e.g., `_Repo`, `_Delivery`, `_ClientA`) to streamline management and reporting.
* Configure **global roles** and **reusable groups** to standardize access control across organizations.

***

### Implementation Steps

#### 1. Create the Repository Organization

* Navigate to **Manage Campus**.
* Under **Organizations**, create a new org (e.g., `TrainingContent_Repo`).
* Assign curriculum developers or QA team members using role-based permissions.

#### 2. Build Curriculum

* Use NexPort Campus tools like the **Section Editor** and **Training Plan Editor** to build curriculum.
* Organize content into reusable **Sections** and **Courses**.
* Conduct internal QA using test groups and controlled enrollments.

> 💡 Use test groups to validate course logic, assessments, and completion workflows.

#### 3. Set Up the Delivery Sub-Organization

* In **Manage Campus**, create the learner-facing org (e.g., `AcmeTraining_Delivery`).
* Assign roles for instructors, facilitators, and learners as needed.
* Define your enrollment strategy: Will students be enrolled manually, in bulk, or via automated integration (API or external source)?
* Create **training plans** linked to groups to support automated enrollment workflows.

#### 4. Share or Copy Curriculum

Choose the best method based on your control and versioning requirements:

**Option A: Share Content**

* Use the **shareable content feature** to grant access to repository sections.
* **Pros**: Always current; centralized updates.
* **Cons**: Changes propagate immediately, requiring tight version control.

**Option B: Copy Content**

* Use the **Copy Course** or **Copy Section** tools to duplicate curriculum into the delivery org.
* **Pros**: Provides isolation for versioning and sandboxing.
* **Cons**: Manual effort required to apply updates.

#### 5. Monitor and Report

* Leverage **NexPort Analytics** in the delivery org to monitor learner progress and completion.
* Maintain version history in the repository to support audits, recertification, and continuous improvement.

***

### Best Practices and Workflow Suggestions

#### QA & Deployment Workflow

1. Author and stage curriculum in the repository org.
2. Conduct QA using test enrollments.
3. Share or copy to the delivery org once approved.
4. Notify instructors or administrators when new content is available.
5. Use analytics to confirm successful deployment and learner engagement.

#### Role Management Tips

* Use **RBAC** to control access based on user roles and responsibilities.
* Consider creating a "Content Curator" role for hybrid author-review workflows.

#### Recommended Roles

* **Course Author** – Builds and edits curriculum within the repository org.
* **QA Reviewer** – Has read-only access in delivery orgs to review content before release.
* **Instructor/Facilitator** – Assigned to learner groups in delivery orgs to support delivery and interaction.
* **Org Admin** – Oversees organizational structure and manages permissions.

***

### Related Features

* **Custom Branding** – Tailor the delivery org’s interface to align with client or partner identities.
* **API Automation** – Use the NexPort WebAPI for seamless content syncing and workflow automation.

***

### Why This Model Works

* **Separation of Duties** – QA and content creation are decoupled from delivery.
* **Scalability** – Supports multiple delivery orgs from one centralized content source.
* **Governance and Compliance** – Only reviewed and approved content reaches learners.

***

### Documentation Links

* [Administrator Quick Start Guide](../)
* [Understanding Permissions in NexPort Campus](../../administrator-reference/campus-management/group-tools/permissions/understanding-permissions-in-nexport-campus.md)
* [Managing Organizations](../../administrator-reference/campus-management/)
