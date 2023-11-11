# Generating SSH Keys in Windows 10

## Generate SSH Key with OpenSSH Client

### Step 1: Verify OpenSSH Client Installation

1. Open Settings, click on Apps.
2. Under Optional Features, check if OpenSSH Client is listed.
3. If not listed, add it by clicking "Add a feature" and selecting OpenSSH Client.

### Step 2: Open Command Prompt

1. Press the Windows key.
2. Type `cmd`.
3. Right-click Command Prompt and select "Run as Administrator."

### Step 3: Use OpenSSH to Generate SSH Key Pair

1. In the command prompt, type: `ssh-keygen`
2. Press Enter to use the default location.
3. Enter a passphrase or press Enter to skip.
4. The system will generate keys; locate them in `C:\Users\your_username/.ssh`.
5. Public key: `id_rsa.pub`, Private key: `id_rsa`

# Generating SSH Keys in Linux

## Generating a new SSH key

1. Open Git Bash.
2. Paste the following command, replacing the email with your GitHub email:
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```
   If your system doesn't support Ed25519, use:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
3. Press Enter to accept the default file location.
4. Type a secure passphrase when prompted.

# Adding a new SSH key to your GitHub account

## About addition of SSH keys to your account

You can access and write data in repositories on GitHub.com using SSH (Secure Shell Protocol). After generating an SSH key pair, you need to add the public key to GitHub.com for SSH access.

1. Check for existing SSH keys.
2. Generate a new SSH key and add it to your machine's SSH agent.

## Adding a new SSH key to your account

1. Copy the SSH public key to your clipboard. Use the following command, replacing the filename if necessary:

   ```bash
   $ clip < ~/.ssh/id_ed25519.pub
   ```

   Notes:

   - On Windows Subsystem for Linux (WSL), you can use `clip.exe`. Otherwise, locate the hidden `.ssh` folder and copy the key manually.
   - On newer versions of Windows with PowerShell, you may use:
     ```bash
     $ cat ~/.ssh/id_ed25519.pub | clip
     ```

2. In the upper-right corner of any GitHub page, click your profile photo, then click **Settings**.

3. In the "Access" section of the sidebar, click **SSH and GPG keys**.

4. Click **New SSH key** or **Add SSH key**.

5. In the "Title" field, add a descriptive label for the new key (e.g., "Personal laptop").

6. Select the type of key: either authentication or signing.

7. In the "Key" field, paste your public key.

8. Click **Add SSH key**.

9. If prompted, confirm access to your GitHub account.

# Exercise

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

## Use the Git Workflow

1. Create a new file in the `git_test` folder called "hello_world.txt" with the command: `touch hello_world.txt`.

   ```bash
   # Create hello_world.txt using CLI
   touch hello_world.txt
   ```

2. Check the status of your repository by typing `git status` in your terminal. The output shows that `hello_world.txt` is in red, indicating it is not staged.

   ```bash
   # Check the status of the repo using CLI
   git status
   ```

3. Add `hello_world.txt` to the staging area using the command: `git add hello_world.txt`. This prepares the file for the commit.

   ```bash
   # Stage hello_world and check repo status again using CLI
   git add hello_world.txt
   ```

4. Type `git status` again. The output now shows `hello_world.txt` in green, indicating it is in the staging area.

   ```bash
   # Check repo status again using CLI
   git status
   ```

5. Make a commit with the message "Add hello_world.txt" using the command: `git commit -m "Add hello_world.txt"`. Then, check the status once more. The output should indicate "nothing to commit, working tree clean."

   ```bash
   # Commit hello_world and check repo status again using CLI
   git commit -m "Add hello_world.txt"
   git status
   ```

6. Check the commit history using git log:

   ```bash
   # Check repo commit history using CLI
   git log
   ```

7. The message "Your branch is ahead of 'origin/main' by 1 commit" indicates that your local branch has one more commit than the remote repository. This will be resolved when you push your changes.

## Modify a File or Two

1. Open `README.md` in your text editor of choice. In this example, we will open the directory in Visual Studio Code by using the command `code .` inside your repository.

   ```bash
   # Edit README using text editor
   code .
   ```

   **Note for MacOS users:** If your terminal reads “command not found: code,” you must head back to [Command Line Basics](#) and follow the instructions provided to allow this command to work.

2. Add “Hello Odin!” to line 3 of `README.md` and save the file with `Ctrl + S` (Mac: `Cmd + S`).

   **Edit README using text editor**

3. Go back to your terminal, or if you’re using Visual Studio Code, you can open the built-in terminal by pressing `Ctrl + \` (backtick). Then type `git status`. You’ll notice that `README.md` is now shown as not staged or committed.

   ```bash
   # Check repo status again using CLI
   git status
   ```

4. Add `README.md` to the staging area with `git add README.md`.

   ```bash
   # Stage README changes and check repo status again using CLI
   git add README.md
   ```

   **Can you guess what `git status` will output now?** `README.md` will be displayed in green text. That means `README.md` has been added to the staging area. The file `hello_world.txt` will not show up because it has not been modified since it was committed.

5. Open `hello_world.txt`, add some text to it, save it, and stage it. You can use `git add .` to add all files in the current directory and all subsequent directories to the staging area. Then, type `git status` once more, and everything should now be in the staging area.

   ```bash
   # Stage all other files in repo and check repo status again using CLI
   git add .
   ```

6. Finally, let’s commit all of the files that are in the staging area and add a descriptive commit message: `git commit -m "Edit README.md and hello_world.txt"`. Then, type `git status` once again, which will output “nothing to commit.”

   ```bash
   # Commit repo changes again and check repo status again using CLI
   git commit -m "Edit README.md and hello_world.txt"
   git status
   ```

7. Take one last look at your commit history by typing `git log`. You should now see three entries.

   ```bash
   # Check repo commit history using CLI
   git log
   ```

## Push Your Work to GitHub

1. Finally, let’s upload your work to the GitHub repository you created at the start of this tutorial.

   ```bash
   # Push changes to remote using CLI
   git push
   ```

   To be more specific, you can type `git push origin main`. Since you are not dealing with another branch (other than `main`) or a different remote, you can leave it as `git push` to save a few keystrokes.

   **Note:** If you receive a message that says “Support for password authentication was removed on August 13, 2021. Please use a personal access token instead,” at this point, you have followed the steps incorrectly and cloned with HTTPS, not SSH. Please follow these [steps to change your remote to SSH](#), then attempt to push to Github.

2. Type `git status` one final time. It should output “Your branch is up to date with ‘origin/main’. Nothing to commit, working tree clean”.

   ```bash
   # Check repo status again to confirm local repo is up to date with remote using CLI
   git status
   ```

3. When you reload the repository on GitHub, you should see the `README.md` and `hello_world.txt` files that you just pushed there from your local machine.

# Cheatsheet

Here's a reference list of commonly used Git commands:

### Commands related to a remote repository:

- `git clone git@github.com:USER-NAME/REPOSITORY-NAME.git`
- `git push` or `git push origin main`

### Commands related to the workflow:

- `git add .`
- `git commit -m "A message describing the changes"`

### Commands related to checking status or log history:

- `git status`
- `git log`

The basic Git syntax is `program | action | destination`.

For example:

- `git add .` is read as `git | add | .`, where the period represents everything in the current directory.
- `git commit -m "message"` is read as `git | commit -m | "message"`.
- `git status` is read as `git | status | (no destination)`.

# Git Best Practices

There's a lot to learn about using Git, but it's worth taking the time to highlight some best practices:

- Git is helpful when collaborating with others and when working independently.
- Two helpful best practices are atomic commits and meaningful commit messages.
- Consider atomic commits as changes related to only one feature or task for easier reversion and better messages.
- Write concise yet descriptive one-line summaries and, if needed, more detailed explanatory text for commit messages.
- Git commit message editor can be changed, especially if you prefer using Visual Studio Code.

Remember, mastering these practices will make you a more effective collaborator and developer.
