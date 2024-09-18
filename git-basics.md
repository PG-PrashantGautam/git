### What is Git?

Git is a **distributed version control system**. It allows multiple people to work on a project (usually code) simultaneously while tracking changes. It helps manage project versions and provides features to collaborate, roll back changes, and handle conflicts when multiple contributors are working together.

### Key Concepts in Git:

1. **Repository (Repo):**
   - A **repository** is a directory or storage space where your project files are stored, along with the entire history of changes made to those files.
   - You can create a repository on your local machine or clone (copy) one from a remote server like GitHub, GitLab, or Bitbucket.

2. **Commit:**
   - A **commit** is a record of changes made to the files in the repository. Think of it like taking a snapshot of your project at a specific moment in time.
   - Every commit has a unique **ID** (called a **SHA hash**) and a **commit message** that describes what changes were made.

3. **Branch:**
   - A **branch** is a pointer to a specific commit, allowing you to work on different features or versions of your project without affecting the main project (usually the `main` or `master` branch).
   - The most common branches are `main` (or `master`), which holds the production code, and feature branches, which developers use to work on new features.

4. **Merge:**
   - **Merging** is the process of integrating changes from one branch into another. It's typically used to incorporate changes from a feature branch into the `main` branch.

---

### Basic Git Workflow

Here’s a simple Git workflow to understand how it works:

1. **Install Git (if not installed):**
   - For Ubuntu:
     ```bash
     sudo apt update
     sudo apt install git
     ```

2. **Configure Git:**
   Set up your Git username and email (this information will be associated with your commits).
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

3. **Create a Git Repository:**
   You can initialize a new Git repository in your project directory:
   ```bash
   git init
   ```

4. **Check Git Status:**
   View the status of your working directory:
   ```bash
   git status
   ```

5. **Add Files to Staging:**
   Add specific files or all modified files to the staging area (files to be included in the next commit).
   ```bash
   git add <file_name>
   # Or add all files
   git add .
   ```

6. **Commit Changes:**
   Once files are staged, you can commit them:
   ```bash
   git commit -m "Your commit message"
   ```

7. **Check Log of Commits:**
   To view the history of commits:
   ```bash
   git log
   ```

   To view a fixed number of commits in the `git log`, you can use the `-n` option followed by the number of commits you want to display. 

   ### Syntax:
   ```bash
   git log -n <number_of_commits>
   ```

   ### Example:
   To view the last 5 commits:
   ```bash
   git log -n 5
   ```

   This will show the most recent 5 commits in the log.

   ### Additional Options:
   - You can also use `--oneline` to display a more concise log:
    ```bash
   git log -n 5 --oneline
    ```
   This will show each commit in a single line with the commit hash and message.

8. **Create a Branch:**
   Create a new branch to work on a feature or issue:
   ```bash
   git branch <branch_name>
   ```
   *To list all the branches in your Git repository, use the following command*

   ```bash
   git branch 
   ```
   *To List All Remote and Local Branches*

   ```bash
   git branch -a
   ```

9. **Switch to Another Branch:**
   Switch to the branch you just created:
   ```bash
   git checkout <branch_name>
   ```

10. **Merge Branches:**
    Once your work is done, switch back to the `main` branch and merge the changes from your feature branch:
    ```bash
    git checkout main
    git merge <branch_name>
    ```

---

### Example Git Workflow

1. **Initialize a Git Repository:**
   ```bash
   mkdir my_project
   cd my_project
   git init
   ```

2. **Create a file and add it to the repository:**
   ```bash
   echo "Hello, Git!" > hello.txt
   git add hello.txt
   git commit -m "Add hello.txt file"
   ```

3. **Create a new branch and modify the file:**
   ```bash
   git branch feature_branch
   git checkout feature_branch
   echo "This is a feature!" >> hello.txt
   git add hello.txt
   git commit -m "Update hello.txt with feature"
   ```

4. **Merge the feature branch into `main`:**
   ```bash
   git checkout main
   git merge feature_branch
   ```

---

This is just the foundation of using Git. As you become more familiar with the basics, we can move into advanced topics such as:

- **Cloning repositories**
- **Push/pull to/from remote repositories**
- **Handling merge conflicts**
- **Git workflows (GitFlow, Forking, etc.)**
