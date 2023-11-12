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
