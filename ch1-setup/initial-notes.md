# Some Initial Things About Git

## Porcelain and Plumbing

In Git, commands are divided into high-level ("porcelain") commands and low-level ("plumbing") commands.
The porcelain commands are the ones that you will use most often as a developer to interact with your code.
Some porcelain commands are:

- `git status`
- `git add`
- `git commit`
- `git push`
- `git pull`
- `git log`

We the use the following command to change the content of the file `~/.gitconfig`, the file
that actually stores global git configurations, we can even manually set configs like this:

```plaintext
[foo]
    bar: "hello git!"
```

We can later retrieve this value with `get` fashion:

```bash
$ git config get foo.bar
$ "hello, git!" # STDOUT
```

Doing this without directly editing the `~/.gitconfig` file would look like this:

```bash
$ git config set --global foo.bar "hello git!"
```

Whenever we create a new git repository with `git init`, which essentially just creates a hidden
directory inside the current directory called `.git`, a default branch is created, this default brach
is also a configuration.

`master` is the default of git and `main` is the default of github.
