# DevOps Micro Internship – Hands-On Portfolio

Welcome to my **DevOps Micro Internship Portfolio**.
This repository showcases all the **practical DevOps assignments, labs, and mini-projects** I completed during the DMI Cohort.
Each week focuses on a core DevOps skill, with short summaries, screenshots, and hands-on tasks.

This repo serves as both a **learning record** and a **professional portfolio** for recruiters.

---

## Weekly Progress Overview

| Week | Topic                               | Status         | Link                                                     |
| ---- | ----------------------------------- | -------------- | -------------------------------------------------------- |
| 00   | Internet, Networking & Tools Basics | ✅ Completed    | [Click here](./week-00-internet-networking-tools-basics) |
| 01   | Linux Basics & Shell Commands       | ✅ Completed    | [Click here](./week-01-aws-linux-setup/)                 |
| 02   | Git & GitHub Workflow               | ✅ Completed    | [Click here](./week-02-git-github/)                      |
| 03   | Networking Basics                   | 🔜 Coming Soon |                                                          |
| 04   | DevOps Lifecycle                    | 🔜 Coming Soon |                                                          |
| 05   | Agile, Scrum & Jira                 | 🔜 Coming Soon |                                                          |
| 06   | AWS Fundamentals                    | 🔜 Coming Soon |                                                          |
| 07   | Azure Fundamentals                  | 🔜 Coming Soon |                                                          |
| 08   | IaC – Terraform & CloudFormation    | 🔜 Coming Soon |                                                          |
| 09   | Ansible – Configuration Management  | 🔜 Coming Soon |                                                          |
| 10   | CI/CD Pipelines                     | 🔜 Coming Soon |                                                          |
| 11   | Docker & Containerization           | 🔜 Coming Soon |                                                          |
| 12   | Kubernetes                          | 🔜 Coming Soon |                                                          |


> **Legend:** ✅ Completed | 🔄 In Progress | 🔜 Coming Soon

---

## Repository Structure

```
devops-micro-internship-portfolio/
│
├── README.md
│
├── Achievements/
│   └── Certificate/
│
├── week-00-internet-networking-tools-basics/
│   ├── README.md
│   └── figures/
│       ├── task1/
│       ├── task2/
│       ├── task3/
│       └── task5/
│
├── week-01-aws-linux-setup/
│   ├── README.md
│   ├── Assignment-3-deployment.md
│   ├── Assignment-4-deployment.md
│   └── Figures/
│       ├── Assignment-3/
│       └── Assignment-4/
│
└── week-02-git-and-github/
    ├── README.md
    ├── Assignment-5/
    │   └── README.md
    ├── Assignment-6/
    │   └── README.md
    ├── Assignment-7/
    │   └── README.md
    ├── Assignment-8/
    │   └── README.md
    ├── Assignment-9/
    │   └── README.md
    └── Figures/
        ├── Assignment-5/
        │   ├── task1/
        │   ├── task2/
        │   └── task3/
        ├── Assignment-6/
        ├── Assignment-7/
        ├── Assignment-8/
        └── Assignment-9/
```

Each week folder includes:

* **What I did** – short summary of tasks completed
* **What I learned** – main takeaways
* **Commands / scripts (if any)**
* **Screenshots / proof of work**
* **Links to external references** (LinkedIn posts, documentation)

---

## Week 0 – Internet, Networking & Tools Basics

This week covers **fundamental concepts required before starting DevOps**, including:

* Using ChatGPT as a learning assistant
* Internet & networking concepts
* Application architecture (2-tier & 3-tier)
* Domain Name System (DNS) basics
* Visual Studio Code setup
* Sharing learning on LinkedIn

### Tasks Completed:

1. **Task 1 – ChatGPT as Learning Assistant**

   * Created a prompt to understand "What is a protocol in networking?"
   * Received a simplified response with a real-life example

2. **Task 2 – Internet & Networking**

   * Explained how a user accesses a website hosted in another country
   * Covered Packet Switching, IP Address, TCP/IP, HTTP/HTTPS

3. **Task 3 – Application Architecture**

   * Created diagrams for 2-tier and 3-tier architectures
   * Listed technologies for Frontend, Backend, Database

4. **Task 4 – Domain & DNS**

   * Explained DNS and connecting domain to IP using A Record

5. **Task 5 – Visual Studio Code Setup**

   * Installed VS Code, ran basic commands, customized theme

6. **Task 6 – LinkedIn Post**

   * Summarized all tasks and shared learning publicly
   * 🔗 **Post:** [Click here](https://www.linkedin.com/posts/anjana-muthunayake_devops-for-beginnersweek-0assignmentanjana-activity-7362170877381132290-rWjP)

---

## Skills Gained Through Week 0

* Understanding Internet and Networking basics
* Using ChatGPT for learning technical concepts
* Application architecture (2-tier & 3-tier)
* DNS fundamentals and domain mapping
* VS Code setup and terminal usage
* Professional documentation with screenshots
* Sharing knowledge publicly via LinkedIn

---

## Week 1 – Linux Basics & AWS Environment Setup

This week focuses on **setting up a cloud-based Linux environment using AWS**, deploying a React app, and practicing Linux administration tasks, including networking, process monitoring, and system information commands.

Perfect! You can update your Week 1 section like this, adding the links to your detailed assignment files for clarity and easy navigation:

---

### Assignments Completed:

1. **Assignment 2 – AWS Free Tier Account Setup**

   * Created an AWS account and explored the AWS Management Console
   * Learned Free Tier service limits and usage examples (EC2, S3, CloudFront)

2. **Assignment 3 – Deploy React App on Ubuntu VM Using Nginx**

   * Installed Node.js, npm, and Nginx on Ubuntu
   * Cloned and built the React app, deployed it to `/var/www/html`
   * Configured Nginx to serve the app from the VM’s public IP
   * Saved screenshots of deployment steps
   * **Detailed Steps & Explanation:** [Assignment-3-deployment.md](./week-01-aws-linux-setup/assignment-3-deployment.md)

3. **Assignment 4 – Linux Administration Practice**

   * Ran networking commands: `ifconfig`, `ping`, `netstat`, `dig`, `host`, `wget`
   * Monitored processes: `ps`, `pstree`, `kill`
   * Checked system information: `uname`, `uptime`, `who`, `free`, `df`, `du`
   * Captured command outputs as screenshots and added explanations
   * Added personal notes about processes vs services for better understanding
   * **Detailed Steps & Explanation:** [Assignment-4-linux-admin.md](./week-01-aws-linux-setup/assignment-4-linux-admin.md)

---

## Skills Gained Through Week 1

* Launching and managing AWS EC2 instances
* Deploying React applications on Ubuntu VMs using Nginx
* Linux system administration: networking, processes, memory, disk, users
* Troubleshooting and monitoring server performance and availability
* Capturing and documenting practical work with screenshots
* Understanding process vs service management in Linux

---

## Week 2 – Git & GitHub Workflow

This week covers Git fundamentals, repository management, and deploying a simple HTML/CSS application to AWS EC2.
It focuses on **tracking, staging, committing changes**, and practicing a basic DevOps workflow.

> **Bonus:** I also wrote a detailed article on Git concepts and workflow, explaining version control, branching, commits, and best practices.<br>
> **Read here:** [Git: Your Best Friend in Version Controlling](https://medium.com/@anjana-muthuanayake/git-your-best-friend-in-version-controlling-9773b87c75a1)

---

### Assignments Completed:

### **Assignment 5 – CodeTrack: Initial Git Setup (Local Only)**

**Objective:**
Set up Git on a local machine, initialize a repository, and configure Git username and email both locally and globally.

**High-Level Tasks Performed:**

* Created a new `CodeTrack` project folder and initialized it as a Git repository.
* Configured Git identity **locally** for the repository.
* Optionally configured Git identity **globally** for the system.
* Verified repository creation and configuration.

**Skills Gained:**

* Initializing Git repositories
* Configuring Git identity (local vs global)
* Understanding the `.git` folder structure
* Applying Git best practices before pushing to GitHub

**Detailed Steps & Explanation:** [Assignment 5 README](./week-02-git-github/Assignment-5-README.md)

---

### **Assignment 6 – Tracking and Staging Changes in a CodeTrack Project**

**Objective:**
Learn to create and track files in a Git repository, stage changes using `git add`, commit updates, and deploy a static web application to AWS EC2 using Nginx.

**High-Level Tasks Performed:**

* Verified Git installation and configuration
* Navigated to the `CodeTrack` project directory
* Created `index.html` and `style.css`, modified content, added optional `screenshots` folder
* Tracked, staged, and committed files with meaningful messages
* Viewed and verified commit history with `git log --oneline`
* Launched AWS EC2 instance, installed Nginx, and deployed the project
* Set proper ownership and permissions on web directory
* Accessed the deployed application via EC2 public IP

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
* Understanding staged vs unstaged changes
* Maintaining meaningful Git commit history
* Modifying and updating project files efficiently
* Deploying a static web application on AWS EC2 using Nginx
* Managing Linux file permissions and ownership
* End-to-end Git + deployment workflow

**Detailed Steps & Explanation:** [Assignment 6 README](./week-02-git-github/Assignment-6-README.md)<br>
**LinkedIn Post:**[Click here](https://www.linkedin.com/posts/anjana-muthunayake_devops-git-github-activity-7367255864790941697-mBtA?utm_source=share&utm_medium=member_desktop&rcm=ACoAADfZ4q8BKp1Dptghjo7ucKUr-n4bgkwr7Kg)

---

### **Assignment 7 – Branching Workflow: Add & Verify a Contact Page**

**Objective:**
Practice a professional Git **feature branching workflow** by creating a separate branch, adding a new feature (`contact.html`), committing changes incrementally, merging into the `main` branch, and verifying the merge using Git history visualization.

**High-Level Tasks Performed:**

* Started from an existing `CodeTrack` repository on the `main` branch.
* Created and switched to a feature branch: `feature/contact-page`.
* Added a new `contact.html` page with contact details.
* Updated `index.html` to include a navigation link to the Contact Page.
* Staged and committed changes with meaningful commit messages.
* Verified branch isolation to ensure `main` remained unchanged before merging.
* Merged the feature branch into `main`.
* Verified merged changes by opening files in a browser.
* Inspected Git history using a graphical commit log.
* Optionally deleted the feature branch after a successful merge.

**Key Commands Used:**

```bash
# Branching
git branch
git checkout -b feature/contact-page
git checkout main

# Staging & committing
git status
git add <file>
git commit -m "Descriptive commit message"

# Merging
git merge feature/contact-page

# Inspect history
git log --oneline --graph --decorate --all

# Cleanup
git branch -d feature/contact-page
```

**Skills Gained:**

* Working with feature branches in Git
* Isolating development work from the main branch
* Writing clear and structured commit messages
* Safely merging feature branches into `main`
* Understanding `HEAD`, branch pointers, and merge commits
* Visualizing Git history using commit graphs
* Following real-world Git workflows used in team and enterprise environments

**Detailed Steps & Explanation:** 
[Assignment 7 README](./week-02-git-github/Assignment-7-README.md)

---

### **Assignment 8 – Setting Up GitHub for CodeTrack**

**Objective:**
Create a GitHub repository for the CodeTrack project, explore core GitHub features, and prepare for pushing code and collaborating remotely.

**High-Level Tasks Performed:**

* Created a GitHub account and accessed the GitHub Dashboard.
* Explored the **Explore** section and browsed **Trending Repositories**.
* Used the search bar to find an open-source repository (`theepicbook`).
* Starred at least one repository to save for future reference.
* Forked a repository to create a personal copy.
* Optionally updated GitHub profile with a short bio, location, company/school, and profile picture.

**Skills Gained:**

* Creating and configuring a GitHub account
* Exploring GitHub repositories and trending projects
* Starring and forking repositories
* Understanding GitHub repository discovery and engagement features
* Preparing for remote collaboration using GitHub

**Detailed Steps & Explanation:** 
[Assignment 8 README](./week-02-git-github/Assignment-8-README.md)

---

### **Assignment 9 – Collaborating on Mini-Finance with GitHub**

**Objective:**
Learn to collaborate on a shared GitHub repository by **forking, cloning, creating branches, making changes, pushing updates, and submitting pull requests**, simulating a real-world team workflow.

**High-Level Tasks Performed:**

* Forked the **Mini-Finance** repository from GitHub to create a personal copy.
* Cloned the forked repository to the local machine.
* Configured **upstream** to track changes from the original repository.
* Created a feature branch: `feature/add-transaction-page`.
* Added new files and updated existing pages (`transaction.html`, `style.css`).
* Staged and committed changes with clear, descriptive messages.
* Pushed the feature branch to the forked repository on GitHub.
* Submitted a **Pull Request (PR)** to the original repository.
* Fetched updates from the upstream repository and merged them locally to stay in sync.
* Resolved minor merge conflicts during synchronization.
* Verified final changes and confirmed successful collaboration workflow.

**Key Commands Used:**

```bash
# Fork & clone
git clone https://github.com/<your-username>/mini-finance.git
cd mini-finance

# Configure upstream
git remote add upstream https://github.com/original-author/mini-finance.git
git fetch upstream
git pull upstream main

# Branching and development
git checkout -b feature/add-transaction-page
git add transaction.html style.css
git commit -m "feat: add transaction page with form validation"

# Push changes
git push origin feature/add-transaction-page

# Create PR on GitHub

# Sync fork with upstream
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

**Skills Gained:**

* Forking and cloning repositories for personal contributions
* Configuring upstream remotes to sync with original projects
* Feature branch workflow in a collaborative environment
* Writing clear and structured Git commit messages
* Pushing changes and submitting Pull Requests on GitHub
* Handling merge conflicts and keeping a repository in sync
* Understanding real-world team Git collaboration workflows

**Detailed Steps & Explanation:** [Assignment 9 README](./week-02-git-github/Assignment-9-README.md)

---

## Purpose of This Portfolio

This repository is created to:

* Document my practical DevOps learning journey
* Serve as a **DevOps portfolio** for hiring managers
* Help others by sharing clean, easy-to-understand DevOps labs
* Build hands-on skills required for real DevOps job roles

---

## 🔗 How to Navigate the Repo

1. Go to any **week folder**
2. Open the `README.md` inside
3. View tasks, explanations, screenshots, and scripts
4. Follow along or reuse the steps for learning

---

## Contact / Connect

If you'd like to connect or discuss DevOps, feel free to reach out:

* **GitHub:** [ANJANA-MM](https://github.com/ANJANA-MM)
* **LinkedIn:** [Anjana Muthunayake](https://www.linkedin.com/in/anjana-muthunayake/)
* **Medium:** [Anjana Muthunayake](https://medium.com/@anjana-muthuanayake)

---


