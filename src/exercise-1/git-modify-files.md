# Exercise

## Modify a File or Two

1. Open `README.md` in your text editor of choice. In this example, we will open the directory in Visual Studio Code by using the command `code .` inside your repository.

   ```bash
   # Edit README using text editor
   code .
   ```

   <details>
      **Note for MacOS users:** If your terminal reads “command not found: code,” you must head back to [Command Line Basics](#) and follow the instructions provided to allow this command to work.
   </details>

2. Add “Hello GDSC!” to line 3 of `README.md` and save the file with `Ctrl + S` (Mac: `Cmd + S`).

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
