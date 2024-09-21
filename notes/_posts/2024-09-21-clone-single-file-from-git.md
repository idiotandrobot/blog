---
title: Cloning a Single File from a Git Repository
tags:
- Git
Links:
- ["StackOverflow: Cloning single file from Git repository", https://stackoverflow.com/a/78875479]
- [Cloning a single file in Git, https://graphite.dev/guides/git-clone-single-file]
- [git sparse-checkout, https://git-scm.com/docs/git-sparse-checkout]
---
1. ```git init```
2. ```git remote add origin <remote-uri>```
3. ```git sparse-checkout set``` [^1]
4. ```git sparse-checkout add <file-path>```
5. ```git fetch origin main``` [^2]
6. ```git checkout main```

[^1]: This is a simpler sparse initialisation, but includes more files by default.
[^2]: This will download the complete repo history so make sure you have space.
