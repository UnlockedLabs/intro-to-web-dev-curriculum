---
title: "toUpperCase Examples"
date: 2024-09-05T16:28:27-05:00
draft: false
weight: 3
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
   stringName.toUpperCase();
```

This method returns a copy of `stringName` with all lowercase letters replaced by their uppercase counterparts. It leaves non-alphabetic characters unchanged.

{{% notice blue "Example" "rocket" %}}

 ```js {linenos=table}
	console.log("LaunchCode".toUpperCase());
	console.log("launchcode".toUpperCase());
	console.log("LaunchCode's LC101".toUpperCase());
```

**Console Output**

```console
	LAUNCHCODE
	LAUNCHCODE
	LAUNCHCODE'S LC101
```
{{% /notice %}}