# SSH Key Authentication with GitHub

- Windows Users: Run this configuration within WSL Ubuntu.
- MacOS Users: Run this configuration using the Terminal.

## Create a Keypair

From your Terminal/WSL command-line, create a new RSA keypair:

```
ssh-keygen -t rsa
```

Follow the prompts.

1. If you already have an `id_rsa` keypair, you should name your new keys something different.
2. You do not need to set up a passphrase with this keypair.
3. `cd` into your `.ssh` directory and inspect the new keys.

## Share your public key with GitHub

1. `cat` out the contents of the public key and copy it to your clipboard

    ```
    cat ~/.ssh/id_rsa.pub
    ```
    
2. Go to your [**GitHub SSH Keys**](https://github.com/settings/ssh) page in Settings.
3. Click the **New SSH Key** button. Give it a name, and paste the contents of your public key into the "key" field.
4. Save new key. You can now run `git push` and `git pull` commands to GitHub without any further authentication.