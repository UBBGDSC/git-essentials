# Modify Files

## Modify a File or Two

1. Open `README.md` in your text editor of choice. In this example, we will open the directory in Visual Studio Code by using the command `code .` inside your repository.

   ```bash
   # Edit README using text editor
   code .
   ```

   <details>
   <summary>What if I don’t have Visual Studio Code?</summary>
      In that case, you can use any text editor of your choice. If you’re using Windows, you can use Notepad. If you’re using Mac, you can use TextEdit. If you’re using a smart fridge, how did you get that in here?
   </details>

2. Add “Hello GDSC!” to line 3 of `README.md` and save the file with `Ctrl + S` (Mac: `Cmd + S`).

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

   **Can you guess what `git status` will output now?** `README.md` will be displayed in green text. That means `README.md` has been added to the staging area.

5. Open `gdsc.txt`, add your name, occupation, a favorite hobby and something you dislike, save it, and stage it. You can use `git add .` to add all files in the current directory and all subsequent directories to the staging area. Then, type `git status` once more, and everything should now be in the staging area.

   Example  `gdsc.txt`
   ```txt
   Name: Armand
   Occupation: Master's Student in Software Engineering at Babes-Bolyai University
   Hobby: Playing Valorant
   Dislike: CFR
   ```

   ```bash
   # Stage all other files in repo and check repo status again using CLI
   git add .
   ```

6. Finally, let’s commit all of the files that are in the staging area and add a descriptive commit message: `git commit -m "Edit README.md and gdsc.txt"`. Then, type `git status` once again, which will output “nothing to commit.”

   ```bash
   # Commit repo changes again and check repo status again using CLI
   git commit -m "Edit README.md and gdsc.txt"
   git status
   ```

7. Take one last look at your commit history by typing `git log`. You should now see three entries.

   ```bash
   # Check repo commit history using CLI
   git log
   ```
