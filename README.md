# Git Lab - Personal Info Page

Welcome to the Git Lab for beginners! This lab will help you understand fundamental Git concepts through hands-on practice.

## 📋 Lab Overview

In this lab, you'll practice Git by editing a simple HTML personal information page. Follow the commands below to learn Git basics.

---

## 🔑 Key Git Concepts

### 1. Repository
**What is it?** A repository (or "repo") is like a project folder that Git tracks. It contains all your files and the complete history of changes.

**Commands:**
```bash
# Initialize a new Git repository in current folder
git init

# Clone an existing repository from a URL
git clone <repository-url>

# Check the status of your repository
git status
```

---

### 2. Working Tree
**What is it?** The working tree is your current project directory where you edit files. It's the actual files you see and work with on your computer.

**Commands:**
```bash
# See which files have been modified in working tree
git status

# View differences in working tree files
git diff

# Discard changes in working tree for a specific file
git checkout -- <filename>
```

---

### 3. Staging Area
**What is it?** The staging area (also called "index") is like a preview of your next commit. You add files here before committing them.

**Commands:**
```bash
# Add a specific file to staging area
git add <filename>

# Add all changed files to staging area
git add .

# Add all HTML files to staging area
git add *.html

# Remove a file from staging area (keep changes in working tree)
git reset <filename>

# View what's in the staging area
git status
```

---

### 4. Commit
**What is it?** A commit is like taking a snapshot of your project at a specific point in time. Each commit has a message describing what changed.

**Commands:**
```bash
# Commit staged changes with a message
git commit -m "Your commit message here"

# Add all changes and commit in one command
git commit -am "Your commit message"

# View commit history
git log

# View commit history with one line per commit
git log --oneline

# View last 5 commits
git log -5

# View detailed information about a specific commit
git show <commit-hash>
```

---

### 5. Branch
**What is it?** A branch is like a parallel version of your project. It allows you to work on new features without affecting the main code.

**Commands:**
```bash
# List all branches (* shows current branch)
git branch

# Create a new branch
git branch <branch-name>

# Switch to a different branch
git checkout <branch-name>

# Create and switch to a new branch in one command
git checkout -b <branch-name>

# Delete a branch
git branch -d <branch-name>

# Force delete a branch (if it has unmerged changes)
git branch -D <branch-name>

# Rename current branch
git branch -m <new-branch-name>
```

---

### 6. Merge
**What is it?** Merging combines changes from one branch into another. This is how you bring your work from a feature branch back into the main branch.

**Commands:**
```bash
# Merge a branch into your current branch
git merge <branch-name>

# Merge with a commit message
git merge <branch-name> -m "Merge message"

# Abort a merge if there are conflicts
git merge --abort

# View branches that have been merged into current branch
git branch --merged

# View branches that haven't been merged
git branch --no-merged
```

---

### 7. Pull Requests
**What is it?** A pull request (PR) is a way to propose changes and ask others to review your code before merging. This is commonly used on platforms like GitHub, GitLab, and Bitbucket.

**Commands:**
```bash
# Push your branch to remote repository (required before creating PR)
git push origin <branch-name>

# Set upstream and push
git push -u origin <branch-name>

# After PR is merged on GitHub, update your local main branch
git checkout main
git pull origin main

# Delete local branch after PR is merged
git branch -d <branch-name>

# Delete remote branch after PR is merged
git push origin --delete <branch-name>
```

**Note:** Pull requests are created through the web interface (GitHub, GitLab, etc.), not directly through Git commands.

---

## 🚀 Getting Started with This Lab

### Step 1: Initialize Repository
```bash
# Navigate to the project folder
cd /path/to/dass

# Initialize Git repository
git init

# Check status
git status
```

### Step 2: Make Your First Commit
```bash
# Add all files to staging area
git add .

# Commit the files
git commit -m "Initial commit: Add personal info page"

# View your commit
git log
```

### Step 3: Edit Personal Information
1. Open `index.html` in a text editor
2. Update your personal information:
   - Change "Your Name Here" to your actual name
   - Update email, phone, college, department
   - Modify your interests

### Step 4: Commit Your Changes
```bash
# Check what changed
git status
git diff

# Stage the changes
git add index.html

# Commit with a descriptive message
git commit -m "Update personal information"
```

### Step 5: Practice Branching
```bash
# Create a new branch for adding hobbies
git checkout -b add-hobbies

# Edit index.html to add more hobbies
# (Make your changes in the editor)

# Commit your changes
git add index.html
git commit -m "Add hobbies section"

# Switch back to main branch
git checkout main

# View all branches
git branch
```

### Step 6: Merge Your Branch
```bash
# Make sure you're on main branch
git checkout main

# Merge the add-hobbies branch
git merge add-hobbies

# View the result
git log --oneline
```

### Step 7: Create Another Feature Branch
```bash
# Create branch for styling changes
git checkout -b improve-styling

# Edit style.css to change colors or layout
# (Make your changes)

# Stage and commit
git add style.css
git commit -m "Improve page styling"

# Go back to main
git checkout main

# Merge the changes
git merge improve-styling
```

---

## 📝 Common Git Workflow

Here's the typical workflow you'll use:

```bash
# 1. Check current status
git status

# 2. Make changes to your files
# (Edit files in your editor)

# 3. View what changed
git diff

# 4. Stage your changes
git add <filename>
# or add all changes
git add .

# 5. Commit with a message
git commit -m "Describe what you changed"

# 6. View history
git log --oneline
```

---

## 🔄 Working with Remote Repositories (GitHub)

```bash
# Add a remote repository
git remote add origin <repository-url>

# View remote repositories
git remote -v

# Push commits to remote
git push origin main

# Pull latest changes from remote
git pull origin main

# Clone a repository
git clone <repository-url>
```

---

## 💡 Tips for Beginners

1. **Commit often**: Make small, frequent commits rather than large ones
2. **Write clear messages**: Describe what you changed and why
3. **Check status frequently**: Use `git status` to see what's happening
4. **Use branches**: Keep your main branch stable and experiment in feature branches
5. **Pull before push**: Always pull latest changes before pushing your work

---

## 🎯 Lab Exercises

### Exercise 1: Basic Operations
- [ ] Initialize a Git repository
- [ ] Add and commit the initial files
- [ ] Make changes to your personal info
- [ ] Stage and commit the changes

### Exercise 2: Branching
- [ ] Create a new branch called `add-skills`
- [ ] Add a new section for skills in index.html
- [ ] Commit your changes on this branch
- [ ] Switch back to main branch
- [ ] Merge the `add-skills` branch

### Exercise 3: More Practice
- [ ] Create another branch for adding a photo section
- [ ] Make your changes and commit
- [ ] Merge back to main
- [ ] View your complete commit history

---

## 📚 Additional Resources

- [Git Official Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

---

## 🆘 Need Help?

If you get stuck, remember:
- `git status` - Shows current state
- `git log` - Shows commit history
- `git help <command>` - Shows help for a specific command
- Ask your instructor or peers!

---

**Happy Learning! 🎉**
