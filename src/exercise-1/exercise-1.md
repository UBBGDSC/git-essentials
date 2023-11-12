# Exercise 1

Welcome to the Git Essentials first exercise! This exercise is designed to guide you through essential Git processes using various operating systems and SSH keys. Below is a breakdown of the tasks you'll explore:

- [Generate SSH Keys in Windows](./generate-ssh-windows.md)
- [Generate SSH Keys in Linux](./generate-ssh-linux.md)
- [Add SSH Key](./add-ssh-key.md)
- [Create Repository](./create-repository.md)
- [Use Git Workflow](./use-git-workflow.md)
- [Modify Files](./git-modify-files.md)
- [Push work to Github](./push-work-to-github.md)
- [Cheatsheet](./cheatsheet.md)
- [Git best practices](./git-best-practices.md)

## Understanding SSH Keys

SSH keys are crucial for secure communication between your computer and remote servers. They act as a secure way to authenticate and establish secure connections, ensuring that data exchanged between systems is encrypted and protected from unauthorized access.

These keys provide a way to verify your identity without a password, making the authentication process more secure and convenient. They consist of a public key, which you share with others or services, and a private key, which remains exclusively on your machine.

GitHub strongly encourages SSH keys due to their security benefits and the limitations of HTTPS. While HTTPS is still an option, it can be less convenient due to frequent password prompts. SSH keys, on the other hand, offer a more secure and seamless way to authenticate without the need for constant password entry. Additionally, GitHub has set rate limits for unauthenticated use of their API, making SSH keys almost essential for smoother and more efficient interactions with their services.