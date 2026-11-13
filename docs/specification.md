# TaskFlow — Team Task Management System

## Project Title and Description

TaskFlow is a web-based project management application for students, study groups,
small organizations, and project teams. It provides one place to organize
projects, assign responsibilities, track task status, and monitor progress.

## Problem Statement

Students and small teams often coordinate responsibilities, deadlines, and
progress across separate tools. TaskFlow brings project and task organization
together in a shared dashboard so teams can see what needs attention and who is
responsible.

## Purpose and Target Audience

- **Purpose:** Help small teams organize projects and follow work through to
  completion.
- **Audience:** Students, study groups, small organizations, and project teams.

## User Stories

1. As a user, I want to register an account so that I can securely access the
   application.
2. As a user, I want to sign in and out so that I can manage my work in a
   protected account.
3. As a user, I want to create and manage projects so that I can organize work
   for a team.
4. As a project owner, I want to add team members so that collaborators can
   participate in a project.
5. As a project member, I want to create, assign, edit, and delete tasks so that
   responsibilities are clear and current.
6. As a project member, I want to move tasks between To Do, In Progress, and
   Completed so that project progress is accurate.
7. As a team member, I want to see project summaries and task progress on a
   dashboard so that I can understand what is on track or needs attention.
8. As a user, I want to manage my profile so that my account information stays
   current.

## Acceptance Criteria

### Story 1: Register an account

- A registration form collects the required account details.
- Required fields and email format are validated before submission.
- Valid details create an account and provide clear success or failure feedback.
- Duplicate or invalid registrations are rejected with an actionable message.

### Story 2: Sign in and out

- A user can submit credentials through a sign-in form.
- Valid credentials establish a session and take the user to the dashboard.
- Invalid credentials do not establish a session and show a useful error.
- Signing out ends the session and prevents access to protected pages.

### Story 3: Manage projects

- A signed-in user can create a project with a title and description.
- A project owner can view, edit, and delete their projects.
- Invalid or missing required project fields prevent saving and are identified.
- Deletion requires confirmation and removes the project from the user's list.

### Story 4: Add team members

- A project owner can select existing users to join a project.
- Members can see projects they are authorized to access.
- Users who are not members cannot change that project's data.

### Story 5: Manage tasks

- A project member can create a task with a title and project.
- A task can be assigned to an eligible project member.
- Authorized members can view and edit task details or delete a task.
- Invalid task data is rejected with clear validation feedback.

### Story 6: Track task status

- A task supports To Do, In Progress, and Completed statuses.
- An authorized member can update a task's status.
- The updated status is reflected in the task list and project summary.

### Story 7: View project progress

- The dashboard lists projects available to the signed-in user.
- Project summaries show task totals and completed versus incomplete tasks.
- Empty states explain when the user has no projects or tasks.

### Story 8: Manage a profile

- A signed-in user can view and update editable profile information.
- Invalid profile changes are rejected without losing the existing information.

## Data Models

- **User:** name, email, password credential (stored securely by the chosen
  authentication provider), profile information.
- **Project:** title, description, owner, members, optional due date.
- **Task:** title, description, status, assigned user, project reference.

Every project and task operation must enforce authorization on the server.
Passwords must never be stored as plaintext.

## Technical Requirements

- **Framework:** Next.js App Router.
- **Language:** TypeScript with strict type checking; avoid `any`.
- **Styling:** Tailwind CSS utility classes, with custom CSS only when necessary.
- **Rendering:** Use Server Components by default; add Client Components only
  for browser-side interactivity.
- **Validation:** Validate untrusted form and API input on the server.
- **Accessibility:** Use semantic HTML, labels, keyboard-operable controls, and
  visible focus states.
- **Testing:** Cover validation, authorization, project/task workflows, and
  responsive layouts with appropriate automated tests.
- **Current repository baseline:** Next.js, React, TypeScript, Tailwind CSS, and
  ESLint are present. Authentication, persistence, and automated test tooling
  are not yet configured; choose and document those before implementing those
  features.

## Proposed API Endpoints

These are planned interfaces, not claims about routes already implemented.

| Method | Endpoint                         | Purpose                                     |
| ------ | -------------------------------- | ------------------------------------------- |
| POST   | `/api/auth/register`             | Register a user                             |
| POST   | `/api/auth/login`                | Start a user session                        |
| POST   | `/api/auth/logout`               | End the current session                     |
| GET    | `/api/projects`                  | List projects available to the current user |
| POST   | `/api/projects`                  | Create a project                            |
| GET    | `/api/projects/:projectId`       | Read an authorized project                  |
| PATCH  | `/api/projects/:projectId`       | Update an authorized project                |
| DELETE | `/api/projects/:projectId`       | Delete an authorized project                |
| GET    | `/api/projects/:projectId/tasks` | List tasks in an authorized project         |
| POST   | `/api/projects/:projectId/tasks` | Create a task in an authorized project      |
| PATCH  | `/api/tasks/:taskId`             | Update an authorized task                   |
| DELETE | `/api/tasks/:taskId`             | Delete an authorized task                   |
| GET    | `/api/profile`                   | Read the current user's profile             |
| PATCH  | `/api/profile`                   | Update the current user's profile           |

## Implementation Priority

- **P0:** Authentication, project creation and listing, task creation and
  assignment, status tracking, and a basic progress dashboard.
- **P1:** Project and task editing/deletion, team membership, profile management,
  authorization hardening, and workflow tests.
- **P2:** Notifications, richer progress reporting, and other enhancements
  selected after the core workflows are evaluated.

## Open Decisions

- Select the authentication provider and persistent database before building
  account and project workflows.
- Define whether projects can be shared by invitation and how invitations are
  accepted.
- Confirm deployment and testing environments with the team.
