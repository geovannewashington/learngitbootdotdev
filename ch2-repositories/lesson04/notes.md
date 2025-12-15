# Commit

The usual stuff, we can create a commit with a message the following way:

```bash
$ git commit -m "commit message goes here"
```

Note: need to study conventional commits and semantic messages

Something new:

If we screw the message we can redo it with the `ammend` command.

```bash
$ git commmit --amend -m "A: add contents.md"
```

## About the --no-pager option

A pager is an editor that some applications open up by default when the output is too long for stdout.
The pager might be less, more, nano even vim...

The `--no-pager` option tells git to ignore that and just render things in the terminal directly.

## To see all the commits

We use the `log`

Example:

```bash
$ git log
```

The log has some subcommands itself: `-n <some_number>`
This way we can limit the amount of commits we see...

For a more visual representation we can use the following two options:

```bash
$ git log --graph --oneline
```
