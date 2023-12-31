# Adding a new SSH key to your GitHub account

1. Copy the SSH public key to your clipboard. Use the following command, replacing the filename:

   ```bash
   $ clip < ~/.ssh/{filename}.pub
   ```

   <details>
   <summary>Alternative for Windows users</summary>
   On Windows Subsystem for Linux (WSL), you can use `clip.exe`. Otherwise, locate the hidden `.ssh` folder and copy the key manually.

   On newer versions of Windows with PowerShell, you may use:
      ```bash
      $ cat ~/.ssh/{filename}.pub | clip
      ```

   Alternatively, you can just open the file and copy its contents.  
   </details>

2. In the upper-right corner of any GitHub page, click your profile photo, then click **Settings**.

   <img src="images/settingsLocation.png" alt="Setting Location" height="400"/>

3. In the "Access" section of the sidebar, click **SSH and GPG keys**.

   <img src="images/SSHandGPGkeysLocation.png" alt="Setting Location" height="400"/>

4. Click **New SSH key** or **Add SSH key**.

5. In the "Title" field, add a descriptive label for the new key (e.g., "Personal laptop").

6. Select the type of key: either authentication or signing.

7. In the "Key" field, paste your public key.

8. Click **Add SSH key**.

9. If prompted, confirm access to your GitHub account.
