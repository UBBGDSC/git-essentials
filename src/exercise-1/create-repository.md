# Create a Repository

## Before You Start

1. Ensure you have Git version 2.28 or later. Check your version with: `git --version`
2. Set your local default Git branch to `main` by running: `git config --global init.defaultBranch main`

## Create the Repository on GitHub

3. Create a GitHub account if you haven't already.
4. Click the "+" button on GitHub to create a new repository.
5. Name it "git-test," check "Add a README file," and click "Create repository."

## Clone the Repository to Your Local Machine

6. Click the green "Code" button on your GitHub repository.
7. Select the SSH option, copy the displayed URL.
8. Open your terminal and create a directory named "repos" in your home folder: `mkdir ~/repos`
9. Move into the new directory: `cd ~/repos`
10. Clone the repository using the copied URL: `git clone git@github.com:USER-NAME/REPOSITORY-NAME.git`
11. Verify the connection: `cd git_test` and `git remote -v`

You've successfully connected your GitHub repository to your local machine. The remote connection is named "origin," a default convention.
