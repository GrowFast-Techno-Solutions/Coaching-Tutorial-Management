# Contributing Guidelines – Coaching Management Project

---

## 1. Getting Started

### Clone the Repository

1. **Fork the repository** to your own GitHub account.

2. **Clone your fork** to your local machine:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   ```

3. **Set up the upstream remote:**
   ```bash
   git remote add upstream https://github.com/<org-name>/<repo-name>.git
   ```

4. **Always sync with upstream before starting new work:**
   ```bash
   git checkout main
   git pull upstream main
   ```

---

## 2. Branching Workflow

We use a feature branch workflow with a protected main branch. We use hybrid branch naming convention to create any new branch.

### Branch Naming Conventions

- `feature/<issue-id><short-description>` → New feature (e.g., `feature/student-registration`)
- `bugfix/<issue-id><short-description>` → Bug fix (e.g., `bugfix/login-error`)
- `hotfix/<issue-id><short-description>` → Urgent production fix

### Example
```bash
git checkout -b feature/11-payment-page
```

---

## 3. Submitting Changes

1. **Work on your own feature branch.**

2. **Run linting and tests before committing:**
   ```bash
   npm run lint
   npm test
   ```

3. **Push your branch to your fork:**
   ```bash
   git push origin feature/11-payment-page
   ```

4. **Open a Pull Request (PR)** to the main branch of the main repository.

5. **In your PR description, link related issues using:**
   ```
   Fixes #<issue-number>
   ```

---

## 4. Code Review

- At least **1 approval** is required before merging.
- Keep PRs **small and focused** (≤ 300 lines of change is preferred).
- Address review comments promptly.

---

## 5. Project Setup (Local Development)

### Installation and Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the development server:**
   ```bash
   npm run dev
   ```

3. **Run tests:**
   ```bash
   npm test
   ```

---

## 6. Code Style

### General Guidelines
- Follow **ESLint** and **Prettier** configurations in the repo.
- Use **functional components** and **React hooks** for frontend.
- Keep functions **short and well-documented**.

### Component Architecture
We follow **Atomic Design methodology** for organizing and building components:

- **Elements** → Basic building blocks (buttons, inputs, labels)
  ```
  src/components/elements/Button/
  src/components/elements/Input/
  ```

- **Modules** → Groups of elements (search bar, form field)
  ```
  src/components/modules/SearchBar/
  src/components/modules/FormField/
  ```

- **Components** → Complex UI sections (header, sidebar, data table)
  ```
  src/components/components/Header/
  src/components/components/StudentTable/
  ```

- **Pages** → Complete views with real content
  ```
  src/pages/Dashboard/
  src/pages/StudentManagement/
  ```


### Component Guidelines as per Our Project
- **Elements(Atoms)**: Single responsibility, highly reusable
- **Modules(Molecules)**: Combine atoms, handle simple interactions
- **Components(Organisms)**: Complex functionality, business logic
- **Pages**: Connect to data sources and routing

---

Thank you for your contribution! 🎉