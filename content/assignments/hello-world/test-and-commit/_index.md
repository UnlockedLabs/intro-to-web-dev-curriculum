---
title: "Task 3: Test and Commit"
date: 2023-05-25T12:55:09-05:00
draft: false
weight: 3
originalAuthor: John Woolbright # to be set by page creator
originalAuthorGitHub: jwoolbright23 # to be set by page creator
reviewer: Rob Thomas
lastEditor: Sally Steuterman # update any time edits are made after review
lastEditorGitHub: gildedgardenia # update any time edits are made after review
lastMod: 2023-11-06 # UPDATE ANY TIME CHANGES ARE MADE
---

### Test Code Locally

Run the following command to test your newly updated code to see if it passes the tests:

```console
npm test
```

![Image of terminal window after running the npm test command](pictures/npm-test.png?classes=border)

If your tests fail, please revisit the previous section and double check that your `hello.js` file is formatted as expected. The test expects the output to be "Hello world!" precisely.

### Commit Your Changes

Now that your program prints `"Hello world!"` and the tests pass, you'll commit your code. Committing your code is part of a process called version control, which we'll get into in a later lesson. For now, open up your terminal and type in the following commands to follow along:

{{% notice blue Note "rocket" %}}
You will notice in the below commands that we are also running the `git status` command to check the current status of git after running commands. It is not required that we run a `git status` command but it does help illustrate what is happening.
{{% /notice %}}

1. `git status`
![Image of terminal window after running the git status command](pictures/git-status.png?classes=border)

1. `git add .`
![Image of terminal window after running the git add . command](pictures/git-add.png?classes=border)

1. `git commit -m "Commit message"`
![Image of terminal window after running the git commit command with "Hello World as commit message](pictures/git-commit.png?classes=border)

1. `git push origin main`
![Image of terminal window after running the git push command](pictures/git-push.png?classes=border)

You may make any number of commits to your solution. In most cases, you won't need to *commit and push* more than once, however. You can verify that your code runs the way we expect by running it and seeing the proper `"Hello world!"` message printed.