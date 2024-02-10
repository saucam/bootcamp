# Introduction to Git

1. `git config`

   - The git config command is used to configure various aspects of Git, including user information,repository settings, and more.
     - For Example:
       `git config --global user.name "Your Name"`

2. `git clone <repository-url>`

   - Used for cloning repo locally

3. `git status`

   - to know the branch is up to date or not

4. `git add <file(s)> `

   - to stage the changes for next commit

5. `git commit -m "Your commit message here"`

   - To commit the changes in the branch locally

6. `git push origin <branch-name>`

   - to commit local changes into remote repo

7. `git pull origin <branch-name>`

   - to fetch and merge changes from remote repo

8. `git merge <branch-name>`

   - Merge changes from one branch to another

9. `git branch <branch-name>`

   - create a new brach

10. `git remote add upstream <original_repository_url>`

    - to add the Original Repository as a Remote

11. `git fetch upstream`

    - to fetch the changes from the original repository

12. `git checkout -b feature-branch-name origin/forked-branch-name`

    - Create a New Branch

13. `git branch -d feature-branch-name`

    - to delete local feature branch

14. `git push origin --delete feature-branch-name`

    - to delete the remote feature branch

15. `git remote -v`
    - to display a list of all remote repositories that your local Git repository is currently connected to,along with their URLs

## Two methods of integrating changes from one branch into another branch

## 1. Rebase

#### The basic steps to rebase a branch onto another branch in Git

- `git fetch origin`
  - Fetch Latest Changes
- `git checkout your-feature-branch`
  - Checkout the Branch to be Rebased
- `git rebase main`
  - Rebase onto the Target Branch
- `git rebase --continue`
  - After resolving the conflicts run this command to continue the rebase process.
- `git push origin your-feature-branch --force`
  - to push your changes to the remote repository.

## 2. Merge

#### The basic steps to rebase a branch onto another branch in Git

- `git checkout main`
  - ensure you're on the branch where you want to merge changes into
- `git pull origin main`
  - to pull the latest changes from the remote repository to ensure you're up to date before merging
- `git merge feature-branch`
  - to merge into the current branch
- `git merge --continue`
  - After resolving the conflicts run this command to continue the Merge process
- `git push origin main`
  - to push your changes to the remote repository.

### 3. For more detailed explanation [Checkout this](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)
