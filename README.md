"# DevOps Git Project" 
# DevOps Git Project

## Objective
Manage a DevOps project using Git best practices, including branching, feature development, pull requests, and tagging.

---

## Tools Used
- Git (CLI)
- GitHub (Remote repository)

---

## Branching Strategy

| Branch        | Purpose                        |
|---------------|--------------------------------|
| `main`        | Production-ready code          |
| `dev`         | Integration and testing        |
| `feature/*`   | Individual features (e.g., `feature/login`) |

---

## Steps Followed

### 1. Initialize Git Repository
```bash
git init

- Created .gitignore and README.md

- Staged and committed:

```bash
git add .
git commit -m "Initial commit with README and .gitignore"

2. Push to GitHub
```bash
git remote add origin <repo-url>
git push -u origin main

3. Create Branches
```bash
git checkout -b dev
git push -u origin dev

git checkout -b feature/login
git push -u origin feature/login

4. Develop Login Feature
- Created login.js with sample code:
console.log("Login feature implemented");

- Committed and pushed:
```bash
git add login.js
git commit -m "Add login feature"
git push

5. Create Pull Request
- Compared feature/login to dev
- GitHub showed:
- Resolved by making sure new commits were pushed to feature/login

6. Merge Pull Request
- Merged feature/login into dev using GitHub UI

7. Tag Release
```bash
git checkout main
git merge dev
git tag v1.0
git push origin v1.0
