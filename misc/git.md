# Git

## Adding ssh key to github.com ##

#### Install ####

```shell
sudo pacman -S openssh
```

Create a ssh key pair

```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Then make create the config file to load the key during ssh usage: `${HOME}/.ssh/config`

```text
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519

```

Finally, add the `id_ed25519.pub` to the appropriate github account, and test the login with

```shell
ssh git@github.com
```

Remember to use the git url when cloning a repo.

## Creating a branch from another ##


Checkout the master branch:

```shell
git checkout master
```

Pull the latest changes from the remote repository:

```shell
git pull origin master
```

Create and switch to the new branch:


```shell
git checkout -b new-branch-name
```

Push the new branch to the remote repository:

```shell
git push -u origin new-branch-name
```


