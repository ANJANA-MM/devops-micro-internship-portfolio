# Week 2 – Git & Version Control Fundamentals

This week focuses on **setting up Git correctly on a local system**, understanding repository initialization, configuring Git identities, tracking changes in a project, working with branches, and interacting with GitHub. These fundamentals are essential before contributing to team and enterprise projects like **CodeTrack** at CloudAdvisory.

The assignments for this week include:

1. **Assignment 5:** CodeTrack — Initial Git Setup (Local Only)
2. **Assignment 6:** Tracking and Staging Changes in a CodeTrack Project
3. **Assignment 7:** Branching Workflow — Add & Verify a Contact Page
4. **Assignment 8:** Setting Up GitHub for CodeTrack
5. **Assignment 9:** Collaborating on Mini-Finance with GitHub

---

## Assignment 5 – CodeTrack: Initial Git Setup (Local Only)

**Objective:**
Set up Git on a local machine by initializing a repository and configuring Git username and email both **locally (per project)** and **globally (system-wide)**, following professional DevOps practices.

**High-Level Tasks Performed:**

* Created a new `CodeTrack` project folder and initialized it as a Git repository.
* Configured Git identity **locally** for the repository.
* Optionally configured Git identity **globally** for the system.
* Verified repository creation and configuration.

**Skills Gained:**

* Initializing a Git repository from scratch
* Configuring Git identity at local and global levels
* Understanding the `.git` folder structure
* Applying Git best practices for team/enterprise projects
* Preparing a clean Git environment before pushing code to GitHub

**Detailed Steps & Screenshots:**
For step-by-step commands, expected outputs, and screenshots, see the [Assignment 5 README](Assignment-5/README.md).

---

## Assignment 6 – Tracking and Staging Changes in a CodeTrack Project

**Objective:**
Learn how to create and track files in a Git repository, stage and commit changes, verify Git history, and deploy a simple HTML/CSS web application on an AWS EC2 instance using Nginx.

**High-Level Tasks Performed:**

* Verified Git installation and configuration.
* Navigated to the existing `CodeTrack` project directory.
* Created `index.html` and `style.css`, modified content, and added optional `screenshots` folder.
* Tracked files using `git add`, staged and committed changes with meaningful messages.
* Viewed and verified commit history with `git log --oneline`.
* Modified files and repeated staging and committing process to reflect updates.
* Launched an AWS EC2 instance, installed and configured Nginx.
* Deployed project files to Nginx’s web directory, set ownership and permissions.
* Accessed the application successfully via the EC2 public IP.

**Key Commands Used:**

```bash
# Track and commit changes
git status
git add .
git commit -m "Descriptive commit message"
git log --oneline

# EC2 deployment
ssh -i your-key.pem ec2-user@<EC2-Public-IP>
sudo yum update -y
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo rm -rf /usr/share/nginx/html/*
sudo cp -r /home/ec2-user/CodeTrack/* /usr/share/nginx/html/
sudo chown -R nginx:nginx /usr/share/nginx/html/
sudo chmod -R 755 /usr/share/nginx/html/
```

**Skills Gained:**

* Tracking, staging, and committing files in Git
* Understanding staged vs. unstaged changes
* Maintaining meaningful Git commit history
* Modifying and updating project files efficiently
* Deploying static web applications on AWS EC2 using Nginx
* Managing Linux file permissions and ownership
* End-to-end Git + deployment workflow

**Detailed Steps & Screenshots:**
For step-by-step commands, expected outputs, and screenshots, see the [Assignment 6 README](Assignment-6/README.md).

---

## Assignment 7 – Branching Workflow: Add & Verify a Contact Page

**Objective:**
Practice a real-world Git **branching workflow** by creating a feature branch, making isolated changes, committing with meaningful messages, merging into the `main` branch, and verifying the merge through Git history visualization.

**High-Level Tasks Performed:**

* Started from an existing Git repository on the `main` branch.
* Created and switched to a dedicated feature branch: `feature/contact-page`.
* Added a new `contact.html` page with basic contact details.
* Updated `index.html` to include a navigation link to the Contact Page.
* Committed changes incrementally with clear, descriptive commit messages.
* Verified branch isolation to ensure `main` remained unaffected before merging.
* Merged the feature branch back into `main`.
* Validated merged changes by opening files in a browser.
* Inspected Git history using a graphical commit log to confirm a clean merge.
* Optionally deleted the feature branch after successful merge.

**Key Concepts Demonstrated:**

* Feature branch–based development workflow
* Safe isolation of changes using branches
* Clean and meaningful commit history
* Fast-forward vs merge commit visualization
* Understanding `HEAD`, branch pointers, and merge commits
* Using `git log --oneline --graph --decorate --all` to analyze repository history

**Key Commands Used:**

```bash
# Branching
git branch
git checkout -b feature/contact-page
git checkout main

# Staging & committing
git status
git add <file>
git commit -m "descriptive message"

# Merging
git merge feature/contact-page

# History inspection
git log --oneline --graph --decorate --all

# Cleanup
git branch -d feature/contact-page
```

**Skills Gained:**

* Creating and managing feature branches in Git
* Isolating development work from the main branch
* Writing clear and structured Git commit messages
* Safely merging feature branches into main
* Reading and interpreting Git commit graphs
* Understanding merge commit pointers (`HEAD -> main, feature/...`)
* Following professional Git workflows used in team and enterprise projects

**Detailed Steps & Screenshots:**
For complete step-by-step commands, explanations, and screenshots, see the
[Assignment 7 README](Assignment-7/README.md).

---

## Assignment 8 – Setting Up GitHub for CodeTrack

**Objective:**
Create a GitHub repository for the CodeTrack project, explore core GitHub features, and prepare for pushing code and collaborating remotely.

---

### Step 1 – Create a GitHub Account

1. Go to [GitHub](https://github.com/) and click **Sign Up**.
2. Enter your email, password, and username.
3. Complete verification and click **Create Account**.
4. Access your **GitHub Dashboard**.

**Expected Outcome:**
You now have a GitHub account and access to the dashboard.

---

### Step 2 – Explore Core GitHub Features

* Open the **Explore** section from the top navigation.
* Browse **Trending Repositories** to see popular projects.
* Use the search bar to find an open-source repository (e.g., `theepicbook`).
* ⭐ **Star** a repository to save it for future reference.
* 🍴 **Fork** a repository to create a personal copy.

**Expected Outcome:**
You have explored GitHub, starred at least one project, and forked a repository, gaining familiarity with discovery and engagement features.

---

### Step 3 – Optional Profile Update

* Add a short bio (e.g., “Cloud & DevOps Enthusiast | Learning Git & GitHub”).
* Optionally add location, company/school, and social links.
* Upload a profile picture and save changes.

**Expected Outcome:**
Your GitHub profile is personalized and professional.

---

### Skills Gained

* Creating and configuring a GitHub account
* Exploring repositories, starring, and forking projects
* Understanding GitHub repository discovery and engagement
* Preparing for pushing code and collaborating on GitHub
* Building confidence with remote Git workflows

---

**Detailed Steps & Screenshots:**
For complete step-by-step commands, explanations, and screenshots, see the
[Assignment 8 README](Assignment-8/README.md).

---

## Assignment 9 – Collaborating on Mini-Finance with GitHub

**Objective:**
Practice a **real-world GitHub collaboration workflow** by contributing to an existing project using forks, remotes, feature branches, rebasing, and Pull Requests — following professional DevOps and open-source standards.

This assignment simulates how developers collaborate on **team-owned or open-source repositories** where direct push access to the main repository is restricted.

---

### High-Level Tasks Performed

* Identified the original (**upstream**) Mini-Finance repository.
* Forked the repository into a personal GitHub account.
* Configured secure GitHub authentication using **SSH keys**.
* Cloned the forked repository locally.
* Configured multiple Git remotes (`origin` and `upstream`).
* Created a dedicated feature branch for changes.
* Made documentation updates and committed changes with clear messages.
* Synced local branches with upstream using `fetch`, `merge`, and `rebase`.
* Pushed the feature branch to the forked repository.
* Created a **Pull Request** to propose changes to the upstream repository.

---

### Key Concepts Demonstrated

* Fork-based GitHub collaboration workflow
* Understanding and managing `origin` vs `upstream`
* Secure GitHub authentication using SSH
* Feature branch–based development
* Syncing forks with upstream repositories
* Rebasing to maintain a clean commit history
* Publishing changes via Pull Requests
* Professional contribution practices used in enterprise and open-source projects

---

### Key Commands Used

```bash
# Fork & clone
git clone git@github.com:<your-username>/mini_finance.git

# Remote configuration
git remote -v
git remote add upstream https://github.com/pravinmishraaws/mini_finance.git

# Branching
git checkout -b feature-readme-update

# Commit changes
git add README.md
git commit -m "docs: update README with assignment note"

# Sync with upstream
git fetch upstream
git checkout main
git merge upstream/main
git checkout feature-readme-update
git rebase main

# Push feature branch
git push -u origin feature-readme-update
```

---

### Skills Gained

* Contributing to shared GitHub repositories safely
* Managing multiple remotes in Git
* Working with feature branches and rebasing
* Keeping forks in sync with upstream projects
* Creating professional Pull Requests
* Understanding real-world Git collaboration workflows
* Preparing for team-based and open-source DevOps environments

---

### Detailed Steps & Screenshots

For complete step-by-step commands, explanations, screenshots, and workflow reasoning, see the
[Assignment 9 README](Assignment-9/README.md).

---

## 📝 Week 2 Technical Article – Git Fundamentals

I authored a beginner-friendly technical article explaining **Git fundamentals using real-world scenarios and hands-on examples**, focused on practical understanding rather than theory.

🔗 **Git: Your Best Friend in Version Controlling**
[https://medium.com/@anjana-muthuanayake/git-your-best-friend-in-version-controlling-9773b87c75a1](https://medium.com/@anjana-muthuanayake/git-your-best-friend-in-version-controlling-9773b87c75a1)

### 🔧 Key Concepts Covered

* Why Git is essential for version control
* Repository initialization and `.git` internals
* File lifecycle: untracked → staged → committed
* Commits, history tracking, and meaningful messages
* Branching, HEAD, and detached HEAD
* Undo strategies: `revert`, `reset --soft`, `reset --hard`
* Ignoring files with `.gitignore`

### 🎯 Outcome

* Strengthened core Git workflows used in DevOps pipelines
* Improved ability to explain Git concepts clearly and practically
* Documented Week 2 learning in a recruiter-friendly technical format

---


