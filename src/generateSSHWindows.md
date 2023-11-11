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
