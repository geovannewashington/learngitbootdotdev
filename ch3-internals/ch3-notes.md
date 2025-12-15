# Some notes on chapter 03 - Internals

## About Commit Hashes

While commit hashes are derived from their content changes, there's also some other stuff that affects
the end hash. For example:

- The commit message
- The author's name and email
- The data and time

That is, in practice hashes are pretty much unique.

Git uses a cryptographic hash function called `SHA-1` to generate commit hashes.

## Git is made up of objects

Objects that stored in the `.git/objects` directory. A commit is just a type of object.

When you a commit, it's hash is used to generate a directory with the two initials digits of it.
For instance: Let's say that my hash is: `c86b9a73fad91f6adf43b469f3dc6409bcfa8b17`

A directory will be created at `.git/objects/c8/b9a73...`, this file is not readable because it's
hashed after all.

## The git cat-file command:

The git cat-file command is a "plumbing" command in Git used to inspect and output the contents or
metadata (type and size) of internal repository objects (blobs, trees, commits, and tags) identified by their SHA-1 hash
