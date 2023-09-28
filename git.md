# Configure Git

## Opinionated Settings

```sh
git config --global init.defaultBranch main
git config --global pull.rebase true
```

## Personal

```sh
git config --global user.email "xu.justin.j@gmail.com"
git config --global user.name "Justin Xu"
```

## GitHub

> See also: [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) and [Testing your SSH connection](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection)

1. [Generate an SSH key.](./ssh.md#generate-a-default-ssh-key)
2. Go to [SSH and GPG keys](https://github.com/settings/keys) in GitHub settings and click `New SSH key`.
3. Copy the public key into the dialog and give the key a descriptive name.
4. Run `ssh -T git@github.com`, and type `yes` if an authenticity warning appears.
