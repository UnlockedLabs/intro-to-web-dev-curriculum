---
title: "slice Examples"
date: 2024-09-05T16:28:27-05:00
draft: false
weight: 6
originalAuthor: Christian Frauenhoffer # to be set by page creator
originalAuthorGitHub: johncfrauen-lc101 # to be set by page creator
reviewer: # update any time edits are made after review
reviewerGitHub: # update any time edits are made after review
lastEditor: # update any time edits are made after review
lastEditorGitHub: # update any time edits are made after review
lastMod: # UPDATE ANY TIME CHANGES ARE MADE
---


The general syntax for this method is:

```console
stringName.slice(i, j);
```

Given a starting index `i` and an optional ending index `j`, return the substring consisting of characters from index `i` through index `j-1`. If the ending index is ommitted, the returned substring includes all characters from the starting index through the end of the string.

```js {linenos=table}
"LaunchCode".slice(0, 6);

"LaunchCode".slice(6);
```

**Console Output**

```console
Launch
Code
```

On some websites, the portion of an email address before the `@` symbol is used as a username. We can extract this portion of an email address using `slice` in conjunction with `indexOf`.


{{% notice blue "Example" "rocket" %}}
```js {linenos=table}
let input = "fake.email@launchcode.org";
let atIndex = input.indexOf("@");
let username = input.slice(0, atIndex);
console.log(username);
```

**Console Output**

```console
fake.email
```

{{% /notice %}}