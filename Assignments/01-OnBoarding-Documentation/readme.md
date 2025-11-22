# ChaiCode Cohort Git Onboard Documentation

This documentation should be clear, action-oriented, and serve as the single source of truth for all code management at Chai Code.

## 1.Foundational Principals (the "WHY")

| Principle                 | Why It Matters (Industry Standard)                                                                                     |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Atomic Commits            | Each commit should represent a single, complete logical change. This makes rollbacks and code reviews cleaner.         |
| Linear History            | We prioritize a clean, understandable history. We use tools like git rebase to keep the history linear before merging. |
| Documentation via Commits | The commit history itself serves as documentation. Messages must be descriptive and follow a strict format.            |

## 2. 🌳 Branching Strategy: Git Flow Light

| Branch Name | Purpose                                                                                             | Protection Rule                                                                                 |
| ----------- | --------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `main`      | Production-Ready Code. This branch should always be deployable.                                     | Strictly Protected. Direct commits are forbidden. Merges only via approved Pull Requests (PRs). |
| `develop`   | Integration Branch. All new features and fixes are merged here first for testing.                   | Protected. Merges only via approved PRs.                                                        |
| `feature/`  | Feature Branches. Used for all new work. Named like `feature/login-page` or `feature/user-profile`. | Unprotected. Created by developers for their tasks.                                             |
| `bugfix/`   | Hotfixes/Patches. Used for urgent fixes that might bypass develop and go straight to main (rarely). | Unprotected. Used for rapid, critical fixes.                                                    |

**Note**: _Key Takeaway_ : **Never commit directly to main or develop. All work must start on a new feature branch.**

## 3. Commits Message Guidelines

This is one of the most critical aspects of industry-standard Git practice. We follow the Conventional Commits specification.

### Commit Structure

A good commit message has a clear Subject Line and an optional Body for more detail.

```
<type>(<scope>): <subject>

<body>

<footer>
```

#### 📌 The Five Types (Chai Code Standard):

| Type       | Purpose                                                                          | Example Subject                                   |
| ---------- | -------------------------------------------------------------------------------- | ------------------------------------------------- |
| `feat`     | A new feature or enhancement.                                                    | `feat(api): add GET /users endpoint`              |
| `fix`      | A bug fix.                                                                       | `fix(auth): correct token expiration logic`       |
| `docs`     | Documentation changes only.                                                      | `docs(readme): update installation steps`         |
| `style`    | Code formatting, missing semicolons, etc. (no change in code logic).             | `style(css): adjust padding on header element`    |
| `refactor` | A code change that neither fixes a bug nor adds a feature (e.g., restructuring). | `refactor(db): convert SQL queries to ORM models` |

#### Example Commit Message (Industry Quality):

```
feat(checkout): Implement tiered shipping rates

The shipping calculation service now checks the cart total and
applies tiered rates (e.g., $10 under $50, $5 over $50).
This required updating the ShippingService interface.

BREAKING CHANGE: The 'calculateShipping' function now expects
'totalCartValue' argument.
```

## 4. 🚀 The Standard Workflow (The "How-To")

This section guides developers through the daily use of Git, emphasizing a clean history.

**Step 1**: Start a New Feature
Action: Create and switch to a new branch off of develop.

**Command**: `git checkout develop &&  git pull origin develop`

**Command**: `git checkout -b feature/your-task-name`

**Step 2**: Commit Your Work

**Action**: Use git add to stage changes and commit frequently, following the message guidelines.

**Command**: `git add .`

**Command**: `git commit -m "feat(component): add new header component"`

**Step 3**: Ensure a Clean History (Key Industry Practice)
Before merging, you must clean up your feature branch to ensure a linear history.

**Action**: Rebase your branch onto the latest develop to get all recent changes without merge commits.

**Command**: `git pull --rebase origin develop`

_If there are conflicts, resolve them, use_ `git add .`, and then `git rebase --continue.`

**Step 4**: Submit for Review (Pull Request)

**Action**: Push your cleaned branch to the remote repository.

**Command**: `git push -u origin feature/your-task-name`

**Action**: Go to the repository hosting platform (GitHub/GitLab/Bitbucket) and create a Pull Request (PR) targeting the develop branch.

**Step 5**: Final Merge

**Action**: Once the PR is approved, it is Squash Merged into develop.

### Why Squash Merge?

This practice takes all of your feature branch's small, in-progress commits (e.g., "WIP," "fix typo") and combines them into one clean commit in the develop history. This keeps the develop history tidy and easy to read.
