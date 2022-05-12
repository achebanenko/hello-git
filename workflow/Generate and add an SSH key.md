# Generate and add an SSH key

https://docs.github.com/en/authentication/connecting-to-github-with-ssh  


## Checking for existing SSH keys

List the files in your .ssh directory, if they exist  
`$ ls -al ~/.ssh`

## Generating a new SSH key and adding it to the ssh-agent

`$ ssh-keygen -t ed25519 -C "your_email@example.com"`

`-C` flag sets a comment or label for identifying your SSH key (using your email is a common practice)  
`-t ed25519` sets the encryption algorithm for your SSH key  

If you are using a legacy system that doesn't support the Ed25519 algorithm, use  `$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`  

When you generate a new SSH key, you can name the new key to better identify its particular use, e.g. `ed25519_github`  
```
>Generating public/private ed25519 key pair.
>Enter a file in which to save the key (/Users/you/.ssh/id_ed25519):
$ /Users/you/.ssh/id_ed25519_github
```

## Adding or changing a passphrase  

You can change the passphrase for an existing private key without regenerating the keypair by typing the following command  
`$ ssh-keygen -p -f ~/.ssh/id_ed25519`  


## Adding your SSH key to the ssh-agent

1. Start the ssh-agent in the background  

```
$ eval "$(ssh-agent -s)"
> Agent pid 6730
```

Depending on your environment, you may need to use root access by running `sudo -s -H` before starting the ssh-agent, or you may need to use `exec ssh-agent bash` or `exec ssh-agent zsh` to run the ssh-agent.


2. Add your SSH private key to the ssh-agent and store your passphrase in the keychain  

`$ ssh-add --apple-use-keychain ~/.ssh/id_ed25519`

`--apple-use-keychain` flag is Apple’s standard version of ssh-add. This adds the passphrase of your SSH key automatically to the keychain so that you don’t have to enter the passphrase every time you make an SSH connection (previously, the flag was `-K`)  

If you have not set a passphrase for your key, you can `$ ssh-add ~/.ssh/id_ed25519`  

The `-A` flag is also deprecated and have been replaced by the  `--apple-load-keychain` flag.  

3. Set up the config file for some convenient options  

You will need to modify your ~/.ssh/config file to automatically load keys into the ssh-agent and store passphrases in your keychain  

```
$ open ~/.ssh/config
> The file /Users/you/.ssh/config does not exist.

$ touch ~/.ssh/config
```

If you chose not to add a passphrase to your key, you should omit the `UseKeychain` line

~/.ssh/config
```
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
```

If you see an error like this `/Users/USER/.ssh/config: line 16: Bad configuration option: usekeychain` add an additional config line to your `Host * section`
```
Host *
  IgnoreUnknown UseKeychain
```

## Adding a new SSH key to your GitHub account

Copy the SSH public key to your clipboard  
`$ pbcopy < ~/.ssh/id_ed25519.pub`  

Paste your key into field at Github > Settings > SSH and GPG keys  


## Testing your SSH connection

Attempts to ssh to GitHub  
`$ ssh -T git@github.com`  

You may see a warning  
The authenticity of host 'github.com (140.82.121.3)' can't be established. ED25519 key fingerprint is ...  

Verify that the fingerprint in the message you see matches GitHub's public key fingerprint https://docs.github.com/en/github/authenticating-to-github/githubs-ssh-key-fingerprints  
If it does, then type `yes`  

This will add Github as a known host in the known_hosts file in the /.ssh folder.  

```
> Hi username! You've successfully authenticated, but GitHub does not
> provide shell access.
```
