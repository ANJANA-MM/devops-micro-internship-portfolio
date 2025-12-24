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
Learn how to create and track files in a Git repository, stage changes using `git add`, commit updates, and verify Git history. Deploy a simple HTML/CSS web application on an AWS EC2 instance using Nginx.

---

## Step 1 – Ensure Git Setup

* Verify Git is installed and configured properly.
* Check local or global Git identity using `git config --list`.

---

## Step 2 – Navigate to Project Folder

**Commands Used:**

```bash
cd path/to/CodeTrack   # Windows
cd ~/path/to/CodeTrack # macOS/Linux
pwd                    # Confirm current directory
```

* Ensures you are inside the `CodeTrack` project folder created in Assignment 5.

---

## Step 3 – Create and Modify Files

**Files Created:**

```bash
touch index.html style.css   # macOS/Linux
echo > index.html            # Windows
echo > style.css             # Windows
```

* Verified files using `ls` or `dir`
* Modified `index.html` and `style.css` in a text editor
* Copied content from GitHub repo: `Week-2---Git-GitHub-Assignment`

---

## Step 4 – Track Files Using Git

**Commands Used:**

```bash
git status       # Check untracked files
git add .        # Stage all files
# or individually
git add index.html
git add style.css
git status       # Verify staged files
```

* Expected output: Files marked as **"Changes to be committed"**

---

## Step 5 – Commit the Changes

```bash
git commit -m "Initial commit - Added index.html and style.css"
git log --oneline   # Verify commit history
```

* Expected output:

```
1a2b3c4 Initial commit - Added index.html and style.css
```

---

## Step 6 – Modify a File and Commit Again

* Open `index.html` in a browser and follow instructions to modify content.
* Stage and commit changes:

```bash
git status
git add index.html
git commit -m "Updated heading in index.html"
git log --oneline
```

* Expected output:

```
3d4e5f6 Updated heading in index.html
1a2b3c4 Initial commit - Added index.html and style.css
```

* Optional: Added `screenshots` folder and modified `style.css`

---

## Step 7 – Deploy Application on EC2

**Steps:**

1. Launch EC2 instance and connect via SSH:

```bash
ssh -i your-key.pem ec2-user@<EC2-Public-IP>
```

2. Update packages & install Nginx:

```bash
sudo yum update -y
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl status nginx
```

3. Deploy project files:

```bash
sudo rm -rf /usr/share/nginx/html/*
sudo cp -r /home/ec2-user/CodeTrack/* /usr/share/nginx/html/
sudo chown -R nginx:nginx /usr/share/nginx/html/
sudo chmod -R 755 /usr/share/nginx/html/
```

4. Access application:

```
http://<EC2-Public-IP>
```

* Application should load successfully in browser.

---

## Skills Gained

* Tracking and staging files with Git
* Committing changes with meaningful messages
* Viewing commit history and understanding Git workflow
* Modifying files and managing staged vs. unstaged changes
* Deploying a static web application on AWS EC2 with Nginx
* Basic server management: file permissions, ownership, and service control

---

## Assignment 7 – Branching Workflow: Add & Verify a Contact Page

**Objective:**
Practice creating branches, committing feature-specific changes, merging them into the main branch, and verifying functionality in a live browser. This workflow mirrors professional Git feature-branch practices.

---

### Step 0 – Start from Existing Repository

**Commands:**

```bash
cd path/to/CodeTrack
git status
git branch
```

* Ensure you are on `main` (or `master`).

---

### Step 1 – Create and Switch to a Feature Branch

```bash
git checkout -b feature/contact-page
git branch
```

* Expected: `* feature/contact-page` indicates active branch.

---

### Step 2 – Add `contact.html` in the Branch

**Create the file:**

```bash
touch contact.html      # macOS/Linux
# ni contact.html       # Windows PowerShell alternative
```

**File content:**

```html
<!doctype html>
<html>
<head>
 <meta charset="utf-8">
 <title>Contact - CodeTrack</title>
 <link rel="stylesheet" href="style.css">
</head>
<body>
 <h1>Contact Us</h1>
 <p>Email: mail@pravinmishra.in</p>
 <p>Website: https://thecloudadvisory.com/</p>
</body>
</html>
```

**Stage and commit changes:**

```bash
git add contact.html
git commit -m "feat(contact): add contact page with email and phone"
```

---

### Step 3 – Add Link to Contact Page in `index.html`

**Insert below existing playlist paragraph:**

```html
<p class="playlist-line">
   Want to reach us? Visit the
   <a href="contact.html">Contact Page</a>.
</p>
```

**Stage and commit changes:**

```bash
git add index.html
git commit -m "feat(nav): add Contact Page link to index.html"
```

---

### Step 4 – Verify Isolation (Switch Back to Main)

```bash
git checkout main
ls
```

* `contact.html` should **not** be present.
* Open `index.html` in browser → Contact Page link should not exist on main.

---

### Step 5 – Merge Feature Branch into Main

```bash
git merge feature/contact-page
```

**Verify:**

* `ls` → `contact.html` is now present
* Open `index.html` → Contact Page link works in browser

---

### Step 6 – Inspect History Graph

```bash
git log --oneline --graph --decorate --all
```

* Optional: Clean up feature branch:

```bash
git branch -d feature/contact-page
```

---

## Skills Gained

* Creating and switching between Git branches
* Adding feature-specific files and committing changes
* Merging feature branches into main
* Verifying changes in the live browser
* Inspecting commit history and understanding branch workflow
* Professional Git branching workflow and cleanup

---

## Assignment 8 – Setting Up GitHub for CodeTrack

**Objective:**
Create a GitHub repository for the CodeTrack project, explore key GitHub features, and prepare for pushing code and collaborating remotely.

---

### Step 1 – Create a GitHub Account

1. Go to [GitHub](https://github.com/) and click **Sign Up**
2. Enter email, password, and username
3. Complete verification and click **Create Account**
4. Access your **GitHub Dashboard**

**Expected Outcome:**
You now have a GitHub account and access to the dashboard.

---

### Step 2 – Explore GitHub Features

* Click **Explore** from the top menu
* Browse **Trending Repositories**
* Search for an open-source project (e.g., `theepicbook`)
* ⭐ Star at least one project
* Fork a repository to create your own copy

**Expected Outcome:**
You have explored GitHub, starred one project, and forked a repository.

---

### Step 3 – Update Your GitHub Profile

1. Click your profile picture → **Your Profile** → **Edit Profile**
2. Add a bio: “Cloud & DevOps Enthusiast | Learning Git & GitHub”
3. Optionally add location, company/school, and social links
4. Upload a profile picture
5. Save changes

**Expected Outcome:**
Your GitHub profile looks personalized and professional.

---

## Assignment 9 – Collaborating on Mini-Finance with GitHub

**Objective:**
Simulate a real-world collaborative GitHub workflow: authenticate, fork, clone, push, pull, and create Pull Requests (PRs) on the `mini_finance` project.

---

### Step 0 – Access Existing Mini-Finance Code

* Upstream repository: [https://github.com/pravinmishraaws/mini_finance](https://github.com/pravinmishraaws/mini_finance)
* Fork it to your GitHub account

---

### Step 1 – Fork & Authenticate

**Fork repository on GitHub**
**Authentication Options:**

**SSH (recommended):**

```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

* Copy contents of `~/.ssh/id_ed25519.pub` to GitHub → Settings → SSH & GPG Keys
* Test connection:

```bash
ssh -T git@github.com
```

**HTTPS alternative:**

```bash
git config --global credential.helper cache
```

**Expected Outcome:**
Forked repo and terminal authentication ready for Git operations.

---

### Step 2 – Clone Your Fork Locally

```bash
git clone git@github.com:yourusername/mini_finance.git
cd mini_finance
git remote -v
git remote add upstream https://github.com/pravinmishraaws/mini_finance.git
```

* Verify origin points to your fork and upstream points to original repo

---

### Step 3 – Create Feature Branch & Make Changes

```bash
git checkout -b feature-readme-update
```

* Open `README.md` and add:

> “This project demonstrates Git operations like clone, pull, push, PR—a hands-on Mini-Finance tool.”

```bash
git add README.md
git commit -m "docs: update README with assignment note"
```

---

### Step 4 – Pull From Upstream & Push to Origin

```bash
git fetch upstream
git checkout main
git merge upstream/main
git checkout feature-readme-update
git rebase main
git push -u origin feature-readme-update
```

**Expected Outcome:**
Feature branch available on GitHub under your fork.

---

### Step 5 – Create a Pull Request

1. Go to your fork on GitHub
2. Click **Compare & Pull Request**
3. Target: `pravinmishraaws/mini_finance:main` ← `feature-readme-update`
4. Title: `docs: update README with assignment note`
5. Description: “This PR adds a new section to the README explaining the project's purpose in the context of this GitHub assignment.”
6. Submit PR

**Expected Outcome:**
Pull Request created and visible on GitHub, ready for review and merge.

---

## Skills Gained

* Creating and configuring GitHub account and profile
* Exploring GitHub repositories, starring, and forking
* Forking repositories and authenticating via SSH/HTTPS
* Cloning, pushing, pulling, and rebasing
* Creating feature branches and committing changes
* Opening Pull Requests to propose changes on a remote repository
* Understanding collaboration workflow in real-world GitHub projects

---
