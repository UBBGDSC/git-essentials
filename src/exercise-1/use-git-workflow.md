# Git Workflow

## Use the Git Workflow

1. Create a new file in the `git_test` folder called "gdsc.txt" with the command: `touch gdsc.txt`.

   ```bash
   # Create gdsc.txt using CLI
   touch gdsc.txt
   ```

2. Check the status of your repository by typing `git status` in your terminal. The output shows that `gdsc.txt` is in red, indicating it is not staged.

   ```bash
   # Check the status of the repo using CLI
   git status
   ```

3. Add `gdsc.txt` to the staging area using the command: `git add gdsc.txt`. This prepares the file for the commit.

   ```bash
   # Stage gdsc and check repo status again using CLI
   git add gdsc.txt
   ```

4. Type `git status` again. The output now shows `gdsc.txt` in green, indicating it is in the staging area.

   ```bash
   # Check repo status again using CLI
   git status
   ```

5. Make a commit with the message "Add gdsc.txt" using the command: `git commit -m "Add gdsc.txt"`. Then, check the status once more. The output should indicate "nothing to commit, working tree clean."

   ```bash
   # Commit gdsc and check repo status again using CLI
   git commit -m "Add gdsc.txt"
   git status
   ```

6. Check the commit history using git log:

   ```bash
   # Check repo commit history using CLI
   git log
   ```

7. The message "Your branch is ahead of 'origin/main' by 1 commit" indicates that your local branch has one more commit than the remote repository. This will be resolved when you push your changes.
