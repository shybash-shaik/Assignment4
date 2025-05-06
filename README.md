
#  Assignment 4: Git Hooks & Automation

## What is Husky?

Husky is a tool that makes it really easy to add Git hooks to your project. Git hooks are scripts that run automatically when you do things like commit or push code. With Husky, we can make sure that only clean, well-formatted code gets committed — automatically.

In this project, we used Husky to:
- Run a **linter (ESLint)** to catch any obvious bugs or style issues
- Use **Prettier** to format our code consistently
- Enforce **commit message rules** with Commitlint to keep our Git history clean

---

##  What We Set Up

Here’s what we added to the project:

- **Husky** to manage Git hooks
- **lint-staged** to only run checks on files that are staged for commit
- **ESLint + Prettier** to clean up code before it gets committed
- **Commitlint** to reject badly formatted commit messages
- **GitHub Actions** to run automated checks on every push and pull request

### Hooks in Action

- When you try to commit code:
  - It runs ESLint and Prettier on the changed files
  - If the code has issues or the formatting is wrong, the commit is blocked
- If your commit message doesn’t follow the conventional format, it’s rejected too

---

##  What We Tested

We tried committing with:
-  Bad code (lint errors) → Commit was rejected
   Messy formatting → Rejected
- Invalid commit message → Rejected
- Clean code and message → Commit successful

##  Why This Is Useful

Automating these checks helps a lot:
- It **catches problems early**, before they get pushed to GitHub
- Makes sure everyone’s code looks the same — no more style debates!
- Keeps commit messages clean and consistent
- Saves time during code reviews and prevents silly mistakes

It might feel like a small thing, but this kind of automation makes a big difference in team projects. Cleaner code, fewer bugs, and a smoother workflow.
