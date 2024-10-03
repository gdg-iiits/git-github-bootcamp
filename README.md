
### Start with a small talk on what is hacktoberfest, registration video.(more on it below)
As a developer, one of the most important skills one must learn is the art of managing and working with large codebases while collaborating with other developers, ensuring the code you write is well documented and free of bugs.<br/>Open source programs allow young developers to learn this specific art, and with Hacktoberfest officially kicking off this month, there's no better opportunity to have this session on Git and GitHub to help you take your first steps into the world of open source with us.<br/>More about open source programs will be discussed in detail during this three-day bootcamp. For now, let’s start with the fundamentals.

# 1. Introduction to Version Control Systems (VCS)
### Definition and Importance
A **Version Control System (VCS)** is a tool that helps track changes to files over time. It allows multiple people to collaborate on a project, maintain version history, and revert to previous states if needed. VCS is crucial for software development because:
- It enables collaboration among team members.
- Keeps a history of changes.
- Facilitates the rollback of mistakes.
- Tracks and manages code across branches.
- Other examples include Subversion(centralized VCS), Mercurial etc.

### Why Git?
Git is one of the most popular VCS, known for its **distributed** nature. Key advantages of Git include:
- **Speed**: Git is very fast compared to other VCS.
- **Distributed**: Every developer has a full copy of the repository, allowing for offline work.
- **Efficient Branching**: Git provides lightweight and flexible branching and merging strategies.

---

# 2. Brief on Git Installation
### Pre-installed on Ubuntu
On most Ubuntu systems, Git comes pre-installed, so no installation steps are required. You can verify this by running the following command:
```bash
git --version
```
### Installing Git on Windows and Linux
To install Git on Windows, you can follow these steps:
1. Visit the official Git website at [https://git-scm.com/downloads](https://git-scm.com/downloads).
2. Download the Git installer for Windows.
3. Run the installer and follow the on-screen instructions.
4. Once the installation is complete, you can open a command prompt and verify the installation by running the following command:
```bash
git --version
```
For Linux systems, you can use the package manager to install Git. For example, on Ubuntu, you can run the following command:
```bash
sudo apt-get install git
```

---

# A little bit of setup
### Git Config Basics

To set your username and email in Git, use the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

This is the name that shows up in commits so that git can identify who did what commit.
You can also set it locally for a repo, using the --local flag instead of the --global flag.

# 3. Basic Git Commands

### Creating a Repository
```bash
git init
```
Initializes a new Git repository in the current directory.

### Cloning a Repository
```bash
git clone <repository_url>
```
Clones an existing repository from a **remote location** (Like github, which we will look at later on).

### Checking Status
```bash
git status
```
Displays the state of the working directory and the staging area.

### Adding Changes
```bash
git add <file>
```
Stages file changes for the next commit.

### Committing Changes
```bash
git commit -m "message"
```
The below can be used too, but it will open a prompt and ask you to type the "message"

```bash
git commit
```
Commits staged changes with a descriptive message.

### Viewing History
```bash
git log
```
Shows the commit history of the repository.

---

### Removing files
```bash
   git rm file_name
```
Git untracks the file and also removes it from the git repository/directory. 
# How to Write Good Commit Messages

- **Subject Line**: Use a concise summary (max 50 characters) in the **imperative mood** (e.g., "Add new feature").
- **Body (optional)**: Include detailed explanation if needed:
    - Explain the "why" behind the change.
    - Describe the impact or reasoning.
- **Issue References**: Link to related issues using `Fixes #<issue-number>` or `Closes #<issue-number>` to automatically close them.
- **Formatting**:
    - Keep subject line under 50 characters.
    - Use present tense, imperative mood.


# 4. Hands-On Activity

### Creating a Repository
Guide:
1. Create a new directory.
2. Navigate to the directory.
3. Initialize a new Git repository using `git init`.

### Making Changes
1. Create or modify a file in the repository.
2. Use `git add <file>` to stage the changes.
3. Use `git commit -m "your message"` to commit the changes.
4. View the commit history with `git log`.

---

# 5. Advanced Git Concepts

### Branches
**Branches** allow developers to work on separate features without affecting the main codebase. 

#### Creating a Branch
```bash
git branch <branch_name>
```

#### Switching Branches
```bash
git checkout <branch_name>
```

#### Merging Branches
```bash
git merge <branch_name>
```
Merges changes from the specified branch into the current branch.
**We will face issues with this merge part later, don't worry for now**

### Pulls and Fetches
- **git fetch**: Retrieves changes from the remote repository without applying them.
- **git pull**: Fetches and merges changes from the remote repository into the current branch.

### Rollbacks
- **git revert**: Reverts a specific commit by creating a new commit that undoes the changes.
- **git reset**: Moves the current branch pointer to a previous commit, potentially discarding commits.

---

# 6. Merge Conflicts and Resolution

### What are Merge Conflicts?
Merge conflicts occur when Git cannot automatically merge changes from different branches. This usually happens when the same lines of code are modified differently in each branch.

### Resolving Conflicts
1. Open the conflicting files and manually resolve the differences.
2. After resolving, use `git add` to mark the conflict as resolved.
3. Finally, commit the resolved changes using `git commit`.

---

# Conclusion

### Recap
- **Version Control** is essential for collaboration and code management.
- **Git** provides fast, distributed version control with efficient branching.
- You’ve learned basic and advanced Git commands, including handling merge conflicts.




# Part 2- Introduction to GitHub and Workflow(Also hacktoberfest)

## 0. Introdunction to Hacktoberfest
**Hacktoberfest** is an event that happens every october, to celebrate the world of open source. Hope you have watched the video to register.
- You must do 4 pull requests to be said to participate
- They used to give goodies, not anymore
- Great chance to enhance your git and github skills. also beneficial from google summer of code point of view
- There are repos that have the hacktoberfest tag on them, search for those and try to contribute to those.
- You need not code, there are no-code contributions too, as a part of the readme project. [Click here for more](Refer https://hacktoberfest.com/participation/#low-or-non-code)


## 1. Introduction to GitHub

### What is GitHub?
**GitHub** is a web-based platform that provides hosting for Git repositories. It is used for version control and collaboration, allowing developers to work together on projects from anywhere. Key features of GitHub include:
- Hosting Git repositories.
- Enabling collaboration through pull requests and issues.
- Providing tools for continuous integration (CI) and project management.
- Alternatives to github include, gitlab, sourceforge, codeberg

### GitHub Workflow
A typical workflow on GitHub includes:
1. **Repositories**: A central place where the project files are stored.
2. **Branches**: Used to work on different features or fixes without affecting the main codebase.
3. **Commits**: Snapshots of changes made to the code.
4. **Pull Requests**: A request to merge changes from one branch into another.

---

## 2. GitHub Workflow

### Creating a Repository
- On GitHub, click the "New" button in the repository section to create a new repository.
- Give the repository a name, optionally add a README, and click "Create Repository".

- If you are working with someone else's repo and you are not a collaborator in it, you are required to fork it before cloning it.
- A Github fork creates a personal copy of a repository, allowing you to make changes and propose updates via pull requests.

### Cloning a Repository
```bash
git clone <repository_url>
```
- Clone the repository to your local machine to start working on it.

### Making Changes
- Modify files in your local repository, then stage and commit the changes using Git.
```bash
git add <file>
git commit -m "Your message"
```

### Creating a Branch
```bash
git branch <branch_name>
git checkout <branch_name>
```
- Create and switch to a new branch where you will make changes.

### Pushing Changes
```bash
git push origin <branch_name>
```
- Push your changes to the new branch on GitHub.

### Creating a Pull Request
- On GitHub, open the repository and click the "New Pull Request" button.
- Select the branch you want to merge from and the branch you want to merge into (e.g., from `feature-branch` to `main`).
- Provide a title and description for the pull request and submit it for review.

### 3.Working with Remote on local machine
- Clone the repo you want to work with onto your local machine.
### Fetching from remote
```bash
git fetch
```
- In Git, fetching means getting the latest changes from a remote repository (like GitHub) to your local repository, but without merging them into your work yet
  
```bash
   git remote show origin
```
- This command is used to check if the local machine is upto date with the changes/commits in the remote repo
- If the local machine/repo is not upto date with the changes, it shows a message telling 'local out of date'
- Then use the git merge command to merge the new changes of the remote to the local machine.
```bash
git pull
```
- It is a command which is nothing but a combination of both fetch and merge commands
- It fetches the changes from the remote and merges it with the local repo.

### Steps to Push a Local Repository to a New Remote Repository on GitHub

**Initialize your local repository** (if you haven't already):
   ```bash
   git init

Add your files to the staging area:
``` bash
git add .
```

Commit your changes:
```git commit -m "Initial commit"```

Add the remote repository. You can find the URL of your new GitHub repository on the GitHub website. It looks like https://github.com/username/repo.git:
```git remote add origin https://github.com/username/repo.git```

Push your changes to the remote repository:
```git push -u origin main```

This will push all your local commits to the remote repository on GitHub.
---


## 4. Hands-On Activity

### Creating Pull Requests
1. Create a branch in a repository and push changes to it.
2. Submit a pull request to merge your changes into the `main` branch.

### Review and Merge
1. Review the submitted pull requests.
2. Test the changes and leave comments if necessary.
3. Merge the pull request into the `main` branch.

---

## 5. Managing Projects on Git and GitHub

### Project Boards
GitHub **Project Boards** help organize and manage your project tasks.<br/>Github Project Boards allows team members to track their daily tasks, create various task management systems like To-Do Lists,Kanban boards,Sprint sessions and many more.<br/>
Roadmaps can be built and linked with other projects as well to ensure a smooth workflow and planned structure of tasks over a long term.

### Issues and Labels
**Issues** are used to track bugs, enhancements, and other project tasks.<br/>You can use **Labels** to categorize issues based on their priority or type (e.g., bug, enhancement).<br/>
Issues can be assigned on **Project Boards** and can also be assigned to multiple developers with their seperate Task Cards to ensure proper management and efficiency.

### Milestones
Set **Milestones** to track the progress of your project and measure what’s been accomplished toward a release or a big goal.

### Collaborators and Permissions
You can invite **Collaborators** to your repository and manage their permissions by going to the repository settings and selecting "Manage Access."


# Some programs to discuss

**Google Summer of Code (GSoC)** is a global program that brings new contributors into open source software development. Launched in 2005, GSoC pairs students and beginners with mentoring organizations to work on real-world coding projects. Participants gain valuable experience, improve their coding skills, and contribute to open source communities. The program runs annually, offering stipends to contributors who successfully complete their projects. GSoC has helped thousands of developers kickstart their careers and foster a passion for open source. By participating, contributors not only enhance their technical skills but also become part of a global community dedicated to collaborative software development.

**Google Solution Challenge** is an annual competition organized by Google Developer Student Clubs (GDSC) on behalf of google. The challenge invites university students to develop innovative solutions using Google technologies to address one or more of the United Nations' 17 Sustainable Development Goals (SDGs). Participants work in teams to create impactful projects that tackle global issues such as poverty, climate change, and inequality. The top teams receive mentorship from Google experts, swag, and cash prizes. The challenge not only enhances participants' technical skills but also fosters a sense of community and purpose among young developers.

**Major League Hacking (MLH)** is a global community that empowers hackers through various programs, including hackathons, workshops, and the MLH Fellowship. The **MLH Fellowship** is a 12-week remote internship alternative where participants work on real-world projects, collaborate in small groups, and receive mentorship from experienced developers. Fellows can choose from different tracks such as Open Source, Explorer, and Externship, each offering unique learning experiences. The program aims to bridge the gap between academic learning and professional software development, providing valuable hands-on experience. MLH also offers stipends to help offset living and educational expenses during the fellowship.



### QandA
Feel free to ask any questions or clarifications.
