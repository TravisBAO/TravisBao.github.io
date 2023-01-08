## Generating a new SSH key
You can generate a new SSH key on your local machine. After you generate the key, you can add the key to your account on GitHub.com to enable authentication for Git operations over SSH.

### 1. Open Git Bash
### 2. Paste the text below, substituting in your GitHub email address
    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
This creates a new SSH key, using the provided email as a label.

    Generating public/private rsa key pair.

When you're prompted to "Enter a file in which to save the key", you can press Enter to accept the default file location. Please note that if you created SSH keys previously, ssh-keygen may ask you to rewrite another key, in which case we recommend creating a custom-named SSH key. To do so, type the default file location and replace id_ssh_keyname with your custom key name.

    Enter file in which to save the key (/c/Users/YOU/.ssh/id_rsa):

### 3. At the prompt, type a secure passphrase. Empty is acceptable
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:

Then the output is:

    Your identification has been saved in /c/Users/You/.ssh/id_rsa.
    Your public key has been saved in /c/Users/You/.ssh/id_rsa.pub.
    The key fingerprint is:
    SHA256:jYynp3LKfikfG5kgKq3uo2SmkDpaH8f2KjHllJ4L9EI your_email@example.com
    The key's randomart image is:
    +---[RSA 4096]----+
    |                 |
    |                 |
    |       .         |
    |    E +o o       |
    |  .o.*..S .      |
    | + .=o==         |
    |=+o .=Xo.        |
    |X+ o++=B         |
    |@+..=O=..        |
    +----[SHA256]-----+

The new gereated ssh key is located in folder .ssh in above path.
- id_rsa
- id_rsa.pub

## Adding a new SSH key to your account

### 1. In the upper-right corner of any page, click your profile photo, then click **Settings**.

### 2. In the "Access" section of the sidebar, click  **SSH and GPG keys**.

### 3. Click **New SSH key** or **Add SSH key**.

### 4. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal laptop, you might call this key "Personal laptop".

### 5. Select the type of key: authentication.

### 6. Paste your key "id_rsa.pub" into the "Key" field.
![picture](img/ssh-key-paste-with-type.png)
### 7. Click **Add SSH key**