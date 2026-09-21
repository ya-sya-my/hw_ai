## Communication & Workflow Rules

1. **Project Scope**
   - Work only with files inside the current repository.
   - Do not modify, delete, or access unrelated projects or parent directories unless explicitly requested.
   - Preserve existing project structure and files unless a change is required by the task.
   - Do not create unnecessary files or dependencies.

2. **Environment & Secrets**
   - Never modify or commit `.env` files.
   - Never expose, print, or commit API keys, tokens, passwords, or other credentials.

3. **API Development**
   - Follow the existing API specification and project requirements.
   - Keep API request and response formats consistent with the OpenAPI specification.
   - Validate API behaviour using real local HTTP requests when applicable.
   - Do not introduce a real database or external backend when the task requires a local mock server.

4. **Testing & Verification**
   - After implementing a logical change, run the relevant tests.
   - Verify that the application starts successfully.
   - For API changes, test the affected endpoints and verify HTTP status codes and response bodies.

5. **Code Quality Before Commits**
   - Run the project's available tests, linting, formatting, and type-checking commands before committing.
   - First inspect `package.json` and the existing project configuration to determine which commands are available.
   - If a required check does not exist, do not invent unnecessary tooling just for the sake of the check.
   - Do not commit code while required tests are failing.

6. **Git Workflow**
   - Before committing, always run `git status` and `git diff`.
   - Briefly summarize the changes to me in 1-2 plain English sentences.
   - Ask for my permission to commit: "Shall I commit these changes?"
   - Briefly summarize the changes in 1–2 sentences.
   - Ask for my permission before creating a commit.
   - Use Conventional Commits format for commit messages.
   - Never push to the remote repository unless I explicitly ask you to.

7. **Documentation**
   - Keep the README.md up to date with setup, installation, usage, testing, and API instructions.
   - When introducing a new command or workflow, document it in README.md.

8. **Project Requirements**
   - Before starting implementation, read `PROJECT_REQUIREMENTS.md`.
   - Treat this file as the source of truth for the project.
   - Keep the implementation simple and limited to the stated requirements.
