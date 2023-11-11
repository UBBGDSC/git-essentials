# Exercise

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
