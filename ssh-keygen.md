# SSH

SSH (Secure SHell) is a way to connect from one computer to another using an encrypted network connection.

## Setting up SSH keys

Run `ssh-keygen` in your terminal.

```bash
root@5d41a3b58587:/# ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/root/.ssh/id_rsa):
Created directory '/root/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /root/.ssh/id_rsa.
Your public key has been saved in /root/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:FtqedMHKu/20neiXnamF02y+1e4WSkbSCjeUmUB7+9M root@5d41a3b58587
The key's randomart image is:
+---[RSA 2048]----+
|        .o. +    |
|         ..=     |
|        ..+..    |
|       + +.=.o   |
|      . S +.=    |
|       + + ..o=..|
|        +   +=.E*|
|         o . =O=+|
|        . .o=o+=+|
+----[SHA256]-----+
```

This sets up a **private key** (`.ssh/id_rsa`) and a **public key** (`.ssh/id_rsa.pub`).
**Don't move these out of your folder.** If you're asked to share your public key,

- make a copy of it.
- or open the `.pub` file and copy its contents.

**NEVER SHARE YOUR PRIVATE KEY**. Each time you're asked to produce or send an SSH key, only send your **public** key.

## Setting up your GitHub account with your public key

1. Go to your GitHub account's **Settings**.
2. Go to the **SSH and GPG keys** tab.
3. Select **New SSH key**.
4. Add a **Title** that makes sense. I usually set the machine name and date on which the key is created, so that it's easy to figure out which computer the key is for.
5. Copy the contents of your public key (usually at `$HOME/.ssh/id_rsa.pub` on macOS, and `%USER_PROFILE%\.ssh\id_rsa.pub` on Windows) and paste it into the **Key** field.
6. Select **Add SSH key** to complete the process.
