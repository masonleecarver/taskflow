# TaskFlow

TaskFlow is a project and task management application for students and small
teams. The current repository is the initial Next.js App Router project
structure; application features are planned in the [project specification](docs/specification.md).

## Team Deliverables

- [Team meeting summary](docs/team-meeting-summary.md)
- [Project specification](docs/specification.md)
- [Project board issue drafts](docs/project-board-issues.md)
- [Code review report and issue draft](docs/code-review-report.md)

The GitHub Project Board URL and published code-review issue URL should be added
to the relevant documents after those items are created on GitHub.

## Technology

- Next.js App Router and React
- TypeScript
- Tailwind CSS
- ESLint
- Prettier, with `eslint-config-prettier`

Authentication, persistent storage, and automated test tooling have not yet been
added. See the specification for the open technical decisions.

## Local Development

Install dependencies and run the development server:

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Code Standards

- Run `npm run lint` before opening a pull request.
- Run `npm run format:check` to verify formatting; use `npm run format` to apply
  the agreed Prettier rules.
- Use TypeScript strict mode and avoid `any`.
- Prefer Next.js Server Components; use Client Components only when browser-side
  interactivity is needed.
- Use feature branches named for the work, such as `feature/user-auth`.
- Do not push directly to `main`. Merge changes through a pull request after at
  least one other team member reviews it.
- The `main` branch protection rules must be enabled in GitHub repository
  settings by a repository administrator.
