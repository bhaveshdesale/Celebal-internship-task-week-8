#  Git Task - Internship Task

Author: **Bhavesh Desale**  
Role: Intern @ Celebal Technologies  
Date: July 2025  

---

## 1. Stage All Changes and Commit with a Meaningful Message

git add .
git commit -m "Add meaningful description of changes"


## 2. You have committed changes to a wrong branch. How would you move these commits to the correct branch?

### Step 1: Create and switch to the correct branch
git checkout -b correct-branch

### Step 2: Commits are carried to the new branch

### Step 3: Go back to the wrong branch and remove those commits
git checkout wrong-branch
git reset --hard HEAD~n    # Replace 'n' with the number of wrong commits

### Step 4: If already pushed, force push to remote
git push origin wrong-branch --force



## 3. You want to create a new branch, make changes, and push the branch to the remote repository. Outline the steps you would take to create a new branch, commit changes, and push the branch to GitHub.

### step 1: Update your main branch
git checkout main
git pull origin main

### step 2: Create and switch to a new feature branch
git checkout -b feature-branch-name

### step 3: Make your code changes

### step 4: Stage and commit your changes
git add .
git commit -m "Add feature: description"

### step 5: Push the branch to GitHub
git push origin feature-branch-name

## 4.You want to contribute to an open-source project hosted on GitHub.What are the steps you would follow to fork the repository, make changes, create a pull request, and collaborate with the original project?

### Step 1: Fork the repository using GitHub UI

### Step 2: Clone the forked repo
git clone https://github.com/your-username/project-name.git
cd project-name

### Step 3: Add the original repository as upstream
git remote add upstream https://github.com/original-owner/project-name.git

### Step 4: Create a new branch
git checkout -b my-feature-branch

### Step 5: Make changes, commit, and push
git add .
git commit -m "Fix: your fix or feature description"
git push origin my-feature-branch

### Step 6: Open a Pull Request from your branch to the original repository

## 5. You are working on a team project, and there are conflicts between your branch and the main branch. How would you resolve these merge conflicts? Provide the necessary commands and steps.


### Step 1: Checkout your branch
git checkout my-feature-branch

### Step 2: Merge changes from main
git fetch origin
git merge origin/main


## 6. You want to create a feature branch based on the latest changes in the main branch. What commands would you use to create a new branch and automatically switch to it, ensuring it's up to date with the latest changes from the main branch?

### Step 1: Checkout the main branch
git checkout main

### Step 2: Pull the latest changes
git pull origin main

### Step 3: Create and switch to a new branch
git checkout -b new-feature-branch


## 7. You have made a series of commits, but you realize that a change made several commits ago is causing issues in your application. How would you revert to a specific commit, discarding all changes made after that commit?

### Step 1: View your commit history
git log

### Step 2: Reset to the commit (replace <commit-hash> with the actual hash)
git reset --hard <commit-hash>

### Step 3: Force push to remote (if needed)
git push origin HEAD --force

## 8. You have accidentally deleted a file in your Git repository and committed the change. What commands would you use to restore the deleted file from the previous commit?

### Step 1: Restore the deleted file from previous commit
git checkout HEAD^ -- path/to/deleted-file

### Step 2: Add and commit the restored file
git add path/to/deleted-file
git commit -m "Restore accidentally deleted file"
