# Pushing to Remote Repository

## Push Your Work to GitHub

1. Finally, let’s upload your work to the GitHub repository you created at the start of this tutorial.

   ```bash
   # Push changes to remote using CLI
   git push
   ```

   To be more specific, you can type `git push origin main`. Since you are not dealing with another branch (other than `main`) or a different remote, you can leave it as `git push` to save a few keystrokes.
   <details>
      <summary>“Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.”</summary>
      **Note:** If you receive a message that says “Support for password authentication was removed on August 13, 2021. Please use a personal access token instead,” at this point, you cloned with HTTPS, not SSH.
   </details>
   <details>
   <summary> What is origin?</summary>
      The origin is the default name given to the remote repository you cloned from. You can view the remote repositories using `git remote -v`.
   </details>


2. Type `git status` one final time. It should output “Your branch is up to date with ‘origin/main’. Nothing to commit, working tree clean”.

   ```bash
   # Check repo status again to confirm local repo is up to date with remote using CLI
   git status
   ```

3. When you reload the repository on GitHub, you should see the `README.md` and `gdsc.txt` files that you just pushed there from your local machine.
