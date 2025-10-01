---
title: "Task 1: Getting Started"
date: 2023-09-26T13:52:51-05:00
draft: false
weight: 1
originalAuthor: Sally Steuterman # to be set by page creator
originalAuthorGitHub: gildedgardenia # to be set by page creator
reviewer: # to be set by the page reviewer
reviewerGitHub: # to be set by the page reviewer
lastEditor: # update any time edits are made after review
lastEditorGitHub: # update any time edits are made after review
lastMod: # UPDATE ANY TIME CHANGES ARE MADE
---

## Code Together

Coding together allows you to work as a team so you can build bigger projects
faster.

In this studio, we will practice the common Git commands used when
multiple people work on the same code base.

You and a partner will code in tag-team shifts. By the end of the studio, you
should have a good idea about how two people can work on the same code at the
same time. You will learn how to:

1. Quickly add code in pull + push cycles *(Important! This is the fundamental
   process!)*
1. Create a *branch* in Git
1. Create a *pull request*
1. Resolve merge conflicts (which are not as scary as they sound)

This lesson reinforces:

1. Creating repositories
1. Cloning repositories
1. Working with Git concepts: Staging, Commits, and Status.

## Overview

The instructor will discuss why Git is worth learning. You already know how
to use a local Git repository with one branch, giving you the ability to move
your code forward and backward in time. Working with branches on Git extends
this ability by allowing multiple people to build different features at the
same time, then combine their work. Pull requests act as checkpoints when code
flows from branch to branch.

Students *must* pair off for this exercise. If you have trouble finding a
partner, ask your TA for help.

{{% notice blue "Note" "rocket" %}}
   **IMPORTANT**: Your TA should have already have a remote repo that you can
   pull and push to. If not, consult with your TA.
 
   {{% /notice %}}
## Gitting Ready

You are going to simulate a radio conversation between a shuttle pilot and
mission control. You and your partner will alternate tasks, so decide who will
be the **Pilot** and who will be the **Control**.

Before you and your partner can begin your collaboration, some preparation is
required first. You will both start by creating a new repository for each of you to work from.

### Step 1: Create a New Local Repository

**Control**: You need to complete steps 1 - 6 on your own
machine.

1. In the terminal, navigate to your development folder. Enter the following
   command to clone the project.

   ```console
   $ git clone http://localhost/srv/git/communication-log.git
   ```


1. Launch Visual Studio Code. Use the *File* menu to open the
   `communication-log` folder.
1. Create a new file called `index.html` and open it in the workspace.
1. Paste this code into `index.html`:

   ```html {linenos=table}
   <!DOCTYPE html>
   <html>
      <body>
         <p>Radio check. Pilot, please confirm.</p>
      </body>
   </html> 
   ```

1. Save your work, then stage and commit it.

   a. First, check the `status`.

      ```console
      $ git status
      On branch main

      Initial commit

      Untracked files:
      (use "Git add <file>..." to include in what will be committed)

         index.html

      nothing added to commit but untracked files present (use "git add" to track)
      ```

   b. The output shows is that `index.html` is not staged. Let's `add`
      everything in this directory, then check the `status` again.

      ```console
      $ git add .
      $ git status
      On branch main

      Initial commit

      Changes to be committed:
      (use "git rm --cached <file>..." to unstage)

         new file:   index.html
      ```

   c. The output tells us that the file is staged. Now let's `commit`. After
      that, we can see a record of our progress by using `git log`.

      ```console
      $ git commit -m "Started communication log."
      [main (root-commit) e1c1719] Started communication log.
      1 file changed, 5 insertions(+)
      create mode 100644 index.html

      $ git log
      commit 679de772612099c77891d2a3fab12af8db08b651
      Author: Chris <chrisbay@gmail.com>
      Date:   Wed Apr 5 10:55:56 2021 -0500

         Started communication log.
      ```

1. Use the command `git branch` to check the name for the default branch. If
   necessary, change the name to `main`.

   ```console
   $ git branch
   * default_name

   $ git branch -m default_name main.
   ```

   GitWeb uses `main` for its default branch. To make things easier, you
   should always try to match your local and remote branch names.

Great! You've got your project going locally. but we're going to need to make it accessible for the Pilot also. Let's push this project up to the server.

```console
   $ git push 
   ```

## Git the Teamwork Started!

Now it's time for you and your partner to start collaborating on the same repo.

For the remaining sections of this studio, keep an eye on the *Control* and
*Pilot* role tags. Make sure that you both perform your tasks in the
recommended order. Mixing things up won't destroy the universe, but it will
make finishing the studio more complicated.

Even when it is not your turn to complete a task, read and observe what your
partner is doing. The steps here mimic a real-world collaborative Git workflow.


### Step 2: Clone the Project
**Pilot**, your're up. 

<!-- {{% notice orange "Warning" "rocket" %}}

**Pilot**, did you and your partner give different names
to your `communication-log` repositories?

If not, take a moment to find your *local* `communication-log` folder on
your machine and rename it!

{{% /notice %}} -->


1. **Pilot**: In your terminal, navigate back to your development folder and
   clone Control's repo. You should be OUTSIDE of any other Git repositories.
   
   The clone command looks something like this:

   ```console
   $ git clone http://localhost/srv/git/communication-log.git
   ```

   Replace the URL with the address you are given by your TA.

1. **Pilot**: You should now have a copy of **Control's** project on your
   machine.

## Git Talking

Whew! That was quite the setup experience. Now you're ready to dive into the
main part of the studio.

On to Part 2!