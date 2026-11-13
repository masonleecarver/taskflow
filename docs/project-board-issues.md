# TaskFlow Project Board Issue Drafts

These are ready-to-create GitHub issue drafts. They are not yet GitHub issues
and are not attached to a Project Board. Apply the `feature` and priority labels
when creating them, then add all seven to the team's board.

## 1. Create account registration

**Labels:** `feature`, `P0`

As a new user, I want to register an account so that I can access TaskFlow.

**Acceptance criteria**

- A registration form collects all required account information.
- Required fields and email format are validated.
- Valid submissions create an account and show a success state.
- Invalid or duplicate submissions show actionable feedback.
- Passwords are never stored as plaintext.

## 2. Implement sign-in and sign-out

**Labels:** `feature`, `P0`

As a user, I want to sign in and out so that I can securely access my projects.

**Acceptance criteria**

- Valid credentials start a session and route the user to the dashboard.
- Invalid credentials show an error without starting a session.
- Signing out ends the session and prevents access to protected pages.
- Authentication failures are handled without exposing sensitive details.

## 3. Create and list projects

**Labels:** `feature`, `P0`

As a signed-in user, I want to create and view projects so that I can organize
team work.

**Acceptance criteria**

- An authorized user can create a project with a title and description.
- The project is persisted and appears in the user's project list.
- Required fields are validated with clear messages.
- Users cannot read projects they are not authorized to access.

## 4. Create and assign tasks

**Labels:** `feature`, `P0`

As a project member, I want to create tasks and assign them to team members so
that responsibilities are clear.

**Acceptance criteria**

- A task requires a title and a valid project.
- The assignee must be a member of that project.
- Authorized members can see the task and its assigned owner.
- Invalid task data is rejected with clear feedback.

## 5. Track task status

**Labels:** `feature`, `P0`

As a project member, I want to update task status so that project progress
stays accurate.

**Acceptance criteria**

- Tasks support To Do, In Progress, and Completed.
- Authorized members can change a task's status.
- The new status is reflected in the task list and project summary.
- Invalid status values are rejected by the server.

## 6. Build the project progress dashboard

**Labels:** `feature`, `P0`

As a team member, I want a project dashboard so that I can quickly understand
current progress.

**Acceptance criteria**

- The dashboard lists projects available to the signed-in user.
- Project summaries show total and completed versus incomplete tasks.
- Empty states explain when no projects or tasks are available.
- The dashboard remains usable on mobile-sized screens.

## 7. Edit and delete projects and tasks

**Labels:** `feature`, `P1`

As an authorized team member, I want to edit or delete outdated project and
task information so that the workspace remains accurate.

**Acceptance criteria**

- Authorized users can edit project and task details.
- Owners can delete their projects; project members can delete tasks if
  authorized by the project policy.
- Destructive actions require confirmation.
- Unauthorized and invalid operations are rejected and provide clear feedback.

## 8. Add project members

**Labels:** `feature`, `P1`

As a project owner, I want to add collaborators so that the team can work in a
shared project.

**Acceptance criteria**

- A project owner can add existing users as members.
- A user can only access projects they own or belong to.
- Duplicate membership is prevented.
- Membership changes are reflected in the project view.

## 9. Add profile management

**Labels:** `feature`, `P1`

As a user, I want to view and update my profile so that my account information
stays current.

**Acceptance criteria**

- A signed-in user can view their profile.
- Editable profile fields are validated on submission.
- A successful change is reflected on the profile.
- Users cannot modify another user's profile.
