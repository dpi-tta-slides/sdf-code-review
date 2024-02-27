---
marp: true
title: Code Review 
description: This lesson introduces code review and pull requests
transition: fade
paginate: true
_paginate: false
---

# <!--fit--> Code Review

---

# 🌟 Why?
- One of the most important components of staying happy for developers is feeling like we’re always continuing to learn.
- One of the best ways to promote learning on a team is a strong Code Review Culture.

---
# 🌟 Why?

- It feels great to get alternative ideas on how to attack a problem right when you are setting out.
- Often, someone else on the team can alert you to a different approach that you hadn’t considered or heard about.

---
# 🌟 Why?

- You would be surprised at how often a junior developer can teach a senior developer a new trick.
- Code Review is an incredibly good way to train junior developers.
- Code Reviews demolish knowledge silos, reducing your risk.
- Oh, and they helps catch bugs sometimes, too.

---
# 🛤️ Git Flow

- Master/Main Branch 🏛️
  - The 'sacred' branch.
  - Always production-ready.
- Feature Branches 🌿
  - Branches created to develop new features without disturbing the main branch.

---

![bg contain](./assets/commit-graph.png)

---

# 🔀 Git Flow Lifecycle

- Create a feature branch 🌿
```bash
# usually want to create branch from main
git checkout main

# fetch latest changes
git pull

# create new branch (follow suggested naming guidelines)
git checkout -b feature/my-new-feature
```

---
# 🔀 Git Flow Lifecycle

- Implement and commit changes 🧑‍💻
```bash
git add .
git commit -m "Implement my new feature"
```

---
# 🔀 Git Flow Lifecycle
- Push branch to remote 'origin' ☁️
```bash
git push
```
---
# 🔀 Git Flow Lifecycle
- Create a Pull Request (PR) of feature branch into main branch.
- Team reviews pull request 👩‍💻👨‍💻
  - Comment 💬
  - Request changes 🔂
  - Implement, commit, and push changes 🧑‍💻
- Teammates approve (or reject) 👍👎
- Merge into main 🔀

---
# 🤔 Why PRs?

![contain](./assets/pr.png)

---
#  🤔 Why PRs?
- Allows team members to review code changes before they're merged.

![bg right contain](./assets/pr-comments.png)

---
#  🤔 Why PRs?
- See a clean diff

![bg right contain](./assets/pr-diff.png)

---

# 🔥 Merge Conflicts

- Merge conflicts happen when git cannot automatically merge changes. 🤷
- Merge conflicts are caused by overlapping changes. ⛏️🚫
- Identify the conflicted areas and decide which code stays, which code goes. ❗
- Commit the resolved changes.

---
# 🔥 Merge Conflicts

![](./assets/merge-conflict.png)

---

# 👩‍🔧 Best Practices

- Regularly pull changes from main branches.

```bash
git pull origin main
```

- Keep feature branches focused and short-lived.

- Clear commit messages.

---

# 👩‍🔧 Best Practices

- Senior and Lead developers are usually very busy
<!-- don't be annoying 😅 -->
- Make sure to reach out if you are waiting on a review

---
# 🤪 Fun Facts
https://github.com/DPI-WE/fun-facts

- Fun Facts is an index of fun facts.
- Follow the contribution guidelines to add your fun fact.


---

# 🛤️ Git Commands & Flow

---

## Check your current branch. Understand where you are.

```bash
git branch
```

---

## Switch to the 'main' branch before creating a new feature branch.

```bash
git checkout main
```

---

## Pull the latest changes from the remote repository (always do this before creating a new branch to ensure you're up-to-date).

```bash
git pull origin main
```

---
## Working on a new feature using Git Flow

1. Create a new feature branch
`git checkout -b feature/cuisine-filter`

2. Make changes & commit

```bash
git add .
git commit -m "Implement cuisine filter functionality"
```

3. Push your feature branch to the remote repository

```bash
git push origin feature/cuisine-filter
```

---
## Switch between branches (eg move back to main).

```bash
git checkout main
```
---

## Update your local branch with the latest changes post-merge (always good to stay updated).

```bash
git pull origin main
```

---
## Checkout Remote Branch

Good idea to checkout someone else's branch when doing a code review to make sure it works on your machine

1. Fetch all remote branches
`git fetch origin`

2. List the branches available for checkout
`git branch -a`

3. Pull changes from a remote branch
`git checkout -b someone-elses-branch origin/someone-elses-branch`

if you make a change, commit, then `git push`, git automatically sets the local branch to track that remote branch

---
## Check your status

This command will tell you what branch you are on, any diffs, staged files, etc.

<!-- TODO: add screenshot -->
`git status`



---
# Make sure to set configuration to resolve conflicts using merge

```bash
git config pull.rebase false
```

![](./assets/config-merge.png)


---

# References

- [RailsConf 2015 - Implementing a Strong Code-Review Culture](https://www.youtube.com/watch?v=PJjmw9TRB7s)